# CSE 15L Lab 2/3 Report: 

## Part1: 
Code used for the web server:
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    String s = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Available commands as paths: /add-message?s=(your string)");
        } 
        else{
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    s += parameters[1] + "\n";
                    return s;
                }  
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

```
After running `java StringServer 4000` the web server gets started on localhost on port 4000
Then, when we put in the URL : [http://localhost:4000/add-message?s=Hello](http://localhost:4000/add-message?s=Hello) we get this on the webpage:

![image](https://user-images.githubusercontent.com/122490362/215367158-87426992-2558-43da-8591-a7fc193c045b.png)

When the URL gets put in the address bar, the method handleRequest gets called. It reads the path and sees that it contains "/add-message". At this point, the parameters array gets filled with the 0th index being filled with "s" and the 1st index being filled with "Hello". This then makes s go from an empty string to "Hello\n", returning s and printing it on the webpage.

The exact same process happens for the when we use the URL: [http://localhost:4000/add-message?s=World](http://localhost:4000/add-message?s=World).
The difference this time, is that instead of s being an empty string in the beginning, it's now "Hello\n". The 1st index in parameters gets set equal to "World", and then s gets added onto it "World\n" so s becomes "Hello\nWorld\n". THen, s is returned and we get the following output on the webpage:

![image](https://user-images.githubusercontent.com/122490362/215367172-ca46508f-fb20-4020-9a0b-65db8c75e74a.png)

