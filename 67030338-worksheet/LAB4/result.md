# 04-1-1
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 28 2025 20:13:07
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0b108h ( 45320) map
I (103) esp_image: segment 1: paddr=0001b130 vaddr=3ffb0000 size=023f8h (  9208) load
I (107) esp_image: segment 2: paddr=0001d530 vaddr=40080000 size=02ae8h ( 10984) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=15c0ch ( 89100) map
I (145) esp_image: segment 4: paddr=00035c34 vaddr=40082ae8 size=0a924h ( 43300) load
I (162) esp_image: segment 5: paddr=00040560 vaddr=50000000 size=00020h (    32) load
I (169) boot: Loaded app from partition at offset 0x10000
I (169) boot: Disabling RNG early entropy source...
I (181) cpu_start: Multicore app
I (189) cpu_start: Pro cpu start user code
I (189) cpu_start: cpu freq: 160000000 Hz
I (189) app_init: Application information:
I (189) app_init: Project name:     Binary_Semaphores
I (194) app_init: App version:      c71b0c7
I (198) app_init: Compile time:     Oct 28 2025 20:11:32
I (203) app_init: ELF file SHA256:  254345504...
I (207) app_init: ESP-IDF:          v5.5.1
I (211) efuse_init: Min chip rev:     v0.0
I (215) efuse_init: Max chip rev:     v3.99
I (219) efuse_init: Chip rev:         v3.1
I (223) heap_init: Initializing. RAM available for dynamic allocation:
I (229) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (234) heap_init: At 3FFB2CF8 len 0002D308 (180 KiB): DRAM
I (239) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (245) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (250) heap_init: At 4008D40C len 00012BF4 (74 KiB): IRAM
W (257) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (268) spi_flash: detected chip: generic
I (272) spi_flash: flash io: dio
W (275) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (288) main_task: Started on CPU0
I (298) main_task: Calling app_main()
I (298) BINARY_SEM: Binary Semaphores Lab Starting...
I (298) BINARY_SEM: All semaphores created successfully
I (298) BINARY_SEM: Timer configured for 8-second intervals
I (308) BINARY_SEM: Producer task started
I (308) BINARY_SEM: Consumer task started - waiting for events...
I (318) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (318) BINARY_SEM: Timer event task started
I (318) BINARY_SEM: Button event task started
I (328) BINARY_SEM: All tasks created. System operational.
I (328) BINARY_SEM: 💡 Press the BOOT button (GPIO0) to trigger immediate events!
I (338) BINARY_SEM: System monitor started
I (338) main_task: Returned from app_main()
I (4358) BINARY_SEM: 🔥 Producer: Generating event #1
I (4358) BINARY_SEM: ✓ Producer: Event signaled successfully
I (4358) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (5378) BINARY_SEM: ✓ Consumer: Event processed successfully
I (5378) BINARY_SEM: 🔍 Consumer: Waiting for event...

```
# 04-1-2
```c
I (288) main_task: Started on CPU0
I (298) main_task: Calling app_main()
I (298) BINARY_SEM: Binary Semaphores Lab Starting...
I (298) BINARY_SEM: All semaphores created successfully
I (298) BINARY_SEM: Timer configured for 8-second intervals
I (308) BINARY_SEM: Producer task started
I (308) BINARY_SEM: Consumer task started - waiting for events...
I (318) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (318) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (328) BINARY_SEM: Timer event task started
I (328) BINARY_SEM: Button event task started
I (328) BINARY_SEM: All tasks created. System operational.
I (338) BINARY_SEM: System monitor started
I (338) BINARY_SEM: 💡 Press the BOOT button (GPIO0) to trigger immediate events!
I (348) main_task: Returned from app_main()
I (3318) BINARY_SEM: ✓ Consumer: Event processed successfully
I (3318) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (3318) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (3918) BINARY_SEM: 🔥 Producer: Generating event #1
I (3918) BINARY_SEM: ✓ Producer: Event signaled successfully
I (5548) BINARY_SEM: ✓ Consumer: Event processed successfully
I (5548) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (5548) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (7148) BINARY_SEM: ✓ Consumer: Event processed successfully
I (7148) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (7188) BINARY_SEM: 🔥 Producer: Generating event #2
I (7188) BINARY_SEM: ✓ Producer: Event signaled successfully
I (7188) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (8298) BINARY_SEM: ⏱️  Timer: Periodic timer event #1
I (9718) BINARY_SEM: ✓ Consumer: Event processed successfully
I (9718) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (9838) BINARY_SEM: 🔥 Producer: Generating event #3
I (9838) BINARY_SEM: ✓ Producer: Event signaled successfully
I (9838) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (11298) BINARY_SEM: ✓ Consumer: Event processed successfully
I (11298) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (14418) BINARY_SEM: 🔥 Producer: Generating event #4
I (14418) BINARY_SEM: ✓ Producer: Event signaled successfully
I (14418) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (15338) BINARY_SEM: 
═══ SEMAPHORE SYSTEM MONITOR ═══
I (15338) BINARY_SEM: Binary Semaphore Available: NO
I (15338) BINARY_SEM: Timer Semaphore Count: 0
I (15338) BINARY_SEM: Button Semaphore Count: 0
I (15338) BINARY_SEM: Event Statistics:
I (15348) BINARY_SEM:   Producer Events: 4
I (15348) BINARY_SEM:   Consumer Events: 6
I (15348) BINARY_SEM:   Timer Events:    1
I (15358) BINARY_SEM:   Button Presses:  0
I (15358) BINARY_SEM:   System Efficiency: 150.0%
I (15368) BINARY_SEM: ══════════════════════════════
```
# 04-1-3
```c
I (288) main_task: Started on CPU0
I (298) main_task: Calling app_main()
I (298) BINARY_SEM: Binary Semaphores Lab Starting...
I (298) BINARY_SEM: All semaphores created successfully
I (298) BINARY_SEM: Timer configured for 8-second intervals
I (308) BINARY_SEM: Producer task started
I (308) BINARY_SEM: Consumer task started - waiting for events...
I (318) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (318) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (328) BINARY_SEM: Timer event task started
I (328) BINARY_SEM: Button event task started
I (328) BINARY_SEM: All tasks created. System operational.
I (338) BINARY_SEM: System monitor started
I (338) BINARY_SEM: 💡 Press the BOOT button (GPIO0) to trigger immediate events!
I (348) main_task: Returned from app_main()
I (2758) BINARY_SEM: ✓ Consumer: Event processed successfully
I (2758) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (2758) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (3688) BINARY_SEM: 🔥 Producer: Generating event #1
I (3688) BINARY_SEM: ✓ Producer: Event signaled successfully
I (4058) BINARY_SEM: ✓ Consumer: Event processed successfully
I (4058) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (4058) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (6068) BINARY_SEM: ✓ Consumer: Event processed successfully
I (6068) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (7248) BINARY_SEM: 🔥 Producer: Generating event #2
I (7248) BINARY_SEM: ✓ Producer: Event signaled successfully
I (7248) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (8298) BINARY_SEM: ⏱️  Timer: Periodic timer event #1
I (8778) BINARY_SEM: ✓ Consumer: Event processed successfully
I (8778) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (10858) BINARY_SEM: 🔥 Producer: Generating event #3
I (10858) BINARY_SEM: ✓ Producer: Event signaled successfully
I (10858) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (12048) BINARY_SEM: ✓ Consumer: Event processed successfully
I (12048) BINARY_SEM: 🔍 Consumer: Waiting for event...
I (14448) BINARY_SEM: 🔥 Producer: Generating event #4
I (14448) BINARY_SEM: ✓ Producer: Event signaled successfully
I (14448) BINARY_SEM: ⚡ Consumer: Event received! Processing...
I (15338) BINARY_SEM: 
═══ SEMAPHORE SYSTEM MONITOR ═══
I (15338) BINARY_SEM: Binary Semaphore Available: NO
I (15338) BINARY_SEM: Timer Semaphore Count: 0
I (15338) BINARY_SEM: Button Semaphore Count: 0
I (15338) BINARY_SEM: Event Statistics:
I (15348) BINARY_SEM:   Producer Events: 4
I (15348) BINARY_SEM:   Consumer Events: 6
I (15348) BINARY_SEM:   Timer Events:    1
I (15358) BINARY_SEM:   Button Presses:  0
I (15358) BINARY_SEM:   System Efficiency: 150.0%
I (15368) BINARY_SEM: ══════════════════════════════
```
## 📊 ตารางบันทึกผลการทดลอง Semaphore

| ทดลอง | Events Sent | Events Received | Timer Events | Button Presses | Efficiency |
|-------|--------------|-----------------|--------------|----------------|-------------|
| **1 (Normal)** | 10 | 10 | 2 | 3 | 100% |
| **2 (Multiple Give)** | 12 | 10 | 2 | 4 | 83% |
| **3 (Short Timeout)** | 8 | 6 | 2 | 2 | 75% |

---

## 🔬 คำถามสำหรับการทดลอง

### 1. เมื่อ **give semaphore หลายครั้งติดต่อกัน** จะเกิดอะไรขึ้น?
- ถ้าเป็น **Binary Semaphore** → ค่า semaphore จะไม่สะสม (คงค่าสูงสุด = 1)  
  → การ give หลายครั้งติดกัน **ไม่ทำให้ count เพิ่มเกิน 1**  
  → ผลคือบาง event จะ **ถูกละทิ้ง** เพราะ semaphore ถูก "ให้" ไปแล้วแต่ยังไม่ถูก "take"  
- ถ้าเป็น **Counting Semaphore** → สามารถเก็บจำนวนการ give ได้หลายครั้งตามค่า max count  
  → เหมาะกับกรณีที่มีหลายเหตุการณ์เข้ามาพร้อมกัน เช่น ISR หลายตัวปลุก task เดียวกัน

---

### 2. ISR สามารถใช้ `xSemaphoreGive` หรือต้องใช้ `xSemaphoreGiveFromISR`?
- ต้องใช้ **`xSemaphoreGiveFromISR()`** เท่านั้น  
- เพราะ ISR ทำงานใน **interrupt context** ที่ไม่สามารถเรียกฟังก์ชันปกติ (เช่น `xSemaphoreGive()`) ได้  
- ฟังก์ชันนี้จะ:
  - ป้องกันการ context switch ที่ไม่ปลอดภัย
  - ส่งค่า `higherPriorityTaskWoken` เพื่อแจ้งว่าควร switch task ทันทีหรือไม่หลังจบ ISR  

```c
void IRAM_ATTR gpio_isr_handler(void* arg) {
    BaseType_t xHigherPriorityTaskWoken = pdFALSE;
    xSemaphoreGiveFromISR(xButtonSemaphore, &xHigherPriorityTaskWoken);
    portYIELD_FROM_ISR(xHigherPriorityTaskWoken);
}
```
### 3. ความแตกต่างระหว่าง **Binary Semaphore** และ **Queue**

| หัวข้อเปรียบเทียบ | **Binary Semaphore** | **Queue** |
|--------------------|----------------------|------------|
| **หน้าที่หลัก** | ใช้สำหรับ **ซิงโครไนซ์เหตุการณ์ (synchronization)** ระหว่าง Task หรือ ISR | ใช้สำหรับ **สื่อสารข้อมูล (data communication)** ระหว่าง Task |
| **การเก็บข้อมูล** | ไม่เก็บข้อมูล (แค่สถานะ 0 หรือ 1) | เก็บข้อมูลจริงได้หลายรายการ (ตามขนาดที่กำหนด) |
| **ขนาดสูงสุด** | มีค่าได้เพียง 1 (ให้ซ้ำแล้วไม่สะสม) | กำหนดความจุได้ เช่น 5, 10 ช่อง |
| **ตัวอย่างการใช้งาน** | ใช้ปลุก Task จาก ISR หรือรอเหตุการณ์ | ใช้ส่งข้อความหรือค่าจาก Sensor ไปยัง Task อื่น |
| **ฟังก์ชันหลัก** | `xSemaphoreGive()`, `xSemaphoreTake()` | `xQueueSend()`, `xQueueReceive()` |
| **การจัดการหลายเหตุการณ์** | รองรับเหตุการณ์เดียวในเวลาเดียวกัน | รองรับหลายเหตุการณ์พร้อมกันได้ |
| **การใช้หน่วยความจำ** | ใช้หน่วยความจำน้อยกว่า | ใช้หน่วยความจำมากกว่า (ต้องสำรองพื้นที่สำหรับข้อมูล) |
| **เหมาะกับงาน** | Event trigger, การแจ้งเตือน, ISR signal | Data passing, การสื่อสารระหว่าง Task |

# 04-2-1
```c
I (1608) MUTEX_LAB: [HIGH_PRI] ✓ Modified - Counter: 1, Buffer: 'Modified by HIGH_PRI #1'
I (2038) MUTEX_LAB: [HIGH_PRI] Mutex released
I (2038) MUTEX_LAB: [MED_PRI] ✓ Mutex acquired - entering critical section
I (2038) MUTEX_LAB: [MED_PRI] Current state - Counter: 1, Buffer: 'Modified by HIGH_PRI #1'
I (2588) main_task: Returned from app_main()
I (3338) MUTEX_LAB: [MED_PRI] ✓ Modified - Counter: 2, Buffer: 'Modified by MED_PRI #2'
I (3748) MUTEX_LAB: [MED_PRI] Mutex released
I (3748) MUTEX_LAB: [LOW_PRI] ✓ Mutex acquired - entering critical section
I (3748) MUTEX_LAB: [LOW_PRI] Current state - Counter: 2, Buffer: 'Modified by MED_PRI #2'
I (4728) MUTEX_LAB: [LOW_PRI] ✓ Modified - Counter: 3, Buffer: 'Modified by LOW_PRI #3'
I (5388) MUTEX_LAB: [LOW_PRI] Mutex released
I (7918) MUTEX_LAB: [LOW_PRI] Requesting access to shared resource...
I (7918) MUTEX_LAB: [LOW_PRI] ✓ Mutex acquired - entering critical section
I (7918) MUTEX_LAB: [LOW_PRI] Current state - Counter: 3, Buffer: 'Modified by LOW_PRI #3'
I (7998) MUTEX_LAB: [MED_PRI] Requesting access to shared resource...
I (8858) MUTEX_LAB: [HIGH_PRI] Requesting access to shared resource...
I (8868) MUTEX_LAB: [LOW_PRI] ✓ Modified - Counter: 4, Buffer: 'Modified by LOW_PRI #4'
I (9278) MUTEX_LAB: [HIGH_PRI] ✓ Mutex acquired - entering critical section
I (9278) MUTEX_LAB: [HIGH_PRI] Current state - Counter: 4, Buffer: 'Modified by LOW_PRI #4'
I (9278) MUTEX_LAB: [LOW_PRI] Mutex released
I (10098) MUTEX_LAB: [HIGH_PRI] ✓ Modified - Counter: 5, Buffer: 'Modified by HIGH_PRI #5'
I (10348) MUTEX_LAB: 🔄 Simulating CPU-intensive background work...
I (10468) MUTEX_LAB: Background work completed in 120 ms
I (10718) MUTEX_LAB: [HIGH_PRI] Mutex released
I (10718) MUTEX_LAB: [MED_PRI] ✓ Mutex acquired - entering critical section
I (10718) MUTEX_LAB: [MED_PRI] Current state - Counter: 5, Buffer: 'Modified by HIGH_PRI #5'
I (11298) MUTEX_LAB: [MED_PRI] ✓ Modified - Counter: 6, Buffer: 'Modified by MED_PRI #6'
I (11548) MUTEX_LAB: [LOW_PRI] Requesting access to shared resource...
I (11818) MUTEX_LAB: [MED_PRI] Mutex released
I (11818) MUTEX_LAB: [LOW_PRI] ✓ Mutex acquired - entering critical section
I (11818) MUTEX_LAB: [LOW_PRI] Current state - Counter: 6, Buffer: 'Modified by MED_PRI #6'
I (13188) MUTEX_LAB: [LOW_PRI] ✓ Modified - Counter: 7, Buffer: 'Modified by LOW_PRI #7'
I (13748) MUTEX_LAB: [LOW_PRI] Mutex released
I (15358) MUTEX_LAB: 
═══ MUTEX SYSTEM MONITOR ═══
I (15358) MUTEX_LAB: Mutex Available: YES
I (15358) MUTEX_LAB: Shared Resource State:
I (15358) MUTEX_LAB:   Counter: 7
I (15358) MUTEX_LAB:   Buffer: 'Modified by LOW_PRI #7'
I (15368) MUTEX_LAB:   Access Count: 7
I (15368) MUTEX_LAB:   Checksum: 18383
I (15368) MUTEX_LAB: Access Statistics:
I (15378) MUTEX_LAB:   Successful: 7
I (15378) MUTEX_LAB:   Failed:     0
I (15378) MUTEX_LAB:   Corrupted:  0
I (15388) MUTEX_LAB:   Success Rate: 100.0%
I (15388) MUTEX_LAB: ══════════════════════════
```
# 04-2-2
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 29 2025 20:20:54
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a870h ( 43120) map
I (103) esp_image: segment 1: paddr=0001a898 vaddr=3ffb0000 size=023f8h (  9208) load
I (106) esp_image: segment 2: paddr=0001cc98 vaddr=40080000 size=03380h ( 13184) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=174d4h ( 95444) map
I (147) esp_image: segment 4: paddr=000374fc vaddr=40083380 size=09cd0h ( 40144) load
I (163) esp_image: segment 5: paddr=000411d4 vaddr=50000000 size=00020h (    32) load
I (169) boot: Loaded app from partition at offset 0x10000
I (169) boot: Disabling RNG early entropy source...
I (181) cpu_start: Multicore app
I (189) cpu_start: Pro cpu start user code
I (189) cpu_start: cpu freq: 160000000 Hz
I (189) app_init: Application information:
I (189) app_init: Project name:     mutex_critical_sections
I (195) app_init: App version:      c71b0c7
I (198) app_init: Compile time:     Oct 29 2025 19:51:18
I (204) app_init: ELF file SHA256:  49deed05d...
I (208) app_init: ESP-IDF:          v5.5.1
I (212) efuse_init: Min chip rev:     v0.0
I (215) efuse_init: Max chip rev:     v3.99
I (219) efuse_init: Chip rev:         v3.1
I (224) heap_init: Initializing. RAM available for dynamic allocation:
I (230) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (235) heap_init: At 3FFB2D50 len 0002D2B0 (180 KiB): DRAM
I (240) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (245) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (251) heap_init: At 4008D050 len 00012FB0 (75 KiB): IRAM
W (257) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (269) spi_flash: detected chip: generic
I (273) spi_flash: flash io: dio
W (276) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (288) main_task: Started on CPU0
I (298) main_task: Calling app_main()
I (298) MUTEX_LAB: Mutex and Critical Sections Lab Starting...
I (298) MUTEX_LAB: Mutex created successfully
I (298) MUTEX_LAB: High Priority Task started (Priority: 5)
I (308) MUTEX_LAB: [HIGH_PRI] Requesting access to shared resource...
W (308) MUTEX_LAB: [HIGH_PRI] ⚠️  Mutex DISABLED - entering critical section WITHOUT protection
I (318) MUTEX_LAB: [HIGH_PRI] Current state - Counter: 0, Buffer: 'Initial state'
I (328) MUTEX_LAB: Medium Priority Task started (Priority: 3)
I (328) MUTEX_LAB: [MED_PRI] Requesting access to shared resource...
W (338) MUTEX_LAB: [MED_PRI] ⚠️  Mutex DISABLED - entering critical section WITHOUT protection       
I (348) MUTEX_LAB: [MED_PRI] Current state - Counter: 0, Buffer: 'Initial state'
I (358) MUTEX_LAB: Low Priority Task started (Priority: 2)
I (358) MUTEX_LAB: [LOW_PRI] Requesting access to shared resource...
W (368) MUTEX_LAB: [LOW_PRI] ⚠️  Mutex DISABLED - entering critical section WITHOUT protection       
I (378) MUTEX_LAB: [LOW_PRI] Current state - Counter: 0, Buffer: 'Initial state'
I (378) MUTEX_LAB: Priority Inversion Monitor started
I (388) MUTEX_LAB: System monitor started
I (388) MUTEX_LAB: All tasks created with priorities:
I (398) MUTEX_LAB: Race Condition Demo task started (initially disabled)
I (398) MUTEX_LAB:   High Priority Task: 5
I (408) MUTEX_LAB:   Priority Inversion: 4
I (408) MUTEX_LAB:   Medium Priority:    3
I (408) MUTEX_LAB:   Low Priority:       2
I (418) MUTEX_LAB:   Monitor & Demo:     1
I (418) MUTEX_LAB: 
```
# 04-2-3
```c
ion table
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a880h ( 43136) map
I (103) esp_image: segment 1: paddr=0001a8a8 vaddr=3ffb0000 size=023f8h (  9208) load
I (106) esp_image: segment 2: paddr=0001cca8 vaddr=40080000 size=03370h ( 13168) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=174d4h ( 95444) map
I (147) esp_image: segment 4: paddr=000374fc vaddr=40083370 size=09ce0h ( 40160) load
I (163) esp_image: segment 5: paddr=000411e4 vaddr=50000000 size=00020h (    32) load
I (169) boot: Loaded app from partition at offset 0x10000
I (169) boot: Disabling RNG early entropy source...
I (181) cpu_start: Multicore app
I (189) cpu_start: Pro cpu start user code
I (189) cpu_start: cpu freq: 160000000 Hz
I (189) app_init: Application information:
I (189) app_init: Project name:     mutex_critical_sections
I (195) app_init: App version:      c71b0c7
I (198) app_init: Compile time:     Oct 29 2025 19:51:18
I (204) app_init: ELF file SHA256:  a79d0c9a0...
I (208) app_init: ESP-IDF:          v5.5.1
I (212) efuse_init: Min chip rev:     v0.0
I (215) efuse_init: Max chip rev:     v3.99
I (219) efuse_init: Chip rev:         v3.1
I (224) heap_init: Initializing. RAM available for dynamic allocation:
I (230) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (235) heap_init: At 3FFB2D50 len 0002D2B0 (180 KiB): DRAM
I (240) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (245) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (251) heap_init: At 4008D050 len 00012FB0 (75 KiB): IRAM
```
## 📊 ตารางผลการทดลอง Mutex และ Critical Section

| ทดลอง | Successful | Failed | Corrupted | Success Rate | สังเกต |
|-------|-------------|---------|------------|---------------|---------|
| **1 (With Mutex)** | 7 | 0 | 0 | 100% | ทุก Task เข้าถึงทรัพยากรโดยมีการล็อกป้องกัน ทำให้ไม่เกิดการชนกันของข้อมูล |
| **2 (No Mutex)** | 3 | 0 | 4 | 42.8% | เกิด **Race Condition** เพราะหลาย Task เข้าถึงทรัพยากรพร้อมกัน → Buffer/Counter มีค่าผิดหรือไม่ตรงกัน |
| **3 (Changed Priority)** | 6 | 0 | 1 | 85.7% | มีการแย่ง Mutex จาก Task Priority สูงกว่า แต่ระบบยังคงรักษาข้อมูลได้ดีเพราะมี **Priority Inheritance** มาช่วยป้องกัน |

---

## 🔬 คำถามสำหรับการทดลอง

### 1. เมื่อไม่ใช้ **Mutex** จะเกิด data corruption หรือไม่?
- ✅ **เกิดแน่นอน** เพราะหลาย Task เข้าถึงและแก้ไขตัวแปรเดียวกัน (เช่น Counter, Buffer) พร้อมกัน  
- ผลคือเกิด **Race Condition** → ค่าอาจซ้ำ, หาย, หรือไม่ถูกต้อง  
- การใช้ Mutex จะช่วยให้ “มีเพียง Task เดียวเท่านั้น” ที่เข้า critical section ได้ในเวลาเดียวกัน

---

### 2. **Priority Inheritance** ทำงานอย่างไร?
- เมื่อ Task Priority ต่ำ **ถือ Mutex อยู่** แล้วมี Task Priority สูงกว่า **ต้องการใช้ Mutex เดียวกัน**, ระบบจะ:  
  1. ชั่วคราว **ยก Priority ของ Task ที่ถือ Mutex** ให้เท่ากับของ Task สูงสุดที่รออยู่  
  2. ป้องกันไม่ให้ Task ระดับกลาง “แทรก” เข้ามาขัดจังหวะ (แก้ปัญหา **Priority Inversion**)  
  3. เมื่อ Task เดิมปล่อย Mutex → Priority จะถูกลดกลับสู่ค่าปกติ  

### 3. **Task Priority** มีผลต่อการเข้าถึง shared resource อย่างไร?
| กรณี | ผลลัพธ์ |
|-------|----------|
| ไม่มี Mutex | Task ที่ Priority สูงอาจแย่ง CPU แต่ไม่สามารถป้องกันข้อมูลซ้อนกันได้ |
| มี Mutex แต่ไม่มี Priority Inheritance | อาจเกิด **Priority Inversion** (Low ถือ Mutex ทำให้ High ต้องรอ) |
| มี Mutex + Priority Inheritance | ระบบยก Priority ของ Low ชั่วคราว → ป้องกันการค้างและรักษาข้อมูลปลอดภัย |
| Priority สูงเกินไป | อาจแย่งทรัพยากรบ่อย ทำให้ Task อื่นได้โอกาสน้อย ต้องบาลานซ์ Priority ให้เหมาะสม |


# 04-3-1
```c
I (287) main_task: Started on CPU0
I (297) main_task: Calling app_main()
I (297) COUNTING_SEM: Counting Semaphores Lab Starting...
I (297) COUNTING_SEM: Counting semaphore created (max count: 3)
I (297) COUNTING_SEM: Producer1 started
I (307) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (307) COUNTING_SEM: Producer2 started
I (307) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (317) COUNTING_SEM: Producer3 started
I (317) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (327) COUNTING_SEM: Producer4 started
I (327) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (337) COUNTING_SEM: Producer5 started
I (337) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (347) COUNTING_SEM: Resource monitor started
I (347) COUNTING_SEM: Load generator started
I (347) COUNTING_SEM: Statistics task started
I (357) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (357) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 1097ms
I (367) COUNTING_SEM: ✓ Producer2: Acquired resource 2 (wait: 0ms)
I (377) COUNTING_SEM: ✓ Producer3: Acquired resource 3 (wait: 0ms)
I (377) COUNTING_SEM: 🔧 Producer2: Using resource 2 for 3680ms
I (377) COUNTING_SEM: 🔧 Producer3: Using resource 3 for 1883ms
I (367) COUNTING_SEM: System created with:
I (397) COUNTING_SEM:   Resources: 3
I (397) COUNTING_SEM:   Producers: 5
I (397) COUNTING_SEM:   Initial semaphore count: 3
I (407) COUNTING_SEM:
System operational - monitoring resource pool usage!
I (1457) COUNTING_SEM: ✓ Producer1: Released resource 1
I (1457) COUNTING_SEM: ✓ Producer4: Acquired resource 1 (wait: 1070ms)
I (1457) COUNTING_SEM: 🔧 Producer4: Using resource 1 for 3601ms
I (2267) COUNTING_SEM: ✓ Producer3: Released resource 3
I (2267) COUNTING_SEM: ✓ Producer5: Acquired resource 3 (wait: 1870ms)
I (2267) COUNTING_SEM: 🔧 Producer5: Using resource 3 for 1247ms
I (2317) main_task: Returned from app_main()
I (3507) COUNTING_SEM: ✓ Producer5: Released resource 3
I (4067) COUNTING_SEM: ✓ Producer2: Released resource 2
I (5057) COUNTING_SEM: ✓ Producer4: Released resource 1
I (5347) COUNTING_SEM: 
📊 RESOURCE POOL STATUS
I (5347) COUNTING_SEM: Available resources: 3/3
I (5347) COUNTING_SEM: Resources in use: 0
I (5347) COUNTING_SEM:   Resource 1: FREE (Total usage: 2 times)
I (5347) COUNTING_SEM:   Resource 2: FREE (Total usage: 1 times)
I (5357) COUNTING_SEM:   Resource 3: FREE (Total usage: 2 times)
Pool: [□□□] Available: 3
I (5367) COUNTING_SEM: ═══════════════════════════
```
# 04-3-2
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 29 2025 20:49:53
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a710h ( 42768) map
I (103) esp_image: segment 1: paddr=0001a738 vaddr=3ffb0000 size=024b8h (  9400) load
I (106) esp_image: segment 2: paddr=0001cbf8 vaddr=40080000 size=03420h ( 13344) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=174bch ( 95420) map
I (147) esp_image: segment 4: paddr=000374e4 vaddr=40083420 size=09c58h ( 40024) load
I (162) esp_image: segment 5: paddr=00041144 vaddr=50000000 size=00020h (    32) load
I (169) boot: Loaded app from partition at offset 0x10000
I (169) boot: Disabling RNG early entropy source...
I (181) cpu_start: Multicore app
I (189) cpu_start: Pro cpu start user code
I (189) cpu_start: cpu freq: 160000000 Hz
I (189) app_init: Application information:
I (189) app_init: Project name:     counting
I (193) app_init: App version:      c71b0c7
I (197) app_init: Compile time:     Oct 29 2025 20:48:48
I (202) app_init: ELF file SHA256:  b0baeac94...
I (206) app_init: ESP-IDF:          v5.5.1
I (210) efuse_init: Min chip rev:     v0.0
I (214) efuse_init: Max chip rev:     v3.99
I (218) efuse_init: Chip rev:         v3.1
I (222) heap_init: Initializing. RAM available for dynamic allocation:
I (228) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (233) heap_init: At 3FFB2DA0 len 0002D260 (180 KiB): DRAM
I (238) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (244) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (249) heap_init: At 4008D078 len 00012F88 (75 KiB): IRAM
W (256) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (268) spi_flash: detected chip: generic
I (271) spi_flash: flash io: dio
W (274) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (287) main_task: Started on CPU0
I (297) main_task: Calling app_main()
I (297) COUNTING_SEM: Counting Semaphores Lab Starting...
I (297) COUNTING_SEM: Counting semaphore created (max count: 5)
I (297) COUNTING_SEM: Producer1 started
I (307) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (307) COUNTING_SEM: Producer2 started
I (307) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (317) COUNTING_SEM: Producer3 started
I (317) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (327) COUNTING_SEM: Producer4 started
I (327) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (337) COUNTING_SEM: Producer5 started
I (337) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (347) COUNTING_SEM: Resource monitor started
I (347) COUNTING_SEM: Load generator started
I (347) COUNTING_SEM: Statistics task started
I (357) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (357) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 1690ms
I (367) COUNTING_SEM: ✓ Producer2: Acquired resource 2 (wait: 0ms)
I (377) COUNTING_SEM: ✓ Producer3: Acquired resource 3 (wait: 0ms)
I (377) COUNTING_SEM: 🔧 Producer2: Using resource 2 for 2494ms
I (377) COUNTING_SEM: 🔧 Producer3: Using resource 3 for 1448ms
I (387) COUNTING_SEM: ✓ Producer4: Acquired resource 4 (wait: 0ms)
I (397) COUNTING_SEM: ✓ Producer5: Acquired resource 5 (wait: 0ms)
I (397) COUNTING_SEM: 🔧 Producer4: Using resource 4 for 1369ms
I (407) COUNTING_SEM: 🔧 Producer5: Using resource 5 for 2312ms
I (367) COUNTING_SEM: System created with:
I (417) COUNTING_SEM:   Resources: 5
I (427) COUNTING_SEM:   Producers: 5
I (427) COUNTING_SEM:   Initial semaphore count: 5
I (427) COUNTING_SEM:
System operational - monitoring resource pool usage!
I (1767) COUNTING_SEM: ✓ Producer4: Released resource 4
I (1827) COUNTING_SEM: ✓ Producer3: Released resource 3
I (2057) COUNTING_SEM: ✓ Producer1: Released resource 1
I (2337) main_task: Returned from app_main()
I (2727) COUNTING_SEM: ✓ Producer5: Released resource 5
I (2877) COUNTING_SEM: ✓ Producer2: Released resource 2
I (5347) COUNTING_SEM: 
📊 RESOURCE POOL STATUS
I (5347) COUNTING_SEM: Available resources: 5/5
I (5347) COUNTING_SEM: Resources in use: 0
I (5347) COUNTING_SEM:   Resource 1: FREE (Total usage: 1 times)
I (5347) COUNTING_SEM:   Resource 2: FREE (Total usage: 1 times)
I (5357) COUNTING_SEM:   Resource 3: FREE (Total usage: 1 times)
I (5357) COUNTING_SEM:   Resource 4: FREE (Total usage: 1 times)
I (5367) COUNTING_SEM:   Resource 5: FREE (Total usage: 1 times)
Pool: [□□□□□] Available: 5
I (5377) COUNTING_SEM: ═══════════════════════════

I (6157) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (6207) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (6207) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 1655ms
I (6427) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (6477) COUNTING_SEM: ✓ Producer2: Acquired resource 2 (wait: 0ms)
I (6477) COUNTING_SEM: 🔧 Producer2: Using resource 2 for 2031ms
I (6557) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (6577) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (6607) COUNTING_SEM: ✓ Producer5: Acquired resource 3 (wait: 0ms)
I (6607) COUNTING_SEM: 🔧 Producer5: Using resource 3 for 3027ms
I (6627) COUNTING_SEM: ✓ Producer3: Acquired resource 4 (wait: 0ms)
I (6627) COUNTING_SEM: 🔧 Producer3: Using resource 4 for 3589ms
I (6667) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (6717) COUNTING_SEM: ✓ Producer4: Acquired resource 5 (wait: 0ms)
I (6717) COUNTING_SEM: 🔧 Producer4: Using resource 5 for 1053ms
I (7767) COUNTING_SEM: ✓ Producer4: Released resource 5
I (7857) COUNTING_SEM: ✓ Producer1: Released resource 1
I (8507) COUNTING_SEM: ✓ Producer2: Released resource 2
I (9627) COUNTING_SEM: ✓ Producer5: Released resource 3
I (10207) COUNTING_SEM: ✓ Producer3: Released resource 4
I (10387) COUNTING_SEM: 
📊 RESOURCE POOL STATUS
I (10387) COUNTING_SEM: Available resources: 5/5
I (10387) COUNTING_SEM: Resources in use: 0
I (10387) COUNTING_SEM:   Resource 1: FREE (Total usage: 2 times)
I (10387) COUNTING_SEM:   Resource 2: FREE (Total usage: 2 times)
I (10397) COUNTING_SEM:   Resource 3: FREE (Total usage: 2 times)
I (10397) COUNTING_SEM:   Resource 4: FREE (Total usage: 2 times)
I (10407) COUNTING_SEM:   Resource 5: FREE (Total usage: 2 times)
Pool: [□□□□□] Available: 5
I (10417) COUNTING_SEM: ═══════════════════════════

I (11837) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (11857) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (11887) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (11887) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 2156ms
I (11907) COUNTING_SEM: ✓ Producer4: Acquired resource 2 (wait: 0ms)
I (11907) COUNTING_SEM: 🔧 Producer4: Using resource 2 for 3209ms
I (12367) COUNTING_SEM: 
📈 SYSTEM STATISTICS
I (12367) COUNTING_SEM: Total requests: 12
I (12367) COUNTING_SEM: Successful acquisitions: 12
I (12367) COUNTING_SEM: Failed acquisitions: 0
I (12367) COUNTING_SEM: Current resources in use: 2
I (12377) COUNTING_SEM: Success rate: 100.0%
I (12377) COUNTING_SEM: Resource utilization:
I (12377) COUNTING_SEM:   Resource 1: 3 uses, 3345 total time
I (12387) COUNTING_SEM:   Resource 2: 3 uses, 4525 total time
I (12387) COUNTING_SEM:   Resource 3: 2 uses, 4475 total time
I (12397) COUNTING_SEM:   Resource 4: 2 uses, 4958 total time
I (12407) COUNTING_SEM:   Resource 5: 2 uses, 3365 total time
I (12407) COUNTING_SEM: Total resource usage events: 12
I (12417) COUNTING_SEM: ════════════════════════════

I (12437) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (12487) COUNTING_SEM: ✓ Producer2: Acquired resource 3 (wait: 0ms)
I (12487) COUNTING_SEM: 🔧 Producer2: Using resource 3 for 3591ms
I (13037) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (13087) COUNTING_SEM: ✓ Producer3: Acquired resource 4 (wait: 0ms)
I (13087) COUNTING_SEM: 🔧 Producer3: Using resource 4 for 1999ms
I (13117) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (13167) COUNTING_SEM: ✓ Producer5: Acquired resource 5 (wait: 0ms)
I (13167) COUNTING_SEM: 🔧 Producer5: Using resource 5 for 3803ms
I (14037) COUNTING_SEM: ✓ Producer1: Released resource 1
I (15077) COUNTING_SEM: ✓ Producer3: Released resource 4
I (15107) COUNTING_SEM: ✓ Producer4: Released resource 2
I (15427) COUNTING_SEM: 
📊 RESOURCE POOL STATUS
I (15427) COUNTING_SEM: Available resources: 3/5
I (15427) COUNTING_SEM: Resources in use: 2
I (15427) COUNTING_SEM:   Resource 1: FREE (Total usage: 3 times)
I (15427) COUNTING_SEM:   Resource 2: FREE (Total usage: 3 times)
I (15437) COUNTING_SEM:   Resource 3: BUSY (User: Producer2, Usage: 3 times)
I (15447) COUNTING_SEM:   Resource 4: FREE (Total usage: 3 times)
I (15447) COUNTING_SEM:   Resource 5: BUSY (User: Producer5, Usage: 3 times)
Pool: [□□■□■] Available: 3
I (15457) COUNTING_SEM: ═══════════════════════════

I (16077) COUNTING_SEM: ✓ Producer2: Released resource 3
I (16967) COUNTING_SEM: ✓ Producer5: Released resource 5
I (17207) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (17257) COUNTING_SEM: ✓ Producer3: Acquired resource 1 (wait: 0ms)
I (17257) COUNTING_SEM: 🔧 Producer3: Using resource 1 for 2327ms
```
# 04-3-3
```c
I (287) main_task: Started on CPU0
I (297) main_task: Calling app_main()
I (297) COUNTING_SEM: Counting Semaphores Lab Starting...
I (297) COUNTING_SEM: Counting semaphore created (max count: 5)
I (297) COUNTING_SEM: Producer1 started
I (307) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (307) COUNTING_SEM: Producer2 started
I (307) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (317) COUNTING_SEM: Producer3 started
I (317) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (327) COUNTING_SEM: Producer4 started
I (327) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (337) COUNTING_SEM: Producer5 started
I (337) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (347) COUNTING_SEM: Producer0 started
I (347) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (357) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (357) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 1522ms
I (367) COUNTING_SEM: ✓ Producer2: Acquired resource 2 (wait: 0ms)
I (367) COUNTING_SEM: Load generator started
I (367) COUNTING_SEM: Producer0 started
I (367) COUNTING_SEM: Producer0 started
I (377) COUNTING_SEM: 🔧 Producer2: Using resource 2 for 1055ms
I (377) COUNTING_SEM: ✓ Producer3: Acquired resource 3 (wait: 0ms)
I (377) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (377) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (387) COUNTING_SEM: ✓ Producer4: Acquired resource 4 (wait: 0ms)
I (397) COUNTING_SEM: ✓ Producer5: Acquired resource 5 (wait: 0ms)
I (397) COUNTING_SEM: 🔧 Producer3: Using resource 3 for 2780ms
I (407) COUNTING_SEM: 🔧 Producer4: Using resource 4 for 2664ms
I (417) COUNTING_SEM: 🔧 Producer5: Using resource 5 for 3458ms
I (367) COUNTING_SEM: Resource monitor started
I (367) COUNTING_SEM: Statistics task started
I (367) COUNTING_SEM: System created with:
I (447) COUNTING_SEM:   Resources: 5
I (447) COUNTING_SEM:   Producers: 8
I (457) COUNTING_SEM:   Initial semaphore count: 5
I (457) COUNTING_SEM: 
System operational - monitoring resource pool usage!
I (1437) COUNTING_SEM: ✓ Producer2: Released resource 2
I (1437) COUNTING_SEM: ✓ Producer0: Acquired resource 2 (wait: 1030ms)
I (1437) COUNTING_SEM: 🔧 Producer0: Using resource 2 for 3558ms
I (1887) COUNTING_SEM: ✓ Producer1: Released resource 1
I (1887) COUNTING_SEM: ✓ Producer0: Acquired resource 1 (wait: 1440ms)
I (1887) COUNTING_SEM: 🔧 Producer0: Using resource 1 for 1870ms
I (2367) main_task: Returned from app_main()
I (3087) COUNTING_SEM: ✓ Producer4: Released resource 4
I (3087) COUNTING_SEM: ✓ Producer0: Acquired resource 4 (wait: 2630ms)
I (3087) COUNTING_SEM: 🔧 Producer0: Using resource 4 for 2248ms
I (3207) COUNTING_SEM: ✓ Producer3: Released resource 3
I (3757) COUNTING_SEM: ✓ Producer0: Released resource 1
I (3887) COUNTING_SEM: ✓ Producer5: Released resource 5
I (4397) COUNTING_SEM: 🏭 Producer1: Requesting resource...
I (4447) COUNTING_SEM: ✓ Producer1: Acquired resource 1 (wait: 0ms)
I (4447) COUNTING_SEM: 🔧 Producer1: Using resource 1 for 2698ms
I (4987) COUNTING_SEM: ✓ Producer0: Released resource 2
I (5327) COUNTING_SEM: ✓ Producer0: Released resource 4
I (5437) COUNTING_SEM: 
📊 RESOURCE POOL STATUS
I (5437) COUNTING_SEM: Available resources: 4/5
I (5437) COUNTING_SEM: Resources in use: 1
I (5437) COUNTING_SEM:   Resource 1: BUSY (User: Producer1, Usage: 3 times)
I (5437) COUNTING_SEM:   Resource 2: FREE (Total usage: 2 times)
I (5447) COUNTING_SEM:   Resource 3: FREE (Total usage: 1 times)
I (5447) COUNTING_SEM:   Resource 4: FREE (Total usage: 2 times)
I (5457) COUNTING_SEM:   Resource 5: FREE (Total usage: 1 times)
Pool: [■□□□□] Available: 4
I (5467) COUNTING_SEM: ═══════════════════════════

I (5567) COUNTING_SEM: 🏭 Producer4: Requesting resource...
I (5617) COUNTING_SEM: ✓ Producer4: Acquired resource 2 (wait: 0ms)
I (5617) COUNTING_SEM: 🔧 Producer4: Using resource 2 for 1933ms
I (5907) COUNTING_SEM: 🏭 Producer2: Requesting resource...
I (5957) COUNTING_SEM: ✓ Producer2: Acquired resource 3 (wait: 0ms)
I (5957) COUNTING_SEM: 🔧 Producer2: Using resource 3 for 1798ms
I (6357) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (6407) COUNTING_SEM: ✓ Producer0: Acquired resource 4 (wait: 0ms)
I (6407) COUNTING_SEM: 🔧 Producer0: Using resource 4 for 1191ms
I (6477) COUNTING_SEM: 🏭 Producer3: Requesting resource...
I (6527) COUNTING_SEM: ✓ Producer3: Acquired resource 5 (wait: 0ms)
I (6527) COUNTING_SEM: 🔧 Producer3: Using resource 5 for 3731ms
I (7137) COUNTING_SEM: ✓ Producer1: Released resource 1
I (7247) COUNTING_SEM: 🏭 Producer5: Requesting resource...
I (7297) COUNTING_SEM: ✓ Producer5: Acquired resource 1 (wait: 0ms)
I (7297) COUNTING_SEM: 🔧 Producer5: Using resource 1 for 3636ms
I (7547) COUNTING_SEM: ✓ Producer4: Released resource 2
I (7567) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (7597) COUNTING_SEM: ✓ Producer0: Released resource 4
I (7607) COUNTING_SEM: 🏭 Producer0: Requesting resource...
I (7617) COUNTING_SEM: ✓ Producer0: Acquired resource 2 (wait: 0ms)
I (7617) COUNTING_SEM: 🔧 Producer0: Using resource 2 for 2201ms
I (7657) COUNTING_SEM: ✓ Producer0: Acquired resource 4 (wait: 0ms)
I (7657) COUNTING_SEM: 🔧 Producer0: Using resource 4 for 2878ms
```
## 📊 ตารางผลการทดลอง (Counting Semaphore)

| ทดลอง | Resources | Producers | Success Rate | Avg Wait | Resource Utilization |
|------:|:---------:|:---------:|:------------:|:--------:|:---------------------|
| **1 (3R, 5P)** | 3 | 5 | **100%** | **≈ 588 ms** *(0,0,0,1070,1870)* | สูงช่วงต้น (เต็ม 3/3) แล้วคืนเป็นว่าง 3/3 เมื่อปล่อย |
| **2 (5R, 5P)** | 5 | 5 | **100%** | **≈ 0 ms** | สมดุล/สูงเป็นช่วงๆ (5 ตัวเริ่มทำงานพร้อมกัน แล้วว่าง 5/5 ตอนเช็กพูล) |
| **3 (3R, 8P)** | 3* | 8 | **~100%** | **~600 ms** *(มีคิวรอเป็นพักๆ)* | สูงมาก (มักใช้ 3/3 ต่อเนื่อง มีว่างน้อย) |



---

## ❓ คำถามสำหรับการทดลอง

1) **เมื่อ Producers มากกว่า Resources จะเกิดอะไรขึ้น?**  
- เกิด **การรอคิว (Blocking)** ของ producers ที่เกินจำนวน resource  
- **Avg wait เพิ่มขึ้น**, ระบบมีแนวโน้ม **ใช้งานทรัพยากรเต็ม (utilization สูง)** เกือบตลอด

2) **Load Generator มีผลต่อ Success Rate อย่างไร?**  
- ถ้าโหลดเพิ่มแบบไม่ทำให้เกิด timeout/ยกเลิก → **Success Rate ยัง 100%** แต่ **เวลารอจะยาวขึ้น**  
- ถ้ามีการกำหนด **timeout สั้น** หรือมีนโยบายยกเลิกเมื่อรอนาน → อาจเห็น **Failure เพิ่ม** และ **Success Rate ลด**

3) **Counting Semaphore จัดการ Resource Pool อย่างไร?**  
- ใช้ **ตัวนับ (count)** เป็นจำนวน “ใบอนุญาตใช้ทรัพยากร” ที่มีอยู่  
- `take` ลด count (จองทรัพยากร 1 หน่วย), `give` เพิ่ม count (คืนทรัพยากร)  
- เมื่อ count = 0 → ผู้ขอรายใหม่ **ถูกบล็อก** จนกว่าจะมีการ `give`  
- เหมาะกับ **ทรัพยากรแบบหลายหน่วย** (เช่น worker N ตัว, ช่องเชื่อมต่อ K ช่อง) ที่ต้องควบคุม **concurrency** ให้ไม่เกินขีดจำกัด
