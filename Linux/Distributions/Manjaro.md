[Manjaro website](https://manjaro.org)

---

### Specifications
- **Based on:** Arch Linux
- **Origin:** France
- **Architecture:** aarch64, x86_64

---

### HOW TO SET THE FASTEST MIRROR FOR DOWNLOADING SOFTWARE
An optimized mirror list can have a noticeable performance impact on the system.
Open the terminal and run this command:
```
sudo pacman-mirrors --fasttrack
```

---

### HOW TO ENABLE TRIM (FOR SSD ONLY)
If your root partition has been installed on an SSD, enabling TRIM is one thing you need to do after installing Manjaro. TRIM helps to clean blocks in your SSD and extends the lifespan of your SSD.

To enable TRIM on Manjaro, run the following comand in a terminal:
```
sudo systemctl enable fstrim.timer
```
