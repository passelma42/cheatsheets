## Goal  

Creating a symbolic link for an executable file in the **/usr/local/bin** folder is a common way to make a program or script accessible system-wide  
Symbolic links allow you to run the program from anywhere in the terminal without specifying its full path  
Here's how you can create a symbolic link for an executable file:

## Workflow   

  1. **Locate the Executable File**: Make sure you know the full path to the executable file you want to create a symbolic link for.
     For this example, let's assume your executable file is located at **/path/to/your/executable**.
  2. **Create the Symbolic Link**: Use the **ln** command with the **-s** option to create a symbolic link.
     The general syntax is:
```bash
ln -s /path/to/your/executable /usr/local/bin/linkname
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

## Code  

```bash
ln -s /path/to/your/executable /usr/local/bin/linkname
```
