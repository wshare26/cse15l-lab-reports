# ***CSE 15L lab report 2***   
Name: William Share

***Part 1***
---
code for `ChatServer`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/1b9572aa-f559-46fd-9275-8d5cb5967bf2)

---

when `ChatServer` has not added anything yet

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/6ee0200e-16a8-4dad-9629-3f3f85843561)

---

when `ChatServer` has added `/add-message?s=Hello&user=jpolitz`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/20a906f0-a323-47cc-ba54-346821622c67)

The methods that are called when are the `handleRequest` method which handles the `/add-message?s=Hello&user=jpolitz`. The methods within this method that are also used are the `getPath`, `equals`, `contains`, `getQuery`, sand `split`. The `getPath` method within the if statement gets the path part of the url, in this case it would get the `/add-message` part of the url and uses the `contains` method to see if it contains `/add-message`. Within this if statement, the methods `getQuery` and `split` are used to split up the url into different String arrays. Afterwards, the parameters are checked to see if they are valid by using the `equals` method and if they are, the correct parameters are added to the starting message.

The relevant argument 

The values of `startingmessage` can change (which it does in this case) if the conditions of values inside the if statement are true. If the condition is true, then the `startingmessage` adds the user and the user's message.

---

when `ChatServer` has added `/add-message?s=How are you&user=yash`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/6f405eeb-bd22-407c-9b79-0de8ee9fac73)

The relevant methods that are called are the `getQuery`,  `split`, and the `equals` method.




The values of `startingmessage` can change (which it does in this case) if the conditions of values inside the if statement are true. If the condition is true, then the `startingmessage` adds the user and the user's message to the next line.


***Part 2***
---
`absolute path to the private key for your SSH key for logging into ieng6`


---


`absolute path to the public key for your SSH key for logging into ieng6`

---


`Logging into wshare@ieng6-201.ucsd.edu without being asked for a password`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/509af768-d213-49a8-afdd-bd70fc985af8)



***Part 3***
---
I think the biggest thing that I have learned in week 3 was learning how to edit the code of NumberServer.java. 


