# Phishing VM

This repository contains Puppet modules to setup computer security challanges inside
a virtual machine. The project as a whole acts like a simulation of how a user, called
'Hacker' would be given an virtual environment and will try to find security breaches
and exploit them. 

**The project as a whole is intended to show the possible vulnerabilities created by 
Phishing and test users' skills learned from the Documentation.**

**These Puppet modules contain security vulnerabilities and are not intended for live
machines.**  

## Overview of the included modules

### Exercise modules

#### Phishing

The phishing module creates a phishing-friendly environment for the purpose to learn how to create attacks
and prevent them from your day-to-day routine. There are 3 (hopefully 5) ways to test your newly learned skills:

-   Web/Email
-   PDF files
-   Macros (VBA)

    *Requirements:*

    -   puppetlabs-java module
    ```
    puppet module install puppetlabs-java --version 1.6.0
    ```

    -   puppetdocker module
    -   metasploit module
    -   mailserver module
    -   sshserver module
    -   genuser module

    *General configuration:*

    This module provides a web server and a email server for an attacker to breach into secondary containers (the victims). Those secondary containers are preset so that the attacker has to first notice the vulnerabilities given a website and then think of the appropriate attack for each victim. The setup is as follows:

    - **Attacker user** (uses metasploit for attacks. In the configuration, the attacker is simply the main user on the VM that has access to the servers);
    - **Email server** (processes the emails sent between the attacker and the victim)
    - **Webserver** running a hiring website (used for pdf and macros attacks)
    - **Victim users** (multiple containers running a script which will behave accordingly depending on the user. It will open unread emails and their attachments and access the files on the webserver. This depends on who the victim is, the position they have and their background. This information comes from the website and can be found in the Solutions document. Will also have preinstalled Acrobat Reader 8.1.2 and Libreoffice)


