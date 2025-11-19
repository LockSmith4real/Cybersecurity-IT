# WiFi Handshake Capture & Hashcat Crack

## Summary
Captured a WPA2 handshake from my home lab router and successfully cracked it using Hashcat.

## Tools Used
- Kali Linux  
- Airodump-ng  
- Aireplay-ng  
- Aircrack-ng  
- Hashcat  
- External WiFi Adapter (Monitor Mode)

## Steps
1. Enabled monitor mode on WLAN interface  
2. Captured handshake using airodump-ng  
3. Sent deauthentication packets to force re-handshake  
4. Converted .cap file to Hashcat format  
5. Ran Hashcat using rockyou.txt  
6. Verified results  

## Commands Used
