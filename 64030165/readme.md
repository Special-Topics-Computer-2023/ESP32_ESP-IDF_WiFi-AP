# 64030165 Ratchanon

## Connect Wifi with smartphone

![MicrosoftTeams-image (2)](https://github.com/RatchanonBusaracome/ESP32_ESP-IDF_WiFi-AP/assets/115066405/3ca9a4b9-a843-4698-8edf-bbd775ed3a1b)

## Terminal output

```css
I (31) boot: ESP-IDF v5.1.1-dirty 2nd stage bootloader
I (31) boot: compile time Oct 21 2023 15:38:45
I (31) boot: Multicore bootloader
I (36) boot: chip revision: v3.0
I (40) boot.esp32: SPI Speed      : 40MHz
I (44) boot.esp32: SPI Mode       : DIO
I (49) boot.esp32: SPI Flash Size : 2MB
I (53) boot: Enabling RNG early entropy source...
I (59) boot: Partition Table:
I (62) boot: ## Label            Usage          Type ST Offset   Length
I (70) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (77) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (85) boot:  2 factory          factory app      00 00 00010000 00100000
I (92) boot: End of partition table
I (96) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=1fcb4h (130228) map
I (152) esp_image: segment 1: paddr=0002fcdc vaddr=3ffb0000 size=0033ch (   828) load
I (152) esp_image: segment 2: paddr=00030020 vaddr=400d0020 size=7ef48h (520008) map
I (345) esp_image: segment 3: paddr=000aef70 vaddr=3ffb033c size=0337ch ( 13180) load
I (351) esp_image: segment 4: paddr=000b22f4 vaddr=40080000 size=156e0h ( 87776) load
I (398) boot: Loaded app from partition at offset 0x10000
I (398) boot: Disabling RNG early entropy source...
I (410) cpu_start: Multicore app
I (410) cpu_start: Pro cpu up.
I (410) cpu_start: Starting app cpu, entry point is 0x4008137c
0x4008137c: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v5.1.1/components/esp_system/port/cpu_start.c:154

I (0) cpu_start: App cpu up.
I (428) cpu_start: Pro cpu start user code
I (428) cpu_start: cpu freq: 160000000 Hz
I (428) cpu_start: Application information:
I (433) cpu_start: Project name:     wifi_softAP
I (438) cpu_start: App version:      1
I (443) cpu_start: Compile time:     Oct 21 2023 15:39:07
I (449) cpu_start: ELF file SHA256:  ba2fd8d065c71896...
Warning: checksum mismatch between flashed and built applications. Checksum of built application is a746a41373d9321d90db94cbcf6f36fe35d83392b308f5afa98bec2ee32f2b2b
I (455) cpu_start: ESP-IDF:          v5.1.1-dirty
I (460) cpu_start: Min chip rev:     v0.0
I (465) cpu_start: Max chip rev:     v3.99 
I (470) cpu_start: Chip rev:         v3.0
I (475) heap_init: Initializing. RAM available for dynamic allocation:
I (482) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (488) heap_init: At 3FFB7780 len 00028880 (162 KiB): DRAM
I (494) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (500) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (507) heap_init: At 400956E0 len 0000A920 (42 KiB): IRAM
I (514) spi_flash: detected chip: generic
I (518) spi_flash: flash io: dio
W (521) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (535) app_start: Starting scheduler on CPU0
I (540) app_start: Starting scheduler on CPU1
I (540) main_task: Started on CPU0
I (550) main_task: Calling app_main()
I (590) wifi softAP: ESP_WIFI_MODE_AP
I (600) wifi:wifi driver task: 3ffbf798, prio:23, stack:6656, core=0
I (620) wifi:wifi firmware version: ce9244d
I (620) wifi:wifi certification version: v7.0
I (620) wifi:config NVS flash: enabled
I (620) wifi:config nano formating: disabled
I (620) wifi:Init data frame dynamic rx buffer num: 32
I (630) wifi:Init management frame dynamic rx buffer num: 32
I (630) wifi:Init management short buffer num: 32
I (640) wifi:Init dynamic tx buffer num: 32
I (640) wifi:Init static rx buffer size: 1600
I (650) wifi:Init static rx buffer num: 10
I (650) wifi:Init dynamic rx buffer num: 32
I (660) wifi_init: rx ba win: 6
I (660) wifi_init: tcpip mbox: 32
I (660) wifi_init: udp mbox: 6
I (670) wifi_init: tcp mbox: 6
I (670) wifi_init: tcp tx win: 5744
I (670) wifi_init: tcp rx win: 5744
I (680) wifi_init: tcp mss: 1440
I (680) wifi_init: WiFi IRAM OP enabled
I (690) wifi_init: WiFi RX IRAM OP enabled
I (700) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (800) wifi:mode : softAP (94:b5:55:f8:30:01)
I (910) wifi:Total power save buffer number: 16
I (910) wifi:Init max length of beacon: 752/752
I (910) wifi:Init max length of beacon: 752/752
I (910) wifi softAP: wifi_init_softap finished. SSID:SSID-165 password:mypassword channel:1
I (910) esp_netif_lwip: DHCP server started on interface WIFI_AP_DEF with IP: 192.168.4.1
I (930) main_task: Returned from app_main()
I (2460) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (2470) wifi:station: 3a:f0:3a:ce:e1:5a join, AID=1, bgn, 20
I (2470) wifi:station: 3a:f0:3a:ce:e1:5a leave, AID = 1, bss_flags is 134242, bss:0x3ffb91d8
I (2470) wifi:new:<1,0>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (2480) wifi:new:<1,0>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (2490) wifi:max connection!
I (9830) wifi:new:<1,0>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (9830) wifi:station: 3a:f0:3a:ce:e1:5a join, AID=1, bgn, 20
I (9860) wifi softAP: station 3a:f0:3a:ce:e1:5a join, AID=1
I (11070) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.2
I (13210) wifi:<ba-add>idx:2 (ifx:1, 3a:f0:3a:ce:e1:5a), tid:0, ssn:2, winSize:64
```
