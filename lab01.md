## Lab Report 1

Running the following commands: ```cd```, ```ls```, and ```cat``` with no argument, with a path to a directory as an argument, and a path to a file as an argument. 

1. ```cd``` with no argument
![Image](cd_no_arg1.png)
This is not an error, as the command to change directory will just return the user to the home directory if no argument is given. Working directory when the command was run:/home/lecture1

2. ```ls``` with no argument
![Image](ls_no_arg.png)
This is not an error, ls will print all the files in the current directory even without an argument, in this example since there was nothing in the current directory the output was empty. Working directory when the command was run:/home

3. ```cat``` with no argument
![Image](cat_no_arg.png)
This is an error, as cat will print out what is present in a file. Had to use control + c to exit the terminal. Working directory when the command was run:/home

4. ```cd``` to directory
![Image](cd_dir.png)
This is not an error, it changed the working directory from home to the directory included in the argument - lecture1. Working directory when the command was run:/home/lecture1

5. ```ls``` of directory
![Image](ls_dir.png)
This is not an error, it shows all the contents of this directory including other directories and files, it will work with or without an argument as long as the directory is not empty.

6. ```cat``` of directory
![Image](cat_dir.png)
This is an error, as the cat command only works on files not directories.

7. ```cd``` to file
![Image](cd_file.png)
This is an error, as the cd command only works for directories not files.

8. ```ls``` of file
![Image](ls_file.png)
This is not an error, it just outputs the same file as there is nothing else in the file.

9. ```cat``` of file
![Image](cat_file.png)
This is not an error, it prints out the contents of the file and works on multiple files given in the same argument.
