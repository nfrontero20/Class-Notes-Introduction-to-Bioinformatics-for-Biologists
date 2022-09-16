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

### Creating, Modifying, and Deleting Files and Directories
* `touch`: (Ex.) `touch my_file.txt`.
* `echo "statement" > file_name.extension`: This is called *output redirection*.  The output from a command using echo like `echo "My first name is Nicole"` usually gets printed to the terminal.  However, you can redirect the output using `>` and save the output `"My first name is Nicole"` to a file.  (Ex.) `echo "My first name is Nicole > my_name.txt"`.
* `echo "Statement to append" >> file_name.extension`: You can append a statement to a file through using `echo` and `>>`.  (Ex.) `echo "My last name is Frontero >> my_name.txt"`.
* `nano file_name.extension`: Creates a file using the editor `nano`.
* `rm`: Stands for "remove".
  - `rm`: Can be used to remove a file.
  - `rm -r`: can be used to *recursively* remove all of the files within a directory.  Must use the `-r` option to get rid of a directory.
* `rmdir`: Stands for "remove directory".  Can only be used to remove empty directories.

### Wildcards
* `*`: Represents any number of characters that are wildcards.
* `?`: Represents only one wildcard character.

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
* `touch [file_name.extension]:` Creates a file, or multiple files, depending upon how many you list.  (Ex.) `touch file1 file2` creates two files, `file` and `file2`.
* `echo`: Can be used to...
  - Print a statement to the terminal: (Ex.) `echo "My first name is Nicole"`.
  - Create a file using output redirection: (Ex.) `echo "My first name is Nicole" > my_name.txt`.
  - Append a statement to a pre-existing file: (Ex.) `echo "My last name is Frontero" >> my_name.txt`.
* `cat`: Used to print out the contents of a file to the terminal.  (Ex.) `cat my_name.txt` would print out the contents of `my_name.txt` to the terminal.
* `less:` Used to print out the contents of a file to the terminal, but the file's contents are only shown one page at a time.  Press "q" on the keyboard to get out of seeing the different pages and return to being able to type in the terminal.  Can also be used to do a simple pattern search in a file.  
  - To do a simple pattern search, type `less [file_name.file_extension]`.  Then, type `/[search_term]`.  The desired search term will be highlighted if it appears in the document.  You can skip to the next occurrence of the search term by pressing "n".  To exit, press "q".
* `head:` Used to print out the first 10 lines of a file to the terminal.
  - `-[number]`: An option can be used with `head` to indicates how many lines of a file you want to show.  (Ex.) `head -20 science.txt` prints out the first 20 lines of the file.  
* `tail:` Used to print out the last 10 lines of a file to the terminal.
  - `-[number]`: An option can be used with `tail` to indicates how many of the final lines of a file you want to show.  (Ex.) `tail -20 science.txt` prints out the last 20 lines of the file. 
* `cp` [file_path/file_name.extension] [new_location_path]: Copies a file from one place to another.  (Ex.) If you have the file `science.txt` in the Desktop of your computer and you want to move it to your current directory (represented by `.`, you would write something like this (what you actually write depends upon the paths on your computer): `cp ~/Desktop/science.txt .`.
  - `-r`: Required when copying a directory/folder. (Ex.) `cp -r test_folder ~/Desktop/bioinformatic_course`.
* `mv [file 1] [file 2]`: Short for "move".  Can be used to move a file to a different directory but can also be used as a way to rename a file by moving that file to the same directory but giving it a different name.
  - *Using `mv` to move a file to a new location:* (Ex.) `mv science.txt ../`.  This would move `science.txt` to the parent directory.
  - *Using `mv` to rename a file:* `mv science.txt science_is_cool.txt`.  This renames `science.txt` to `science_is_cool.txt`.
* `grep [options] [search_term] [file_name.file_extension]`:
  - `-i`: Not sure, but probably stands for **ignore** case.  This option allows you to search for a term and not worry about if it's capitalized or not in the file.
  - `n`: Not sure, but probably stands for line **number**.  This option provides the line numbers for the lines where the pattern occurs in the file.
  - `-v`: No idea what this stands for.  This option provides the lines that *do not* contain the searched for pattern.  
  - `-c`: Not sure, but probably stands for **count**.  This option returns the number of lines that contain searched for pattern. 
* `wc [file_name.file_extension]`: Stands for "word count". Returns, from left to right, the number of *lines*, *words*, and *characters*.
  - `-l`: This option results in only the number of lines being printed.
  - `-w`: This option results in only the number of words being printed.
  - `-c`: This option results in only the number of chatacters being printed.
* 

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
