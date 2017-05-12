10 useful Windows command-line commands 
=======================================


This list includes some of the most useful and less known commands that you can run at Windows command prompt.

![](/img/posts/cmd.png)

1. Quickly create an empty file of an arbitrary size
---------------------------------------------------- 

    This command is useful if you quickly need a file of a certain size. The command execution is instantaneous (no matter what you put for length), but the file contains only zeros.

    ```sh
    fsutil file createnew filename length
    ```

2. Create a hardlink 

    A hardlink is useful when you want to make the same file appear in different folders. Even if you can see it in many places on your drive, the hard drive space is allocated for only one instance.

    The file is physically deleted when the last hardlink is removed.

    ```sh
    fsutil hardlink create new_filename existing_filename
    ```


3. Associate a path with a drive letter 

    The command is very useful for testing installation kits or running a CD from a folder. It basically creates a new drive letter that points to the indicated folder.

    ```sh
    subst [drive1: [drive2:]path]
    ```

4. Compares two binary files 

    This command is useful to check if two files are identical. Checking only the file sizes is not enough since the content may be different.

    The fc command, with /b switch, compares the files in binary mode and tells if they are identical or not.

    ```sh
    fc /B [drive1:][path1]filename1 [drive2:][path2]filename2
    ```

5. Create a list with all files in a given folder 

    ```sh
    dir *.doc /b > documents.txt
    ```

    If you want to search also in the subfolders, add the /s switch in the above command line.

    ```sh
    dir /s *.doc /b > documents.txt
    ```

6. Concatenate two files 

    This command can be used to concatenate both text and binary files.

    ```sh
    copy /b a.txt + b.txt c.txt
    ```

7. Check if a server is up 

    When a machine (internal server, web site, etc) doesn’t respond from the regular application, try to open a command prompt and ping that machine.

    Ping can be also used to find the IP behind a web address.

    ```sh
    ping itobserver.blogspot.com
    ```

8. Display network configuration and IP addresses 

    If you are using a DHCP server in your network, then you can use this command to check the IP address leased to your computer.

    ```sh
    ipconfig /all
    ```

9. Lock workstation 

You can lock your workstation by running this command.

    ```sh
    rundll32.exe user32.dll,LockWorkStation
    ```
    
10. Shutdown local computer 

You can use this command to automate the process of computer shutdown. Some prefer to put it as a link on the desktop.

    ```sh
    shutdown -s -f -t 00 
    ```

Article reposted from [www.itobserver.net](http://www.itobserver.net/2007/09/10-useful-windows-command-line-commands.html) blog.
