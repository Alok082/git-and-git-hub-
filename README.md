# git-and-git-hub-
A version  control system for handling a large scale projects where multiple developers can work together  (it helps to  track changes in the code )
version control system keep the history of the code , when and what changes done at which line  of code 
Cd - change directory 
ls - list all files except hidden 
ls -a - list all files include hidden 
cd .. to get back from a dir 
mkdir newdir - to make a new directory

**workflow by apna college ==> github repo > clone repo > make changes > add changes > commit changes > push 

**Woekflow to upload the code on the github ==> git init-> git add . -> git commit -> git remote add origin <link> -> git branch (to check branch)-> git branch -M <branch name > -> git push origin <branch name>**

**Git** is also a version control system to help to work multiple developer on a single project, git is a tool that runs at our computer system </br>
before using git in our system we have to download vs code, window(git bash), mac (terminal) then run this command to check git --version </br>
----> after install and setup the git , we have to configure the git (ham git ko bta rahe hain ki ham kon se account k  andar change karnne ja rahe hai )</br>
there are two type of changes , global and local </br>
 ===> global - system me jo v changes hoga vo bas ek hi account pe change hoga , </br>
 i. git config --global user.name 'My name'</br>
 ii. git config --global user.email 'email'</br>
 iii. git config --list  (to test whichh account have we set up )</br>
 ===> Local - this is for any specific repository of specific github  id (if you have multiple github account account )</br>
 i. git config user.name "Your Name Here"</br>
 ii. git config user.email "email"</br>
 
**github**  it is a website that allow the developers to store and manage thheir code using git- http//:www.github.com
 1. we upload the file on git hub in  the  form of folder that folder is called repositpory in the git language
 2. there is two step process to upload on github , first add the things and second commit the things
 3. before commit the changes we have to give a message to the github that what i have done in the changes(commits)
 4. git store  our commits in the forms of history

**Git branches**  Branches in GitHub isolate work, enable parallel development, and facilitate safe collaboration without affecting the main codebase.
  # Merge -> A GitHub merge combines changes from one branch into another, typically integrating a feature or fix into the main codebase.
  # Branch Commands => 
    a. git branch (to check branch),
    b. git branch -M <branch name > (to rename branch) 
    c. git checkout <branch name > (to navigate from one branch to another)
    d. git checkout -b <new branch name > (to  create a new branch)
    e. git checkout -d <branch name > (to delete branch)
    f. git chheckout - (previous checkout branch=)

![githubbranch](./githubbranch.png)

  # Merge Commands => There are two way to merge 
   **Way 1** 
    a. git diff <branch name >(shows the differences between two versions of files in your Git repository, highlighting changes like added, modified, or deleted lines of code.),
    b. git merge <branch name > (to merge 2 branches) 
    c. git checkout <branch name > (to navigate from one branch to another)
    d. git checkout -b <new branch name > (to  create a new branch)
    e. git checkout -d <branch name > (to delete branch)

   **Way 2** 
    a. Create a PR -> PR is a pull  request 
       A pull request (PR) is a feature in GitHub (and other version control platforms) that allows you to propose changes from one branch to another, enabling code review, discussion, and approval before merging 
        those changes into the main codebase.
  #  jab ek hi project par multiple dev kaam kr rahe ho aur vo main branch k sath merge karna chahte ho aur main branch kisi senior dev k andar me ho to rest of dev PR raise krte hain main ke sath merge karne k liye aur senior dev unke changes ko review karta hai aur then merge  karta hai jisse main branch safe rahe, aur senior dev us PR k upr comment v kar skte hai if koi issue ho PR k andar 

  #  here how to merge a PR =======>
  click on compare and pull  request 
  ![shot1](./shot1.png)
  write title and description and click on create pull request 
  ![shot2](./shot2.png)
  then click on merge pull request 
  ![shot3](./shot3.png)

  # Resolving Merge Conflicts  => An event that takes place when git is unable to automatically resolve differences in code between two commits
  git can't do merge automatically  so we need to resolve this mannaully then we can merge 
     
  ![mergeconflict](./mergeconflict.png)
     

**Git commands**
  1. clone - to clone a repository on our local machine -> git clone <URL>
  2. status command - to check the status of the code -> git status
      in the git status there is 4 types of status -
     i. untracked - the file which git is not tracking some new file 
     ii. modified - some changes  in the existing file
     iii. Staged - file is ready to commited (after adding the file and right before commited status will  be staged )
     iv. Unmodified - unchanged
  3. init command - to initialise a new repository -------> git init , git remote add origin <link> , git remote -v (to verify remote) , git branch (to check branch), git branch -M <branch name > (to rename branch) , 
  4. Add and commit - add new or changed file in git staging area -> git add <file name> if we have multiple changes the -> git add . , commit - it is record of the changes - git commit -m <some message>
  5. To add a remote origin- (if repo is private then use personal access token otherwise without token) git remote add origin 
              https://Alok082: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@github.com/Alok082/pocketdoctor.git ,
  6. To remove the remote origin - git remote remove origin
  7. To check the remote origin - git remote -v  
  8. Push command - after commit the code on thhe local machine we have to update the code on the github repository at server (to upload local repo content to remote repo) -> git push origin <branch name> ,  git push  -u origin <branch name> (here -u is used to tell the github that in future we will push on only this branch , ) next time we will only hit - git push
  9. To unstage the code - git restore --staged <file> , after git add command if it need to get back the added file
  10. Pull commond -> git pull , command fetches changes from a remote repository and immediately merges them into your current branch, It's essentially a combination of git fetch (which downloads the changes) and 
      git merge (which integrates them).
  11. git log (to check all the commits on the git hub ) , git log --oneline (show all the commits in one line )     

**Undoing changes**   sometime by mistake we add or commit any thing which we don't have to do , so we need to undo that changes
 # case 1 ===> staged changes (jo changes add ho gye hain but commit nhi hue )
      git reset <file name > OR git reset (for all files changes)
      run -> git reset --hard to make changes in vs code or your local platform 
      
 # case 2 ===> commited changes (for one changes) 
      git reset ~HEAD1 , all the commits stored in like linked list , and the last commit name is by default HEAD and ~1 mean 1 step 

 # case 2 ===>multiple commited changes 
       git reset <commit hash>  every commits has hash code to identify that commit , so we can check that hash code by git log and , rest that commit by using that hash code 
       run -> git reset --hard to make changes in vs code or your local platform 
      
**Fork**  A fork in Git is a personal copy of someone else's repository that you create under your own GitHub account, allowing you to freely experiment with changes without affecting the original project.
          Its like as rough copy
   # fork ka use krke ham kisi dusre person k account ka pura code apne account me copy kar skte hain uske bad ham usme change krke PR raise kar skte hain then ham jaha se copy kiye honge us repo ka owner merge kr   dega basically isko ham kisi open source me contibute krne k liye karte hain

  
# Short tricks =>>
  
    a. git commit -am "message" (this command add and commit at same time),
    b. git commit --amend -m <message > (used to update the message of last commit )
    c. git commit --amend --no-edit (command modifies the most recent commit without changing its commit message. It’s often used to include additional changes in the last commit.)# but while push you need to do with force (git push origin <branch name > --force)
    d. git revert <hash code> (command creates a new commit that undoes the changes made by a previous commit, effectively reversing its effects without altering the project's history.)
    e. git stash command temporarily saves (or "stashes") your uncommitted changes, allowing you to switch branches or work on something else without committing those changes. You can later reapply the stashed changes when you're ready (github does not allow user to change directory if you have anyting add and not commited , stash will help here)
    f. git stash pop OR git stash apply Once the changes are reapplied, you can commit them.
    g. git stash save <name> (this command will save followed by a name) , after that > git stash list (list of all stashes) then git stash apply <index> (to get back for commit )
    h. git log --graph --online --decorate  (to get the commit history in for of graph and decorated)
    i. git rebase  (command is used to move or combine a sequence of commits to a new base commit. It’s often used to:
Integrate Changes: Apply your changes on top of the latest changes from another branch, effectively "replaying" your commits on top of it.
Clean Up History: Modify commit history by squashing, editing, or reordering commits for a cleaner, linear history.)
    j. git rebase <branch name> --interactive (or git rebase -i <branch name>) allows you to interactively rebase your current branch onto the specified branch. This means you can review and modify your commits before they are applied on top of the target branch.

Here’s what you can do interactively:

      Reorder Commits: Change the order of commits.
      Squash Commits: Combine multiple commits into one.
      Edit Commit Messages: Modify the messages of individual commits.
      Drop Commits: Remove specific commits.
      When you run the command, it opens an editor with a list of your commits, and you can choose actions like pick, reword, squash, edit, or drop to apply to each commit. After saving and closing the editor, Git applies the changes according to your instructions.
    k. git fetch -> command retrieves updates from a remote repository, downloading any new commits, branches, or tags without merging them into your local branches. It allows you to see changes made by others before deciding to integrate them into your local repository with commands like git merge or git rebase


    
# open a repo and a project which you want to use , and press > this button on keyboard it automatically set a pull request and redirect to the vs code 
   
     

 
  
  
     
     
