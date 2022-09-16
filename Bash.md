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
* *Absolute path:* The absolute path always starts from the root directory (`/`).  (Eg.) `/Users/nicolefrontero`.
* *Relative path:* The relative path starts from the current directory

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
