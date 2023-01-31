# Servers and Bugs
## Purpose of this Lab
The purpose of this lab is to create a simple web server called StringServer that takes in Strings as inputs and displays them on the web server. Along with the web server, we must also identify bugs in code provided during the Lab on week 3 and come up with ways to fix the bugs.
## Part 1 - Web Server
The following code block displays the code I made in order to process and display the Strings on my web server.
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The string that will be modified after taking in requests
    String input = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(input);
        } else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                    input += (parameters[1] + "\n");
                    return String.format(input);
                }     
            }
        return String.format(input);
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
The following screenshots show the web server taking in requests that modify the page. The requests have a format that looks like this :
`/add-message?s=<string>`

Example 1:

![Image](ss1.jpg)

- In the following image, the method that is called is `public String handleRequest(URI url)`
- Some important fields and arguments of this method are the `url` parameter and the String value labeled `input`
- After taking in the request `/add-message?s=Hello`, the `url` parameter gets changed to the new url of the web server. After the code exectutes, input is changed to the String at the end of the request. In this example, that string is `Hello`

Example 2:

![Image](ss2.jpg)
