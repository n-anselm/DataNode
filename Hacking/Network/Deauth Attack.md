### Deauth attack

A deauthentification attack disconnects a client from an access point / wireless network. There is no need to be connected to the target access point, or to know the password.

*Note: It is a good idea to have airodump-ng capturing packets on the access point simultaneously with a deauth attack.*

The wireless adapter needs to be in monitor mode.

To launch a deauth attack, run this command:

    aireplay-ng --deauth <number_of_deauth_packets> -a <target_access_point_bssid> -c <target_client_bssid> <wireless_interface_name>
