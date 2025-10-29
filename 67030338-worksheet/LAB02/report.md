# 02-1-1
```c
--- 0x40080400: _invalid_pc_placeholder at C:/Users/09677/esp/v5.5.1/esp-idf/components/xtensa/xtensa_vectors.S:2235
entry 0x40080638
--- 0x40080638: call_start_cpu0 at C:/Users/09677/esp/v5.5.1/esp-idf/components/bootloader/subproject/main/bootloader_start.c:25
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 14 2025 09:09:28
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a640h ( 42560) map
I (103) esp_image: segment 1: paddr=0001a668 vaddr=3ffb0000 size=023f8h (  9208) load
I (106) esp_image: segment 2: paddr=0001ca68 vaddr=40080000 size=035b0h ( 13744) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=14c0ch ( 85004) map
I (143) esp_image: segment 4: paddr=00034c34 vaddr=400835b0 size=09a00h ( 39424) load
I (159) esp_image: segment 5: paddr=0003e63c vaddr=50000000 size=00020h (    32) load
I (165) boot: Loaded app from partition at offset 0x10000
I (165) boot: Disabling RNG early entropy source...
I (177) cpu_start: Multicore app
I (185) cpu_start: Pro cpu start user code
I (185) cpu_start: cpu freq: 160000000 Hz
I (185) app_init: Application information:
I (185) app_init: Project name:     Task-Priority
I (190) app_init: App version:      1
I (193) app_init: Compile time:     Oct 14 2025 09:08:25
I (198) app_init: ELF file SHA256:  612e01815...
I (203) app_init: ESP-IDF:          v5.5.1
I (206) efuse_init: Min chip rev:     v0.0
I (210) efuse_init: Max chip rev:     v3.99
I (214) efuse_init: Chip rev:         v3.1
I (218) heap_init: Initializing. RAM available for dynamic allocation:
I (224) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (229) heap_init: At 3FFB2CD0 len 0002D330 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (240) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008CFB0 len 00013050 (76 KiB): IRAM
W (252) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (264) spi_flash: detected chip: generic
I (267) spi_flash: flash io: dio
W (270) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (283) main_task: Started on CPU0
I (293) main_task: Calling app_main()
I (293) PRIORITY_DEMO: === FreeRTOS Priority Scheduling Demo ===
I (293) PRIORITY_DEMO: Creating tasks with different priorities...
I (293) PRIORITY_DEMO: High Priority Task started (Priority 5)
I (303) PRIORITY_DEMO: Medium Priority Task started (Priority 3)
I (303) PRIORITY_DEMO: Control Task started
I (313) PRIORITY_DEMO: Low Priority Task started (Priority 1)
I (313) PRIORITY_DEMO: Press button to start priority test
I (323) PRIORITY_DEMO: Watch LEDs: GPIO2=High, GPIO4=Med, GPIO5=Low priority
I (333) main_task: Returned from app_main()
```
# 02-1-2
```c
--- 0x40080400: _invalid_pc_placeholder at C:/Users/09677/esp/v5.5.1/esp-idf/components/xtensa/xtensa_vectors.S:2235
entry 0x40080638
--- 0x40080638: call_start_cpu0 at C:/Users/09677/esp/v5.5.1/esp-idf/components/bootloader/subproject/main/bootloader_start.c:25
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 14 2025 09:09:28
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a640h ( 42560) map
I (103) esp_image: segment 1: paddr=0001a668 vaddr=3ffb0000 size=023f8h (  9208) load     
I (106) esp_image: segment 2: paddr=0001ca68 vaddr=40080000 size=035b0h ( 13744) load     
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=14c0ch ( 85004) map
I (143) esp_image: segment 4: paddr=00034c34 vaddr=400835b0 size=09a00h ( 39424) load     
I (159) esp_image: segment 5: paddr=0003e63c vaddr=50000000 size=00020h (    32) load     
I (165) boot: Loaded app from partition at offset 0x10000
I (165) boot: Disabling RNG early entropy source...
I (177) cpu_start: Multicore app
I (185) cpu_start: Pro cpu start user code
I (185) cpu_start: cpu freq: 160000000 Hz
I (185) app_init: Application information:
I (185) app_init: Project name:     Task-Priority
I (190) app_init: App version:      1
I (193) app_init: Compile time:     Oct 14 2025 09:08:25
I (198) app_init: ELF file SHA256:  9fcc2e2d1...
I (203) app_init: ESP-IDF:          v5.5.1
I (206) efuse_init: Min chip rev:     v0.0
I (210) efuse_init: Max chip rev:     v3.99
I (214) efuse_init: Chip rev:         v3.1
I (218) heap_init: Initializing. RAM available for dynamic allocation:
I (224) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (229) heap_init: At 3FFB2CD0 len 0002D330 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (240) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008CFB0 len 00013050 (76 KiB): IRAM
W (252) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (264) spi_flash: detected chip: generic
I (267) spi_flash: flash io: dio
W (270) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (283) main_task: Started on CPU0
I (293) main_task: Calling app_main()
I (293) PRIORITY_DEMO: === FreeRTOS Priority Scheduling Demo ===
I (293) PRIORITY_DEMO: Creating tasks with different priorities...
I (293) PRIORITY_DEMO: High Priority Task started (Priority 5)
I (303) PRIORITY_DEMO: Medium Priority Task started (Priority 3)
I (303) PRIORITY_DEMO: Control Task started
I (313) PRIORITY_DEMO: Low Priority Task started (Priority 1)
I (313) PRIORITY_DEMO: Press button to start priority test
I (323) PRIORITY_DEMO: Watch LEDs: GPIO2=High, GPIO4=Med, GPIO5=Low priority
I (333) main_task: Returned from app_main()

```

# 02-1-3
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 14 2025 09:09:28
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a640h ( 42560) map       
I (103) esp_image: segment 1: paddr=0001a668 vaddr=3ffb0000 size=023f8h (  9208) load
I (106) esp_image: segment 2: paddr=0001ca68 vaddr=40080000 size=035b0h ( 13744) load     
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=14c0ch ( 85004) map
I (143) esp_image: segment 4: paddr=00034c34 vaddr=400835b0 size=09a00h ( 39424) load     
I (159) esp_image: segment 5: paddr=0003e63c vaddr=50000000 size=00020h (    32) load
I (165) boot: Loaded app from partition at offset 0x10000
I (165) boot: Disabling RNG early entropy source...
I (177) cpu_start: Multicore app
I (185) cpu_start: Pro cpu start user code
I (185) cpu_start: cpu freq: 160000000 Hz
I (185) app_init: Application information:
I (185) app_init: Project name:     Task-Priority
I (190) app_init: App version:      1
I (193) app_init: Compile time:     Oct 14 2025 09:08:25
I (198) app_init: ELF file SHA256:  b45ed87d6...
I (203) app_init: ESP-IDF:          v5.5.1
I (206) efuse_init: Min chip rev:     v0.0
I (210) efuse_init: Max chip rev:     v3.99
I (214) efuse_init: Chip rev:         v3.1
I (218) heap_init: Initializing. RAM available for dynamic allocation:
I (224) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (229) heap_init: At 3FFB2CD0 len 0002D330 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (240) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008CFB0 len 00013050 (76 KiB): IRAM
W (252) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (264) spi_flash: detected chip: generic
I (267) spi_flash: flash io: dio
W (270) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (283) main_task: Started on CPU0
I (293) main_task: Calling app_main()
I (293) PRIORITY_DEMO: === FreeRTOS Priority Scheduling Demo ===
I (293) PRIORITY_DEMO: Creating tasks with different priorities...
I (293) PRIORITY_DEMO: High Priority Task started (Priority 5)
I (303) PRIORITY_DEMO: Medium Priority Task started (Priority 3)
I (303) PRIORITY_DEMO: Control Task started
I (303) PRIORITY_DEMO: Press button to start priority test
I (303) PRIORITY_DEMO: Low Priority Task started (Priority 1)
I (313) PRIORITY_DEMO: Watch LEDs: GPIO2=High, GPIO4=Med, GPIO5=Low priority
I (333) main_task: Returned from app_main()
W (513) PRIORITY_DEMO: === STARTING PRIORITY TEST ===
I (523) PRIORITY_DEMO: Low priority running (1)
I (553) PRIORITY_DEMO: Equal Priority Task 1 running
I (553) PRIORITY_DEMO: Equal Priority Task 2 running
I (563) PRIORITY_DEMO: Equal Priority Task 3 running
I (603) PRIORITY_DEMO: HIGH PRIORITY RUNNING (1)
I (613) PRIORITY_DEMO: Medium priority running (1)
I (643) PRIORITY_DEMO: Equal Priority Task 1 running
I (643) PRIORITY_DEMO: Equal Priority Task 2 running
I (673) PRIORITY_DEMO: Equal Priority Task 3 running
I (723) PRIORITY_DEMO: Equal Priority Task 1 running
I (723) PRIORITY_DEMO: Equal Priority Task 2 running
I (753) PRIORITY_DEMO: Equal Priority Task 3 running
I (803) PRIORITY_DEMO: Equal Priority Task 1 running
I (803) PRIORITY_DEMO: Equal Priority Task 2 running
I (813) PRIORITY_DEMO: HIGH PRIORITY RUNNING (2)
I (833) PRIORITY_DEMO: Equal Priority Task 3 running
I (883) PRIORITY_DEMO: Equal Priority Task 1 running
I (893) PRIORITY_DEMO: Equal Priority Task 2 running
I (913) PRIORITY_DEMO: Equal Priority Task 3 running
I (933) PRIORITY_DEMO: Medium priority running (2)
I (963) PRIORITY_DEMO: Equal Priority Task 1 running
I (973) PRIORITY_DEMO: Equal Priority Task 2 running
I (993) PRIORITY_DEMO: Equal Priority Task 3 running
I (1023) PRIORITY_DEMO: HIGH PRIORITY RUNNING (3)
I (1043) PRIORITY_DEMO: Equal Priority Task 1 running
I (1053) PRIORITY_DEMO: Equal Priority Task 2 running
I (1073) PRIORITY_DEMO: Equal Priority Task 3 running
I (1123) PRIORITY_DEMO: Equal Priority Task 1 running
I (1133) PRIORITY_DEMO: Equal Priority Task 2 running
I (1153) PRIORITY_DEMO: Equal Priority Task 3 running
I (1203) PRIORITY_DEMO: Equal Priority Task 1 running
I (1213) PRIORITY_DEMO: Equal Priority Task 2 running
I (1233) PRIORITY_DEMO: HIGH PRIORITY RUNNING (4)
I (1243) PRIORITY_DEMO: Equal Priority Task 3 running
I (1243) PRIORITY_DEMO: Low priority running (2)
I (1253) PRIORITY_DEMO: Medium priority running (3)
I (1293) PRIORITY_DEMO: Equal Priority Task 1 running
I (1293) PRIORITY_DEMO: Equal Priority Task 2 running
I (1323) PRIORITY_DEMO: Equal Priority Task 3 running
I (1373) PRIORITY_DEMO: Equal Priority Task 1 running
I (1373) PRIORITY_DEMO: Equal Priority Task 2 running
I (1403) PRIORITY_DEMO: Equal Priority Task 3 running
I (1443) PRIORITY_DEMO: HIGH PRIORITY RUNNING (5)
I (1453) PRIORITY_DEMO: Equal Priority Task 1 running
I (1453) PRIORITY_DEMO: Equal Priority Task 2 running
I (1483) PRIORITY_DEMO: Equal Priority Task 3 running
I (1533) PRIORITY_DEMO: Equal Priority Task 1 running
I (1533) PRIORITY_DEMO: Equal Priority Task 2 running
I (1563) PRIORITY_DEMO: Equal Priority Task 3 running
I (1573) PRIORITY_DEMO: Medium priority running (4)
I (1613) PRIORITY_DEMO: Equal Priority Task 1 running
I (1613) PRIORITY_DEMO: Equal Priority Task 2 running
I (1643) PRIORITY_DEMO: Equal Priority Task 3 running
I (1653) PRIORITY_DEMO: HIGH PRIORITY RUNNING (6)
I (1693) PRIORITY_DEMO: Equal Priority Task 1 running
I (1693) PRIORITY_DEMO: Equal Priority Task 2 running
I (1723) PRIORITY_DEMO: Equal Priority Task 3 running
I (1773) PRIORITY_DEMO: Equal Priority Task 1 running
I (1773) PRIORITY_DEMO: Equal Priority Task 2 running
I (1803) PRIORITY_DEMO: Equal Priority Task 3 running
I (1853) PRIORITY_DEMO: Equal Priority Task 1 running
I (1853) PRIORITY_DEMO: Equal Priority Task 2 running
I (1863) PRIORITY_DEMO: HIGH PRIORITY RUNNING (7)
I (1883) PRIORITY_DEMO: Equal Priority Task 3 running
I (1893) PRIORITY_DEMO: Medium priority running (5)
I (1933) PRIORITY_DEMO: Equal Priority Task 1 running
I (1943) PRIORITY_DEMO: Equal Priority Task 2 running
I (1963) PRIORITY_DEMO: Equal Priority Task 3 running
I (2013) PRIORITY_DEMO: Equal Priority Task 1 running
I (2013) PRIORITY_DEMO: Low priority running (3)
I (2023) PRIORITY_DEMO: Equal Priority Task 2 running
I (2043) PRIORITY_DEMO: Equal Priority Task 3 running
I (2073) PRIORITY_DEMO: HIGH PRIORITY RUNNING (8)
I (2093) PRIORITY_DEMO: Equal Priority Task 1 running
I (2103) PRIORITY_DEMO: Equal Priority Task 2 running
I (2123) PRIORITY_DEMO: Equal Priority Task 3 running
I (2173) PRIORITY_DEMO: Equal Priority Task 1 running
I (2183) PRIORITY_DEMO: Equal Priority Task 2 running
I (2203) PRIORITY_DEMO: Equal Priority Task 3 running
I (2213) PRIORITY_DEMO: Medium priority running (6)
I (2253) PRIORITY_DEMO: Equal Priority Task 1 running
I (2263) PRIORITY_DEMO: Equal Priority Task 2 running
I (2283) PRIORITY_DEMO: HIGH PRIORITY RUNNING (9)
I (2293) PRIORITY_DEMO: Equal Priority Task 3 running
I (2343) PRIORITY_DEMO: Equal Priority Task 1 running
I (2343) PRIORITY_DEMO: Equal Priority Task 2 running
I (2373) PRIORITY_DEMO: Equal Priority Task 3 running
I (2423) PRIORITY_DEMO: Equal Priority Task 1 running
I (2423) PRIORITY_DEMO: Equal Priority Task 2 running
I (2453) PRIORITY_DEMO: Equal Priority Task 3 running
I (2493) PRIORITY_DEMO: HIGH PRIORITY RUNNING (10)
I (2503) PRIORITY_DEMO: Equal Priority Task 1 running
I (2503) PRIORITY_DEMO: Equal Priority Task 2 running
I (2533) PRIORITY_DEMO: Medium priority running (7)
I (2533) PRIORITY_DEMO: Equal Priority Task 3 running
I (2583) PRIORITY_DEMO: Equal Priority Task 2 running
I (2583) PRIORITY_DEMO: Equal Priority Task 1 running
I (2613) PRIORITY_DEMO: Equal Priority Task 3 running
I (2663) PRIORITY_DEMO: Equal Priority Task 2 running
I (2663) PRIORITY_DEMO: Equal Priority Task 1 running
I (2693) PRIORITY_DEMO: Equal Priority Task 3 running
I (2703) PRIORITY_DEMO: HIGH PRIORITY RUNNING (11)
I (2743) PRIORITY_DEMO: Equal Priority Task 2 running
I (2743) PRIORITY_DEMO: Equal Priority Task 1 running
I (2773) PRIORITY_DEMO: Equal Priority Task 3 running
I (2823) PRIORITY_DEMO: Equal Priority Task 2 running
I (2823) PRIORITY_DEMO: Equal Priority Task 1 running
I (2853) PRIORITY_DEMO: Medium priority running (8)
I (2853) PRIORITY_DEMO: Equal Priority Task 3 running
I (2883) PRIORITY_DEMO: Low priority running (4)
I (2903) PRIORITY_DEMO: Equal Priority Task 2 running
I (2913) PRIORITY_DEMO: HIGH PRIORITY RUNNING (12)
I (2913) PRIORITY_DEMO: Equal Priority Task 1 running
I (2943) PRIORITY_DEMO: Equal Priority Task 3 running
I (2993) PRIORITY_DEMO: Equal Priority Task 1 running
I (3003) PRIORITY_DEMO: Equal Priority Task 2 running
I (3023) PRIORITY_DEMO: Equal Priority Task 3 running
I (3073) PRIORITY_DEMO: Equal Priority Task 1 running
I (3083) PRIORITY_DEMO: Equal Priority Task 2 running
I (3103) PRIORITY_DEMO: Equal Priority Task 3 running
I (3123) PRIORITY_DEMO: HIGH PRIORITY RUNNING (13)
I (3153) PRIORITY_DEMO: Equal Priority Task 1 running
I (3163) PRIORITY_DEMO: Equal Priority Task 2 running
I (3173) PRIORITY_DEMO: Medium priority running (9)
I (3193) PRIORITY_DEMO: Equal Priority Task 3 running
I (3253) PRIORITY_DEMO: Equal Priority Task 1 running
I (3253) PRIORITY_DEMO: Equal Priority Task 2 running
I (3283) PRIORITY_DEMO: Equal Priority Task 3 running
I (3333) PRIORITY_DEMO: HIGH PRIORITY RUNNING (14)
I (3333) PRIORITY_DEMO: Equal Priority Task 1 running
I (3343) PRIORITY_DEMO: Equal Priority Task 2 running
I (3363) PRIORITY_DEMO: Equal Priority Task 3 running
I (3413) PRIORITY_DEMO: Equal Priority Task 1 running
I (3423) PRIORITY_DEMO: Equal Priority Task 2 running
I (3443) PRIORITY_DEMO: Equal Priority Task 3 running
I (3493) PRIORITY_DEMO: Medium priority running (10)
I (3493) PRIORITY_DEMO: Equal Priority Task 1 running
I (3513) PRIORITY_DEMO: Equal Priority Task 2 running
I (3523) PRIORITY_DEMO: Equal Priority Task 3 running
I (3543) PRIORITY_DEMO: HIGH PRIORITY RUNNING (15)
I (3573) PRIORITY_DEMO: Equal Priority Task 1 running
I (3603) PRIORITY_DEMO: Equal Priority Task 2 running
I (3603) PRIORITY_DEMO: Equal Priority Task 3 running
I (3653) PRIORITY_DEMO: Low priority running (5)
I (3663) PRIORITY_DEMO: Equal Priority Task 1 running
I (3683) PRIORITY_DEMO: Equal Priority Task 2 running
I (3683) PRIORITY_DEMO: Equal Priority Task 3 running
I (3753) PRIORITY_DEMO: HIGH PRIORITY RUNNING (16)
I (3753) PRIORITY_DEMO: Equal Priority Task 1 running
I (3763) PRIORITY_DEMO: Equal Priority Task 2 running
I (3783) PRIORITY_DEMO: Equal Priority Task 3 running
I (3813) PRIORITY_DEMO: Medium priority running (11)
I (3843) PRIORITY_DEMO: Equal Priority Task 1 running
I (3843) PRIORITY_DEMO: Equal Priority Task 2 running
I (3873) PRIORITY_DEMO: Equal Priority Task 3 running
I (3923) PRIORITY_DEMO: Equal Priority Task 1 running
I (3923) PRIORITY_DEMO: Equal Priority Task 2 running
I (3953) PRIORITY_DEMO: Equal Priority Task 3 running
I (3963) PRIORITY_DEMO: HIGH PRIORITY RUNNING (17)
I (4003) PRIORITY_DEMO: Equal Priority Task 1 running
I (4003) PRIORITY_DEMO: Equal Priority Task 2 running
I (4033) PRIORITY_DEMO: Equal Priority Task 3 running
I (4083) PRIORITY_DEMO: Equal Priority Task 1 running
I (4083) PRIORITY_DEMO: Equal Priority Task 2 running
I (4113) PRIORITY_DEMO: Equal Priority Task 3 running
I (4133) PRIORITY_DEMO: Medium priority running (12)
I (4163) PRIORITY_DEMO: Equal Priority Task 1 running
I (4163) PRIORITY_DEMO: Equal Priority Task 2 running
I (4173) PRIORITY_DEMO: HIGH PRIORITY RUNNING (18)
I (4193) PRIORITY_DEMO: Equal Priority Task 3 running
I (4243) PRIORITY_DEMO: Equal Priority Task 1 running
I (4253) PRIORITY_DEMO: Equal Priority Task 2 running
I (4273) PRIORITY_DEMO: Equal Priority Task 3 running
I (4323) PRIORITY_DEMO: Equal Priority Task 1 running
I (4333) PRIORITY_DEMO: Equal Priority Task 2 running
I (4353) PRIORITY_DEMO: Equal Priority Task 3 running
I (4383) PRIORITY_DEMO: HIGH PRIORITY RUNNING (19)
I (4403) PRIORITY_DEMO: Equal Priority Task 1 running
I (4413) PRIORITY_DEMO: Equal Priority Task 2 running
I (4433) PRIORITY_DEMO: Equal Priority Task 3 running
I (4453) PRIORITY_DEMO: Medium priority running (13)
I (4463) PRIORITY_DEMO: Low priority running (6)
I (4483) PRIORITY_DEMO: Equal Priority Task 1 running
I (4493) PRIORITY_DEMO: Equal Priority Task 2 running
I (4513) PRIORITY_DEMO: Equal Priority Task 3 running
I (4563) PRIORITY_DEMO: Equal Priority Task 1 running
I (4573) PRIORITY_DEMO: Equal Priority Task 2 running
I (4593) PRIORITY_DEMO: HIGH PRIORITY RUNNING (20)
I (4603) PRIORITY_DEMO: Equal Priority Task 3 running
I (4653) PRIORITY_DEMO: Equal Priority Task 1 running
I (4653) PRIORITY_DEMO: Equal Priority Task 2 running
I (4683) PRIORITY_DEMO: Equal Priority Task 3 running
I (4733) PRIORITY_DEMO: Equal Priority Task 1 running
I (4733) PRIORITY_DEMO: Equal Priority Task 2 running
I (4763) PRIORITY_DEMO: Equal Priority Task 3 running
I (4773) PRIORITY_DEMO: Medium priority running (14)
I (4803) PRIORITY_DEMO: HIGH PRIORITY RUNNING (21)
I (4813) PRIORITY_DEMO: Equal Priority Task 1 running
I (4813) PRIORITY_DEMO: Equal Priority Task 2 running
I (4843) PRIORITY_DEMO: Equal Priority Task 3 running
I (4893) PRIORITY_DEMO: Equal Priority Task 1 running
I (4893) PRIORITY_DEMO: Equal Priority Task 2 running
I (4923) PRIORITY_DEMO: Equal Priority Task 3 running
I (4973) PRIORITY_DEMO: Equal Priority Task 1 running
I (4973) PRIORITY_DEMO: Equal Priority Task 2 running
I (5003) PRIORITY_DEMO: Equal Priority Task 3 running
I (5013) PRIORITY_DEMO: HIGH PRIORITY RUNNING (22)
I (5053) PRIORITY_DEMO: Equal Priority Task 1 running
I (5053) PRIORITY_DEMO: Equal Priority Task 2 running
I (5083) PRIORITY_DEMO: Equal Priority Task 3 running
I (5093) PRIORITY_DEMO: Medium priority running (15)
I (5133) PRIORITY_DEMO: Equal Priority Task 1 running
I (5133) PRIORITY_DEMO: Equal Priority Task 2 running
I (5163) PRIORITY_DEMO: Equal Priority Task 3 running
I (5203) PRIORITY_DEMO: Low priority running (7)
I (5213) PRIORITY_DEMO: Equal Priority Task 1 running
I (5213) PRIORITY_DEMO: Equal Priority Task 2 running
I (5223) PRIORITY_DEMO: HIGH PRIORITY RUNNING (23)
I (5243) PRIORITY_DEMO: Equal Priority Task 3 running
I (5293) PRIORITY_DEMO: Equal Priority Task 1 running
I (5303) PRIORITY_DEMO: Equal Priority Task 2 running
I (5323) PRIORITY_DEMO: Equal Priority Task 3 running
I (5373) PRIORITY_DEMO: Equal Priority Task 1 running
I (5383) PRIORITY_DEMO: Equal Priority Task 2 running
I (5403) PRIORITY_DEMO: Equal Priority Task 3 running
I (5413) PRIORITY_DEMO: Medium priority running (16)
I (5433) PRIORITY_DEMO: HIGH PRIORITY RUNNING (24)
I (5453) PRIORITY_DEMO: Equal Priority Task 1 running
I (5463) PRIORITY_DEMO: Equal Priority Task 2 running
I (5483) PRIORITY_DEMO: Equal Priority Task 3 running
I (5533) PRIORITY_DEMO: Equal Priority Task 1 running
I (5543) PRIORITY_DEMO: Equal Priority Task 2 running
I (5563) PRIORITY_DEMO: Equal Priority Task 3 running
I (5613) PRIORITY_DEMO: Equal Priority Task 1 running
I (5623) PRIORITY_DEMO: Equal Priority Task 2 running
I (5643) PRIORITY_DEMO: HIGH PRIORITY RUNNING (25)
I (5653) PRIORITY_DEMO: Equal Priority Task 3 running
I (5703) PRIORITY_DEMO: Equal Priority Task 1 running
I (5703) PRIORITY_DEMO: Equal Priority Task 2 running
I (5733) PRIORITY_DEMO: Medium priority running (17)
I (5733) PRIORITY_DEMO: Equal Priority Task 3 running
I (5783) PRIORITY_DEMO: Equal Priority Task 1 running
I (5783) PRIORITY_DEMO: Equal Priority Task 2 running
I (5813) PRIORITY_DEMO: Equal Priority Task 3 running
I (5853) PRIORITY_DEMO: HIGH PRIORITY RUNNING (26)
I (5863) PRIORITY_DEMO: Equal Priority Task 1 running
I (5863) PRIORITY_DEMO: Equal Priority Task 2 running
I (5893) PRIORITY_DEMO: Equal Priority Task 3 running
I (5943) PRIORITY_DEMO: Equal Priority Task 1 running
I (5943) PRIORITY_DEMO: Equal Priority Task 2 running
I (5973) PRIORITY_DEMO: Equal Priority Task 3 running
I (6023) PRIORITY_DEMO: Equal Priority Task 1 running
I (6023) PRIORITY_DEMO: Equal Priority Task 2 running
I (6053) PRIORITY_DEMO: Medium priority running (18)
I (6053) PRIORITY_DEMO: Equal Priority Task 3 running
I (6063) PRIORITY_DEMO: HIGH PRIORITY RUNNING (27)
I (6083) PRIORITY_DEMO: Low priority running (8)
I (6103) PRIORITY_DEMO: Equal Priority Task 1 running
I (6113) PRIORITY_DEMO: Equal Priority Task 2 running
I (6133) PRIORITY_DEMO: Equal Priority Task 3 running
I (6183) PRIORITY_DEMO: Equal Priority Task 1 running
I (6193) PRIORITY_DEMO: Equal Priority Task 2 running
I (6213) PRIORITY_DEMO: Equal Priority Task 3 running
I (6263) PRIORITY_DEMO: Equal Priority Task 1 running
I (6273) PRIORITY_DEMO: HIGH PRIORITY RUNNING (28)
I (6273) PRIORITY_DEMO: Equal Priority Task 2 running
I (6303) PRIORITY_DEMO: Equal Priority Task 3 running
I (6353) PRIORITY_DEMO: Equal Priority Task 2 running
I (6353) PRIORITY_DEMO: Equal Priority Task 1 running
I (6383) PRIORITY_DEMO: Medium priority running (19)
I (6383) PRIORITY_DEMO: Equal Priority Task 3 running
I (6433) PRIORITY_DEMO: Equal Priority Task 2 running
I (6433) PRIORITY_DEMO: Equal Priority Task 1 running
I (6463) PRIORITY_DEMO: Equal Priority Task 3 running

Done
PS C:\work-2025-1\FreeRTOS\LAB02\Task-Priority> 
```

### คำถามสำหรับวิเคราะห์
Priority ไหนทำงานมากที่สุด? เพราะอะไร?
- คำตอบ: Task ที่มี Priority สูงที่สุด จะทำงานมากที่สุด
- เหตุผล: Scheduler ของ RTOS เลือก task ที่มี priority สูงสุดที่ “ready” อยู่ให้ใช้ CPU ก่อนเสมอ จนกว่า task นั้นจะ block หรือต้อง delay ระบบจึงสลับไปให้ task อื่น
เกิด Priority Inversion หรือไม่? จะแก้ไขได้อย่างไร?
- คำตอบ: อาจเกิดขึ้นได้ เมื่อ task priority สูง ต้องรอ resource (เช่น mutex) ที่ถูก task priority ต่ำ ครอบครองอยู่ ในขณะที่ task กลาง คอยทำงานคั่นกลาง → ทำให้ task สูง ถูก “ขวาง”
- วิธีแก้:
    ใช้ Priority Inheritance Protocol – เมื่อ task ต่ำ ถือ mutex อยู่ จะ ยก priority ขึ้นเท่ากับ task ที่รออยู่ จนกว่าจะปล่อย mutex
    ใช้ Ceiling Protocol หรือ ออกแบบ ไม่ให้มี resource sharing ระหว่าง priority ต่างระดับ
Tasks ที่มี priority เดียวกันทำงานอย่างไร? 
- Scheduler จะสลับ task ที่มี priority เท่ากัน แบบ Round-Robin (แบ่ง time slice เท่า ๆ กัน)
การเปลี่ยน Priority แบบ dynamic ส่งผลอย่างไร?
- การปรับ priority ระหว่าง runtime สามารถเปลี่ยนลำดับการสลับ task ได้ ทันที
CPU utilization ของแต่ละ priority เป็นอย่างไร?
- Priority สูง: ใช้ CPU มากสุด เพราะถูกเรียกก่อนเสมอ
- Priority กลาง: ได้เวลาทำงานเมื่อ priority สูง block หรือ delay
- Priority ต่ำ: ทำงานน้อย หรือแทบไม่ได้ทำงาน ถ้า task สูง ไม่เคย block

# 02-2-1
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 15 2025 09:58:19
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a970h ( 43376) map       
I (103) esp_image: segment 1: paddr=0001a998 vaddr=3ffb0000 size=02418h (  9240) load     
I (107) esp_image: segment 2: paddr=0001cdb8 vaddr=40080000 size=03260h ( 12896) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=14c48h ( 85064) map      
I (143) esp_image: segment 4: paddr=00034c70 vaddr=40083260 size=0a0f4h ( 41204) load     
I (160) esp_image: segment 5: paddr=0003ed6c vaddr=50000000 size=00020h (    32) load     
I (166) boot: Loaded app from partition at offset 0x10000
I (166) boot: Disabling RNG early entropy source...
I (178) cpu_start: Multicore app
I (186) cpu_start: Pro cpu start user code
I (186) cpu_start: cpu freq: 160000000 Hz
I (186) app_init: Application information:
I (186) app_init: Project name:     Task-States
I (191) app_init: App version:      1
I (194) app_init: Compile time:     Oct 15 2025 09:52:59
I (199) app_init: ELF file SHA256:  6540587a7...
I (203) app_init: ESP-IDF:          v5.5.1
I (207) efuse_init: Min chip rev:     v0.0
I (211) efuse_init: Max chip rev:     v3.99
I (215) efuse_init: Chip rev:         v3.1
I (219) heap_init: Initializing. RAM available for dynamic allocation:
I (225) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (230) heap_init: At 3FFB2CF8 len 0002D308 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (241) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008D354 len 00012CAC (75 KiB): IRAM
W (253) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (265) spi_flash: detected chip: generic
I (268) spi_flash: flash io: dio
W (271) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (284) main_task: Started on CPU0
I (294) main_task: Calling app_main()
I (294) TASK_STATES: === FreeRTOS Task States Demo ===
E (294) gpio: gpio_pullup_en(78): GPIO number error (input-only pad has no internal PU)   
I (294) TASK_STATES: LED Indicators:
I (304) TASK_STATES: GPIO2 = Running, GPIO4 = Ready
I (304) TASK_STATES: GPIO5 = Blocked, GPIO18 = Suspended
I (314) TASK_STATES: Button Controls:
I (314) TASK_STATES: GPIO0 = Suspend/Resume, GPIO35 = Give Semaphore
I (324) TASK_STATES: State Demo Task started
I (324) TASK_STATES: === Cycle 1 ===
I (324) TASK_STATES: Task is RUNNING
I (434) TASK_STATES: Task will be READY (yielding to other tasks)
I (434) TASK_STATES: Ready state demo task running
I (444) TASK_STATES: Control Task started
I (444) TASK_STATES: Self-deleting task will live for 10 seconds
I (444) TASK_STATES: Self-deleting task countdown: 10
I (454) TASK_STATES: System Monitor started
I (454) TASK_STATES: External delete task running: 0
I (454) TASK_STATES: All tasks created. Monitoring task states...
I (464) TASK_STATES:
=== SYSTEM MONITOR ===
I (464) main_task: Returned from app_main()
I (474) TASK_STATES: Total tasks: 11
I (474) TASK_STATES: StateDemo: Prio=3, StackRemaining=2268 bytes
I (484) TASK_STATES: Control: Prio=4, StackRemaining=1232 bytes
W (494) TASK_STATES: === GIVING SEMAPHORE ===
I (534) TASK_STATES: Task will be BLOCKED (waiting for semaphore)
I (534) TASK_STATES: Got semaphore! Task is RUNNING again
I (594) TASK_STATES: Ready state demo task running
I (754) TASK_STATES: Ready state demo task running
I (914) TASK_STATES: Ready state demo task running
I (1034) TASK_STATES: Task is BLOCKED (in vTaskDelay)
I (1074) TASK_STATES: Ready state demo task running
I (1234) TASK_STATES: Ready state demo task running
I (1394) TASK_STATES: Ready state demo task running
I (1454) TASK_STATES: Self-deleting task countdown: 9
I (1464) TASK_STATES: External delete task running: 1
I (1554) TASK_STATES: Ready state demo task running
I (1714) TASK_STATES: Ready state demo task running
I (1874) TASK_STATES: Ready state demo task running
```

# 02-2-2
```c
I (199) app_init: ELF file SHA256:  73ad20971...
I (203) app_init: ESP-IDF:          v5.5.1
I (207) efuse_init: Min chip rev:     v0.0
I (211) efuse_init: Max chip rev:     v3.99
I (215) efuse_init: Chip rev:         v3.1
I (219) heap_init: Initializing. RAM available for dynamic allocation:
I (225) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (230) heap_init: At 3FFB2CF8 len 0002D308 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (241) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008D354 len 00012CAC (75 KiB): IRAM
W (253) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (265) spi_flash: detected chip: generic
I (268) spi_flash: flash io: dio
W (271) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (284) main_task: Started on CPU0
I (294) main_task: Calling app_main()
I (294) TASK_STATES: === FreeRTOS Task States Demo ===
E (294) gpio: gpio_pullup_en(78): GPIO number error (input-only pad has no internal PU)   
I (294) TASK_STATES: LED Indicators:
I (304) TASK_STATES: GPIO2 = Running, GPIO4 = Ready
I (304) TASK_STATES: GPIO5 = Blocked, GPIO18 = Suspended
I (314) TASK_STATES: Button Controls:
I (314) TASK_STATES: GPIO0 = Suspend/Resume, GPIO35 = Give Semaphore
I (324) TASK_STATES: State Demo Task started
I (324) TASK_STATES: === Cycle 1 ===
I (324) TASK_STATES: Task is RUNNING
I (434) TASK_STATES: Task will be READY (yielding to other tasks)
I (434) TASK_STATES: Ready state demo task running
I (444) TASK_STATES: Control Task started
I (444) TASK_STATES: Self-deleting task will live for 10 seconds
I (444) TASK_STATES: Self-deleting task countdown: 10
I (454) TASK_STATES: System Monitor started
I (454) TASK_STATES: External delete task running: 0
I (454) TASK_STATES: All tasks created. Monitoring task states...
I (464) TASK_STATES:
=== SYSTEM MONITOR ===
I (464) main_task: Returned from app_main()
I (474) TASK_STATES: Total tasks: 11
I (474) TASK_STATES: StateDemo: Prio=3, StackRemaining=2268 bytes
I (484) TASK_STATES: Control: Prio=4, StackRemaining=1232 bytes
W (494) TASK_STATES: === GIVING SEMAPHORE ===
I (534) TASK_STATES: Task will be BLOCKED (waiting for semaphore)
I (534) TASK_STATES: Got semaphore! Task is RUNNING again
I (594) TASK_STATES: Ready state demo task running
I (754) TASK_STATES: Ready state demo task running
I (914) TASK_STATES: Ready state demo task running
I (1034) TASK_STATES: Task is BLOCKED (in vTaskDelay)
I (1074) TASK_STATES: Ready state demo task running
I (1234) TASK_STATES: Ready state demo task running
I (1394) TASK_STATES: Ready state demo task running
I (1454) TASK_STATES: Self-deleting task countdown: 9
I (1464) TASK_STATES: External delete task running: 1
I (1554) TASK_STATES: Ready state demo task running
I (1714) TASK_STATES: Ready state demo task running
I (1874) TASK_STATES: Ready state demo task running
I (2034) TASK_STATES: === Cycle 2 ===
I (2034) TASK_STATES: Task is RUNNING
I (2034) TASK_STATES: Ready state demo task running
I (2134) TASK_STATES: Task will be READY (yielding to other tasks)
I (2194) TASK_STATES: Ready state demo task running
I (2234) TASK_STATES: Task will be BLOCKED (waiting for semaphore)
I (2354) TASK_STATES: Ready state demo task running
I (2454) TASK_STATES: Self-deleting task countdown: 8
I (2464) TASK_STATES: External delete task running: 2
I (2514) TASK_STATES: Ready state demo task running
I (2674) TASK_STATES: Ready state demo task running
I (2834) TASK_STATES: Ready state demo task running
I (2994) TASK_STATES: Ready state demo task running
I (3154) TASK_STATES: Ready state demo task running
I (3314) TASK_STATES: Ready state demo task running
```
# 02-2-3
```c
--- 0x40080400: _invalid_pc_placeholder at C:/Users/09677/esp/v5.5.1/esp-idf/components/xtensa/xtensa_vectors.S:2235
entry 0x40080638
--- 0x40080638: call_start_cpu0 at C:/Users/09677/esp/v5.5.1/esp-idf/components/bootloader/subproject/main/bootloader_start.c:25
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 15 2025 09:58:19
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a970h ( 43376) map       
I (103) esp_image: segment 1: paddr=0001a998 vaddr=3ffb0000 size=02418h (  9240) load
I (107) esp_image: segment 2: paddr=0001cdb8 vaddr=40080000 size=03260h ( 12896) load     
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=14c48h ( 85064) map      
I (143) esp_image: segment 4: paddr=00034c70 vaddr=40083260 size=0a0f4h ( 41204) load
I (160) esp_image: segment 5: paddr=0003ed6c vaddr=50000000 size=00020h (    32) load     
I (166) boot: Loaded app from partition at offset 0x10000
I (166) boot: Disabling RNG early entropy source...
I (178) cpu_start: Multicore app
I (186) cpu_start: Pro cpu start user code
I (186) cpu_start: cpu freq: 160000000 Hz
I (186) app_init: Application information:
I (186) app_init: Project name:     Task-States
I (191) app_init: App version:      1
I (194) app_init: Compile time:     Oct 15 2025 09:52:59
I (199) app_init: ELF file SHA256:  93b306556...
I (203) app_init: ESP-IDF:          v5.5.1
I (207) efuse_init: Min chip rev:     v0.0
I (211) efuse_init: Max chip rev:     v3.99
I (215) efuse_init: Chip rev:         v3.1
I (219) heap_init: Initializing. RAM available for dynamic allocation:
I (225) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (230) heap_init: At 3FFB2CF8 len 0002D308 (180 KiB): DRAM
I (235) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (241) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (246) heap_init: At 4008D354 len 00012CAC (75 KiB): IRAM
W (253) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (265) spi_flash: detected chip: generic
I (268) spi_flash: flash io: dio
W (271) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (284) main_task: Started on CPU0
I (294) main_task: Calling app_main()
I (294) TASK_STATES: === FreeRTOS Task States Demo ===
E (294) gpio: gpio_pullup_en(78): GPIO number error (input-only pad has no internal PU)   
I (294) TASK_STATES: LED Indicators:
I (304) TASK_STATES: GPIO2 = Running, GPIO4 = Ready
I (304) TASK_STATES: GPIO5 = Blocked, GPIO18 = Suspended
I (314) TASK_STATES: Button Controls:
I (314) TASK_STATES: GPIO0 = Suspend/Resume, GPIO35 = Give Semaphore
I (324) TASK_STATES: State Demo Task started
I (324) TASK_STATES: === Cycle 1 ===
I (324) TASK_STATES: Task is RUNNING
I (434) TASK_STATES: Task will be READY (yielding to other tasks)
I (434) TASK_STATES: Ready state demo task running
I (444) TASK_STATES: Control Task started
I (444) TASK_STATES: Self-deleting task will live for 10 seconds
I (444) TASK_STATES: Self-deleting task countdown: 10
I (454) TASK_STATES: System Monitor started
I (454) TASK_STATES: External delete task running: 0
I (454) TASK_STATES: All tasks created. Monitoring task states...
I (464) TASK_STATES:
=== SYSTEM MONITOR ===
I (464) main_task: Returned from app_main()
I (474) TASK_STATES: Total tasks: 11
I (474) TASK_STATES: StateDemo: Prio=3, StackRemaining=2268 bytes
I (484) TASK_STATES: Control: Prio=4, StackRemaining=1232 bytes
I (534) TASK_STATES: Task will be BLOCKED (waiting for semaphore)
W (594) TASK_STATES: === GIVING SEMAPHORE ===
I (594) TASK_STATES: Got semaphore! Task is RUNNING again
I (594) TASK_STATES: Ready state demo task running
I (754) TASK_STATES: Ready state demo task running
I (914) TASK_STATES: Ready state demo task running
I (1074) TASK_STATES: Ready state demo task running
I (1094) TASK_STATES: Task is BLOCKED (in vTaskDelay)
I (1234) TASK_STATES: Ready state demo task running
I (1394) TASK_STATES: Ready state demo task running
I (1454) TASK_STATES: Self-deleting task countdown: 9
I (1464) TASK_STATES: External delete task running: 1
I (1554) TASK_STATES: Ready state demo task running
I (1714) TASK_STATES: Ready state demo task running
I (1874) TASK_STATES: Ready state demo task running
I (2034) TASK_STATES: Ready state demo task running
I (2094) TASK_STATES: === Cycle 2 ===
I (2094) TASK_STATES: Task is RUNNING
I (2194) TASK_STATES: Ready state demo task running
I (2194) TASK_STATES: Task will be READY (yielding to other tasks)
I (2294) TASK_STATES: Task will be BLOCKED (waiting for semaphore)
I (2354) TASK_STATES: Ready state demo task running
I (2454) TASK_STATES: Self-deleting task countdown: 8
I (2464) TASK_STATES: External delete task running: 2
I (2514) TASK_STATES: Ready state demo task running
I (2674) TASK_STATES: Ready state demo task running
I (2834) TASK_STATES: Ready state demo task running
I (2994) TASK_STATES: Ready state demo task running

```

## 🧠 การวิเคราะห์สถานะของ Task ใน FreeRTOS

### 1. Task อยู่ใน **Running state** เมื่อไหร่บ้าง?
- เมื่อ **Scheduler** เลือกให้ Task นั้นเป็นผู้ได้ใช้ **CPU** ในขณะนั้น  
- มีเพียง **หนึ่ง task ต่อหนึ่ง core** เท่านั้นที่สามารถอยู่ในสถานะ Running ได้  
- ตัวอย่าง: Task ที่มี **priority สูงสุด** และ **พร้อมทำงาน (Ready)** จะถูกเลือกมาทำงานก่อน

---

### 2. ความแตกต่างระหว่าง **Ready** และ **Blocked state**
| สถานะ | คำอธิบาย | ตัวอย่าง |
|--------|-----------|-----------|
| **Ready** | Task พร้อมทำงานทันที รอเพียง CPU ว่าง | หลังจาก `vTaskDelay()` ครบเวลา, Task ที่ถูกปลุกจาก interrupt |
| **Blocked** | Task รอเหตุการณ์บางอย่าง เช่น การรับข้อมูล หรือครบเวลา delay | รอ queue, semaphore, หรือ delay timer หมดเวลา |

---

### 3. การใช้ `vTaskDelay()` ทำให้ task อยู่ใน state ใด?
- Task จะเข้าสู่ **Blocked state**  
- เพราะระบบจะ “หน่วงเวลา” task ไว้ชั่วคราว จนกว่าจะครบเวลาที่กำหนด จากนั้นจึงกลับไป **Ready state**

---

### 4. การ **Suspend task** ต่างจาก **Block** อย่างไร?
| การ Block | การ Suspend |
|------------|-------------|
| Task หยุดทำงานชั่วคราว **เพราะเหตุการณ์ภายใน** เช่น delay, รอ queue | Task ถูกหยุดโดย **คำสั่งของโปรแกรมเมอร์** (`vTaskSuspend()`) |
| ระบบจะ **ปลุกอัตโนมัติ** เมื่อเงื่อนไขครบ | ต้องใช้คำสั่ง **`vTaskResume()`** เพื่อปลุกกลับมาเอง |
| ตัวอย่าง: `vTaskDelay(1000)` | ตัวอย่าง: `vTaskSuspend(TaskHandle)` |

---

### 5. Task ที่ถูก **Delete** จะกลับมาได้หรือไม่?
- ❌ **ไม่ได้**  
- เมื่อใช้ `vTaskDelete()` ระบบจะ **ลบ Task ออกจาก Scheduler** และ **คืนหน่วยความจำ (Stack + TCB)** ให้ระบบ  
- หากต้องการให้กลับมา ต้อง **สร้าง Task ใหม่ด้วย `xTaskCreate()`**

---

# 02-3-1
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 28 2025 16:42:23
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
I (80) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0abb0h ( 43952) map
I (103) esp_image: segment 1: paddr=0001abd8 vaddr=3ffb0000 size=023f8h (  9208) load
I (107) esp_image: segment 2: paddr=0001cfd8 vaddr=40080000 size=03040h ( 12352) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=17db4h ( 97716) map
I (148) esp_image: segment 4: paddr=00037ddc vaddr=40083040 size=09f60h ( 40800) load
I (164) esp_image: segment 5: paddr=00041d44 vaddr=50000000 size=00020h (    32) load
I (171) boot: Loaded app from partition at offset 0x10000
I (171) boot: Disabling RNG early entropy source...
I (182) cpu_start: Multicore app
I (190) cpu_start: Pro cpu start user code
I (190) cpu_start: cpu freq: 160000000 Hz
I (190) app_init: Application information:
I (191) app_init: Project name:     stack_monitoring
I (195) app_init: App version:      c71b0c7
I (199) app_init: Compile time:     Oct 28 2025 16:41:06
I (204) app_init: ELF file SHA256:  2eae06265...
I (208) app_init: ESP-IDF:          v5.5.1
I (212) efuse_init: Min chip rev:     v0.0
I (216) efuse_init: Max chip rev:     v3.99
I (220) efuse_init: Chip rev:         v3.1
I (224) heap_init: Initializing. RAM available for dynamic allocation:
I (230) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (235) heap_init: At 3FFB2CD0 len 0002D330 (180 KiB): DRAM
I (241) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (246) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (251) heap_init: At 4008CFA0 len 00013060 (76 KiB): IRAM
```
# 02-3-2
```c
I (289) main_task: Started on CPU0
I (299) main_task: Calling app_main()
I (299) STACK_MONITOR: === FreeRTOS Stack Monitoring Demo ===
I (299) STACK_MONITOR: LED Indicators:
I (299) STACK_MONITOR: GPIO2 = Stack OK, GPIO4 = Stack Warning/Critical
I (309) STACK_MONITOR: Creating tasks with different stack sizes...
I (309) STACK_MONITOR: Light Stack Task sGuru Meditation Error: Core  0 panic'ed (LoadProhibited). Exception was unhandled.

Core  0 register dump:
PC      : 0x400d485e  PS      : 0x00060a30  A0      : 0x800d57dd  A1      : 0x3ffb4a90  
--- 0x400d485e: uart_write at C:/Users/09677/esp/v5.5.1/esp-idf/components/esp_driver_uart/src/uart_vfs.c:238
A2      : 0x00000040  A3      : 0x400d4160  A4      : 0x00000000  A5      : 0x00000000  
--- 0x400d4160: uart_tx_char at C:/Users/09677/esp/v5.5.1/esp-idf/components/esp_driver_uart/src/uart_vfs.c:186
A6      : 0x00000073  A7      : 0x00000029  A8      : 0x0006004c  A9      : 0x3ffb4a60
A10     : 0x3f408480  A11     : 0x00000073  A12     : 0x00060820  A13     : 0x00000040
A14     : 0x00000000  A15     : 0x3ffaec30  SAR     : 0x00000004  EXCCAUSE: 0x0000001c  
EXCVADDR: 0x0006004c  LBEG    : 0x400014fd  LEND    : 0x4000150d  LCOUNT  : 0xfffffffc
--- 0x400014fd: strlen in ROM
--- 0x4000150d: strlen in ROM
```
# 02-3-3
```c
--- 0x40080400: _invalid_pc_placeholder at C:/Users/09677/esp/v5.5.1/esp-idf/components/xtensa/xtensa_vectors.S:2235
entry 0x40080638
--- 0x40080638: call_start_cpu0 at C:/Users/09677/esp/v5.5.1/esp-idf/components/bootloader/subproject/main/bootloader_start.c:25
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 28 2025 16:42:23
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
I (80) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0abc0h ( 43968) map
I (103) esp_image: segment 1: paddr=0001abe8 vaddr=3ffb0000 size=023f8h (  9208) load
I (107) esp_image: segment 2: paddr=0001cfe8 vaddr=40080000 size=03030h ( 12336) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=17db4h ( 97716) map
I (148) esp_image: segment 4: paddr=00037ddc vaddr=40083030 size=09f70h ( 40816) load
I (164) esp_image: segment 5: paddr=00041d54 vaddr=50000000 size=00020h (    32) load
I (171) boot: Loaded app from partition at offset 0x10000
I (171) boot: Disabling RNG early entropy source...
I (182) cpu_start: Multicore app
```
## คำถามสำหรับวิเคราะห์

1. Task ไหนใช้ stack มากที่สุด? เพราะอะไร?
- งานที่มี “กรอบเรียกฟังก์ชันลึก + ตัวแปรโลคัลขนาดใหญ่ + ใช้ printf()/          ไลบรารีรูปแบบจัดข้อความ” มักใช้มากสุด
ลักษณะงานที่เสี่ยงสูง: งานประมวลผลสตริง/ฟอร์แมต, งานเข้ารหัส/ถอดรหัส, งานที่ถือ buffer ชั่วคราวใหญ่ ๆ (เช่น uint8_t buf[2*1024];) และงานที่เรียกผ่านเลเยอร์ไลบรารีหลายชั้น
2. การใช้ heap แทน stack มีข้อดีอย่างไร?
- ลดขนาด stack ต่อ task: ย้าย buffer ใหญ่ ๆ จาก stack ไป heap (ผ่าน pvPortMalloc()/free) ทำให้ตั้งค่า usStackDepth เล็กลงได้
3. Stack overflow เกิดขึ้นเมื่อไหร่และทำอย่างไรป้องกัน?
- เกิดเมื่อกรอบเรียกซ้อนรวม + ตัวแปรโลคัล + บันทึกคอนเท็กซ์ เกินขนาด stack ที่จองให้ task
4. การตั้งค่า stack size ควรพิจารณาจากอะไร?
- รูปแบบการเรียกฟังก์ชัน (ความลึกของ call chain) และจำนวน/ขนาดตัวแปรโลคัล
5. Recursion ส่งผลต่อ stack usage อย่างไร?
- ทุกระดับการเรียกเพิ่มกรอบสแตกใหม่ ⇒ การใช้สแตกเติบโตเป็นเชิงเส้นกับความลึกของ recursion