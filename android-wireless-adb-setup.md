## Setting Up Android Wireless ADB

Using `adb` to connect and debug android from your PC using USB has been a common practice and there is a major reason to it i.e. **speed**. However, there are times when we prefer wireless ADB over wired. So here's how youcan do it:

#### Method 1: TCPIP Approach

- Connect your android device with your PC (don't worry, it's just for the first time)
- Enable **developer options** by tapping on the _Build number_ in your phone's about section inside settings app
- Go to **developer options** and also enable **USB Debugging** option
- Allow prompt for USB Debugging (if asked) when connected android with your PC
- Run `adb devices` command to ensure that adb is properly set up
- Run `adb tcpip 5555` to restart adb in tcpip mode
- Check your phone's IP address from your phone's about section inside settings app
- Run `adb connect <phone_ip_address>` to connect your phone wirelessly
- That's all. Now you can run adb commands wirelessly without USB.

#### Method 4: Wireless Debugging Setting

- Follow steps 1 & 2 (step 3 optional but recommended) in above method
- ALso enable **Wireless Debugging** option in **developer settings**
- Allow prompt for Wireless Debugging (if asked)
- Go inside that **Wireless Debugging** setting in your phone
- Tap on the **Pair device with pairing code** option which'll expose code and IP address with port to you
- Now run `adb pair <phone_ip_address_with_port>` on your PC
- It'll ask you to enter pairing code where you need to enter the pairing code shown in your phone
- That's all. Now you can run adb commands wirelessly without USB.

---

**Note:** For wireless ADB, you need to make sure that your phone and PC is on the same WiFi network.
