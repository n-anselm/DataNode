## Getting the WiFi password from an Android device

---

### Via ADB (Android Debug Bridge)

*NOTE: Developer options and ADB have to be enabled for this to work. No root is required.*

Connect to ADB and execute this command:

	adb services

Then run this command:

    adb pull /data/misc/wifi/wpa\_supplicant.conf

This will pull the file from your Android device to your current working directory.

Opent the file with a text editor.

The ssid is the network name and the psk is the password.
