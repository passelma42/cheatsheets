## Goal  
A permanent environmental variable, also known as a persistent environmental variable or a system-wide environmental variable, is a variable that is set in the system and remains available across different sessions and even after system reboots. These variables are not limited to a specific user or terminal session and are accessible by all users and processes on the system.

Permanent environmental variables are often used to configure system-wide settings or to provide information that various applications or services running on the system may need to access.

In Unix-like operating systems (including Linux), permanent environmental variables are typically set in system-wide configuration files, such as:

- **/etc/environment**: This file is used to set system-wide environmental variables that should be available to all users and processes.  

- **/etc/profile.d/**: You can create custom script files in this directory with a .sh extension to set system-wide environmental variables. These scripts are executed when users log in.  

- **/etc/profile**: This is a system-wide shell initialization script where you can set environmental variables and configure the system's default environment for all users.  

- **/etc/bash.bashrc**: On some systems, this file is sourced by /etc/profile and can be used to set system-wide Bash-specific environmental variables.  

It's important to note that setting permanent environmental variables often requires administrative privileges (root access) because they affect the entire system. Users can typically set their own user-specific environmental variables in their own ~/.bashrc or ~/.bash_profile files, but these are specific to their user accounts and not system-wide.

Permanent environmental variables are useful for configuring various aspects of the system, such as default paths, system-wide settings, and global configurations that need to be accessible to all users and processes.

## Workflow   

### User specific  

To create a permanent environmental variable in your ~/.bashrc file in Bash, you can follow these steps:  
  1. Open a terminal window.
  2. Use a text editor to open your ~/.bashrc file. You can use a command-line text editor like nano, vim, or gedit.
     For example, to open it with nano, you can use the following command:  
```bash
nano ~/.bashrc
```
  3. Scroll to the bottom of the ~/.bashrc file to add your environmental variable
     Environmental variables are typically written in the format export VARIABLE_NAME="variable_value".
     Replace VARIABLE_NAME with the name of your variable and variable_value with the desired value.
     For example, to create an environmental variable named MY_VAR with a value of "example_value," add the following line to ~/.bashrc:
```bash 
export MY_VAR="example_value"
```
  4. Save the file and exit the text editor. In nano, you can do this by pressing Ctrl + O, then pressing Enter to confirm, followed by Ctrl + X to exit.
  5. To make the changes take effect, you can either close and reopen your terminal or source the ~/.bashrc file using the following command:
```bash
source ~/.bashrc
```
  6. You can verify that your environmental variable is set by running:
```bash
echo $MY_VAR
```

For example, to create an environmental variable named MY_VAR with a value of "example_value," add the following line to ~/.bashrc:
### System wide (all users)  

## Code  

