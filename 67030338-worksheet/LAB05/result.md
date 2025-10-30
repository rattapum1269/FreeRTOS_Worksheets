# 05-1-1
```c
I (284) main_task: Started on CPU0
I (294) main_task: Calling app_main()
I (294) SW_TIMERS: Software Timers Lab Starting...
I (294) SW_TIMERS: Creating software timers...
I (294) SW_TIMERS: All timers created successfully
I (294) SW_TIMERS: Starting timers...
I (304) SW_TIMERS: Timer control task started
I (304) SW_TIMERS: Timer system operational!
I (314) SW_TIMERS: LEDs indicate different timer activities:
I (314) SW_TIMERS:   GPIO2  - Blink Timer (toggles every 500ms)
I (324) SW_TIMERS:   GPIO4  - Heartbeat Timer (double blink every 2s)
I (324) SW_TIMERS:   GPIO5  - Status Timer (flash every 5s)
I (334) SW_TIMERS:   GPIO18 - One-shot Timer (5 quick flashes)
I (334) main_task: Returned from app_main()
I (804) SW_TIMERS: 💫 Blink Timer: Toggle #1 (LED: ON)
I (1304) SW_TIMERS: 💫 Blink Timer: Toggle #2 (LED: OFF)
I (1804) SW_TIMERS: 💫 Blink Timer: Toggle #3 (LED: ON)
I (2304) SW_TIMERS: 💓 Heartbeat Timer: Beat #1
I (2604) SW_TIMERS: 💫 Blink Timer: Toggle #4 (LED: OFF)
I (2804) SW_TIMERS: 💫 Blink Timer: Toggle #5 (LED: ON)
I (3304) SW_TIMERS: 💫 Blink Timer: Toggle #6 (LED: OFF)
I (3804) SW_TIMERS: 💫 Blink Timer: Toggle #7 (LED: ON)
I (4304) SW_TIMERS: 💓 Heartbeat Timer: Beat #2
I (4604) SW_TIMERS: 💫 Blink Timer: Toggle #8 (LED: OFF)
I (4804) SW_TIMERS: 💫 Blink Timer: Toggle #9 (LED: ON)
I (5304) SW_TIMERS: 📊 Status Timer: Update #1
I (5504) SW_TIMERS: ═══ TIMER STATISTICS ═══
I (5504) SW_TIMERS: Blink events:     9
I (5504) SW_TIMERS: Heartbeat events: 2
I (5504) SW_TIMERS: Status updates:   1
I (5504) SW_TIMERS: One-shot events:  0
I (5504) SW_TIMERS: Dynamic events:   0
I (5514) SW_TIMERS: ═══════════════════════
```
# 05-2-1
```c
--- 0x40080400: _invalid_pc_placeholder at C:/Users/09677/esp/v5.5.1/esp-idf/components/xtensa/xtensa_vectors.S:2235
entry 0x40080638
--- 0x40080638: call_start_cpu0 at C:/Users/09677/esp/v5.5.1/esp-idf/components/bootloader/subproject/main/bootloader_start.c:25
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 30 2025 14:53:04
I (29) boot: Multicore bootloader
I (31) boot: chip revision: v3.1
I (33) boot.esp32: SPI Speed      : 40MHz
I (37) boot.esp32: SPI Mode       : DIO
I (41) boot.esp32: SPI Flash Size : 2MB
I (44) boot: Enabling RNG early entropy source...
I (49) boot: Partition Table:
I (51) boot: ## Label            Usage          Type ST Offset   Length
I (58) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (64) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (71) boot:  2 factory          factory app      00 00 00010000 00100000
I (77) boot: End of partition table
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=1b3d4h (111572) map
I (126) esp_image: segment 1: paddr=0002b3fc vaddr=3ffb0000 size=03f84h ( 16260) load
I (132) esp_image: segment 2: paddr=0002f388 vaddr=40080000 size=00c90h (  3216) load
I (134) esp_image: segment 3: paddr=00030020 vaddr=400d0020 size=8bbd0h (572368) map
I (333) esp_image: segment 4: paddr=000bbbf8 vaddr=40080c90 size=179ech ( 96748) load
I (371) esp_image: segment 5: paddr=000d35ec vaddr=50000000 size=00020h (    32) load
I (383) boot: Loaded app from partition at offset 0x10000
I (383) boot: Disabling RNG early entropy source...
I (394) cpu_start: Multicore app
I (402) cpu_start: Pro cpu start user code
I (402) cpu_start: cpu freq: 160000000 Hz
I (402) app_init: Application information:
I (402) app_init: Project name:     timer_applications
I (407) app_init: App version:      dd6eab9
I (411) app_init: Compile time:     Oct 30 2025 14:45:56
I (416) app_init: ELF file SHA256:  60d4eadf3...
I (420) app_init: ESP-IDF:          v5.5.1
I (424) efuse_init: Min chip rev:     v0.0
I (428) efuse_init: Max chip rev:     v3.99
I (432) efuse_init: Chip rev:         v3.1
I (436) heap_init: Initializing. RAM available for dynamic allocation:
I (442) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (447) heap_init: At 3FFB82A0 len 00027D60 (159 KiB): DRAM
I (452) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (458) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (463) heap_init: At 4009867C len 00007984 (30 KiB): IRAM
W (470) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (482) spi_flash: detected chip: generic
I (485) spi_flash: flash io: dio
W (488) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
W (500) ADC: legacy driver is deprecated, please migrate to `esp_adc/adc_oneshot.h`
I (509) main_task: Started on CPU0
I (519) main_task: Calling app_main()
I (519) TIMER_APPS_PLUS: === Lab 2 PLUS Starting ===
I (539) TIMER_APPS_PLUS: Loaded pattern_secs from NVS
I (549) TIMER_APPS_PLUS: Favorite pattern from NVS = 1
I (559) wifi:wifi driver task: 3ffc0cbc, prio:23, stack:6656, core=0
I (569) wifi:wifi firmware version: 14da9b7
I (569) wifi:wifi certification version: v7.0
I (569) wifi:config NVS flash: enabled
I (569) wifi:config nano formatting: disabled
I (579) wifi:Init data frame dynamic rx buffer num: 32
I (579) wifi:Init static rx mgmt buffer num: 5
I (589) wifi:Init management short buffer num: 32
I (589) wifi:Init dynamic tx buffer num: 32
I (589) wifi:Init static rx buffer size: 1600
I (599) wifi:Init static rx buffer num: 10
I (599) wifi:Init dynamic rx buffer num: 32
I (609) wifi_init: rx ba win: 6
I (609) wifi_init: accept mbox: 6
I (609) wifi_init: tcpip mbox: 32
I (609) wifi_init: udp mbox: 6
I (619) wifi_init: tcp mbox: 6
I (619) wifi_init: tcp tx win: 5760
I (619) wifi_init: tcp rx win: 5760
I (629) wifi_init: tcp mss: 1440
I (629) wifi_init: WiFi IRAM OP enabled
I (629) wifi_init: WiFi RX IRAM OP enabled
I (639) phy_init: phy_version 4861,b71b5ad,Aug  5 2025,11:16:06
I (729) wifi:mode : sta (88:57:21:ad:64:98)
I (729) wifi:enable tsf
I (739) TIMER_APPS_PLUS: WiFi STA init, connecting to YOUR_SSID…
I (739) TIMER_APPS_PLUS: UDP heartbeat to 192.168.1.255:33333
I (739) TIMER_APPS_PLUS: Sensor consumer with priority via QueueSet
I (739) TIMER_APPS_PLUS: TEMP  : 3.61 C @ 230ms
I (749) TIMER_APPS_PLUS: HUM   : 9.6 %RH @ 230ms
W (749) TIMER_APPS_PLUS: Low humidity! change to SOS
I (759) TIMER_APPS_PLUS: LUX   : 163 lux @ 230ms
I (759) TIMER_APPS_PLUS: System up. Watch LEDs & logs.
I (759) main_task: Returned from app_main()
I (1239) TIMER_APPS_PLUS: TEMP  : 4.14 C @ 730ms
I (1739) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 1230ms
I (1739) TIMER_APPS_PLUS: HUM   : 11.1 %RH @ 1230ms
W (1739) TIMER_APPS_PLUS: Low humidity! change to SOS
I (2239) TIMER_APPS_PLUS: TEMP  : 2.62 C @ 1730ms
I (2739) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 2230ms
I (2739) TIMER_APPS_PLUS: HUM   : 7.2 %RH @ 2230ms
W (2739) TIMER_APPS_PLUS: Low humidity! change to SOS
I (2739) TIMER_APPS_PLUS: LUX   : 135 lux @ 2230ms
I (3239) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 2730ms
I (3739) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 3230ms
I (3739) TIMER_APPS_PLUS: HUM   : 4.3 %RH @ 3230ms
W (3739) TIMER_APPS_PLUS: Low humidity! change to SOS
I (3739) TIMER_APPS_PLUS:
--- STATUS ---
uptime=3s healthy=OK feeds=1 timeouts=0
sensors total=13 (T=7,H=4,L=2)
pattern=4 changes=0
net fail-streak=0 sock=54
--------------
W (3749) TIMER_APPS_PLUS: Heartbeat send failed (1/3)
I (4239) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 3730ms
I (4739) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 4230ms
I (4739) TIMER_APPS_PLUS: HUM   : 4.3 %RH @ 4230ms
W (4739) TIMER_APPS_PLUS: Low humidity! change to SOS
I (4739) TIMER_APPS_PLUS: LUX   : 79 lux @ 4230ms
I (5239) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 4730ms
I (5739) TIMER_APPS_PLUS: TEMP  : 2.15 C @ 5230ms
I (5739) TIMER_APPS_PLUS: HUM   : 4.3 %RH @ 5230ms
```
# 05-3-1
```c
I (288) main_task: Started on CPU0
I (288) main_task: Calling app_main()
I (288) ADV_TIMERS: Advanced Timer Management Lab Starting...
I (298) ADV_TIMERS: Timer pool initialized with 20 slots
I (298) ADV_TIMERS: Monitoring systems initialized
I (308) ADV_TIMERS: System timers started
I (308) ADV_TIMERS: Performance analysis task started
I (1308) ADV_TIMERS: 🏥 Health Monitor:
I (1308) ADV_TIMERS:   Active Timers: 0/0
I (1308) ADV_TIMERS:   Pool Utilization: 0%
I (1308) ADV_TIMERS:   Dynamic Timers: 0/10
I (1308) ADV_TIMERS:   Free Heap: 311944 bytes
I (1308) ADV_TIMERS:   Failed Creations: 0
I (2308) ADV_TIMERS: 🏥 Health Monitor:
I (2308) ADV_TIMERS:   Active Timers: 0/0
I (2308) ADV_TIMERS:   Pool Utilization: 0%
I (2308) ADV_TIMERS:   Dynamic Timers: 0/10
I (2308) ADV_TIMERS:   Free Heap: 311944 bytes
I (2308) ADV_TIMERS:   Failed Creations: 0
I (3308) ADV_TIMERS: 🏥 Health Monitor:
I (3308) ADV_TIMERS:   Active Timers: 0/0
I (3308) ADV_TIMERS:   Pool Utilization: 0%
I (3308) ADV_TIMERS:   Dynamic Timers: 0/10
I (3308) ADV_TIMERS:   Free Heap: 311944 bytes
I (3308) ADV_TIMERS:   Failed Creations: 0
I (4308) ADV_TIMERS: 🏥 Health Monitor:
I (4308) ADV_TIMERS:   Active Timers: 0/0
I (4308) ADV_TIMERS:   Pool Utilization: 0%
I (4308) ADV_TIMERS:   Dynamic Timers: 0/10
I (4308) ADV_TIMERS:   Free Heap: 311944 bytes
I (4308) ADV_TIMERS:   Failed Creations: 0
I (5308) ADV_TIMERS: 🔥 Starting stress test...
I (5308) ADV_TIMERS: 🏥 Health Monitor:
I (5308) ADV_TIMERS:   Active Timers: 1/1
I (5308) ADV_TIMERS:   Pool Utilization: 5%
I (5308) ADV_TIMERS:   Dynamic Timers: 0/10
I (5308) ADV_TIMERS:   Free Heap: 309508 bytes
I (5318) ADV_TIMERS:   Failed Creations: 0
I (5318) ADV_TIMERS: 🚀 Advanced Timer Management System Running
I (5328) ADV_TIMERS: Monitor LEDs for system status:
I (5328) ADV_TIMERS:   GPIO2  - Performance Warning
I (5338) ADV_TIMERS:   GPIO4  - Health Status
I (5338) ADV_TIMERS:   GPIO5  - Stress Test Activity
I (5348) ADV_TIMERS:   GPIO18 - Error/Memory Warning
I (5348) main_task: Returned from app_main()
I (6308) ADV_TIMERS: 🏥 Health Monitor:
I (6308) ADV_TIMERS:   Active Timers: 10/10
I (6308) ADV_TIMERS:   Pool Utilization: 50%
I (6308) ADV_TIMERS:   Dynamic Timers: 0/10
I (6308) ADV_TIMERS:   Free Heap: 313568 bytes
I (6308) ADV_TIMERS:   Failed Creations: 0
I (7308) ADV_TIMERS: 🏥 Health Monitor:
I (7308) ADV_TIMERS:   Active Timers: 10/10
I (7308) ADV_TIMERS:   Pool Utilization: 50%
I (7308) ADV_TIMERS:   Dynamic Timers: 0/10
I (7308) ADV_TIMERS:   Free Heap: 313568 bytes
I (7308) ADV_TIMERS:   Failed Creations: 0
I (8208) ADV_TIMERS: 💪 Stress test callback #100
I (8308) ADV_TIMERS: 🏥 Health Monitor:
I (8308) ADV_TIMERS:   Active Timers: 10/10
I (8308) ADV_TIMERS:   Pool Utilization: 50%
I (8308) ADV_TIMERS:   Dynamic Timers: 0/10
I (8308) ADV_TIMERS:   Free Heap: 313568 bytes
I (8308) ADV_TIMERS:   Failed Creations: 0
I (9308) ADV_TIMERS: 🏥 Health Monitor:
I (9308) ADV_TIMERS:   Active Timers: 10/10
I (9308) ADV_TIMERS:   Pool Utilization: 50%
I (9308) ADV_TIMERS:   Dynamic Timers: 0/10
I (9308) ADV_TIMERS:   Free Heap: 313568 bytes
I (9308) ADV_TIMERS:   Failed Creations: 0
I (10308) ADV_TIMERS: 📊 Performance Analysis:
I (10308) ADV_TIMERS:   Callback Duration: Avg=48μs, Max=81μs, Min=18μs
I (10308) ADV_TIMERS:   Timer Accuracy: 100.0% (19/19)
I (10308) ADV_TIMERS:   Callback Overruns: 0
I (10308) ADV_TIMERS:
═══ PERFORMANCE REPORT ═══
I (10318) ADV_TIMERS: Total Timers Created: 10
I (10318) ADV_TIMERS: Current Active: 10
I (10328) ADV_TIMERS: Pool Utilization: 50%
I (10328) ADV_TIMERS: Average Accuracy: 100.0%
I (10338) ADV_TIMERS: Callback Overruns: 0
I (10338) ADV_TIMERS: Command Failures: 0
I (10338) ADV_TIMERS: ═════════════════════════

I (10348) ADV_TIMERS: 🏥 Health Monitor:
I (10358) ADV_TIMERS:   Active Timers: 10/10
I (10358) ADV_TIMERS:   Pool Utilization: 50%
I (10358) ADV_TIMERS:   Dynamic Timers: 0/10
I (10368) ADV_TIMERS:   Free Heap: 313328 bytes
I (10368) ADV_TIMERS:   Failed Creations: 0
I (10658) ADV_TIMERS: 💪 Stress test callback #200
I (11308) ADV_TIMERS: 🏥 Health Monitor:
I (11308) ADV_TIMERS:   Active Timers: 10/10
I (11308) ADV_TIMERS:   Pool Utilization: 50%
I (11308) ADV_TIMERS:   Dynamic Timers: 0/10
I (11308) ADV_TIMERS:   Free Heap: 313328 bytes
I (11308) ADV_TIMERS:   Failed Creations: 0
```