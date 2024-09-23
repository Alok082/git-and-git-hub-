# git-and-git-hub-
A version  control system for handling a large scale projects where multiple developers can work together  (it helps to  track changes in the code )
version control system keep the history of the code , when and what changes done at which line  of code 
Cd - change directory 
ls - list all files except hidden 
ls -a - list all files include hidden 
cd .. to get back from a dir 
mkdir newdir - to make a new directory


**Git** is also a version control system to help to work multiple developer on a single project , git is a tool that runs at our computer system 
before using git in our system we have to download vs code , window(git bash), mac (terminal) then run this command to check git --version
----> after install and setup the git , we have to configure the git (ham git ko bta rahe hain ki ham kon se account k  andar change karnne ja rahe hai )
there are two type of changes , global and local 
 ===> global - system me jo v changes hoga vo bas ek hi account pe change hoga , 
 i. git config --global user.name 'My name'
 ii. git config --global user.email 'email'
 iii. git config --list  (to test whichh account have we set up )
 ===> Local - this is for any specific repository of specific github  id (if you have multiple github account account )
 i. git config user.name "Your Name Here"
 ii. git config user.email "email"
 
**github**  it is a website that allow the developers to store and manage thheir code using git- http//:www.github.com
 1. we upload the file on git hub in  the  form of folder that folder is called repositpory in the git language
 2. there is two step process to upload on github , first add the things and second commit the things
 3. before commit the changes we have to give a message to the github that what i have done in the changes(commits )
 4. git store  our commits in the forms of history



**Git commands**
  1. clone - to clone a repository on our local machine -> git clone <URL>
  2. status command - to check the status of the code -> git status
      in the git status there is 4 types of status -
     i. untracked - the file which git is not tracking some new file \
     ii. modified - some changes  in the existing file
     iii. Staged - file is ready to commited (after adding the file and right before commited status will  be staged )
     iv. Unmodified - unchanged
  3. Add and commit - add new or changed file in git staging area -> git add <file name> if we have multiple changes the -> git add . , commit - it is record of the changes - git commit -m <some message>
  4. Push command - after commit the code on thhe local machine we have to update the code on the github repository at server (to upload local repo content to remote repo) -> git push origin <branch name>
  5. init command - to initialise a new repository
     -------> git init , git remote add origin <link> , git remote -v (to verify remote) , git branch (to check branch), git branch -M main (to rename branch) 
  
  
     
     
