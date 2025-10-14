# bash

# Command line arguments

We use the variables **$1** to represent the first command line argument, **$2** to represent the second command line argument and so on.

simple example:
> ./copy.sh ht-omni-v3 ht-omni-v3-update
> ```
> #!/bin/bash
> 
> cp -rp $1 $2
> 
> echo "Copied successfully"
> ```

There are a few other variables that the system sets for you,
```
* $0 - The name of the Bash script.
* $1 - $9 - The first 9 arguments to the Bash script. (As mentioned above.)
* $# - How many arguments were passed to the Bash script.
* $@ - All the arguments supplied to the Bash script.
* $? - The exit status of the most recently run process.
* $$ - The process ID of the current script.
* $USER - The username of the user running the script.
* $HOSTNAME - The hostname of the machine the script is running on.
* $SECONDS - The number of seconds since the script was started.
* $RANDOM - Returns a different random number each time is it referred to.
* $LINENO - Returns the current line number in the Bash script.
```

# Variables

Like any other programming language, **variable** is a temporary store for a piece of information. \

`name="surya"`

Note there is no space on either side of the equals (=) sign. \
Variable names can be upper, lower case. But bash is case sensitive.
Single quotes will treat every character literally. \
Double quotes will allow you to do substitution (that is include variables within the setting of the value). \

eg:
```
firstname="Surya"
place="Home"
message="Hi $firstname, welcome $place"
```

* Command substitution
Command substitution allows us to take the output of the command/program & save it in the variable.
```
myvar=$( ls /etc | wc -l )
echo There are $myvar entries in the directory /etc
```

One form of user input is command line argument. Now introducing you to another user input method is **READ**

```
#!/bin/bash
# Ask the user for their name
echo Hello, who am I talking to?
read fullname
echo "It's nice to meet you $fullname"
```

read - command saves the user response in the variable $fullname
