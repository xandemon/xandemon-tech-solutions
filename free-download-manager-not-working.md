## Free Download Manager (FDM) Not Working in Edge Browser

There could be many reasons for this issue but one of the most common reason is because your FDM desktop app cannot connect to the browser's FDM extension.

### For Windows

- Remove both the FDM desktop app and extension
- Download and install the FDM desktop app first
- After it is installed and running, install the FDM extension in the browser
- Now when you click on FDM extension icon, and then **Options**, it should open desktop FDM app for you which indicates that everything is well set up.

(If ther is **Loading...**instead og **Options** in FDM extension, then that means extension is not connected to your desktop app)

### For Linux

- For Linux too, you could try installing and running desktop app first, then installing extension.
- Copy this file from `~/.config/google-chrome/NativeMessagingHosts/org.freedownloadmanager.fdm5.cnh.json` to `~./config/.config/BraveSoftware/Brave-Browser/NativeMessagingHosts/org.freedownloadmanager.fdm5.cnh.json` for Brave browser or similarly for any other browser you're using.
