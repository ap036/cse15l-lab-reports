## Lab Report 2

**Part 1:**

1. String Server Code:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    String str = "";
    int counter = 1;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Apru's Number: %d", num);
        } else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } else {
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].endsWith("s")) {
                    str += counter + ". " + parameters[1].replace("%20", " ") + "\n";
                    counter ++;
                    return str;
                }
            }
            return "404 Not Found!";
        }
    }
}

class SearchEngine {
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

2. Hello
![Image](Screen Shot 2023-10-22 at 11.51.52 PM.png)
Hello Webserver Example

4. How are you?
![Image](Screen Shot 2023-10-22 at 11.52.08 PM.png)
How are you webserver example


**Part 2:**

1. Path to the private key for SSH key:
![Image](private_key.png)

3. Path to the public key for SSH key:
![Image](public_key.png)

5. Logging into ieng6 without password:
![Image](no_pw_login.png)

**Part 3:**

In week 2 and 3 I learned how to create an ssh key pair and login to a remote server without a password which was both new to me. While I often use ssh for tasks I would enter my password each time so this is a more efficient login process I am excited to keep using.