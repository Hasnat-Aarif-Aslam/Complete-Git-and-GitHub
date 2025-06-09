# **What is Git?**


![image](https://github.com/user-attachments/assets/d30b8a16-3164-44f4-9f2b-e11b63b035d1)


# **Git Configuration:**

**Configuring Git involves defining key user settings that Git uses to track who is making changes in a repository. These configurations are stored in Git's config file.**

* git config --global user.name "My Name"
(This sets your global username. Git uses this name to label your commits.)

* git config --global user.email "someone@email.com"
(This sets your global email address. GitHub or other Git servers use this to associate commits with your online account.)

* git config --list
(Displays the current configuration Git is using (including username, email, editor, merge tool, etc.).)


---------------------------------

# **Commands:**

![image](https://github.com/user-attachments/assets/642e2c0a-c16d-42e7-b247-4d6c6f44383a)

# **The status can be in any 1 of these 4 states:**

![image](https://github.com/user-attachments/assets/1d61522c-1e9b-4423-a4b6-e324b7b0df18)


![image](https://github.com/user-attachments/assets/1e32502b-6ead-4c95-b4de-b6781c3cb833)

**RATHER THAN ADDING EACH FILE ONE BY ONE, WE CAN ALSO ADD ALL THE NEW(UN-TRACKED) OR MODIFIED FILES TO THE STAGED PHASE BY USING THIS COMMAND:**
* git add .


**As we know, when we clone a repo. its one original copy is on github(remote) and the other copy is present locally(our pc), so ``origin means: original copy`` while ``main means: main branch``**
![image](https://github.com/user-attachments/assets/fa1ba52a-2af6-4278-b97b-f6a7d82d0625)
