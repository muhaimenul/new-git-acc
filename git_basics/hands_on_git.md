---------------------------------------------------
Basic initial git commands:
---------------------------------------------------
1. create repository
2. git clone clone-link
3. copy project to the clonned repository
4. git add . or git add -A
5. git commit -m "Give a token to remember"
6. git remote add origin clone-link
7. git push -u origin master
8. username password


---------------------------------------------------
See or change origin:
---------------------------------------------------
git remote -v
git remote add origin <url>
git remote set-url origin <url>


---------------------------------------------------
To see Git Info:
---------------------------------------------------
git remote get-url origin
git config user.name
git config user.email

---------------------------------------------------
Stage or Commit Related:
---------------------------------------------------
git show --summary                                //see last Commit
git reset --soft HEAD~1                           //undo last commit
git reset --hard 0ad5a7a6 or git checkout <sha1>  //return to specific commit
git stash                                         //hide you changes without commit
git stash list                                    //see your list with hidden changes
git stash apply                                   //apply your last changes from stash list
git stash drop stash@{0}                          //remove from stash list
git stash pop stash@{1}                           //apply choosed stash and drop it from stash list

---------------------------------------------------
Pull-Push or Merge Related:
---------------------------------------------------
git pull --allow-unrelated-histories


---------------------------------------------------
All about branch:
---------------------------------------------------
git branch                //branch list
git branch <name>         //create branch 
git checkout <name>       //switch branch
git checkout -b <name>    //create and switch branch
git merge <branch>        //merge branch from master
git branch -d <branch>    // delete local branch (-D for force delete)
git push origin --delete <branch> //delete remote branch




---------------------------------------------------
Replace user info of git commit:
---------------------------------------------------
git filter-branch -f --env-filter "
    GIT_AUTHOR_NAME='Muhaimenul Islam'
    GIT_AUTHOR_EMAIL='muhaimenulislam@iut-dhaka.edu'
    GIT_COMMITTER_NAME='Muhaimenul Islam'
    GIT_COMMITTER_EMAIL='muhaimenulislam@iut-dhaka.edu'
  " HEAD


---------------------------------------------------
Git cheat sheet:
---------------------------------------------------
https://medium.freecodecamp.org/git-cheat-sheet-and-best-practices-c6ce5321f52