## Goal  

Creating a symbolic link for an executable file in the **/usr/local/bin** folder is a common way to make a program or script accessible system-wide  
Symbolic links allow you to run the program from anywhere in the terminal without specifying its full path  
Here's how you can create a symbolic link for an executable file:

## Workflow  

### One By One  

  0. Move to the directory where you need the symbolic links first (your destination folder)
  1. **Locate the Executable File**: Make sure you know the full path to the executable file you want to create a symbolic link for.
     For this example, let's assume your executable file is located at **/path/to/your/executable**.
  2. **Create the Symbolic Link**: Use the **ln** command with the **-s** option to create a symbolic link.
     The general syntax is:
```bash
ln -s /path/to/your/executable /usr/local/bin/linkname # original folder => destination folder
```
Replace **/path/to/your/executable **with the actual path to your executable file and **linkname** with the desired name of the symbolic link  
(the name you'll use to run the program).

For example, if your executable is called **myprogram** and you want to create a symbolic link called **mylink**, you can run:  

```bash
ln -s /path/to/your/executable /usr/local/bin/mylink
```
  3. **Verify the Symbolic Link**: You can verify that the symbolic link has been created successfully by using the **ls** command with the **-l** option to list         the contents of the **/usr/local/bin directory**:
```bash
ls -l /usr/local/bin
```
  4. **Test the Symbolic Link**: You can now run your program using the symbolic link name (in this case,**mylink**) from any directory in your terminal:
```bash
mylink
```
This will execute the original executable file located at **/path/to/your/executable**.  

### All at once
If you want to create symbolic links for all executable files in one folder to another with designated link names  
you can achieve it in a single command using a combination of find, xargs, and ln. Here's how you can do it:  
```bash
find /path/to/source_folder -type f -executable -exec sh -c 'ln -s "$0" "/path/to/destination_folder/$(basename "$0")_link"' {} \;
```

  1. **find /path/to/source_folder -type f -executable**: This part of the command uses the find command to locate all executable files **(-type f -executable)**         within the specified source folder (/path/to/source_folder).
  2. **-exec sh -c 'ln -s "$0" "/usr/local/bin/$(basename "$0")_link"' {} \;**: For each executable file found
     this part of the command runs the **ln -s** command to create a symbolic link in the **/path/to/destination_folder/** directory with a designated link name.  

    - **sh -c 'ln -s "$0" "/usr/local/bin/$(basename "$0")_link"' {}** is a shell command that takes the found executable file ({}) and uses it to create a              symbolic link with the desired link name.  
    - **basename "$0"** extracts the filename without the path from the executable file.

    - **"$(basename "$0")_link"** appends "_link" to the filename to create the link name.

    - The symbolic link is created in the **/usr/local/bin** directory.

## Code  

```bash
ln -s /path/to/your/executable /usr/local/bin/linkname
```
