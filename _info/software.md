---
title: Software
layout: default
---

# Software to Install or Configure (and/or update as needed)


## Recommmended for Everyone


1. Zoom Client 

   Be sure that you have the *latest* version of the Zoom client.  Older versions may not have some of the features we'll need for this course.
    
   If you click on "About Zoom" inside zoom, you want a version that is 5.9.1 or later.
   
   Download it here: <https://zoom.us/download>

1. UCSB VPN Client (Pulse Secure)

   What it does:
   * Reroutes all your network traffic through the UCSB network, so that it appears that
     your machine is directly connected to the UCSB Campus network

   What it allows you to do:

   * Access the textbooks for the course online without having to buy them.
   * Mount your CSIL home directory as a shared network drive using Samba

   Where to get it:  <https://www.it.ucsb.edu/pulse-secure-campus-vpn/get-connected-vpn>

2. Samba Access to your CSIL home directory

   What it does:

   * Mounts your CSIL home directory "as if" it were connected directly to your
     computer.


   What it allows you to do:
   * Click on files on CSIL and open them in software on your own machine
     (e.g. an editor such as Sublime Text, VSCode, or a web browser.)

   Where to get it:
   * You don't have to download anything (though you do need the UCSB VPN Client first)
   * Instead, follow the instructions here:

     | Platform | Text Instructions | YouTube Video Instructions |
     |-|-|-|
     | MacOS | [Text](https://ucsb-cs156.github.io/topics/csil_mount_drive_to_macOs_using_samba/)  | [Video](https://youtu.be/FTlxjhjwbt0) |
     | Windows | [Text](https://ucsb-cs156.github.io/topics/csil_mount_drive_to_windows_using_samba/) | [Video](https://www.youtube.com/watch?v=fgORcrGWBH0) |
     | Linux | (ask staff) | |
     {:.table .table-sm .table-striped .table-bordered}

3. VSCode Text Editor for your local computer

   While `vim` and `emacs` are perfectly fine for the work you may have done in CS16/24/32, when it comes to 
   professional level application development, it's time to graduate to some more professional tools.
   
   We have found that VSCode (a free download for Windows/Mac/Linux) is in the sweet spot between too few features, and too complicated.
  
   If you haven't worked with it before, we suggest you download it and start getting used to it.
   
   What it does for you:
   * Autocompletion
   * Syntax highlighting and checking
   * Automatic import detection
   * Ability to see an entire directory tree at once
   * Search and replace across multiple files
   * and much much more...
   
   Download it here: <https://code.visualstudio.com/download>
  
<!-- 4. Docker

   Docker provides a way for you to run a standardized Linux environment inside another platform (whether that be Windows, Mac, or Linux).  It gives us the ability
   to have a consistent development environment, but running on your own machine.
   
   https://www.docker.com/products/docker-desktop
   
   We'll be recommending Docker as a platform for running the legacy code applications later in the quarter. -->

## Recommmended for MacOS Users

1. Brew (package manager)

   For MacOS, we'll be installing several packages for Java and JavaScript (node) development.  
   In many cases, installing those is easier if you *first* install the brew package manager.
   
   To install `brew`, visit <https://brew.sh/> and follow the instructions.
   
2. Java 17

   Yes, we want Java 17.  Not 8, Not 11, Not the early access to 18 or 19.  Java 17.

   You can download an installer from: <http://jdk.java.net/17/>

   To check if you now have Java 17, open a new Terminal window and do:

   ```
   java -version
   ```

   If it worked, you should see something like this:

   ```
   # java -version
   openjdk version "11.0.2" 2019-01-15
   OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.2+9)
   OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.2+9, mixed mode)
   ```

3. Maven

   After installing Java 11, you can use `brew`  to install maven:

   ```
   brew update
   brew install maven
   ```

   Or if you already have Maven installed, do this to upgrade your version to the latest one:

   ```
   brew update
   brew upgrade maven
   ```

   Then to check that it is installed, do:

   ```
   mvn --version
   ```

4. npm

   To install npm, do:
   
   ```
   brew update
   brew install npm
   ```
   
   Or to update to the latest version:

   ```
   brew update
   brew upgrade npm
   ```

 ## Recommmended for Windows Users
 
 TODO

