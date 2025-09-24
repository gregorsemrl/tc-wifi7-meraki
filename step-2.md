The new Wi-Fi 7 certification is based on the IEEE 802.11be standard and supports operations in the 2.4 GHz, 5 GHz, and 6 GHz bands. Wi-Fi 7 also introduces new features and enhancements compared to previous certifications.

Key features of Wi-Fi 7 are:
- **Higher data rates**: up to 30 Gbps
- **Wider channel bandwidth**: Wi-Fi 7 can utilize up to 320 Mhz of channel bandwidth, which is higher compared to Wi-Fi 6 and Wi-Fi 6E (160Mhz)
- **Multi-link operation (MLO)**: this feature enables devices to connect across multiple frequency bands simultaneosly (2.4 GHz, 5 GHz, and 6 GHz)
- **Improved latency**
- **Target wake time (TWT) enhancements**: TWT allows devices to schedule when they wake up to transmit or receive data, reducing power consumption and improving battery life, particularly for IoT devices.
- **Enhanced multi-user, multiple input, multiple output (MU-MIMO) and orthogonal frequency-division multiple access (OFDMA)**
- **Advanced interference management**
- **Security enhancements with Wi-Fi Protected Access 3 (WPA3)**


![Wi-Fi 7](./images/2-01.png)



**6 GHz band requirements**

Supporting the 6 GHz band and Wi-Fi 7 comes with specific requirements, often necessitating new configurations and RF designs, especially when compared to the established practices for the 2.4 GHz and 5 GHz bands with Wi-Fi 6. The 6 GHz band only allows WPA3 or Enhanced Open WLANs, which means one of these security options:

- **WPA3-Enterprise with 802.1X authentication**
- **WPA3 Simultaneous Authentication of Equals (WPA3-SAE or WPA3-Personal)** with passphrase. SAE-FT (SAE with Fast Transition) is another possible Authentication and Key Management (AKM) and is recommended for use since the SAE handshake is not trivial, and FT allows skipping that longer exchange.
- **Enhanced Open with Opportunistic Wireless Encryption (OWE)**


There are no new specific ciphers or algorithm requirements for WPA3-Enterprise, apart from 802.11w/Protected Management Frame (PMF) enforcement. Many vendors, including Cisco, consider 802.1X-SHA256 or "FT + 802.1X" only to be WPA3 compliant and plain 802.1X, which uses SHA1, is considered part of WPA2, therefore not supported for 6 GHz.



**Wi-Fi 7 requirements**

With the Wi-Fi 7 certification of the 802.11be standard, the Wi-Fi Alliance increased the security requirements. Some of them allow to use of the 802.11be data rates and protocol improvements, while some others are specific for supporting Multi-Link Operations (MLO), allowing compatible devices (clients and/or APs) to use multiple frequency bands while maintaining the same association.

In general, Wi-Fi 7 mandates one of these security types:

- **WPA3-Enterprise with AES** (CCMP128) and 802.1X-SHA256 or FT + 802.1X. This does not represent a change compared to previously existing WPA3 security prerequisites for the 6 GHz band.
- **WPA3-Personal with GCMP256 and SAE-EXT-KEY** and/or FT + SAE-EXT-KEY (AKM 24 or 25). Wi-Fi 6E mandates WPA3 SAE and/or FT + SAE with regular AES(CCMP128) and no additional extended key usages; this means that a new cipher was specifically introduced for Wi-Fi 7:
Enhanced Open / OWE with GCMP256. While AES (CCMP128) can still be configured on the same SSID, clients using AES 128 do not support Wi-Fi 7. Before Wi-Fi 7, most clients supporting Enhanced Open were using AES 128 only, so this is a new, stronger requirement. As for 6 GHz support, no transition mode is allowed. Protected Management Frames (PMF) and Beacon Protection are required to support Wi-Fi 7 on the WLAN.
- **WPA3-OWE** for *open* networks where traffic is encrypted, and authorization is optional once connection is already established using a portal. The purpose of OWE based authentication is avoid open unsecured wireless connectivity between the AP’s and clients.

Cisco has been progressively enforcing the configuration options to be compliant with the Wi-Fi 7 certification. 


**More Information on the Topic**

For further learning, explore these additional resources: 

- [Wi-Fi 7 and the Growing Future of Wireless Design Guide](https://www.cisco.com/c/en/us/products/collateral/networking/wireless/wifi7-future-of-wireless-dg.html)

- [Wi-Fi 7 Technical Guide](https://documentation.meraki.com/MR/Wi-Fi_Basics_and_Best_Practices/Wi-Fi_7_(802.11be)_Technical_Guide)
