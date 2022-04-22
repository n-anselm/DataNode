### Remove password on Linux:
1. Open `/etc/passwd` . (Note: You need root or boot into a live system for this.)
2. Locate the username of the targeted account.
3. Remove the `x` in between the two colons after the username of the account you want to unlock and save the file. The account will not ask for a password now, and a new password can be created.
