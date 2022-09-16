### General Structure of Commands

Commands contain 3 parts: 
```
[command] [options] [arguments]
```
* *Options:* Options tweak the behavior of the command.  Represented by a hyphen `-`.
* *Arguments:* Arguments can be files, raw data, or other options that the command requires.

### Directories
* `/`: Stands for the *root*.
* `~`: Stands for the *home directory*.  The home directory is the default working directory when a user logs in.
* `.`: Stands for *current directory* (also known as *working directory*). 
* `..`: Stands for *parent of the current directory*.
* *Absolute path:* The absolute path always starts from the root directory (`/`).  (Ex.) `/Users/nicolefrontero`.
* *Relative path:* The relative path starts from the current directory

### Creating and Modifying Files
* `touch`: (Ex.) `touch my_file.txt`.
* `echo "statement" > file_name.extension`: This is called *output redirection*.  The output from a command using echo like `echo "My first name is Nicole"` usually gets printed to the terminal.  However, you can redirect the output using `>` and save the output `"My first name is Nicole"` to a file.  (Ex.) `echo "My first name is Nicole > my_name.txt".
* `echo "Statement to append" >> file_name.extension`: You can append a statement to a file through using `echo` and `>>`.  (Ex.) "My last name is Frontero >> my_name.txt".
* `nano file_name.extension`: Creates a file using the editor `nano`.

### Running List of Commands

* `clear`:  Clears the console.
* `date`:  Prints the date.
* `echo`:  Prints any phrase to the console.
* `ls`:  Short for "list".  Prints the names of the contents of the working directory, and does not print hidden files (whose names start with a `.`).  
  - `-l`:  Short for "long format".  Provides additional columns, from left to right, file permissions, owner, group, size (bytes), last modification time.
  - `-h`: Provides unit suffixes for file sizes.
  - `-a`: Prints hidden files that start with a `.`.  **Caution:** Do not change these files!
  - *It's common to see combinations of `-l` and `-a` or `-h`, like `-lh` and `-la`.*
* `mkdir [directory_name]`: Short for "make directory".  Creates a directory.  
* `cd [file_path]`: Short for "change directory".  Changes the current working directory according to the new file path given.
* `pwd:` Short for "print working directory".
* `touch [file_name.extension]:` Creates a file.
* `echo`: Can be used to...
  - Print a statement to the terminal: (Ex.) `echo "My first name is Nicole"`.
  - Create a file using output redirection: (Ex.) `echo "My first name is Nicole" > my_name.txt`.
  - Append a statement to a pre-existing file: (Ex.) `echo "My last name is Frontero" >> my_name.txt`.
* `cat`: Used to print out the contents of a file to the terminal.  (Ex.) `cat my_name.txt` would print out the contents of `my_name.txt` to the terminal.
* `cp` [file_path/file_name.extension] [new_location_path]: Copies a file from one place to another.  (Ex.) If you have the file `science.txt` in the Desktop of your computer and you want to move it to your current directory (represented by `.`, you would write something like this (what you actually write depends upon the paths on your computer): `cp ~/Desktop/science.txt .`.
  - `-r`: Required when copying a directory/folder. (Ex.) `cp -r test_folder ~/Desktop/bioinformatic_course`.
* `mv [file 1] [file 2]`: Short for "move".  Can be used to move a file to a different directory but can also be used as a way to rename a file by moving that file to the same directory but giving it a different name.
  - *Using `mv` to move a file to a new location:* (Ex.) `mv science.txt ../`.  This would move `science.txt` to the parent directory.
  - *Using `mv` to rename a file:* `mv science.txt science_is_cool.txt`.  This renames `science.txt` to `science_is_cool.txt`.



### Other

`echo`: 

* `-e`: recognizes escape characters.  

`sleep`: pauses for the number of seconds that you indicate in the sleep command.  Ex. `sleep 2`.  There is a 2 second pause after the time when someone puts the information and you display their answer.

`test` command and `[[]]` are interchangeable (I think):

`test -d code` tests if a directory exists

`if [[ -d code ]];then echo "directory exists";fi`

`colors=(red blue green)`
`echo {colors[0]}`
`echo ${colors[0]}`
`echo ${colors[*]}`
