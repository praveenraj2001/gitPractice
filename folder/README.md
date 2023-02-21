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

Suppose you edited three files (a.rb, b.rb, and c.rb). Now you want to commit all the changes, but you want the changes in a.rb and b.rb to be a single commit, while the changes to c.rb are not logically related to the first two files and should be a separate commit
1. echo "written to c " > c.md __write someting to a,b,c .md files__
2. git add a.rb, b.rb
3. git commit -m "Changes for a and b"
4. git add c.rb
5. git commit -m "Unrelated change to c"

### To get back to previous commit ###
1. git log and select first 5 digits for the commit that you want to revert
2. git checkout <5digit>
3. __NOTE__ if you want to commit you have to get back to last commit