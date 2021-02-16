# Lab 2a — First project and subprojects

##Lab goals
1. Configuring Git and Qt Creator to work with each other, and creating the first project in the process.
2. Understanding Qt Creator subprojects to create a more structured work environment.

--------------------------------

## Steps

## X11 Forwarding---Launching GUI applications on the server

As mentioned previously in Lab 1, we will be conducting all our software development on the CS Department servers. To do so, we will need to be able to run GUI applications on the server. In Lab 1, we were able to run terminal commands on the server via ssh. To enable GUI applications, we just need to specify one additional flag, the -X or -Y flag, when we ssh to the lab server.

For the rest of the course, hen you connect to the lab server, be sure to specify the -X or -Y flag (depending on your local system). This will create a session with X11 forwarding enabled.

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



## Troubleshooting X11 Connections
-X or -Y 

1. Install the latest copy of Qt Creator.
If you have an older copy of Qt Creator installed on your computer, remove it. Obtain a copy of the open-source version of Qt Creator via this link.


2. Check that Git and Qt Creator are configured by completing the Git and Qt tutorial (see Tutorials section).


3. Now it's time to add a new subproject. Right-click the top item in your repository (for me that is "qtrepo"), then select "New Subproject." Again choose "Non-Qt project > C++ project" and name it "tools."


4. Use the "tools" subproject for Lab 2b. Also, when creating new classes, use the "Add New ..." menu by right-clicking on the subproject name.

5. With Terminal, change directory into your repository and add any new files, perform a commit, and push the changes so your lab partner has access to everything.

6. You can experiment with the Git commands provided in the Tools menu, but you still need to work with the command line as you go along.

7. For the remainder of the project, you do not need to perform any branching — just focus on normal commits and pushes and pulls. The next part of the lab will just require you and your partner to work on separate classes.

## Git and QT Creator
