# Bash Commands

[Charmm gui Unix lessons](https://charmm-gui.org/?doc=lecture&module=unix&lesson=1)

- `ls`: lists visible files and folders in current directory.
- `ls -a`: lists invisible files and folders in current directory.
- `ls -l`: list permissions and associated files.
- `cd` or `cd ~` or `cd ../..` or `cd /`: takes you to the home directory (`C:\Users\username` or `home/ubuntu` etc.). (change directory)
- `cd C:/Users/username/folder1` or `cd ~/folder1`: takes you to the directory 'folder1' at the path `C:\Users\username\folder1`.
- `cd ..`: takes you back one folder.
- `pwd`: outputs current location path. (print working directory)
- `mkdir directory1`: makes a folder/directory called 'directory1' in the current location.
- `touch file-name.txt`: modify file 'file-name.txt' or create file 'file-name.txt' if none exists.
- `cat file-name.txt`: output contents of file called 'file-name.txt'. (concatenates and displays files)
- `cat file-name.txt | head -n5` or `head -n5 file-name.txt`: display the first 5 lines of the file 'file-name.txt'. (Change number to be number of lines you want to select).
- `cat file-name.txt | tail -n5` or `tail -n5 file-name.txt`: display the last 5 lines of the file 'file-name.txt'. (Change number to be number of lines you want to select).
- `echo "Any message you would like the terminal to output"`: output a message to the terminal to be read.
- `echo "A message" > file-name.txt`: replace contents of 'file-name.txt' with the echoed message "A message".
- `echo "Additional message" >> file-name.txt`: appends the echoed message "Additional message" to the 'file-name.txt' file.
- `test -f file-name.txt && echo "file exists" || echo "file does not exist"`: check if a file exists in the current repository/directory.
- `wc file-name.txt`: display the number of lines, words, and/or bytes of output.
- `wc -m < file-name.txt` or `cat file-name.txt | wc -m`: display the number of characters (includes new line characters) in the file 'file-name.txt' without the file name in the output.
- `wc -m file-name.txt`: display the number of characters (includes new line characters) in the file 'file-name.txt' and the file name.
- `wc -c < file-name.txt`  or `cat file-name.txt | wc -c`: display the number of bytes in the file 'file-name.txt' without the file name in the output.
- `wc -c file-name.txt`: display the number of bytes in the file 'file-name.txt'.
- `wc -l file-name.txt`: display the number of lines in the file 'file-name.txt' and the file name.
- `wc -l < filename.txt` or `cat file-name.txt | wc -l` or `sed -n '$=' file-name.txt`: display the number of lines in the file 'file-name.txt' without the file name in the output.
- `cat -n file-name.txt`: displays each line, ennumerated in the file 'file-name.txt' (e.g. where each /n is a new line in the output: /n1 First line. /n2 Second line. /n3 Third line).
- `sed -n '=' file-name.txt`: displays numbers for each line in the file 'file-name.txt' (e.g. where each /n is a new line in the output: /n1 /n2 /n3).
- `mv file1 file-name.txt`: renames 'file1' to be 'file-name.txt'. (Note that, if you use mv to give a file a name that already exists, it will cause that file to be overwritten)
- `mv file-name.txt ~/folder/file-name.txt`: moves 'file-name.txt' to location '~/folder/file-name.txt'.
- `rm file-name.txt`: removes file 'file-name.txt'.
- `rm -r folder1`: removes directory and its contents. (Note: The -r option means "remove files recursively", i.e. it removes all files you specify, and if that file is a directory, it removes all files in that directory. If that directory has sub-directories of its own, it removes those, etc.)
- `rm -r folder1/*`: removes all the contents of 'folder1' directory while still keeping the 'folder1' directory itself.
- `rmdir folder1`: removes 'folder1' directory if empty.
- `cp file1.txt file2.txt`: copies 'file1.txt' to another file called 'file2.txt'.
- `diff file1.txt file2.txt`: shows differences between 'file1.txt' and 'file2.txt' or nothing if there are no differences.
- `chmod u+x file-name.txt`: changes permissions of the file 'file-name.txt', giving the user executable permissions for the file. (Before `+` or `-` you can choose `u` for user, `g` for group, and or `o` for other to specify who the change is for (can leave blank or use `a` or `ugo` for all). after the `+` or `-` you can choose `w` for write, `r` for read and or `x` for execute permissions. The `+` gives the permission(s) and the `-` removes the permission(s).)
- `ps`: gives a list of processes running and their process IDs.
- `kill process-id`: kills a process if you replace `process-id` with the actual process ID.
- `variable_name=variable_value`: sets a variable called `variable_name` to be the value `valriable_value`, and can be called on using `echo $variable_name` or `echo ${variable_name}` when working with multiple variables or punctuation. (Note: variables are case-sensitive, connot contain spaces or special characters except `_` and it must start with a letter. If you want things to be as they are without using an escape character then use `'` `'`)
- `env` or `printenv`: lists all environment variables.
- `printenv ENV_VAR` or `echo $ENV_VAR`: returns the value of the environment variable 'ENV_VAR'.
- `grep "part-of-word-or-sentence" ./path/to/file-name.txt`: searches for and returns the line that contains "part-of-word-or-sentence" in './path/to/file-name.txt'. (using `-i` with grep makes its search case-insensitive, `-i "^ip"` will search for lines that start with 'ip', `-i "ip$"` will search for lines ending in 'ip', `-iv` will exclude the lines containing whatever is specified.)

## Additional useful things to know

`\` is an escape character. (Example use case: So if you have a file name and have not placed it in quotation marks that has a space you can use the escape character before the space to make sure the file name is correctly referenced. - can be used for other special characters that are not meant to perform a function)

`|` is pipe operator and is used to connect commands together.

`#!/bin/bash` is the line necessary at the start of a shell script file. (`#!` is known as a shebang)

`Ctrl` + `C` cancels a process.

`Ctrl` + `Z` suspends a process. `bg` moves the suspended process to the background. `fg` moves the process to the foreground.
