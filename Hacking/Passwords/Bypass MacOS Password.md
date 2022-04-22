### Bypass MacOS Password
1. Boot and hold `Cmd+S`
2. A prompt will appear. Enter these commands:

```
mount -uw /
rm /var/db/.applesetupdone
shutdown -h now
```
3. Reboot
