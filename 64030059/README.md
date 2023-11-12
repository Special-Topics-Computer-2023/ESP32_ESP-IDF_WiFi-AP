## REPO 
https://github.com/DanupatSangseekaew/Wifi_AP
## code
```
entry 0x40080694
I (27) boot: ESP-IDF v4.4.2-dirty 2nd stage bootloader
I (27) boot: compile time 23:37:34
I (27) boot: chip revision: 3
I (31) boot_comm: chip revision: 3, min. bootloader chip revision: 0
I (38) boot.esp32: SPI Speed      : 40MHz
I (42) boot.esp32: SPI Mode       : DIO
I (47) boot.esp32: SPI Flash Size : 2MB
I (51) boot: Enabling RNG early entropy source...
I (57) boot: Partition Table:
I (60) boot: ## Label            Usage          Type ST Offset   Length
I (68) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (75) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (83) boot:  2 factory          factory app      00 00 00010000 00100000
I (90) boot: End of partition table
I (94) boot_comm: chip revision: 3, min. application chip revision: 0
I (101) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=12b4ch ( 76620) map
I (138) esp_image: segment 1: paddr=00022b74 vaddr=3ffb0000 size=03804h ( 14340) load
I (144) esp_image: segment 2: paddr=00026380 vaddr=40080000 size=09c98h ( 40088) load
I (160) esp_image: segment 3: paddr=00030020 vaddr=400d0020 size=6d138h (446776) map
I (322) esp_image: segment 4: paddr=0009d160 vaddr=40089c98 size=0a848h ( 43080) load
I (340) esp_image: segment 5: paddr=000a79b0 vaddr=50000000 size=00010h (    16) load
I (350) boot: Loaded app from partition at offset 0x10000
I (350) boot: Disabling RNG early entropy source...
I (363) cpu_start: Pro cpu up.
I (363) cpu_start: Starting app cpu, entry point is 0x40081198
0x40081198: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v4.4.2/components/esp_system/port/cpu_start.c:160

I (0) cpu_start: App cpu up.
I (379) cpu_start: Pro cpu start user code
I (379) cpu_start: cpu freq: 160000000
I (379) cpu_start: Application information:
I (384) cpu_start: Project name:     softAP
I (388) cpu_start: App version:      v4.4.2-dirty
I (394) cpu_start: Compile time:     Nov 12 2023 23:36:50
I (400) cpu_start: ELF file SHA256:  bed98ab6c46f6f9e...
I (406) cpu_start: ESP-IDF:          v4.4.2-dirty
I (412) heap_init: Initializing. RAM available for dynamic allocation:
I (419) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (425) heap_init: At 3FFB74C8 len 00028B38 (162 KiB): DRAM
I (431) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (437) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (444) heap_init: At 400944E0 len 0000BB20 (46 KiB): IRAM
I (451) spi_flash: detected chip: generic
I (455) spi_flash: flash io: dio
W (458) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (473) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (561) wifi softAP: ESP_WIFI_MODE_AP
I (571) wifi:wifi driver task: 3ffc0104, prio:23, stack:6656, core=0
I (571) system_api: Base MAC address is not set
I (571) system_api: read default base MAC address from EFUSE
I (591) wifi:wifi firmware version: eeaa27d
I (591) wifi:wifi certification version: v7.0
I (591) wifi:config NVS flash: enabled
I (591) wifi:config nano formating: disabled
I (601) wifi:Init data frame dynamic rx buffer num: 32
I (601) wifi:Init management frame dynamic rx buffer num: 32
I (611) wifi:Init management short buffer num: 32
I (611) wifi:Init dynamic tx buffer num: 32
I (621) wifi:Init static rx buffer size: 1600
I (621) wifi:Init static rx buffer num: 10
I (621) wifi:Init dynamic rx buffer num: 32
I (631) wifi_init: rx ba win: 6
I (631) wifi_init: tcpip mbox: 32
I (631) wifi_init: udp mbox: 6
I (641) wifi_init: tcp mbox: 6
I (641) wifi_init: tcp tx win: 5744
I (651) wifi_init: tcp rx win: 5744
I (651) wifi_init: tcp mss: 1440
I (651) wifi_init: WiFi IRAM OP enabled
I (661) wifi_init: WiFi RX IRAM OP enabled
I (671) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (771) wifi:mode : softAP (94:b5:55:f2:64:f9)
I (771) wifi:Total power save buffer number: 16
I (771) wifi:Init max length of beacon: 752/752
I (781) wifi:Init max length of beacon: 752/752
I (781) wifi softAP: wifi_init_softap finished. SSID:myssid-059 password:mypassword channel:1

```

## ผลลัพธ์
![02](https://github.com/DanupatSangseekaew/ESP32_ESP-IDF_WiFi-AP/assets/100436724/a76592ec-42bc-4075-8e39-c7b6aa92064a)
