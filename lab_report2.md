# **Lab Report 2**
---
## Part 1
**`Chat Server` Code:**
```
import java.io.IOException;
import java.net.URI;
import java.util.List;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    private List<String> comments = new ArrayList<>();

    public String handleRequest(URI url) {

        if (url.getPath().equals("/")) {
            return "Please provide arguments.";
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] information = url.getQuery().split("&");
                String[] message = information[0].split("=");
                String[] user = information[1].split("=");
                if (user[0].equals("user") && message[0].equals("s")) {
                    String comment = String.format("%s: %s", user[1], message[1]);
                    comments.add(comment);
                    return String.join("\n", comments);
                }
            }
            return "404 Not Found!";
        }
    }
}

class ChatServer {
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
**First `/add-message`:**
