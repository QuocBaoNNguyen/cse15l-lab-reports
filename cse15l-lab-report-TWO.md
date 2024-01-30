# CSE 15L Lab Report 2
## Part 1
**Code for ChatServer:**
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
import java.util.List;

class Handler implements URLHandler {
   
    List<String> entireChat = new ArrayList<>();

    public String handleRequest(URI url) {

        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            String name = null;
            String message = null;

            for (int i = 0; i < parameters.length; i++) {
                String[] curr = parameters[i].split("=");
                if (curr[0].equals("s")) {
                    message = curr[1];
                } else if (curr[0].equals("user")) {
                    name = curr[1];
                }
                if (message != null && name != null) {
                    String TheMessages = name + ": " + message + "\n";
                    entireChat.add(TheMessages);
                }
            }

            StringBuilder finalChat = new StringBuilder();
            for (String chatMessage : entireChat) {
                finalChat.append(chatMessage);
            }

            return finalChat.toString();
        }
        return "404 Not Found!";
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
Screenshot 1:
<br/>
![Image](cs15l-labreport-ss1.png)






