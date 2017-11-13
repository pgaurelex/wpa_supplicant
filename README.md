# wpa_supplicant
Notes on WiFi Direct or P2P Communication


## WPA Supplicant tutorial links

// wpa supplicant documentation from wifi.org
http://w1.fi/wpa_supplicant/
https://w1.fi/wpa_supplicant/devel/


http://www.tutorial-reports.com/wireless/wlanwifi/introduction_wifi.php
https://chaitanyaganoo.files.wordpress.com/2009/10/old_wpa_supplicant1.pdf
http://linuxwireless.sipsolutions.net/attachments/en/developers/Documentation/overview.pdf
http://www.au-kbc.org/comm/Docs/papers/Vipin_Analysis_of_open_source_WLAN_driver_paper.pdf
https://www.elektronik-kompendium.de/sites/net/0907071.htm


// Important in term of setup of configuration for P2P communication
http://riya80211.blogspot.de/2013/07/p2p-configuration-of-wpasupplicant-in.html

// organisation of wifi networking stack from userspace --> kernel space
https://www.linux.com/blog/linux-wireless-Networking-short-walk


// How to setup wifi direct on 2 linux machines:
http://processors.wiki.ti.com/index.php/OMAP_Wireless_Connectivity_NLCP_WiFi_Direct_Configuration_Scripts#p2p_group_add

// IP Tables and Masquerading technique
http://www.oreilly.com/openbook/linag2/book/ch11.html




## WiFi Direct Wiki

DFS --> Dynamic Frequency Switching ( http://wifi-insider.com/wlan/dfs.htm )

DRCS --> Dynamic Rate Channel Switching
An intentional part of the 802.11 standard is Dynamic Rate Switching (DRS). DRS adjusts the data rate in order to reduce retransmissions. If the data rate remains at a high rate when the client is farther from the AP, it will result in so many retransmissions that the actual throughput is greatly reduced. These retransmissions hurt other clients as well since the wireless medium is being consumed for the transmission of the same information multiple times. For this reason, part of the 802.11 standard accommodates data rate changes. The goal is simple: maintain optimum throughput by reducing the data rate and, therefore, reducing errors and retransmissions.
 
If you are experiencing decreased throughput and the data rate is also being lowered, a potential solution is to increase the output power of the AP and client (using either actual power gains at both ends or greater antenna gain at one or both ends) or to move closer to the AP. If you are experiencing decreased throughput and the data rate is not being lowered, check for interference sources or for other clients connecting to the same AP that have disabled DRS.
 
DRS functions are not defined in the 802.11-2012 standard. As stated in the standard:
 
	9.7.1
	Some PHYs have multiple data transfer rate capabilities that allow implementations to perform dynamic rate switching with the opbjective of improving performance. The algorithm for performing rate switching is beyond the scope of this standard, but in order to provide coexistence and interoperability on multirate-capable PHYs, this standard defines a set of rules to be followed by all STAs.
 
In other words, the exact DRS algorithm is not defined, but the parameters for implementing it are. They are more complicated than warranted in this post, but they include consideration of protection mechanisms, the High Throughput (HT) PHY and backward compatibility.
 
If you are just beginning your journey into the vast land of 802.11 knowledge, the most important thing to remember for now is that DRS allows a STA to transmit at varying data rates depending on the quality of the connection and the type of devices it "sees" on the network.

From <https://www.cwnp.com/dynamic-rate-switching-drs-and-performance-wlan-foundations/> 
