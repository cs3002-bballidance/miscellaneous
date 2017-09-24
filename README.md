# miscellaneous
Some miscellaneous scripts that are used

### informup
[info]  
This script sends a telegram message to the specified receiver with the following info when an interface goes up (specifically wlan interface):  
1. SSID connected
2. IP address of device  

[usage]  
Modify userid and key accordingly.   
userid: telegram user id ofthe receiver  
key: telegram bot secret key    

Add the following line in /etc/network/interfaces under the interface that you want to run this script.  
```up <informup directory>```  

Eg.  
```
auto wlan0
iface wlan0 inet dhcp
    wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
    up /home/hazmei/informup
```  

[dependencies]  
None  

---
