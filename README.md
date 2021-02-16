# Lab 2a—First project and subprojects

## Lab goals
1. Configuring Git and Qt Creator to work with each other, and creating the first project in the process.
2. Understanding Qt Creator subprojects to create a more structured work environment.

--------------------------------

## X11 Forwarding—Launching GUI applications on the server

As mentioned in Lab 1, we will be conducting all our software development on the CS Department servers. To do so, we will need to be able to run GUI applications remotely. In Lab 1, we ran terminal commands on the server via ssh. To enable GUI applications, we just need to specify one additional flag, the -X or -Y flag, when we ssh to the lab server.

For the rest of the course, when you connect to the lab server, be sure to specify the -X or -Y flag (depending on your local system). This will create a session with X11 forwarding enabled.

```
$ ssh -Y smithjus@139.147.9.XXX   # Use -Y on Windows
```
or
```
$ ssh -X smithjus@139.147.9.XXX   # Use -X on Mac and Linux
```


## Testing X11 Connection
Once you have connected to your account with the -X or -Y flag on the Department server launch a graphical application, such as:

```$ xclock```
or
```$ qtcreator```

You should see a clock (or the QT creator IDE) appear. (If you don't see anything immediatly, allow a minute or so for the command to be processed.) You can skip the next "Trobleshooting" section if the QT Creator GUI is visible.

## Troubleshooting X11 Connections

If you are on Mac, you may need to download and install [xQuartz](https://www.xquartz.org) to enable X11 forwarding. Once you have downloaded and installed xQuartz, from the terminal retry ssh -X command:

```
$ ssh -X smithjus@139.147.9.XXX   # Use -X on Mac and Linux
```


## Configure QT Creator and Git
In general, your workflow will be to (1) create a folder for each lab you are working on; (2) clone the repository for that lab into that folder; (3) then create a QT project in that folder. The subsequent steps will walk you through how to do that for the first time.

```
$ cd ~          # Make sure you are in your home directory
$ cd labs       # Keep all your labs in a dir called labs to keep things tidy :)
                # You may need to create this dir if you haven't already
$ mkdir lab-2a  # Make a new (appropriately named) dir for this lab
$ cd lab-2a     # Let's head into that new dir
```

Now clone the starter code from GitHub

```
$ git clone git@github.com:CS-205-S21/lab-2a.git  # Paste the clone string from GitHub here. Mine is here for reference, your string will be different...
```

Let's check to see that everything was cloned
```
$ ls
lab-2a
$ cd lab-2a
$ls -a     # The -a flag says show "all" files, including hidden files that start with '.'
.  ..  .git  .gitignore  README.md
```





2. Check that Git and Qt Creator are configured by completing the Git and Qt tutorial (see Tutorials section).


3. Now it's time to add a new subproject. Right-click the top item in your repository (for me that is "qtrepo"), then select "New Subproject." Again choose "Non-Qt project > C++ project" and name it "tools."


4. Use the "tools" subproject for Lab 2b. Also, when creating new classes, use the "Add New ..." menu by right-clicking on the subproject name.

5. With Terminal, change directory into your repository and add any new files, perform a commit, and push the changes so your lab partner has access to everything.

6. You can experiment with the Git commands provided in the Tools menu, but you still need to work with the command line as you go along.

7. For the remainder of the project, you do not need to perform any branching — just focus on normal commits and pushes and pulls. The next part of the lab will just require you and your partner to work on separate classes.

## Git and QT Creator
