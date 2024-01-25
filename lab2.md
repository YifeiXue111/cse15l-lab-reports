# Lab2 Report
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> chat = new ArrayList<String>();
    String outcome="";
    String page_print="";
    int num=0;
    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String parameter[] = url.getQuery().split("=");
            String message= parameter[1].split("&")[0];
            String name= url.getQuery().split("user=")[1];
            outcome=name+": "+message+"\n";
            chat.add(outcome);
            outcome="";
            page_print+=chat.get(num);
            num++;
            return page_print;
        }  else {
            return "404 Not Found!";
        }
    }
}

public class ChatServer {
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

![Image](85430753c456b9abb352794d8a292f5.png)

![Image](037ff13b782edd17f57021f8ea1a332.png)
