## Goal  
A permanent environmental variable, also known as a persistent environmental variable or a system-wide environmental variable, is a variable that is set in the system and remains available across different sessions and even after system reboots. These variables are not limited to a specific user or terminal session and are accessible by all users and processes on the system.

Permanent environmental variables are often used to configure system-wide settings or to provide information that various applications or services running on the system may need to access.

In Unix-like operating systems (including Linux), permanent environmental variables are typically set in system-wide configuration files, such as:

- /etc/environment: This file is used to set system-wide environmental variables that should be available to all users and processes.  

- /etc/profile.d/: You can create custom script files in this directory with a .sh extension to set system-wide environmental variables. These scripts are executed when users log in.  

- /etc/profile: This is a system-wide shell initialization script where you can set environmental variables and configure the system's default environment for all users.  

- /etc/bash.bashrc: On some systems, this file is sourced by /etc/profile and can be used to set system-wide Bash-specific environmental variables.  

It's important to note that setting permanent environmental variables often requires administrative privileges (root access) because they affect the entire system. Users can typically set their own user-specific environmental variables in their own ~/.bashrc or ~/.bash_profile files, but these are specific to their user accounts and not system-wide.

Permanent environmental variables are useful for configuring various aspects of the system, such as default paths, system-wide settings, and global configurations that need to be accessible to all users and processes.

## Workflow  

## Code  

