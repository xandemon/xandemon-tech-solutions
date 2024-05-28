# Fix Lenovo Touchpad Gestures Issues

The problem I had with Lenovo touchpad gestures is that none or only some of the touchpad gestures would work. For example: touchpad works, two finger scrolling works, three and four finger gestures work but two-finger tap gesture didn't work. Whatever the problems with Lenovo touchpad gestures, here's how to fix them all:

By the way , my machine is **Lenovo Ideapad 130-15Ikb** but this should work for majority of Lenovo laptops or laptop with **Elantech** or **Synaptics** touchpad.

> **NOTE:** Install `EtdProperties` app from Microsoft Store if you have an Elantech touchpad and go inside _Options_ within the app. If you're able to access _Options_ or are able to change touchpad settings from there, then your touchpad driver is most probably correct and working.

## Method 1 (Resetting to default touchpad driver)

- Firstly, open **_Device Manager_** in your windows laptop and uninstall the touchpad driver (mine was named **Elan pointing device**) under _Mice and other pointing devices_.
- Use your external mouse to click on **Scan for hardware changes** option in Device manager to let Windows automatically install default touchpad driver for your PC.
- Restart your Windows and check if the gestures are working correctly. If not, resort to other methods.

## Method 2 (Installing official touchpad drivers)

- Go to [Lenovo official site for drivers](https://pcsupport.lenovo.com/np/en) and download latest touchpad drivers for your model.
- Extract and install the drivers using the built-in installation wizard and follow the steps show.
- Restart your Windows and check if the gestures are working correctly. If not, resort to other methods.

## Method 3 (Tweaking the Windows registry)

- This method requires correct driver to be installed. So make sure to follow above methods to have the correct driver installed.
- Open **Registry Editor** and go to `Computer\HKEY_CURRENT_USER\Software\Elantech\SmartPad`. Find the gesture that is not working and enable it by changing its value to 1. In my case, two-finger tap was not working, so I changed `Tap_Two_Finger_Enable` to `1`, `Tap_Two_Finger_ShowItem` to `1`. These are like boolean values that enable the tap-two-finger functionality. And I copied the value of `Tap_Three_Finger` to `Tap_Two_Finger` which defines the function because `Tap_Three_Finger` was working.
- Then restart your Windows and the gestures should be working. You should also be able to see all gestures listed inside **EtdProperties** app and be able to assign different functions to different gestures
