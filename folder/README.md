1. mkdir folder
2. touch README.md
3. git add folder/README.md __make the changes you made__
4. git commit -m "commitName"
5. git commit -a -m "messageName" here this will not create new commit it will add to existing commit
6. git push origin __Push to the folder__
7. git status __To get the status of the git__

1. git log __TO see what you have done__
2. git log --pretty=oneline __TO see what you have done in one line__

###   Staging and Committing  ###

Suppose you edited three files (a.md, b.md, and c.md). Now you want to commit all the changes, but you want the changes in a.md and b.md to be a single commit, while the changes to c.md are not logically related to the first two files and should be a separate commit
1. echo "written to c " > c.md __write someting to a,b,c .md files__
2. git add a.md, b.md
3. git commit -m "Changes for a and b"
4. git add c.md
5. git commit -m "Unrelated change to c"
6. git reset filename.md To reset stagged files use

### To get back to previous commit ###
1. git log and select first 5 digits for the commit that you want to revert
2. git checkout <5digit>
3. __NOTE__ if you want to commit you have to get back to last commit (you can only see if you want to update you have to create new branch)
4. git checkout main __to get back to the last commit__

#### Undoing comitted changes ####
1. git commit -m "comment"
2. git revert HEAD __This will uncommit the last commit__

#### Creating a branch without conflict ####
1. git checkout -b branchName1 __create a branch and checkout to branchName1__
2. git status
3. git branch __to check where you are in branch__ 
4. __add,then commit__ git add. to all all changes
5. git push origin branch1  __to push to branch1__
6. git checkout main
7. git merge branchName1
8. git push
9. git push origin -d branch1 __to delete branch for remote__
10. git branch --d branch1 __to delete branch for local__

#### Creating a branch with conflict ####
use gui and select add both/ any other according to your requirement

    m1 ---- m2 ---- m3
            |
            p1------p2

now in normal merg the output will show   __(cmd:  git merge branchName1)__

    m1 ---- m2 ---- m3---- \ -----> final
            |               |  
            p1------p2---- /

now in merg squash the output will show   __(cmd: git merge --squash branch1)__

    m1 ---- m2 ---- m3 -----> final
           

now in merg and rebase output will show   __(cmd: git rebase <>)__

    m1 ---- m2 ---- m3 ---- p1 ---- p2 ----> final
    
#### Rebasing ####
1. git rebase main (do this from branch)
2. git rebase branch (do this from master branch)