# MassEffectPermissionsGranter
Grants permissions to folders and registry keys for Mass Effect modding activities.

This program will request elevation when run. You can use the following parameters to perform a limited set of elevated tasks.
```
Usage:
PermissionsGranter.exe \"domain\\username\" [-create-directory directory] [-create-hklm-reg-key subkey] [FolderToGivePermissionsTo ] ...
      -create-directory <directory>
            Create specified directory and give the passed in user permissions to that folder.
      -create-hklm-reg-key <subkeypath>
            Creates a specified registry key under HKLM and assigns user permissions to it for editing.
            If the key already exists, it will just set permissions instead.

      Having no parameter before a path will default to granting permissions to a folder.
      You can chain commands together into a list to do all actions in one elevation run.
      ```
      
This program does not assign permissions to the Everyone group to limit the scope of permissons granting. Make sure you are passing the correct user to the program - if the user is running in a different context (such as elevated through UAC) you may be unable to determine which user you need to assign permisisons to.
