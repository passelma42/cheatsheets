# Untar  

##Goal  
To unpack a tar.gz (also known as a .tar.gz or .tgz) file to another folder, you can use the tar command in a terminal or command prompt.  

##Workflow  

  1. Open a terminal or command prompt on your computer.  
  2. Navigate to the folder where the tar.gz file is located using the cd command. For example, if your tar.gz file is on the desktop and you want to extract it to a folder named "my_folder,"  
     you can navigate to the desktop like this (replace "your_username" with your actual username):
```bash
cd /home/your_username/Desktop
```
  3. Once you're in the correct directory, use the tar command to unpack the tar.gz file to another folder.
     Here's the basic command structure:
```bash
tar -xzvf file.tar.gz -C /path/to/destination_folder
    # -x: Extract the archive.
    # -z: Use gzip compression.
    # -v: Verbose mode (optional, for displaying progress).
    # -f: Specify the filename of the archive.
    # -C: Specify the destination folder where you want to extract the contents.
```
Replace file.tar.gz with the name of your tar.gz file and /path/to/destination_folder with the path to the folder where you want to extract the contents.  
If you want to extract it in the current directory, you can omit the -C option.

For example, if you want to extract a file called "example.tar.gz" to a folder named  
"my_folder" on the desktop, the command would look like this:
```bash
tar -xzvf example.tar.gz -C /home/your_username/Desktop/my_folder
```

##Code  

```bash
tar -xzvf example.tar.gz -C /home/your_username/Desktop/my_folder
```
