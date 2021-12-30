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
  
  
4. Install Java 17 on your local system.  Please install Java 17, and NOT Java 8, Java 11, or a preview version of Java 18 or 19.   It won't matter for the 
   `"Hello World"` program in the first week, but when we move on to complex Java applications involving third-party libraries, it will definitely matter.
   
   For Mac users, instructions for installing with Homebrew appear below.
  
<!-- 4. Docker

   Docker provides a way for you to run a standardized Linux environment inside another platform (whether that be Windows, Mac, or Linux).  It gives us the ability
   to have a consistent development environment, but running on your own machine.
   
   https://www.docker.com/products/docker-desktop
   
   We'll be recommending Docker as a platform for running the legacy code applications later in the quarter. -->

## Recommmended for MacOS Users

1. Command Line Tools XCode for MacOS, including `git`

   On MacOS, `git` typically gets installed as part of the "Command Line XCode Tools" the first time you ask to use it.  To be sure that `git` is installed,
   try typing:
   
   ```
   git --version
   ```
   
   If it shows something like this, you are good:
   
   ```
   git version 2.24.3 (Apple Git-128)
   ```

   Otherwise, you might get a message that you need to install the XCode Command Line Tools.  In that case, please just follow the instructions given.

1. Brew (package manager)

   For MacOS, we'll be installing several packages for Java and JavaScript (node) development.  
   In many cases, installing those is easier if you *first* install the brew package manager.
   
   To install `brew`, visit <https://brew.sh/> and follow the instructions.
   
2. Java 17

   
   To install Java with homebrew, use:
   
   ```
   brew update
   brew install openjdk@17
   ```
   
   Then you must do this step, which is documneted in the output that shows up when you run the `brew install openjdk@17` command:
   
   ```
   sudo ln -sfn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk
   ```

   To check if you now have Java 17, open a new Terminal window and do:

   ```
   java -version
   ```

   If it worked, you should see something like this:

   ```
   # java -version
   openjdk 17.0.1 2021-10-19
   OpenJDK Runtime Environment Homebrew (build 17.0.1+1)
   OpenJDK 64-Bit Server VM Homebrew (build 17.0.1+1, mixed mode, sharing)
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

4. nvm (Node Version Manager)

   To install nvm, do:
   
   ```
   brew update
   brew install nvm
   ```
   
   Or to update to the latest version:

   ```
   brew update
   brew upgrade nvm
   ```
   
   To see if it installed properly:
   
   ```
   nvm --version
   ```

   This should produce output such as `0.39.1` as opposed to `command not found: nvm`
   
   You may then need to put the following lines in your `~/.zshrc` 
   
   ```
   export NVM_DIR=~/.nvm

   [[ -f $(/usr/local/bin/brew --prefix nvm)/nvm.sh ]] && source $(/usr/local/bin/brew --prefix nvm)/nvm.sh && nvm use 14
   ```
   
   Note that the part that says `nvm use 14` is current as of right now; if for some reason we decide to use a different version of node,
   that can be changed (e.g. to `nvm use 15` or `nvm use 16`, etc.)
   
5. `npm` (Node Pacakge Manager)

   If you used `nvm` to select and install a version of `node`, the `npm` package manager likely just came along for the ride when you installed `node`.  But you can update the version to the latest one
   by typing:
   
   ```
   npm install -g npm
   ```
   

   
 ## Recommmended for Windows Users
 
 Install Windows Subsystem for Linux.

 It turns out that almost everything in terms of installing software (Java, Maven, Node, etc.) is easier under Linux than under native Windows.
 Therefore we strongly suggest that if you have a Windows environment, you install the Windows Subsystem for Linux (WSL) and then follow the 
 instructions under Linux/WSL.
    
 If you are unable to install WSL because of limitations on your machine, please reach out to the course staff via Slack using the [help-windows channel on Slack](https://ucsb-cs156-w22.slack.com/archives/C02SY4JSJ3S).   In that case, we will try to find an alternative for you.
 
 TODO: Add some instructions (or pointers to instructions) for installing WSL.
 
 ## Recommended for Linux/WSL Users
 
TODO: Put in advice here on installing the following on Linux/WSL:

* git (should be preinstalled)
* Java 17
* Maven
* Recommended version of Node



