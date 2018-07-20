# Shell Log

In **practice/**

Created Directory **shell-playground/**

`$ mkdir shell-playground`

- mkdir => make directory

Entering directory **shell-playground/**

`$ cd shell-playground`

- cd => change directory

Get Present Working Directory

`$ pwd`

- pwd => present working directory

Tag the result as *%1*

This gives us a exact location of the directory we r in

Lets go to root , **/** => root directory

`$ cd /`

This directory contains everything in the OS

Get Present Working Directory

`$ pwd`

Lets see whats in this directory

`$ ls`

- ls => list

Lets move around, entering **bin**

`$ cd Bin`

List again

`$ ls`

Lots of files,lets go back

`$ cd ..`

- .. => parent directory
- . => Current dirctory
- ~ => Home directory

lets go home

`$ cd ~`

Get Location 

`$ pwd`

Tag this as %2

**/home/saikat** => **root** then **home** directory then **saikat** derectory

Lets go to Playground, use *%1*

`$ cd %1`

List contents

`$ ls`

It should be empty

Lets create 3 directories

`$ mkdir games movies songs`

List containts

`$ ls`

Now you see 3 directories

Now lets create another directory in **games**, **strategy**

`$ mkdir games/stratergy`

Lets list the contents of **games**

`ls games`

Now lets create **fiction** within **books**

```
$ mkdir books
$ mkdir books/fiction
```

Possible wrong answer 

`$ mkdir books/fiction`

This gives an error

`mkdir: cannot create directory ‘books/fiction’: No such file or directory`

Shortcut

`$ mkdir -p books/fiction`

Lets Remove **movies**

`$ rmdir movies`

- rmdir => Remove directory

Check by `ls` to see its removed

Lets try to remove **books**

```
$ rmdir books/fiction
$ rmdir books
```

Possible Wrong solution

`$ rmdir books`

It gives a error

`rmdir: failed to remove 'books': Directory not empty`

Shortcut

`$ rmdir -p books/fiction`

Lets create some files **temp**,**hello**,**scripts**,**log**

`$ touch temp hello scripts log`

**Directory is a special type of file which contains more files**

Lets see which are directories and which are normal files

`$ ls -l`

- Minus ( - ) => Options
- ls -l => Long List

Output

```
total 8
drwxr-xr-x 3 saikat saikat 4096 Jul 20 13:22 games
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 hello
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 log
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 scripts
drwxr-xr-x 2 saikat saikat 4096 Jul 20 13:19 songs
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 temp
```

See the first column,one starting with **d** is a directory, rest are files

You can also see the time and date when the files are created

More options

`$ ls -lt`

- ls -lt => Long list sorted by time

Output

```
total 8
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 hello
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 log
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 scripts
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 temp
drwxr-xr-x 3 saikat saikat 4096 Jul 20 13:22 games
drwxr-xr-x 2 saikat saikat 4096 Jul 20 13:19 songs
```

`$ ls -lrt`

- ls -lrt => Long list sorted by time reversed


Output

```
total 8
drwxr-xr-x 2 saikat saikat 4096 Jul 20 13:19 songs
drwxr-xr-x 3 saikat saikat 4096 Jul 20 13:22 games
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 temp
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 scripts
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 log
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 hello
```

Lets create some hidden files

**Files starting with . are hidden**

`$ touch .mongo`

List to see that the file is not visible

`$ ls -a`

- ls -a => List all files(Hidden + Visible)

Output

```
.  ..  games  hello  log  .mongo  scripts  songs  temp
```

We can create hidden directories too

`$ mkdir .ucantseeme`

Lets see all of them

`$ ls -al`

Output

```
total 16
drwxr-xr-x 4 saikat saikat 4096 Jul 20 14:38 .
drwxr-xr-x 5 saikat saikat 4096 Jul 20 12:48 ..
drwxr-xr-x 3 saikat saikat 4096 Jul 20 13:22 games
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 hello
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 log
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:38 .mongo
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 scripts
drwxr-xr-x 2 saikat saikat 4096 Jul 20 13:19 songs
-rw-r--r-- 1 saikat saikat    0 Jul 20 14:14 temp
```



Feed ur Stomach
