## Creating Alias in Windos Powershell

Aliases are very handy techniques to quickly get your terminal commands executed. With the help of aliases, you can execute large/multiple commands at the same time with just a word. So here's how you can create aliases in Windows Powershell:

```
New-Alias -Name <alias_keyword> -Value <command_or_path_to_executable>
```

The syntax is just this simple.

---

In my case, I used alias to setup shortcuts for `adb` and `scrcpyy` commands as follows:

**adb**: `New-Alias -Name adb -Value "D:\Utilities\platform-tools\adb.exe"`

**scrcpy**: `New-Alias -Name scrcpy -Value "D:\Utilities\scrcpy-win64-v2.4\scrcpy.exe"`

---

**\*NOTE**: This command will only set aliases for the current session and will reset on terminal close/restart.\*

So solution for this is to add above commands to your powersell profile like this:

- Open **powershell** and enter command: `notepad $PROFILE`
- If it says, the file doesn't exist or such, then create the file.
- Then copy and paste alias-setting commands on separate lines on the profile file.
- Save the file and it's done.

What this does is that this creates those aliases for you each time you open **powershell** and you can use them right away.
