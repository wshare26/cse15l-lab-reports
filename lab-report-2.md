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

The relevant argument to the methods are the url that is being added which in this case would be `/add-message?s=Hello&user=jpolitz`. This is because the methods such as `getQuery`,  `split`, and the `equals` method splits up the query part of the `url`, and checks to see if it is equal to the conditions. In this case it is and it can proceed to add the user and the user's message to the next line. The value of the `startingmessage` field would be empty because there has not been anything added yet. After code has added the user and the user's message, the value of the `startingmessage` becomes `jpolitz: Hello`.

The values of `startingmessage` can change (which it does in this case) if the conditions of values inside the if statement are true. If the condition is true, then the `startingmessage` adds the user and the user's message.

---

when `ChatServer` has added `/add-message?s=How are you&user=yash`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/6f405eeb-bd22-407c-9b79-0de8ee9fac73)

The relevant methods that are called are the `getQuery`,  `split`, and the `equals` method.

The relevant argument to the methods are the url that is being added which in this case would be `/add-message?s=How are you&user=yash`. This is because the methods such as `getQuery`,  `split`, and the `equals` method splits up the query part of the `url`, and checks to see if it is equal to the conditions. In this case it is and it can proceed to add the user and the user's message to the next line. The value of the `starting message` field would be `jpolitz: Hello` because it was added in previously. After the code has added the user and the user's message to the starting message, the value of the `startingmessage` becomes
`jpolitz:Hello`
`yash: How+are+you` in separate lines.


The values of `startingmessage` can change (which it does in this case) if the conditions of values inside the if statement are true. If the condition is true, then the `startingmessage` adds the user and the user's message to the next line.


***Part 2***
---
`absolute path to the private key for your SSH key for logging into ieng6`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/40b7f6c6-1a77-40d2-a4da-b189ed4e8893)

After typing in `ssh-keygen` into the terminal, it generates a file to save the key. The identification was saved in `/home/.ssh/id_ed25519` which I `ls` to show that it is there. 

---


`absolute path to the public key for your SSH key for logging into ieng6`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/2ce273f2-f840-42c9-b2ae-689054fe4315)

After using `scp` to copy the key to the server. I was able to use `ls` to show that the public key is there.


---


`Logging into wshare@ieng6-201.ucsd.edu without being asked for a password`

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/509af768-d213-49a8-afdd-bd70fc985af8)

Because I `scp` the path to the public key to the server, it is saved there and I am able to log in without using my password.



***Part 3***
---
I think the biggest thing that I have learned in week 3 was learning how to edit the code of NumberServer.java to make the intended usage slightly different. This is because when we first started the server, all that we had done was git clone an implementation of a web server that was given to us. However, in the lab report, we had to change the code to make it fit the requirements which caused me to learn more about the `getQuery`, `getPath`, `contains`, and `split` methods. As a result, I was able to change the code of the NumberServer.java and make it so that it fits the requirements of lab report 2.


