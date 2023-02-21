1. mkdir folder
2. touch README.md
3. git commit -m "commitName"
4. git commit -a -m "messageName" here this will not create new commit it will add to existing commit
5. git push origin __Push to the folder__
6. git status __To get the status of the git__
7. git add folder/README.md __make the changes you made__

# git log __TO see what you have done__
###   Staging and Committing  ###

Suppose you edited three files (a.rb, b.rb, and c.rb). Now you want to commit all the changes, but you want the changes in a.rb and b.rb to be a single commit, while the changes to c.rb are not logically related to the first two files and should be a separate commit
1. echo "written to c " > c.md __write someting to a,b,c .md files__
2. git add a.rb, b.rb
3. git commit -m "Changes for a and b"
4. git add c.rb
5. git commit -m "Unrelated change to c"