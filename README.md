# network-scan-tection

similar to netdiscover

How to Use and Set Up:

Install Scapy: pip install scapy

Save: Save the code as a Python file (e.g., net_discover.py).

oui.txt: Create a file named oui.txt in the same directory as your script. This file should contain OUI (Organizationally Unique Identifier) to vendor mappings. You can find up-to-date OUI lists online (search for "OUI database" or "IEEE OUI"). A simple format would be:

000000 Cisco
000001 Hewlett-Packard
...

Permissions: Make the script executable: chmod +x net_discover.py

Run with Root Privileges: sudo ./net_discover.py -i <your_interface> -r <ip_range> (e.g., sudo ./net_discover.py -i eth0 -r 192.168.1.0/24) or simply sudo ./net_discover.py -i <your_interface> to scan the network of that interface.
______________________________________________________________________________________________________________

Shebang: The #!/usr/bin/env python3 line allows you to execute the script directly (e.g., ./net_discover.py).
IP Range: Now scans a specified IP range (e.g., 192.168.1.0/24) or, if no range is specified, it scans the network of the provided interface.
Verbose Output: The -v or --verbose flag provides more detailed output during the scan.
MAC Vendor Lookup: The get_mac_vendor() function attempts to determine the vendor of a network device based on its MAC address. It uses a local oui.txt file (you'll need to create this). Online MAC address lookup services are also an option, but that would add more complexity.
Error Handling: More robust error handling throughout the script.
Logging: Uses the logging module for better output and debugging.
Root Check: Checks if the script is run with root privileges and exits if not.
Clearer Output: Improved output formatting.

______________________________________________________________________________________________________________

