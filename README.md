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
