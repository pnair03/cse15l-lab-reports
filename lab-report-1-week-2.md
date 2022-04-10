# Week 2 Lab Report

This lab report will contain a tutorial about how to log in to a course-specific account on `ieng6`. 

> Installing VScode

The first step is to install [Visual Studio Code](https://code.visualstudio.com/).

After installing and opening VScode, my screen looked like this:

![Image](ss1.png)

While some differences may exist, everybody's starting page shou.d look relatively the same. 

> Remotely Connecting

I first looked up my course-specific account here:
https://code.visualstudio.com/

Everybody's username should start with `cs15lsp22`, and it will be followd by three letters.

The first step I took to remotely connect to the server is opening a terminal in VScode:

![Image](ss2.png)

I then typed the following command:

`ssh <my_account_name>@ieng6.ucsd.edu`

Since it is my first time logging in, it asked me to confirm my log-in. After clicking "yes," I entered in my password (will not be visible when entering). The following output was part of what should be visible if the password is entered correctly:

![Image](ss3.png)

I am now connected remotely!

> Trying Some Commands

Here are screenshots of my trying some commands on the remote computer.

![Image](ss4.png)

![Image](ss5.png)

Here are some other commands that can be tried:
* `ls -lat`
* `cd ~`
* `cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/`
* `cat /home/linux/ieng6/cs15lsp22/public/hello.txt`
* `mkdir <directory/file name>`

> Moving Files with `scp`

To try moving files using `scp`, I first created `WhereAmI.java` and typed the following:
```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```

After running this on my personal computer by using `javac` and `java`, I entered the following line in the terminal:

`scp WhereAmI.java <my_account_name>@ieng6.ucsd.edu:~/`

I then logged back in using `ssh`, and I ran the file on the remote computer. Here is the output:

![Image](ss6.png)

> Setting an SSH Key

 


