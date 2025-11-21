# Directory
``` shell
//List of directories 
ls
//Change directory
cd dir_name
//Move file from "origin" to "destination"
mv <origin_dir> <destination_dir>
//Rename or move file from directory
mv <file_name> {<new_file_name>, <new_directory_path>}
//Execute shell script
bash <file_name>[.sh]
//Create new directory
mkdir <dir_name>

```
___
# Files
```bash
//Create new files
touch [<file_name>]
```
## Cat
```bash
//Print all data in file
cat <file_name>
//Filer lines by matched word
cat <file_name> | grep <filer_word> 

``` 
___
# Process
## Display list process
```shell
//Display process
ps
//Display all process
ps -e
//filter by name
ps -C process_name
```

## Interactive list
```shell
ps
top
//Commands
k - Terminate process
M - Sort by memory usage
N - Sort by PID
c - Displays absolute path of process
q - Exit
```
## Kill a process
``` shell
kill <process_PID>
```