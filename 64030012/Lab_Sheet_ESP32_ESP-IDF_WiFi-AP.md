# ใบงานการทดลอง ESP32_ESP-IDF_WiFi-AP

## ขั้นตอนการทดลอง

1. สร้าง Espressif IDF project ใหม่ ชื่อ  ESP32_ESP-IDF_WiFi-AP 


1.1  หลังจากใส่ชื่อ คลิก next เพื่อเลือก template project

![Alt text](./Pictures/1.Create-new-project.png)


1.2 เลือก template project เป็น softAP

![Alt text](Pictures/2.Select-template.png)


### 2. แก้ไขไฟล์ config

2.1 เปิดไฟล์ Kconfig.projbuild  ในโฟลเดอร์ main ด้วย text editor


![Alt text](./Pictures/3.open-Kconfig-file.png)

[1] เปิด folder  main
 
[2] คลิกขวาที่ชื่อไฟล์ Kconfig.projbuild

[3] เลือก Open With
 
[4] เลือก Text Editor


2.2 แก้ไขไฟล์

![Alt text](./Pictures/4.Edit-Kconfig-file.png) 

[1] แก้ไข SSID  ให้มีความแตกต่างจากของเพื่อน โดยใส่เลข 3 ตัวท้ายของรหัสนักศึกษากำกับไว้ เช่น `"SSID-001"` เป็นต้น

[2]  อาจจะแก้ password ตามต้องการ

หมายเหตุ ไฟล์นี้สามารถแก้ได้ภายหลังจากการเรียก  sdkconfig

### 3. Build โปรเจค

### 4. Run โปรเจค ดูผลจาก Terminal

### 5. ใช้ Laptop หรือ Smartphone ค้นหา Accesspoint 

ควรจะต้องเจอ `"SSID-..."` ในรายการ Wifi ที่เราสร้างขึ้น

### 6. บันทึกผลการทดลอง 

ทั้งที่หน้าจอ Laptop หรือ Smartphone และที่ terminal ของ ESP32

รวมทั้งหน้าจอ properties ของ wifi ดังตัวอย่าง
![52244](https://github.com/Fixckpx/ESP32_ESP-IDF_WiFi-AP/assets/115066186/7aae718e-61f0-4976-b2c3-6fb8fa2162d3)
![S__1253396](https://github.com/Fixckpx/ESP32_ESP-IDF_WiFi-AP/assets/115066186/baa681fa-d5b2-4f67-947b-009de1ed21ec)


![Alt text](./Pictures/5.Example_Wifi_Properties.png)


```c
entry 0x4008064c
I (27) boot: ESP-IDF v5.0.2-dirty 2nd stage bootloader
I (27) boot: compile time 15:12:12
I (28) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 2MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=21518h (136472) map
I (145) esp_image: segment 1: paddr=00031540 vaddr=3ffb0000 size=0335ch ( 13148) load
I (151) esp_image: segment 2: paddr=000348a4 vaddr=40080000 size=0b774h ( 46964) load
I (170) esp_image: segment 3: paddr=00040020 vaddr=400d0020 size=842d4h (541396) map
I (366) esp_image: segment 4: paddr=000c42fc vaddr=4008b774 size=09524h ( 38180) load
I (393) boot: Loaded app from partition at offset 0x10000
I (393) boot: Disabling RNG early entropy source...
I (404) cpu_start: Pro cpu up.
I (404) cpu_start: Starting app cpu, entry point is 0x400812b8
0x400812b8: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v5.0.2/components/esp_system/port/cpu_start.c:141

I (0) cpu_start: App cpu up.
I (421) cpu_start: Pro cpu start user code
I (421) cpu_start: cpu freq: 160000000 Hz
I (421) cpu_start: Application information:
I (426) cpu_start: Project name:     simple
I (430) cpu_start: App version:      1
I (435) cpu_start: Compile time:     Oct 22 2023 15:14:49
I (441) cpu_start: ELF file SHA256:  d9b9043416705db8...
I (447) cpu_start: ESP-IDF:          v5.0.2-dirty
I (452) cpu_start: Min chip rev:     v0.0
I (457) cpu_start: Max chip rev:     v3.99 
I (462) cpu_start: Chip rev:         v3.0
I (467) heap_init: Initializing. RAM available for dynamic allocation:
I (474) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (480) heap_init: At 3FFB6FC8 len 00029038 (164 KiB): DRAM
I (486) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (492) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (499) heap_init: At 40094C98 len 0000B368 (44 KiB): IRAM
I (506) spi_flash: detected chip: generic
I (510) spi_flash: flash io: dio
W (514) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (528) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (615) example_connect: Start example_connect.
I (625) wifi:wifi driver task: 3ffbecc4, prio:23, stack:6656, core=0
I (625) system_api: Base MAC address is not set
I (625) system_api: read default base MAC address from EFUSE
I (655) wifi:wifi firmware version: 57982fe
I (655) wifi:wifi certification version: v7.0
I (655) wifi:config NVS flash: enabled
I (655) wifi:config nano formating: disabled
I (655) wifi:Init data frame dynamic rx buffer num: 32
I (665) wifi:Init management frame dynamic rx buffer num: 32
I (665) wifi:Init management short buffer num: 32
I (675) wifi:Init dynamic tx buffer num: 32
I (675) wifi:Init static rx buffer size: 1600
I (675) wifi:Init static rx buffer num: 10
I (685) wifi:Init dynamic rx buffer num: 32
I (685) wifi_init: rx ba win: 6
I (695) wifi_init: tcpip mbox: 32
I (695) wifi_init: udp mbox: 6
I (695) wifi_init: tcp mbox: 6
I (705) wifi_init: tcp tx win: 5744
I (705) wifi_init: tcp rx win: 5744
I (715) wifi_init: tcp mss: 1440
I (715) wifi_init: WiFi IRAM OP enabled
I (715) wifi_init: WiFi RX IRAM OP enabled
I (725) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (825) wifi:mode : sta (94:b5:55:f3:29:58)
I (825) wifi:enable tsf
I (835) example_connect: Connecting to __fixckpx...
I (835) example_connect: Waiting for IP(s)
I (3245) wifi:new:<6,0>, old:<1,0>, ap:<255,255>, sta:<6,0>, prof:1
I (3915) wifi:state: init -> auth (b0)
I (4025) wifi:state: auth -> assoc (0)
I (5025) wifi:state: assoc -> init (2700)
I (5025) wifi:new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (5025) example_connect: Wi-Fi disconnected, trying to reconnect...
I (7445) example_connect: Wi-Fi disconnected, trying to reconnect...
I (9855) wifi:new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (9855) wifi:state: init -> auth (b0)
I (9865) wifi:state: auth -> assoc (0)
I (9885) wifi:state: assoc -> run (10)
I (9945) wifi:connected with __fixckpx, aid = 2, channel 6, BW20, bssid = 92:9d:96:07:54:1e
I (9945) wifi:security: WPA2-PSK, phy: bgn, rssi: -61
I (9945) wifi:pm start, type: 1

I (9985) wifi:AP's beacon interval = 102400 us, DTIM period = 2
I (10955) esp_netif_handlers: example_netif_sta ip: 192.168.155.18, mask: 255.255.255.0, gw: 192.168.155.195
I (10955) example_connect: Got IPv4 event: Interface "example_netif_sta" address: 192.168.155.18
I (11615) example_connect: Got IPv6 event: Interface "example_netif_sta" address: fe80:0000:0000:0000:96b5:55ff:fef3:2958, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (11615) example_common: Connected to example_netif_sta
I (11625) example_common: - IPv4 address: 192.168.155.18,
I (11625) example_common: - IPv6 address: fe80:0000:0000:0000:96b5:55ff:fef3:2958, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (11635) example: Starting server on port: '80'
I (11645) example: Registering URI handlers
W (37785) httpd_uri: httpd_uri: URI '/' not found
W (37795) httpd_txrx: httpd_resp_send_err: 404 Not Found - Nothing matches the given URI
W (37845) httpd_uri: httpd_uri: URI '/favicon.ico' not found
W (37845) httpd_txrx: httpd_resp_send_err: 404 Not Found - Nothing matches the given URI
I (38675) wifi:<ba-add>idx:0 (ifx:0, 92:9d:96:07:54:1e), tid:0, ssn:16, winSize:64
W (194225) httpd_uri: httpd_uri: URI '/' not found
W (194225) httpd_txrx: httpd_resp_send_err: 404 Not Found - Nothing matches the given URI
â†�[0;33m--- idf_monitor on \\.\COM5 115200 ---â†�[0m
--- Quit: Ctrl+] | Menu: Ctrl+T | Help: Ctrl+T followed by Ctrl+H ---
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6944
load:0x40078000,len:15500
load:0x40080400,len:3844
0x40080400: _init at ??:?

entry 0x4008064c
I (27) boot: ESP-IDF v5.0.2-dirty 2nd stage bootloader
I (27) boot: compile time 15:12:12
I (28) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 2MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=21518h (136472) map
I (145) esp_image: segment 1: paddr=00031540 vaddr=3ffb0000 size=0335ch ( 13148) load
I (151) esp_image: segment 2: paddr=000348a4 vaddr=40080000 size=0b774h ( 46964) load
I (170) esp_image: segment 3: paddr=00040020 vaddr=400d0020 size=842e8h (541416) map
I (366) esp_image: segment 4: paddr=000c4310 vaddr=4008b774 size=09524h ( 38180) load
I (393) boot: Loaded app from partition at offset 0x10000
I (393) boot: Disabling RNG early entropy source...
I (404) cpu_start: Pro cpu up.
I (404) cpu_start: Starting app cpu, entry point is 0x400812b8
0x400812b8: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v5.0.2/components/esp_system/port/cpu_start.c:141

I (0) cpu_start: App cpu up.
I (421) cpu_start: Pro cpu start user code
I (421) cpu_start: cpu freq: 160000000 Hz
I (421) cpu_start: Application information:
I (426) cpu_start: Project name:     simple
I (430) cpu_start: App version:      1
I (435) cpu_start: Compile time:     Oct 22 2023 15:30:00
I (441) cpu_start: ELF file SHA256:  3bc012f680840d1f...
I (447) cpu_start: ESP-IDF:          v5.0.2-dirty
I (452) cpu_start: Min chip rev:     v0.0
I (457) cpu_start: Max chip rev:     v3.99 
I (462) cpu_start: Chip rev:         v3.0
I (467) heap_init: Initializing. RAM available for dynamic allocation:
I (474) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (480) heap_init: At 3FFB6FC8 len 00029038 (164 KiB): DRAM
I (486) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (492) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (499) heap_init: At 40094C98 len 0000B368 (44 KiB): IRAM
I (507) spi_flash: detected chip: generic
I (510) spi_flash: flash io: dio
W (514) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (528) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (615) example_connect: Start example_connect.
I (625) wifi:wifi driver task: 3ffbecc4, prio:23, stack:6656, core=0
I (625) system_api: Base MAC address is not set
I (625) system_api: read default base MAC address from EFUSE
I (655) wifi:wifi firmware version: 57982fe
I (655) wifi:wifi certification version: v7.0
I (655) wifi:config NVS flash: enabled
I (655) wifi:config nano formating: disabled
I (655) wifi:Init data frame dynamic rx buffer num: 32
I (665) wifi:Init management frame dynamic rx buffer num: 32
I (665) wifi:Init management short buffer num: 32
I (675) wifi:Init dynamic tx buffer num: 32
I (675) wifi:Init static rx buffer size: 1600
I (675) wifi:Init static rx buffer num: 10
I (685) wifi:Init dynamic rx buffer num: 32
I (685) wifi_init: rx ba win: 6
I (695) wifi_init: tcpip mbox: 32
I (695) wifi_init: udp mbox: 6
I (695) wifi_init: tcp mbox: 6
I (705) wifi_init: tcp tx win: 5744
I (705) wifi_init: tcp rx win: 5744
I (715) wifi_init: tcp mss: 1440
I (715) wifi_init: WiFi IRAM OP enabled
I (715) wifi_init: WiFi RX IRAM OP enabled
I (725) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (835) wifi:mode : sta (94:b5:55:f3:29:58)
I (835) wifi:enable tsf
I (835) example_connect: Connecting to __fixckpx...
I (835) example_connect: Waiting for IP(s)
I (3245) wifi:new:<6,0>, old:<1,0>, ap:<255,255>, sta:<6,0>, prof:1
I (3925) wifi:state: init -> auth (b0)
I (4025) wifi:state: auth -> assoc (0)
I (5025) wifi:state: assoc -> init (2700)
I (5035) wifi:new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (5035) example_connect: Wi-Fi disconnected, trying to reconnect...
I (7445) example_connect: Wi-Fi disconnected, trying to reconnect...
I (9865) wifi:new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (9865) wifi:state: init -> auth (b0)
I (9875) wifi:state: auth -> assoc (0)
I (9885) wifi:state: assoc -> run (10)
I (9915) wifi:connected with __fixckpx, aid = 2, channel 6, BW20, bssid = 92:9d:96:07:54:1e
I (9915) wifi:security: WPA2-PSK, phy: bgn, rssi: -45
I (9925) wifi:pm start, type: 1

I (9935) wifi:AP's beacon interval = 102400 us, DTIM period = 2
I (10925) esp_netif_handlers: example_netif_sta ip: 192.168.155.18, mask: 255.255.255.0, gw: 192.168.155.195
I (10925) example_connect: Got IPv4 event: Interface "example_netif_sta" address: 192.168.155.18
I (11615) example_connect: Got IPv6 event: Interface "example_netif_sta" address: fe80:0000:0000:0000:96b5:55ff:fef3:2958, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (11615) example_common: Connected to example_netif_sta
I (11625) example_common: - IPv4 address: 192.168.155.18,
I (11625) example_common: - IPv6 address: fe80:0000:0000:0000:96b5:55ff:fef3:2958, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (11635) example: Starting server on port: '80'
I (11645) example: Registering URI handlers
I (17235) wifi:<ba-add>idx:0 (ifx:0, 92:9d:96:07:54:1e), tid:0, ssn:17, winSize:64
W (17245) httpd_uri: httpd_uri: URI '/' not found
W (17245) httpd_txrx: httpd_resp_send_err: 404 Not Found - Nothing matches the given URI
W (25825) httpd_uri: httpd_uri: URI '/jello' not found
W (25825) httpd_txrx: httpd_resp_send_err: 404 Not Found - Nothing matches the given URI
I (31765) example: Found header => Host: 192.168.155.18
I (31765) example: Request headers lost
To exit from IDF monitor please use "Ctrl+]". Alternatively, you can use Ctrl-T Ctrl-X to exit.
â†�[0;33m--- idf_monitor on \\.\COM5 115200 ---â†�[0m
--- Quit: Ctrl+] | Menu: Ctrl+T | Help: Ctrl+T followed by Ctrl+H ---
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6944
load:0x40078000,len:15500
load:0x40080400,len:3844
0x40080400: _init at ??:?

entry 0x4008064c
I (27) boot: ESP-IDF v5.0.2-dirty 2nd stage bootloader
I (27) boot: compile time 16:16:31
I (28) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 2MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=1e490h (124048) map
I (141) esp_image: segment 1: paddr=0002e4b8 vaddr=3ffb0000 size=01b60h (  7008) load
I (144) esp_image: segment 2: paddr=00030020 vaddr=400d0020 size=79de0h (499168) map
I (327) esp_image: segment 3: paddr=000a9e08 vaddr=3ffb1b60 size=017dch (  6108) load
I (329) esp_image: segment 4: paddr=000ab5ec vaddr=40080000 size=14c98h ( 85144) load
I (378) boot: Loaded app from partition at offset 0x10000
I (378) boot: Disabling RNG early entropy source...
I (390) cpu_start: Pro cpu up.
I (390) cpu_start: Starting app cpu, entry point is 0x400812b8
0x400812b8: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v5.0.2/components/esp_system/port/cpu_start.c:141

I (0) cpu_start: App cpu up.
I (406) cpu_start: Pro cpu start user code
I (406) cpu_start: cpu freq: 160000000 Hz
I (406) cpu_start: Application information:
I (411) cpu_start: Project name:     wifi_softAP
I (416) cpu_start: App version:      1
I (421) cpu_start: Compile time:     Oct 22 2023 16:16:13
I (427) cpu_start: ELF file SHA256:  e3a551011f62ca4f...
Warning: checksum mismatch between flashed and built applications. Checksum of built application is 3bc012f680840d1fd485b6bc160ac440696f62275a93cbe4f221ed1785225253
I (433) cpu_start: ESP-IDF:          v5.0.2-dirty
I (438) cpu_start: Min chip rev:     v0.0
I (443) cpu_start: Max chip rev:     v3.99 
I (448) cpu_start: Chip rev:         v3.0
I (453) heap_init: Initializing. RAM available for dynamic allocation:
I (460) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (466) heap_init: At 3FFB6F98 len 00029068 (164 KiB): DRAM
I (472) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (478) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (485) heap_init: At 40094C98 len 0000B368 (44 KiB): IRAM
I (492) spi_flash: detected chip: generic
I (496) spi_flash: flash io: dio
W (500) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (514) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (600) wifi softAP: ESP_WIFI_MODE_AP
I (610) wifi:wifi driver task: 3ffbf084, prio:23, stack:6656, core=0
I (610) system_api: Base MAC address is not set
I (610) system_api: read default base MAC address from EFUSE
I (630) wifi:wifi firmware version: 57982fe
I (630) wifi:wifi certification version: v7.0
I (630) wifi:config NVS flash: enabled
I (630) wifi:config nano formating: disabled
I (640) wifi:Init data frame dynamic rx buffer num: 32
I (640) wifi:Init management frame dynamic rx buffer num: 32
I (650) wifi:Init management short buffer num: 32
I (650) wifi:Init dynamic tx buffer num: 32
I (660) wifi:Init static rx buffer size: 1600
I (660) wifi:Init static rx buffer num: 10
I (660) wifi:Init dynamic rx buffer num: 32
I (670) wifi_init: rx ba win: 6
I (670) wifi_init: tcpip mbox: 32
I (680) wifi_init: udp mbox: 6
I (680) wifi_init: tcp mbox: 6
I (680) wifi_init: tcp tx win: 5744
I (690) wifi_init: tcp rx win: 5744
I (690) wifi_init: tcp mss: 1440
I (700) wifi_init: WiFi IRAM OP enabled
I (700) wifi_init: WiFi RX IRAM OP enabled
I (710) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (810) wifi:mode : softAP (94:b5:55:f3:29:59)
I (810) wifi:Total power save buffer number: 16
I (820) wifi:Init max length of beacon: 752/752
I (820) wifi:Init max length of beacon: 752/752
I (820) wifi softAP: wifi_init_softap finished. SSID:SSID-012 password:Rattanakit123 channel:1
I (188790) wifi:new:<1,1>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (188790) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (192800) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (192800) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (194810) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (194820) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (198820) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (198820) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (200420) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (200420) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (204430) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (204430) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (206850) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (206850) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (208460) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (208460) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (224770) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (224780) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (228780) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (228780) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (230170) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (230170) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (234180) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 134242, bss:0x3ffb89f0
I (234180) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (236430) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (236430) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (240430) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (240440) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (242630) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (242630) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (244670) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 134242, bss:0x3ffb89f0
I (244670) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (298270) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (298270) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (302280) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (302280) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (303600) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (303600) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (307610) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (307610) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (308630) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (308640) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (312640) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (312640) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (313350) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (313350) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (317360) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (317360) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (356170) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (356170) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (360180) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (360180) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (362360) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (362360) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (366370) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (366370) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (368760) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (368760) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (372770) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (372770) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (375520) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (375530) wifi:station: c4:23:60:34:84:ba join, AID=1, bgn, 40U
I (376020) wifi:station: c4:23:60:34:84:ba leave, AID = 1, bss_flags is 658530, bss:0x3ffb89f0
I (376020) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
```





### 7. ส่งงาน

โดยการ pull request พร้อมแนบ link ไปยัง Repository ของโปรเจคมาด้วย
https://github.com/Fixckpx/ESP32_ESP-IDF_WiFi-AP
