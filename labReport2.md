**String Server Code**

![StringServer 1](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/98433674-6417-4b2e-aa68-1999b798d211)

![StringServer 2](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/27fdc254-934f-4ece-a305-05a58365cf01)


**Using /add-message "Hello"**

![add-message Hello](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/606ea0e6-0eca-4355-99d5-7480b3f0feb0)

1) Here, when add-message is used, the Handler class is called and within the Handler class, the handleRequest method is invoked.
2) When we use add-message initially to add the message "Hello", the part of the handleRequest method that is invoked is the block contained within the second if-statement. Here, line 21 sets element 1 of the messages array equal to the message that is trying to be added, which has been saved in element 1 of the parameters array. Next the for-loop executes, but only once, because te value of the num variable is currently 1, as it was incremented in line 21. In this loop, the message is saved in a new string. This string is then added to another string that holds all of the strings that have been added, currently there is just 1 string contained here.
3) The values change as parameters[1] and messages[1], now hold a new value (the message that was added). String st is assigned a new value, which will contain the number of the add message request (in this case, 1) and also the message that is going to be added. This string is then added to a variable messagesTotal, which is a cumulative string that will store all of the messages added. Currently, the only message in messagesTotal is the only one that we added, being "1. Hello".

**Using /add-message "How are you"**

![add-message How are you](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/588cc45d-f357-45cd-a50d-41656f902981)

1) Here, when add-message is used, the Handler class is called and within the Handler class, the handleRequest method is invoked. This is the same as in the previous add-message, as both of these requests are managed by the same part of the code.
2) When we use add-message a second time to add the message "How are you", similarly, the part of the handleRequest method that is invoked is the block that is contained within the second if-statement. Here, line 21 sets the second element (in using num++) of the messages array equal to the message that is trying to be added (in this case, "How are you"), which was saved in element 1 of our parameters array. Next, the for-loop will execute, twice in this case, because our num variable is now equal to 2. The first time it executes, it will save the first message in String st (this would be "1. Hello"), and it will then add this string to messagesTotal. The second time the loop executes, it will save the second message trying to be added (in this case "2. How are you") to our String st. This is then added to messagesTotal, which now contains both messages, "1. Hello" and "2. How are you". Finally, messagesTotal is returned, which returns both messages.
3) The values change as now, parameters[1] holds the new message, which is then assigned to messages[2] (messages[2] was previously empty). String st now also holds a new value, which is the the number of the add message request (in this case 2) and also the message that is going to be added (in this case "How are you"). This string is then added to the cumulative string messagesTotal, which now contains both messages that were added. Now messagesTotal holds, "1. Hello" and "2. How are you".

**Path to private key for my SSH key for logging into ieng6**

![labReport 2 q2 a](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/5c32ea56-9414-4b4f-9c3a-71a1d8a0557b)

**Path to public key for my SSH key for logging into ieng6**

![labReport 2 q2 b](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/3e3eaae1-0f3c-4321-811a-800aae8e3fdb)

**Logging into ieng6 course-specific account without being asked for password**

![logging into remote server using public key p1](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/026f968a-1629-4da3-9ca9-49a3f9f47ef9)

![logging into remote server using public key p2](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/d5563f7c-9748-4a9a-923f-e2c1a039d7fb)

**Something new that I learned from lab in week 2 or 3 that I didn't know before**

Over the past couple weeks in lab, I feel that I have learned a lot of concepts that I never knew before. Firstly, I did not know that you can change a server simply by editing the query or the path. I also did not know that you could login or access another computer while physically using a different computer. I also did not know anything about SSH keys or how they work, and I feel that now, I have a pretty good understanding of them. Additionally, I was not familiar with commands such as ssh or scp, and I feel that I am now able to work comfortably using both commands.


