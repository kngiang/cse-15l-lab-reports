# Lab Report 2
## Part 1
Code for StringServer.java:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String message = " ";

    public String handleRequest(URI url) {
        if (url.getPath().contains("add-message")) {
            if (url.getQuery().contains("s=")) {
                String[] parameters = url.getQuery().split("=");
                message = message + " " + parameters[1];
                message = message.trim();
                return message.replace(" ", "\n");
            }
            else {
                return "Invalid query";
            }
        }
        else {
            return "Invalid path";
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

Example 1:
<br /> ![Image](lab2_ex1.png)
<br /> First, the getPath method is called to get the path of the url. Then, the contains method is called on the url's path and makes sure it contains "add-message". If the url satisfies the first requirement, a getQuery method to get the url's query. Next, another contains method is called and checks if the url's query matches the syntax of "s=". If both path and query satisfy the requirements, the getQuery method is called again on the url to get the query and a split method with a provided argument of "=" is called to isolate the "s" and the word following the "=". The message variable is then updated with the original message along with a space and the word specified (word following the "="). The message would look like this: "  Sick". Then the trim method is called on the message string to remove the leading spaces, so message would be "Sick". Finaly, a replace method with the given arguments, (" ", "\n"), would be called on the string to replace any empty spaces between the words with a line break. In this case, message is not changed and will return the word "Sick".

Example 2:
<br /> ![Image](lab2_ex2.png)
