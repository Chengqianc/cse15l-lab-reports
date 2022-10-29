# Week 3 Lab Report
## Part 1
`SearchEngine.java`
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {
    ArrayList<String> list = new ArrayList<String> ();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("%s", list.toString());
        }
        else if (url.getPath().contains("/search")) {
            String[] param = url.getQuery().split("=");
            if (param.length >= 2 && param[0].equals("s")) {
                ArrayList<String> output = new ArrayList<String> ();
                for (String str : list) {
                    if (str.contains(param[1])) {
                        output.add(str);
                    }
                }
                return String.format("%s", output.toString());
            }
        }
        if (url.getPath().contains("/add")) {
            String[] param = url.getQuery().split("=");
            if(param.length >= 2 && param[0].equals("s")) {
                list.add(param[1]);
                return String.format("%s has been added.", param[1]);
            }
        }
        return "404 Not Found!";
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

`Screenshot of using add`
![Image](week3-lab-report-screenshots/sc9.png)
In the above step, the add part of the handleRequest method got executed. The argument for the method was the URL. The query part of the URL provide both the selection of the add option as well as the actual string the user wants to add, which in this case is "apple". The effect of that was the size of the arraylist increased by one because of the new addition of string "apple".

`Screenshot of using add`
![Image](week3-lab-report-screenshots/sc8.png)
In the above step, the add part of the handleRequest method got executed. The argument for the method was the URL. The query part of the URL provide both the selection of the add option as well as the actual string the user wants to add, which in this case is "pineapple". The effect of that was the size of the arraylist increased by one because of the new addition of string "pineapple".

`Screenshot of using query`
![Image](week3-lab-report-screenshots/sc7.png)
In the above step, the seach part of the handleRequest method got executed. The argument for the method was the URL. The query part of the URL provide both the selection of the search option as well as the actual substring that the user wants to search for, which in this case is "app". Both the strings "apple" and "pineapple" were printed out as the result as they both contained the substring "app".


## Part 2
### Bug #1
* The failure-inducing input (the code of the test)
![Image](week3-lab-report-screenshots/sc1.png)
The test input I gave was an integer array containing elements 3 and 4.

* The symptom (the failing test output)
![Image](week3-lab-report-screenshots/sc2.png)
Instead of having 4 and 3 in the new array, the output was 4 and 4, which was incorrect.

* The bug (the code fix needed)
![Image](week3-lab-report-screenshots/sc6.png)
The bug was fixed by storing the value that's being swapped out and assigning it to the right position.

* Then, explain the connection between the symptom and the bug. Why does the bug cause that particular symptom for that particular input?
`The bug was that the original code failed to save the replaced value. As a result, the output was 4 and 4 instead of 4 and 3 being stored in the array.`

### Bug #2
* The failure-inducing input (the code of the test)
![Image](week3-lab-report-screenshots/sc4.png)
The test input I gave was two lists of strings, namely listA containing "a","a","b","c" and listB containing "a","x","y","z".

* The symptom (the failing test output)
![Image](week3-lab-report-screenshots/sc3.png)
Instead of displaying the output, the program was having an error of running out of heap space.

* The bug (the code fix needed)
![Image](week3-lab-report-screenshots/sc5.png)
The bug was fixed by replacing the index1 with index2.

* Then, explain the connection between the symptom and the bug. Why does the bug cause that particular symptom for that particular input?
`The bug was that the original code was updating the wrong variable. Therefore, the program kept running in a infinite loop, resulting in the OutOfMemoryError.`