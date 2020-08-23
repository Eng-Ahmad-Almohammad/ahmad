# *Text Editor.*
## When I first started out learning about web development, one of the things that I felt compelled to do was to download a text editor. I figured that I was going to be writing a good deal of code, and a good text editor should help me do that.
## 1. The Command Line!
## Linux has a graphical user interface and it works pretty much like the GUI's on other systems that you are familiar with such as Windows and OSX.
### A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.
1. Opening a Terminal.
#### Opening a terminal is fairly easy. I can't tell you exactly how to do it as every system is different but here are a few places to start looking.
##### If you're on a Mac then you'll find the program Terminal under Applications -> Utilities. An easy way to get to it is the key combination 'command + space' which will bring up Spotlight, then start typing Terminal and it will soon show up.
##### If on Linux then you will probably find it in Applications -> System or Applications -> Utilities. Alternatively you may be able to 'right-click' on the desktop and there may be an option 'Open in terminal'.
##### If you are on Windows and intend to remotely log into another machine then you will need an SSH client. A rather good one is Putty (free) .
2. The Shell, Bash.
##### Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called *bash* which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.
##### If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. *echo* is a command which is used to display messages.
3. Shortcuts.
##### The terminal may seem daunting but don't fret. Linux is full of shortcuts to help make your life easier. You'll be introduced to several of them throughout this tutorial. Take note of them as not only do they make your life easier, they often also save you from making silly mistakes such as typos.
##### Here's your first shortcut. When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys. So don't bother re-typing out commands you have previously entered, you can usually just hit the up arrow a few times. You can also edit these commands using the left and right arrow keys to move the cursor where you want.
## 2. Basic Navigation!
### In this section, we'll learn the basics of moving around the system. Many tasks rely on being able to get to, or reference the correct location in the system. As such, this stuff really forms the foundation of being able to work effectively in Linux. Make sure you understand it well.
#### a. The first command we are going to learn is *pwd* which stands for Print Working Directory. The command does just that. It tells you what your current or present working directory is. Give it a try now.
#### b. It's one thing to know where we are. Next we'll want to know what is there. The command for this task is *ls*. It's short for list. Let's give it a go.
## c. Paths
### In the previous commands we started touching on something called a path. I would like to go into more detail on them now as they are important in being proficient with Linux. Whenever we refer to either a file or directory on the command line, we are in fact referring to a path. ie. A path is a means to get to a particular file or directory on the system.
### Absolute and Relative Paths.
#### There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.
## d. Let's Move Around a Bit.
### In order to move around in the system we use a command called *cd* which stands for change directory.
## 3. More About Files!
### After the previous section I'm sure you're keen and eager to get stuck into some more commands and start doing some actual playing about with the system. We will get to that shortly but first we need to cover some theory so that when we do start playing with the system you can fully understand why it is behaving the way it is and how you can take the commands you learn even further. That is what this section and the next intend to do. After that it will start getting interesting, I promise.
## a. Everything is a File
### Ok, the first thing we need to appreciate with linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.
## b. Linux is an Extensionless System.
### This one can sometimes be hard to get your head around but as you work through the sections it will start to make more sense. A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is. The following are common extensions:
#### 1. file.exe - an executable file, or program.
#### 2. file.txt - a plain text file.
#### 3. file.png, file.gif, file.jpg - an image.
### n other systems such as Windows the extension is important and the system uses it to determine what type of file it is. Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file. As such it can sometimes be hard to know for certain what type of file a particular file is. Luckily there is a command called *file* which we can use to find this out.
### Now you may be wondering why I specified the command line argument above as path instead of file. If you remember from the previous section, whenever we specify a file or directory on the command line it is actually a path. Also because directories (as mentioned above) are actually just a special type of file, it would be more accurate to say that a path is a means to get to a particular location in the system and that location is a file.
## c. Linux is Case Sensitive.
### This is very important and a common source of problems for people new to Linux. Other systems such as Windows are case insensitive when it comes to referring to files. Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.
### Also be aware of case sensitivity when dealing with command line options. For instance with the command ls there are two options s and S both of which do different things. A common mistake is to see an option which is upper case but enter it as lower case and wonder why the output doesn't match your expectation.
## d. Spaces in names.
### Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. They are how we know what is the program name and can identify each command line argument. If we wanted to move into a directory called *Holiday Photos* for example the following would not work.
### What happens is that Holiday Photos is seen as two command line arguments. cd moves into whichever directory is specified by the first command line argument only. To get around this we need to identify to the terminal that we wish Holiday Photos to be seen as a single command line argument. There are two ways to go about this, either way is just as valid.
## Quotes
#### The first approach involves using quotes around the entire item. You may use either single or double quotes (later on we will see that there is a subtle difference between the two but for now that difference is not a problem). Anything inside quotes is considered a single item.
## Escape Characters.
#### Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.
## e. Hidden Files and Directories.
### Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . (full stop) then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.
### To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command *ls* which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option *-a* so that it does show hidden files and directories.
