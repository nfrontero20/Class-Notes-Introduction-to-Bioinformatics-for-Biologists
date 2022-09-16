### Commands

Commands contain 3 parts: 

```
[command] [options] [arguments]
```

**Options:** Options tweak the behavior of the command.  Represented by a hyphen `-`.

**Arguments:** Arguments can be files, raw data, or other options that the command requires. 







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
