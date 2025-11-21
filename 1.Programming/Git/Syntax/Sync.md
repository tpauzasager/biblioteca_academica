```bash
//Add to stage
git add <file_path>
git add . //add all file with any non-saved changes 

//Show current stage status (optional)
git status

//Create snapshot of the staging
git commit -m "<commit_message>" //if there is no message => opens text editor

//Push snapshots saved localy (bran_name usually == {master, main})
git push origin <branch_name> 
```
___
# Download unsaved changes 
```bash
git pull
```
___
# Rollback
```bash
//Shows all commits saved in history
git log
//Copie hash from a commit

//Rollback
git checkout <commit_hash> 

```