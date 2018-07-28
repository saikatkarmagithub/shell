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

Lets Delete a file **log**

`$ rm log`

- rm => Remove (Not For Direcroies)

Lets take an assignment

#### Problem Description

- Create a directory **assignment-1**
- Go inside it
- Create another directory **actors** with directory **heroes** within it
- Create five heroes files within **assignment-1/actors/heroes**
  - **tej**
  - **shahrukh**
  - **vijay**
  - **rao**
  - **mahesh**
- Hide **rao** and **mahesh**
- Create a directory **heroine** in **assignment-1/actors**
- Create two files
  - **samantha**
  - **kajal**
- Now create a hidden directory **underrated**
- Create three files which are hidden
  - **nawaz**
  - **saswato**
  - **boomba**
- Check your work that you have done it correctly
- *Bonus: Use `tree` command*
- delete everything


#### SOLUTION

Create block
```
$ mkdir -p assignment-1/actors/heroes
$ cd assignment-1/actors/heroes
$ touch tej shahrukh vijay rao mahesh
$ rm rao mahesh
$ touch .rao .mahesh
$ cd ..
$ mkdir heroines
$ cd heroines
$ touch samantha kajal
$ cd ..
$ mkdir .underrated
$ cd .underrated
$ touch .nawaz .saswato .boomba
$ cd ../..
```

Use *tree* command

`$ tree`

OUTPUT
```
.
└── actors
    ├── heroes
    │   ├── shahrukh
    │   ├── tej
    │   └── vijay
    └── heroine
        ├── kajal
        └── samantha
```

`$ tree -a`

OUTPUT
```
.
└── actors
    ├── heroes
    │   ├── .mahesh
    │   ├── .rao
    │   ├── shahrukh
    │   ├── tej
    │   └── vijay
    ├── heroine
    │   ├── kajal
    │   └── samantha
    └── .underrated
        ├── .boomba
        ├── .nawaz
        └── .saswato

```

Starting Delete

```
$ cd assignment-1/actors/heroes
$ rm tej shahrukh vijay .rao .mahesh
$ cd ../heroines
$ rm samantha kajal
$ cd ../.underrated
$ rm .nawaz .boomba .saswato
$ cd ..
$ rmdir heroes heroines .underrated
$ cd ..
$ rmdir actors
$ cd ..
$ rmdir assignment-1
```

Shortcut
`rm -r assignment-1`

- rm -r => recursive delete

Turn the create block into a script, save this as **assign1-create.sh**

Add this line at top
`#!/bin/sh`

Lets run this script

`$ sh assign1-create.sh`

Simillarly create a shell script for delete **assign1-delete.sh**

Lets rename some files **hello** into **renamed-hello**

`$ mv hello renamed-hello`

- mv => Move

`$ ls` to check its renamed

Lets move **songs** and **scripts** into **games**

`$ mv songs scripts games/`

Last argument is the destination