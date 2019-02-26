## File Operations:

1. Create the following directory structure.

```
hello
├── five
│   └── six
│       ├── c.txt
│       └── seven
│           └── error.log
└── one
    ├── a.txt
    ├── b.txt
    └── two
        ├── d.txt
        └── three
            ├── e.txt
            └── four
                └── access.log
```

`hello`, `one`, `two`, `three`, `four`, `five`, `six`  and `seven` are directories. The remaining items are empty files. 

2. Print the locations of all the `txt` files in `hello` and its subdirectories.

3. Delete all the files with the `.log` extension.

4. Add the following content to `a.txt`

```
Unix is a family of multitasking, multiuser computer operating systems that derive from the original AT&T Unix, development starting in the 1970s at the Bell Labs research center by Ken Thompson, Dennis Ritchie, and others.
```


5. Compress the `hello` directory into a `zip` file

6. Copy all the `contents` of `hello` into another directory called `world`

7. Delete the `hello` directory

________

## Harry Potter

1. Download the contents of "Harry Potter and the Goblet of fire" using the command line from https://raw.githubusercontent.com/bobdeng/owlreader/master/ERead/assets/books/Harry%20Potter%20and%20the%20Goblet%20of%20Fire.txt

2. Print the first three lines in the book

3. Print the last 10 lines in the book

Use pipes to solve the following problems:

Refer 

* https://swcarpentry.github.io/shell-novice/04-pipefilter/index.html
* https://ryanstutorials.net/linuxtutorial/piping.php
* https://www.geeksforgeeks.org/piping-in-unix-or-linux/

to learn about pipes

4. How many times do the following words occur in the book?
    * Harry
    * Ron
    * Hermione
    * Dumbledore

5. Print lines from 100 through 200 in the book

6. How many unique words are present in the book?

___________

## Processes

1. List your browser's process ids (pid) and parent process ids(ppid)
2. Stop the browser application from the command line
3. List the top 3 processes by CPU usage.

____________

## Managing software

Use `apt` (Ubuntu) or `homebrew` (Mac) to:


1. Install `git`, `vim` and `nginx`
2. Uninstall `nginx`
_____________

## Misc

1. What's your local ip address?
2. Find the ip address of `google.com`
3. Where is the `python` command located? What about `python3`?
