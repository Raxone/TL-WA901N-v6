# TL-WA901N-EU-v6

<<<<<<< HEAD
Openwrt firmware for TL-WA901ND v5 work on TL-WA901N v6.
This build is Openwrt v19.07.7 for TL-WA901ND v5 but work web flash from stock firmware.
Changed PRODUCT_ID 0x09010005 to 0x09010006.
This firmware is NOT STABILE.
Whan use wifi client mode and test speed or download wa901n reset itself.
I try reduce network/wireless/Maximum transmit power lower to 18mw.
Also i build u-boot and fix problem with 120000 baudrate on uart/ttl
=======
Openwrt firmware for TL-WA901N v6.
This build is Openwrt v19.07.7 for TL-WA901N v6 web flash from stock firmware to openwrt.

Also i build u-boot and fix problem with strange baudrate on uart/ttl
>>>>>>> 85a92e1ede0ef6ab6e09be4f64589e33e1f4412c
Now is 115200 8N1 not 120000 8N1.
U-boot tftp address is:
server 192.168.1.10
client 192.168.1.1.
To stop u-boot load just need push on keyboard latter "t" no need "tpl" 
To flash u-boot need tftp server with ip address 192.168.1.10
and tuboot.bin in tftp and u-boot command:

ap151>run lu


Tootpick/reset recovery work but you need another router with 192.168.1.1 ip and tftp server ip 192.168.1.10 and wa901n v6 is 192.168.1.2 automatic ip adress.
Name of tftp recovery firmware is wa901nv6_tp_recovery.bin. 

On flash adress 0x1fc00 is mac address, 0x1fd00 is version of router (0901000600000001)
in this case is v6. 


