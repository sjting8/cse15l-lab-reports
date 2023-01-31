# **Lab Report 1**
By: Sean Ting

## Part 1
StringServer.java:

![Image](StringServerSnippet.png)

**/add-message?s=Hello as path:**

![Image](AddMessageOne.png)

* When the above is put into the URL, the handleRequest method is called, with the URL as the parameter.
* Since the path is not equal to "/", the else statement is executed.
* The code will print the path in the terminal that runs the server and since the path contains "/add", the code will execute the if statement.
* The query is split at "=" so the "s" is taken in for the first element of the parameters String array and the message after the equal sign is taken in as the second element.
* Since "s" is the first element of the parameters array, the String variable, message, will concatenate with the second parameter, or the message, and start a new line (*\n*).


**Reload with /add-message?s=How are you as path:**

![Image](AddMessageTwo.png)

* When the above is put into the URL, the handleRequest method is called, with the URL as the parameter.
