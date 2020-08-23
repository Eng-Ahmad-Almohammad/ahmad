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
#### The first command we are going to learn is **pwd** which stands for Print Working Directory. The command does just that. It tells you what your current or present working directory is. Give it a try now.