# linux-command
Frequently used basic linux command references

# How to install ubuntu bash in windows 10?

  To install ubuntu bash in windows 10 first enable your developer mode with following steps.
  
  **Setting > Update & Security > For Developers** and select **Developer Mode**.
  
  Now go to **Turn Windows features on or off** you will find it in your control panel and select/check **Windows Subsystem for Linux (Beta)**. Click ok.
  
  Now you have two option to install ubuntu bash.
  
  **Option 1:**
  Press windows key and search `bash`. Press enter key selecting displayed bash command. The command will ask you to confirm your choice and enter a username and password for the user account in the Bash environment. 
  
  **Option 2:**
  Open windows command prompt and type 
  ```
  lxrun /install
  ```
 This process will also ask you to confirm your choice and enter a username and password for the user account in the Bash environment. 
 
 *To skip above process, you can run the following command instead. This command will automatically agree to the prompts, setting the “root” account as the default user account without a password. This is helpful if you want to automate the process of installing Bash in a script. In this process you don't need to set username and password during installation and also wont ask your root password if you use sudo command.*
 
 ```
 lxrun /install /y
 ```

# How to uninstall ubuntu bash in windows 10?
  
  To uninstall ubuntu bash from windows 10 you need to open windows command prompt and type following.
  ```
  lxrun /uninstall /full
  ```
  It will ask your confirmation for your uninstallation. Just press/type `y` it will do rest to uninstall.
  
  
# How to solve 'sudo: unable to resolve host user' problem in linux?
  
   If you are seeing **sudo: unable to resolve host user** in your screen while using `sudo` command, it means your host name is not present in `/etc/hosts` file. Host means your machine name. Suppose your machine name is **developer** then you must see **sudo: unable to resolve host developer** in your screen while using sudo command. You can check your host name in **/etc/hostname** file. To check your host name type following command and you must see **developer** as host name.
   
   ```
   cat /etc/hostname
   ```
 In case you are unable to see your host name because of permission use **sudo** before cat command like following:
 
 ```
 sudo cat /etc/hostname
 ```
 
Now add your host name in **/etc/hosts** file. To add you must edit your **/etc/hosts** file. Type following command which will open vim editor. Here is the steps to add your host name in **/etc/hosts** file.

1. Open terminal and type following command that will open vim editor 

```
sudo vi /etc/hosts
```

2. To edit this file you need to press *INSERT* command that is `I`. Just press `I`. Now you can edit this file.

3. Map your host name *developer* with ip address *127.0.0.1* like following.

```
127.0.0.1 developer
```

4. Press **ESC** key to skip editor and type following to write your changes in that file.

```
:w
```

Above command make changes your file.

5. Again type following to exit vim editor.

```
:q
```

You can verify whether your host name **developer** is maped with ip **127.0.0.1** or not. You can verify this with `cat /etc/hosts ` command. 

Now when you type any command follwoed by `sudo` command it will not display **sudo: unable to resolve host user**.
