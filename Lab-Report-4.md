# ***CSE 15L lab report 4***   
Name: William Share

***Step 4: Log into ieng6***
---

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/6e0f9cfa-fd11-4196-b65d-8106c6a6d2c6)

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/7c0bb0f8-00ae-4d28-a23a-eb2652576e0d)

I opened the terminal and typed `ssh <space> wshare@ieng-201.ucsd.edu` and pressed  `<enter> `


***Step 5: Clone your fork of the repository from your Github account (using the SSH URL)***

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/99af031a-df93-479c-917e-1e381a457929)

I copied the SSH URL to git clone. Afterwards, I typed in `git <space> clone` and I pasted the copied link in and pressed `<enter>.` After the git clone is over I type `ls` and press `<enter>`to make sure that the directory is there.

***Step 6: Run the tests, demonstrating that they fail***


![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/d460585c-138e-4cd7-b8fc-226c132d2b19)


Afterwards I `cd` into the lab7 directory so that I can run the bash script to run the test files. I do this by typing `cd <space> lab7` and `<enter>`. I then type `pwd` and `<enter>` to see my current directory

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/4b57a23f-6683-4d92-85e6-3433b1a06b08)

I then type `bash <space> test.sh` and `<enter>`into the terminal to run the bash script that runs the test cases. As we can see, one of the tests fails.

***Step 7: Edit the code file to fix the failing test***


![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/0c141afb-bc6a-4f8b-87ec-ec913f47e023)

We can use `vim` to edit the code. We can type vim List then press `<tab>` to autocomplete and then .java and press `<enter>` to enter the file in vim.

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/8b545280-1d28-4287-b1a5-ac385330bedf)
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/e9f9098e-83cb-4b69-88e0-9dd9bb5e7512)


We see that the error is where it says `index1 += 1;`, so we must move our vim cursor to that place. To do this we can press `j` `43` times to move the vim cursor down until it is on the same horizontal line as `index1 +=1;`. 



![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/b8150ecc-7850-40c5-9fd6-7aa35d0b1ce7)


We can then press `l` `11` times to get our vim cursor onto the `1` in `index1` to change.


![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/0315f78c-f68f-4f67-a4fe-cb36ec436c02)



We can then press `x` to delete the `1` and then press `i` to enter insert mode so that we can insert the number that we want, that being 2. So we then type `2` and press `<esc>` to exit the insert mode. Afterwards, we can type `:wq` and `<enter>` to save and quit out of vim.


***Step 8: Run the tests, demonstrating that they now succeed***


![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/91999f32-563e-4148-b478-b88d0d9ea1d8)

Before running the tests, we can type `cat <space> ListExamples.java` and `<enter>` to see if the changes were made in the line that we changed, as we can see the changes were made successfully so we can move on to running the tests.

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/20b25436-3b55-4ec4-915b-e8cbea9cdcbf)

We retype `bash <space> test.sh` `<enter>` into the terminal to compile and run the test cases and we now see that the test run successfully.


***Step 9:***

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/9f84579f-b96b-4841-be79-d0c5abf03e19)
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/08f4103a-3e8a-416b-acb2-c9a6fd7e5212)
![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/3b796d98-a4ba-4562-869e-4102198cdb5c)


We type in `git <space> add <space> ListExamples.java` `<enter>` to stage a change for the next commit. Afterwards, we type `git <space> commit <space> -m <space> "fixed index1 to index2 error"` `<enter>` to comitt to the Git Repository. Afterwards I push it by typing `git <space> push <space> origin <space> main` `<enter>`
The changes made are now pushed to the fork of the repository on Github.







