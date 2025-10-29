### Lab1
# 1.1
```c
I (263) spi_flash: flash io: dio
W (266) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (279) main_task: Started on CPU0
I (289) main_task: Calling app_main()
Hello, ESP32 World!
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
ESP32 is running...
```
# Exercise 1
ANS
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct  8 2025 08:00:31
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=09a58h ( 39512) map
I (102) esp_image: segment 1: paddr=00019a80 vaddr=3ffb0000 size=023d8h (  9176) load
I (105) esp_image: segment 2: paddr=0001be60 vaddr=40080000 size=041b8h ( 16824) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=135f8h ( 79352) map
I (140) esp_image: segment 4: paddr=00033620 vaddr=400841b8 size=08df8h ( 36344) load
I (154) esp_image: segment 5: paddr=0003c420 vaddr=50000000 size=00020h (    32) load
I (161) boot: Loaded app from partition at offset 0x10000
I (161) boot: Disabling RNG early entropy source...
I (173) cpu_start: Multicore app
I (181) cpu_start: Pro cpu start user code
I (181) cpu_start: cpu freq: 160000000 Hz
I (181) app_init: Application information:
I (181) app_init: Project name:     hello_esp32
I (185) app_init: App version:      1
I (189) app_init: Compile time:     Oct  8 2025 07:59:38
I (194) app_init: ELF file SHA256:  83b5956b2...
I (198) app_init: ESP-IDF:          v5.5.1
I (202) efuse_init: Min chip rev:     v0.0
I (206) efuse_init: Max chip rev:     v3.99
I (210) efuse_init: Chip rev:         v3.1
I (214) heap_init: Initializing. RAM available for dynamic allocation:
I (220) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (225) heap_init: At 3FFB2CA0 len 0002D360 (180 KiB): DRAM
I (230) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (236) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (241) heap_init: At 4008CFB0 len 00013050 (76 KiB): IRAM
W (248) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (259) spi_flash: detected chip: generic
I (263) spi_flash: flash io: dio
W (266) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (279) main_task: Started on CPU0
I (289) main_task: Calling app_main()
=== My First ESP32 Project ===
Chip model: v5.5.1
Free heap: 305156 bytes
Running for 0 seconds
Running for 1 seconds
Running for 2 seconds
Running for 3 seconds
Running for 4 seconds
Running for 5 seconds
Running for 6 seconds
Running for 7 seconds
Running for 8 seconds
Running for 9 seconds
Running for 10 seconds
Running for 11 seconds
Running for 12 seconds
Running for 13 seconds
Running for 14 seconds
Running for 15 seconds
Running for 16 seconds
```
# Exercise 2
ANS
```c
I (154) esp_image: segment 5: paddr=0003c420 vaddr=50000000 size=00020h (    32) load
I (161) boot: Loaded app from partition at offset 0x10000
I (161) boot: Disabling RNG early entropy source...
I (173) cpu_start: Multicore app
I (181) cpu_start: Pro cpu start user code
I (181) cpu_start: cpu freq: 160000000 Hz
I (181) app_init: Application information:
I (181) app_init: Project name:     hello_esp32
I (185) app_init: App version:      1
I (189) app_init: Compile time:     Oct  8 2025 07:59:38
I (194) app_init: ELF file SHA256:  83b5956b2...
--- Warning: Checksum mismatch between flashed and built applications. Checksum of built application is c6e4a42a37f2f72f4d4c011c42940c20e23acf1edbe98601eaf8d14acb1f480e
I (198) app_init: ESP-IDF:          v5.5.1
I (202) efuse_init: Min chip rev:     v0.0
I (206) efuse_init: Max chip rev:     v3.99
I (210) efuse_init: Chip rev:         v3.1
I (214) heap_init: Initializing. RAM available for dynamic allocation:
I (220) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (225) heap_init: At 3FFB2CA0 len 0002D360 (180 KiB): DRAM
I (230) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (236) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (241) heap_init: At 4008CFB0 len 00013050 (76 KiB): IRAM
W (248) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (259) spi_flash: detected chip: generic
I (263) spi_flash: flash io: dio
W (266) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (279) main_task: Started on CPU0
I (289) main_task: Calling app_main()
=== My First ESP32 Project ===
Chip model: v5.5.1
Free heap: 305156 bytes
Running for 0 seconds
Running for 1 seconds
Running for 2 seconds
Running for 3 seconds
Running for 4 seconds
Running for 5 seconds
Running for 6 seconds
Running for 7 seconds
Running for 8 seconds
Running for 9 seconds
Running for 10 seconds
Running for 11 seconds
Running for 12 seconds
Running for 13 seconds
Running for 14 seconds
Running for 15 seconds
Running for 16 seconds
Running for 17 seconds
Running for 18 seconds
Running for 19 seconds
Running for 20 seconds
```
### LAB2
# 2-1
```c
I (278) main_task: Started on CPU0
I (288) main_task: Calling app_main()
Hello, ESP32 World!
ESP32 is running...
ESP32 is running...
ESP32 is running...
I (288) main_task: Returned from app_main()
```
# 2-2
```c
--- Formatted Logging Demo ---
I (335) LOGGING_DEMO: Sensor readings:
I (345) LOGGING_DEMO:   Temperature: 25°C
I (345) LOGGING_DEMO:   Voltage: 3.30V
I (345) LOGGING_DEMO:   Status: OK
I (355) LOGGING_DEMO: Data dump:
I (355) LOGGING_DEMO: de ad be ef
I (355) LOGGING_DEMO:
--- Conditional Logging Demo ---
I (365) LOGGING_DEMO: System is running normally
I (375) LOGGING_DEMO: NVS initialized successfully
I (375) LOGGING_DEMO: Main loop iteration: 0
I (2375) LOGGING_DEMO: Main loop iteration: 1
I (4375) LOGGING_DEMO: Main loop iteration: 2
I (6375) LOGGING_DEMO: Main loop iteration: 3
I (8375) LOGGING_DEMO: Main loop iteration: 4
I (10375) LOGGING_DEMO: Main loop iteration: 5
I (12375) LOGGING_DEMO: Main loop iteration: 6
I (14375) LOGGING_DEMO: Main loop iteration: 7
I (16375) LOGGING_DEMO: Main loop iteration: 8
I (18375) LOGGING_DEMO: Main loop iteration: 9
I (18375) LOGGING_DEMO: Memory status - Free: 303044 bytes
I (20375) LOGGING_DEMO: Main loop iteration: 10
I (22375) LOGGING_DEMO: Main loop iteration: 11
```
# 2-3
```c
I (12375) LOGGING_DEMO: Main loop iteration: 6
I (14375) LOGGING_DEMO: Main loop iteration: 7
I (16375) LOGGING_DEMO: Main loop iteration: 8
I (18375) LOGGING_DEMO: Main loop iteration: 9
I (18375) LOGGING_DEMO: Memory status - Free: 303044 bytes
I (20375) LOGGING_DEMO: Main loop iteration: 10
I (22375) LOGGING_DEMO: Main loop iteration: 11
I (24375) LOGGING_DEMO: Main loop iteration: 12
I (26375) LOGGING_DEMO: Main loop iteration: 13
I (28375) LOGGING_DEMO: Main loop iteration: 14
I (30375) LOGGING_DEMO: Main loop iteration: 15
I (32375) LOGGING_DEMO: Main loop iteration: 16
I (34375) LOGGING_DEMO: Main loop iteration: 17
I (36375) LOGGING_DEMO: Main loop iteration: 18
I (38375) LOGGING_DEMO: Main loop iteration: 19
I (38375) LOGGING_DEMO: Memory status - Free: 303044 bytes
W (38375) LOGGING_DEMO: Warning: Counter reached 20
I (40375) LOGGING_DEMO: Main loop iteration: 20
I (42375) LOGGING_DEMO: Main loop iteration: 21
I (44375) LOGGING_DEMO: Main loop iteration: 22
I (46375) LOGGING_DEMO: Main loop iteration: 23
I (48375) LOGGING_DEMO: Main loop iteration: 24
I (50375) LOGGING_DEMO: Main loop iteration: 25
I (52375) LOGGING_DEMO: Main loop iteration: 26
I (54375) LOGGING_DEMO: Main loop iteration: 27
I (56375) LOGGING_DEMO: Main loop iteration: 28

```
# 2-4
```c

```
## คำถามทบทวน

1. ความแตกต่างระหว่าง `printf()` และ `ESP_LOGI()` คืออะไร?
- printf() → แสดงข้อความออกทาง Serial Console ตรง ๆ ไม่มีระบบจัดการระดับ Log หรือ Tag
ESP_LOGI(TAG, "ข้อความ") → เป็น ระบบ logging ของ ESP-IDF
มี Tag สำหรับระบุโมดูล (เช่น “WIFI”, “MAIN”)
มี ระดับความสำคัญ (Log Level) เช่น ERROR, WARN, INFO, DEBUG, VERBOSE
สามารถเปิด–ปิด Log เฉพาะส่วนได้ ทำให้เหมาะกับการดีบักโปรแกรมขนาดใหญ่
2. Log level ไหนที่จะแสดงใน default configuration?
- โดยค่าเริ่มต้น (default) คือ INFO level
→ หมายถึงจะแสดงข้อความที่ระดับ INFO, WARN, ERROR, และ CRITICAL
(แต่จะไม่แสดง DEBUG หรือ VERBOSE)
3. การใช้ `ESP_ERROR_CHECK()` มีประโยชน์อย่างไร?
- ใช้เพื่อตรวจสอบว่าคำสั่งของ ESP-IDF
4. คำสั่งใดในการออกจาก Monitor mode?
- ใช้ Ctrl + ]
→ เพื่อออกจากโหมด idf.py monitor และกลับไปยัง command line
5. การตั้งค่า Log level สำหรับ tag เฉพาะทำอย่างไร?
- ใช้ฟังก์ชัน
`esp_log_level_set("TAG_NAME", ESP_LOG_DEBUG)`

### Lab3
# 3-1
```c
I (312) BASIC_TASKS: === System Information ===
I (322) BASIC_TASKS: Free heap: 296860 bytes
I (322) BASIC_TASKS: Min free heap: 296860 bytes
I (332) BASIC_TASKS: Number of tasks: 8
I (332) BASIC_TASKS: Uptime: 0 seconds
I (322) BASIC_TASKS: System Info Task created successfully
I (342) BASIC_TASKS: All tasks created. Main task will now idle.
I (342) BASIC_TASKS: Task handles - LED1: 0x3ffafe30, LED2: 0x3ffb5c94, Info: 0x3ffb69fc
I (352) BASIC_TASKS: Main task heartbeat
I (792) BASIC_TASKS: LED1 OFF
I (1292) BASIC_TASKS: LED1 ON
I (1792) BASIC_TASKS: LED1 OFF
I (2292) BASIC_TASKS: LED1 ON
I (2312) BASIC_TASKS: LED2 Blink Fast
I (2792) BASIC_TASKS: LED1 OFF
I (3292) BASIC_TASKS: LED1 ON
I (3332) BASIC_TASKS: === System Information ===
I (3332) BASIC_TASKS: Free heap: 296860 bytes
I (3332) BASIC_TASKS: Min free heap: 296860 bytes
I (3332) BASIC_TASKS: Number of tasks: 8
I (3332) BASIC_TASKS: Uptime: 3 seconds
I (3792) BASIC_TASKS: LED1 OFF
I (4292) BASIC_TASKS: LED1 ON
I (4312) BASIC_TASKS: LED2 Blink Fast
I (4792) BASIC_TASKS: LED1 OFF
I (5292) BASIC_TASKS: LED1 ON
I (5362) BASIC_TASKS: Main task heartbeat
I (5792) BASIC_TASKS: LED1 OFF
I (6292) BASIC_TASKS: LED1 ON
I (6312) BASIC_TASKS: LED2 Blink Fast
I (6332) BASIC_TASKS: === System Information ===
I (6332) BASIC_TASKS: Free heap: 296860 bytes
I (6332) BASIC_TASKS: Min free heap: 296860 bytes
I (6332) BASIC_TASKS: Number of tasks: 8
I (6332) BASIC_TASKS: Uptime: 6 seconds
I (6792) BASIC_TASKS: LED1 OFF
I (7292) BASIC_TASKS: LED1 ON
I (7792) BASIC_TASKS: LED1 OFF
```
# 3-2
