# 64030207 Sittinon
- Repo
## Connected Wifi


## Output
```
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
I (27) boot: compile time 13:09:31
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
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=1e488h (124040) map
I (141) esp_image: segment 1: paddr=0002e4b0 vaddr=3ffb0000 size=01b68h (  7016) load
I (144) esp_image: segment 2: paddr=00030020 vaddr=400d0020 size=79ddch (499164) map
I (327) esp_image: segment 3: paddr=000a9e04 vaddr=3ffb1b68 size=017d4h (  6100) load
I (329) esp_image: segment 4: paddr=000ab5e0 vaddr=40080000 size=14c98h ( 85144) load
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
I (421) cpu_start: Compile time:     Oct 16 2023 13:09:05
I (427) cpu_start: ELF file SHA256:  e69e34f176d9e8b1...
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
I (603) wifi softAP: ESP_WIFI_MODE_AP
I (613) wifi:wifi driver task: 3ffbf020, prio:23, stack:6656, core=0
I (613) system_api: Base MAC address is not set
I (613) system_api: read default base MAC address from EFUSE
I (633) wifi:wifi firmware version: 57982fe
I (643) wifi:wifi certification version: v7.0
I (643) wifi:config NVS flash: enabled
I (643) wifi:config nano formating: disabled
I (643) wifi:Init data frame dynamic rx buffer num: 32
I (643) wifi:Init management frame dynamic rx buffer num: 32
I (653) wifi:Init management short buffer num: 32
I (653) wifi:Init dynamic tx buffer num: 32
I (663) wifi:Init static rx buffer size: 1600
I (663) wifi:Init static rx buffer num: 10
I (673) wifi:Init dynamic rx buffer num: 32
I (673) wifi_init: rx ba win: 6
I (673) wifi_init: tcpip mbox: 32
I (683) wifi_init: udp mbox: 6
I (683) wifi_init: tcp mbox: 6
I (693) wifi_init: tcp tx win: 5744
I (693) wifi_init: tcp rx win: 5744
I (693) wifi_init: tcp mss: 1440
I (703) wifi_init: WiFi IRAM OP enabled
I (703) wifi_init: WiFi RX IRAM OP enabled
I (713) phy_init: phy_version 4670,719f9f6,Feb 18 2021,17:07:07
I (813) wifi:mode : softAP (94:b5:55:f6:f5:91)
I (813) wifi:Total power save buffer number: 16
I (813) wifi:Init max length of beacon: 752/752
I (823) wifi:Init max length of beacon: 752/752
I (823) wifi softAP: wifi_init_softap finished. SSID:myssid-207 password:0972840460 channel:1
```
