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
