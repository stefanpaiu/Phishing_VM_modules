# Security Challenge Modules

This repository contains a bunch of puppet modules to setup computer security
based challenges inside a virtual machine. Most of the modules include their
own documentation but for more general documentation then checkout the
[\_docs folder](_docs).

**These puppet modules contain security vulnerabilities and are not intended
for live machines.**

## Overview of the included modules

### Exercise modules

| Module Name                                          | Current Module Status | [SecGen Framework Supported](https://github.com/SecGen/SecGen) | Brief Description                                         |
| ---------------------------------------------------- | --------------------- | -------------------------------------------------------------- | --------------------------------------------------------- |
| [phishing](./phishing)                               | prototype             | no                                                             | Prototype for sending phishing emails to scripted victims |

### Helper modules

| Module Name                    | Current Module Status | [SecGen Framework Supported](https://github.com/SecGen/SecGen) | Brief Description                                                   |
| ------------------------------ | --------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------- |
| [gateway](./gateway)           | done                  | no                                                             | Configures a container to be a network gateway                      |
| [genuser](./genuser)           | done                  | no                                                             | Creates users easier than puppet does                               |
| [mailserver](./mailserver)     | usable                | no                                                             | Configures a postfix/dovecot unencrypted mailserver                 |
| [puppetdocker](./puppetdocker) | usable                | no                                                             | Creates containers and networks to simulate the internet            |
| [sshserver](./sshserver)       | done                  | no                                                             | Configures an ssh server for password authentication and root login |

### Package installer modules

| Module Name                  | Current Module Status | [SecGen Framework Supported](https://github.com/SecGen/SecGen) | Brief Description                               |
| ---------------------------- | --------------------- | -------------------------------------------------------------- | ----------------------------------------------- |
| [adobereader](./adobereader) | done                  | no                                                             | Installs Adobe Reader 8.1.2 through wine        |
| [metasploit](./metasploit)   | done                  | no                                                             | Installs metasploit                             |
| [wine](./wine)               | done                  | no                                                             | Installs wine for windows applications in linux |
| [wireshark](./wireshark)     | done                  | yes                                                            | Installs wireshark                              |
