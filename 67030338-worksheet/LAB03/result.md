# 03-1-1
```c
Queue: [□□□□□]
I (27606) QUEUE_LAB: Sent: ID=13, MSG=Hello from sender #13, Time=2732
I (27606) QUEUE_LAB: Received: ID=13, MSG=Hello from sender #13, Time=2732
I (29706) QUEUE_LAB: Sent: ID=14, MSG=Hello from sender #14, Time=2942
I (29706) QUEUE_LAB: Received: ID=14, MSG=Hello from sender #14, Time=2942
I (30336) QUEUE_LAB: Queue Status - Messages: 0, Free spaces: 5
Queue: [□□□□□]
I (31806) QUEUE_LAB: Sent: ID=15, MSG=Hello from sender #15, Time=3152
I (31806) QUEUE_LAB: Received: ID=15, MSG=Hello from sender #15, Time=3152
I (33336) QUEUE_LAB: Queue Status - Messages: 0, Free spaces: 5
Queue: [□□□□□]
I (33906) QUEUE_LAB: Sent: ID=16, MSG=Hello from sender #16, Time=3362
I (33906) QUEUE_LAB: Received: ID=16, MSG=Hello from sender #16, Time=3362
I (36006) QUEUE_LAB: Sent: ID=17, MSG=Hello from sender #17, Time=3572
I (36006) QUEUE_LAB: Received: ID=17, MSG=Hello from sender #17, Time=3572
I (36336) QUEUE_LAB: Queue Status - Messages: 0, Free spaces: 5
Queue: [□□□□□]
```
# 03-1-2
```c
Queue: [□□□□□]
I (54906) QUEUE_LAB: Sent: ID=91, MSG=Hello from sender #91, Time=5462
I (54906) QUEUE_LAB: Received: ID=91, MSG=Hello from sender #91, Time=5462
I (55506) QUEUE_LAB: Sent: ID=92, MSG=Hello from sender #92, Time=5522
I (55506) QUEUE_LAB: Received: ID=92, MSG=Hello from sender #92, Time=5522
I (56106) QUEUE_LAB: Sent: ID=93, MSG=Hello from sender #93, Time=5582
I (56106) QUEUE_LAB: Received: ID=93, MSG=Hello from sender #93, Time=5582
I (56706) QUEUE_LAB: Sent: ID=94, MSG=Hello from sender #94, Time=5642
I (56706) QUEUE_LAB: Received: ID=94, MSG=Hello from sender #94, Time=5642
I (57306) QUEUE_LAB: Sent: ID=95, MSG=Hello from sender #95, Time=5702
I (57306) QUEUE_LAB: Received: ID=95, MSG=Hello from sender #95, Time=5702
I (57336) QUEUE_LAB: Queue Status - Messages: 0, Free spaces: 5
Queue: [□□□□□]
I (57906) QUEUE_LAB: Sent: ID=96, MSG=Hello from sender #96, Time=5762
I (57906) QUEUE_LAB: Received: ID=96, MSG=Hello from sender #96, Time=5762
I (58506) QUEUE_LAB: Sent: ID=97, MSG=Hello from sender #97, Time=5822
I (58506) QUEUE_LAB: Received: ID=97, MSG=Hello from sender #97, Time=5822
```

## 📊 ตารางบันทึกผลการทดลอง Queue Communication

| ทดลอง | Sender Rate | Receiver Rate | Queue Status | สังเกต |
|-------|--------------|----------------|---------------|---------|
| **1** | 2s | 1.5s | Normal | การส่งและรับมีอัตราใกล้เคียงกัน จึงไม่เกิด Overflow หรือ Underflow ของ Queue |
| **2** | 0.5s | 1.5s | Full | Sender ส่งข้อมูลเร็วกว่า Receiver ทำให้ Queue เต็ม และ Task Sender ต้องรอ (Blocked) |
| **3** | 2s | 0.1s | Empty | Receiver อ่านเร็วกว่า Sender ทำให้ Queue ว่างบ่อย Receiver ต้องรอข้อมูล (Blocked) |


## 🔬 คำถามสำหรับการทดลอง Queue ใน FreeRTOS

### 1. เมื่อ **Queue เต็ม** การเรียก `xQueueSend` จะเกิดอะไรขึ้น?
- ถ้า **ไม่มีการกำหนดเวลารอ (timeout = 0)** → ฟังก์ชันจะ **ส่งไม่สำเร็จทันที** และคืนค่า `pdFALSE`  
- ถ้ามีการกำหนด **timeout > 0** → Task จะเข้าสู่ **Blocked state** เพื่อรอจนกว่า Queue จะมีที่ว่าง  
- หากหมดเวลาแล้วยังเต็มอยู่ → ฟังก์ชันจะคืนค่า `pdFALSE`

---

### 2. เมื่อ **Queue ว่าง** การเรียก `xQueueReceive` จะเกิดอะไรขึ้น?
- ถ้า **ไม่มี timeout** → จะ **อ่านไม่สำเร็จทันที** และคืนค่า `pdFALSE`  
- ถ้ามี timeout → Task จะเข้าสู่ **Blocked state** เพื่อรอจนกว่าจะมีข้อมูลเข้ามาใน Queue  
- เมื่อมี Task อื่นส่งข้อมูล (`xQueueSend`) → Task ที่รออยู่จะถูกปลุกขึ้นมาทำงานต่อทันที

---

### 3. ทำไม **LED จึงกะพริบตามการส่งและรับข้อความ?**
- เพราะแต่ละการ **ส่ง (Send)** และ **รับ (Receive)** ข้อความใน Queue  
  มักมีโค้ดสั่งให้ LED **เปลี่ยนสถานะ (toggle)**  
- เช่น Task A ส่งข้อมูล → LED1 ติด  
  Task B รับข้อมูล → LED2 ติด  
  ทำให้เกิดการกะพริบสลับกัน สะท้อนว่า Queue ทำงานปกติ  
- กล่าวคือ LED ใช้เป็น “ตัวบ่งชี้การสื่อสารระหว่าง Task” ผ่าน Queue  

---

# 03-2-1
```c
═══ SYSTEM STATISTICS ═══
Products Produced: 53
Products Consumed: 51
Products Dropped:  0
Queue Backlog:     2
System Efficiency: 96.2%
Queue: [■■□□□□□□□□]
═══════════════════════════

✓ Producer 3: Created Product-P3-#17 (processing: 1379ms)
✓ Consumer 1: Finished Product-P3-#16
→ Consumer 1: Processing Product-P2-#19 (queue time: 1030ms)
✓ Consumer 1: Finished Product-P2-#19
→ Consumer 1: Processing Product-P1-#15 (queue time: 1150ms)
✓ Producer 2: Created Product-P2-#20 (processing: 1378ms)
✓ Consumer 2: Finished Product-P1-#14
→ Consumer 2: Processing Product-P3-#17 (queue time: 1270ms)
✓ Producer 1: Created Product-P1-#16 (processing: 1466ms)
✓ Producer 3: Created Product-P3-#18 (processing: 1814ms)
✓ Consumer 2: Finished Product-P3-#17
→ Consumer 2: Processing Product-P2-#20 (queue time: 1470ms)
✓ Consumer 1: Finished Product-P1-#15
→ Consumer 1: Processing Product-P1-#16 (queue time: 1370ms)
✓ Producer 2: Created Product-P2-#21 (processing: 696ms)
✓ Producer 1: Created Product-P1-#17 (processing: 1403ms)
✓ Consumer 2: Finished Product-P2-#20
→ Consumer 2: Processing Product-P3-#18 (queue time: 1660ms)
✓ Consumer 1: Finished Product-P1-#16
→ Consumer 1: Processing Product-P2-#21 (queue time: 1230ms)
✓ Producer 3: Created Product-P3-#19 (processing: 1920ms)
✓ Producer 2: Created Product-P2-#22 (processing: 730ms)
✓ Producer 1: Created Product-P1-#18 (processing: 1125ms)
✓ Consumer 1: Finished Product-P2-#21
→ Consumer 1: Processing Product-P1-#17 (queue time: 1910ms)

═══ SYSTEM STATISTICS ═══
Products Produced: 62
Products Consumed: 59
Products Dropped:  0
Queue Backlog:     3
System Efficiency: 95.2%
Queue: [■■■□□□□□□□]
═══════════════════════════

✓ Consumer 2: Finished Product-P3-#18
→ Consumer 2: Processing Product-P3-#19 (queue time: 1280ms)
✓ Consumer 1: Finished Product-P1-#17
→ Consumer 1: Processing Product-P2-#22 (queue time: 1670ms)
✓ Producer 3: Created Product-P3-#20 (processing: 2118ms)
✓ Consumer 1: Finished Product-P2-#22
→ Consumer 1: Processing Product-P1-#18 (queue time: 2170ms)
✓ Producer 2: Created Product-P2-#23 (processing: 1895ms)
✓ Producer 1: Created Product-P1-#19 (processing: 727ms)
✓ Consumer 2: Finished Product-P3-#19
→ Consumer 2: Processing Product-P3-#20 (queue time: 830ms)
✓ Consumer 1: Finished Product-P1-#18
→ Consumer 1: Processing Product-P2-#23 (queue time: 1100ms)
✓ Producer 1: Created Product-P1-#20 (processing: 779ms)
✓ Producer 2: Created Product-P2-#24 (processing: 797ms)
✓ Producer 3: Created Product-P3-#21 (processing: 1159ms)
```
# 03-2-2
```c
═══ SYSTEM STATISTICS ═══
Products Produced: 23
Products Consumed: 21
Products Dropped:  0
Queue Backlog:     2
System Efficiency: 91.3%
Queue: [■■□□□□□□□□]
═══════════════════════════

✓ Producer 1: Created Product-P1-#8 (processing: 1892ms)
✓ Consumer 1: Finished Product-P2-#5
→ Consumer 1: Processing Product-P2-#6 (queue time: 1370ms)
✓ Producer 3: Created Product-P3-#8 (processing: 1257ms)
✓ Consumer 2: Finished Product-P1-#7
→ Consumer 2: Processing Product-P3-#7 (queue time: 1890ms)
✓ Producer 2: Created Product-P2-#7 (processing: 1891ms)
✓ Producer 1: Created Product-P1-#9 (processing: 2016ms)
```
# 03-2-3
```c
═══ SYSTEM STATISTICS ═══
Products Produced: 16
Products Consumed: 9
Products Dropped:  0
Queue Backlog:     7
System Efficiency: 56.2%
Queue: [■■■■■■■□□□]
═══════════════════════════

✓ Producer 2: Created Product-P2-#4 (processing: 944ms)
✓ Consumer 1: Finished Product-P3-#2
→ Consumer 1: Processing Product-P2-#2 (queue time: 4850ms)
✓ Producer 3: Created Product-P3-#5 (processing: 987ms)
✓ Producer 1: Created Product-P1-#7 (processing: 544ms)
✓ Producer 2: Created Product-P2-#5 (processing: 2028ms)
✓ Consumer 1: Finished Product-P2-#2
→ Consumer 1: Processing Product-P1-#4 (queue time: 5420ms)
⚠️  HIGH LOAD DETECTED! Queue size: 9
💡 Suggestion: Add more consumers or optimize processing
✓ Producer 1: Created Product-P1-#8 (processing: 2273ms)
✗ Producer 3: Queue full! Dropped Product-P3-#6
⚠️  HIGH LOAD DETECTED! Queue size: 10
💡 Suggestion: Add more consumers or optimize processing
✗ Producer 1: Queue full! Dropped Product-P1-#9
✓ Consumer 1: Finished Product-P1-#4
→ Consumer 1: Processing Product-P3-#3 (queue time: 6760ms)
✓ Producer 2: Created Product-P2-#6 (processing: 1779ms)
⚠️  HIGH LOAD DETECTED! Queue size: 10
💡 Suggestion: Add more consumers or optimize processing
✗ Producer 3: Queue full! Dropped Product-P3-#7

```
### ตารางผลการทดลอง
| ทดลอง | Producers | Consumers | Produced | Consumed | Dropped | Efficiency |
|------:|:---------:|:---------:|---------:|---------:|--------:|-----------:|
| **1** | 3 | 2 | 62 | 59 | 0 | 95.2% |
| **2** | 4 | 2 | 23 | 21 | 0 | 91.3% |
| **3** | 3 | 1 | 16 | 9 | 3* | 56.2%* |

---

## 2) คำตอบคำถามสำหรับการทดลอง

### 1) ในทดลองที่ 2 เกิดอะไรขึ้นกับ Queue?
- ระบบ **ค่อนข้างสมดุล**: มีผู้ผลิต 4 ตัว กับผู้บริโภค 2 ตัว ผลรวม **Produced 23 / Consumed 21**, **Dropped 0**, **Backlog 2**  
- แปลว่า Queue มีการค้างเล็กน้อย (รอคิวสั้น ๆ) แต่ **ไม่ล้น** และ **ไม่สูญหาย** ประสิทธิภาพยังดีที่ **91.3%**

### 2) ในทดลองที่ 3 ระบบทำงานเป็นอย่างไร?
- ผู้ผลิต 3 ตัว แต่มีผู้บริโภคเพียง 1 ตัว → **อัตราบริโภคไม่ทันผลิต**  
- เห็น **Queue Backlog สะสม** จนขึ้นเตือน “HIGH LOAD DETECTED!” และเกิด **Dropped** หลายรายการ  
- ประสิทธิภาพที่สรุปช่วงต้นอยู่ที่ **56.2%** และมีแนวโน้ม **ลดลง** เมื่อมีการดรอปเพิ่ม  
- แนวทางแก้: **เพิ่มจำนวน Consumers**, **ลดอัตราการผลิต**, หรือ **เพิ่มขนาด Queue**/ปรับจังหวะทำงาน

### 3) Load Balancer แจ้งเตือนเมื่อไหร่?
- จาก log มีข้อความ `HIGH LOAD DETECTED! Queue size: 9` และต่อมาที่ `10`  
- อนุมานเกณฑ์เตือน ≈ เมื่อ **ขนาดคิว ≥ 90% ของความจุ** (ที่นี่ความจุคิว = 10) หรืออย่างน้อย **ตั้งแต่ 9 ขึ้นไป**

---

## 3) หมายเหตุจาก 03-1-1 และ 03-1-2 (Sender/Receiver ตรงกัน)
- เห็นรูปแบบ **ส่งแล้วรับทันที** และสถานะคิวรายงาน `Messages: 0, Free spaces: 5` ซ้ำ ๆ  
- สื่อว่า **อัตราส่ง≈อัตรารับ** และ **Receiver ตอบสนองทัน** → คิวว่างอยู่บ่อย ไม่เกิดค้างสะสม

---
# 03-3-1
```c
═══ SYSTEM MONITOR ═══
I (30373) QUEUE_SETS: Queue States:
I (30373) QUEUE_SETS:   Sensor Queue:  0/5
I (30383) QUEUE_SETS:   User Queue:    0/3
I (30383) QUEUE_SETS:   Network Queue: 0/8
I (30393) QUEUE_SETS: Message Statistics:
I (30393) QUEUE_SETS:   Sensor:  10 messages
I (30393) QUEUE_SETS:   User:    5 messages
I (30403) QUEUE_SETS:   Network: 12 messages
I (30403) QUEUE_SETS:   Timer:   2 events
I (30403) QUEUE_SETS: ═══════════════════════

I (30523) QUEUE_SETS: ⏰ Timer: Periodic timer fired
I (30573) QUEUE_SETS: → Processing TIMER event: Periodic maintenance
I (30573) QUEUE_SETS: 📈 Stats - Sensor:10, User:5, Network:12, Timer:3
I (30723) QUEUE_SETS: 🔘 User: Button 1 pressed for 1062ms
I (30773) QUEUE_SETS: → Processing USER input: Button 1 (1062ms)
I (30773) QUEUE_SETS: 💡 Action: Toggle LED
I (31593) QUEUE_SETS: → Processing NETWORK msg: [Bluetooth] Alert notification
W (31593) QUEUE_SETS: 🚨 High priority network message!
I (31593) QUEUE_SETS: 🌐 Network [Bluetooth]: Alert notification (P:4)
I (32553) QUEUE_SETS: → Processing SENSOR data: T=29.4°C, H=53.8%
I (32553) QUEUE_SETS: 📊 Sensor: T=29.4°C, H=53.8%, ID=1
I (34153) QUEUE_SETS: → Processing NETWORK msg: [LoRa] Heartbeat signal
I (34153) QUEUE_SETS: 🌐 Network [LoRa]: Heartbeat signal (P:2)
I (36833) QUEUE_SETS: → Processing USER input: Button 2 (105ms)
I (36833) QUEUE_SETS: 📊 Action: Show status
I (36833) QUEUE_SETS: 🔘 User: Button 2 pressed for 105ms
I (37073) QUEUE_SETS: → Processing SENSOR data: T=31.4°C, H=41.8%
I (37073) QUEUE_SETS: 📊 Sensor: T=31.4°C, H=41.8%, ID=1
I (37143) QUEUE_SETS: 🌐 Network [Ethernet]: Data synchronization (P:1)
I (37273) QUEUE_SETS: → Processing NETWORK msg: [Ethernet] Data synchronization
I (40143) QUEUE_SETS: → Processing SENSOR data: T=21.4°C, H=36.7%
I (40143) QUEUE_SETS: 📊 Sensor: T=21.4°C, H=36.7%, ID=1
I (40623) QUEUE_SETS: → Processing TIMER event: Periodic maintenance
I (40623) QUEUE_SETS: 📈 Stats - Sensor:13, User:7, Network:15, Timer:4
I (40623) QUEUE_SETS: ⏰ Timer: Periodic timer fired
I (41103) QUEUE_SETS: → Processing NETWORK msg: [Bluetooth] Heartbeat signal
I (41103) QUEUE_SETS: 🌐 Network [Bluetooth]: Heartbeat signal (P:2)

```
# 03-3-2
```c
I (29) boot: ESP-IDF v5.5.1 2nd stage bootloader
I (29) boot: compile time Oct 28 2025 19:27:43
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
I (81) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=0a458h ( 42072) map
I (102) esp_image: segment 1: paddr=0001a480 vaddr=3ffb0000 size=023f8h (  9208) load
I (106) esp_image: segment 2: paddr=0001c880 vaddr=40080000 size=03798h ( 14232) load
I (112) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=142e8h ( 82664) map
I (142) esp_image: segment 4: paddr=00034310 vaddr=40083798 size=099e8h ( 39400) load
I (158) esp_image: segment 5: paddr=0003dd00 vaddr=50000000 size=00020h (    32) load
I (164) boot: Loaded app from partition at offset 0x10000
I (164) boot: Disabling RNG early entropy source...
I (176) cpu_start: Multicore app
I (184) cpu_start: Pro cpu start user code
I (184) cpu_start: cpu freq: 160000000 Hz
I (184) app_init: Application information:
I (184) app_init: Project name:     queue_sets
I (188) app_init: App version:      c71b0c7
I (192) app_init: Compile time:     Oct 28 2025 19:26:05
I (197) app_init: ELF file SHA256:  fd68da410...
I (202) app_init: ESP-IDF:          v5.5.1
I (206) efuse_init: Min chip rev:     v0.0
I (209) efuse_init: Max chip rev:     v3.99
I (213) efuse_init: Chip rev:         v3.1
I (218) heap_init: Initializing. RAM available for dynamic allocation:
I (224) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (229) heap_init: At 3FFB2CE8 len 0002D318 (180 KiB): DRAM
I (234) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (239) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (245) heap_init: At 4008D180 len 00012E80 (75 KiB): IRAM
W (251) spi_flash: Detected boya flash chip but using generic driver. For optimal functionality, enable `SPI_FLASH_SUPPORT_BOYA_CHIP` in menuconfig
I (263) spi_flash: detected chip: generic
I (267) spi_flash: flash io: dio
W (270) spi_flash: Detected size(4096k) larger than the size in the bining app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SEing app_main()
I (292) QUEUE_SETS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation LaTS: Queue Sets Implementation Lab Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETb Starting...
I (292) QUEUE_SETS: Queue set created and configured successfully
I (292) QUEUE_SETS: User input task started
I (302) QUEUE_SETS: 🔘 User: Button 1 pressed for 985ms
I (302) QUEUE_SETS: Network task started
I (302) QUEUE_SETS: 🌐 Network [WiFi]: Heartbeat signal (P:2)
I (312) QUEUE_SETS: Timer task started
I (312) QUEUE_SETS: Processor task started - waiting for events...
I (322) QUEUE_SETS: → Processing USER input: Button 1 (985ms)
I (332) QUEUE_SETS: 💡 Action: Toggle LED
I (332) QUEUE_SETS: All tasks created. System operational.
I (332) QUEUE_SETS: System monitor started
I (532) QUEUE_SETS: → Processing NETWORK msg: [WiFi] Heartbeat signal
I (2432) main_task: Returned from app_main()
I (3002) QUEUE_SETS: → Processing NETWORK msg: [Bluetooth] Configuration changed
I (3002) QUEUE_SETS: 🌐 Network [Bluetooth]: Configuration changed (P:3)
I (6932) QUEUE_SETS: → Processing NETWORK msg: [WiFi] Data synchronization
I (6932) QUEUE_SETS: 🌐 Network [WiFi]: Data synchronization (P:2)
I (7332) QUEUE_SETS: → Processing USER input: Button 2 (148ms)
I (7332) QUEUE_SETS: 📊 Action: Show status
I (7332) QUEUE_SETS: 🔘 User: Button 2 pressed for 148ms
I (10312) QUEUE_SETS: → Processing TIMER event: Periodic maintenance
I (10312) QUEUE_SETS: 📈 Stats - Sensor:0, User:2, Network:3, Timer:1
I (10312) QUEUE_SETS: ⏰ Timer: Periodic timer fired
I (10452) QUEUE_SETS: 🌐 Network [Ethernet]: Status update received (P:3)
I (10512) QUEUE_SETS: → Processing NETWORK msg: [Ethernet] Status update received
I (12782) QUEUE_SETS: → Processing NETWORK msg: [Bluetooth] Configuration changed
I (12782) QUEUE_SETS: 🌐 Network [Bluetooth]: Configuration changed (P:2)
```

# 03-3-3
```c
I (282) main_task: Started on CPU0
I (292) main_task: Calling app_main()
I (292) QUEUE_SETS: Queue Sets Implementation Lab Starting...
I (292) QUEUE_SETS: Queue set created and configured successfully
I (292) QUEUE_SETS: User input task started
I (302) QUEUE_SETS: 🔘 User: Button 1 pressed for 391ms
I (302) QUEUE_SETS: Network task started
I (302) QUEUE_SETS: 🌐 Network [LoRa]: Configuration changed (P:1)
I (312) QUEUE_SETS: Timer task started
I (312) QUEUE_SETS: Processor task started - waiting for events...
I (322) QUEUE_SETS: → Processing USER input: Button 1 (391ms)
I (332) QUEUE_SETS: 💡 Action: Toggle LED
I (332) QUEUE_SETS: All tasks created. System operational.
I (342) QUEUE_SETS: System monitor started
I (532) QUEUE_SETS: → Processing NETWORK msg: [LoRa] Configuration changed
I (2442) main_task: Returned from app_main()
I (2662) QUEUE_SETS: → Processing NETWORK msg: [WiFi] Alert notification
I (2662) QUEUE_SETS: 🌐 Network [WiFi]: Alert notification (P:2)
I (4452) QUEUE_SETS: → Processing NETWORK msg: [Ethernet] Heartbeat signal
W (4452) QUEUE_SETS: 🚨 High priority network message!
I (4452) QUEUE_SETS: 🌐 Network [Ethernet]: Heartbeat signal (P:4)
I (4732) QUEUE_SETS: → Processing USER input: Button 3 (830ms)
I (4732) QUEUE_SETS: ⚙️  Action: Settings menu
I (4732) QUEUE_SETS: 🔘 User: Button 3 pressed for 830ms
I (6912) QUEUE_SETS: → Processing NETWORK msg: [LoRa] Data synchronization
W (6912) QUEUE_SETS: 🚨 High priority network message!
I (6912) QUEUE_SETS: 🌐 Network [LoRa]: Data synchronization (P:4)
I (7942) QUEUE_SETS: → Processing USER input: Button 1 (1010ms)
I (7942) QUEUE_SETS: 💡 Action: Toggle LED
I (7942) QUEUE_SETS: 🔘 User: Button 1 pressed for 1010ms
I (10312) QUEUE_SETS: → Processing TIMER event: Periodic maintenance
I (10312) QUEUE_SETS: 📈 Stats - Sensor:0, User:3, Network:4, Timer:1
I (10312) QUEUE_SETS: ⏰ Timer: Periodic timer fired
I (10792) QUEUE_SETS: → Processing NETWORK msg: [WiFi] Status update received
I (10792) QUEUE_SETS: 🌐 Network [WiFi]: Status update received (P:3)
I (12582) QUEUE_SETS: → Processing NETWORK msg: [Ethernet] Heartbeat signal
I (12582) QUEUE_SETS: 🌐 Network [Ethernet]: Heartbeat signal (P:1)
I (13662) QUEUE_SETS: → Processing USER input: Button 3 (559ms)
I (13662) QUEUE_SETS: ⚙️  Action: Settings menu
I (13662) QUEUE_SETS: 🔘 User: Button 3 pressed for 559ms
I (15052) QUEUE_SETS: → Processing NETWORK msg: [WiFi] Alert notification
W (15052) QUEUE_SETS: 🚨 High priority network message!
I (15052) QUEUE_SETS: 🌐 Network [WiFi]: Alert notification (P:5)
I (15342) QUEUE_SETS: 
═══ SYSTEM MONITOR ═══
I (15342) QUEUE_SETS: Queue States:
I (15342) QUEUE_SETS:   Sensor Queue:  0/5
I (15342) QUEUE_SETS:   User Queue:    0/3
I (15342) QUEUE_SETS:   Network Queue: 0/8
I (15342) QUEUE_SETS: Message Statistics:
I (15352) QUEUE_SETS:   Sensor:  0 messages
I (15352) QUEUE_SETS:   User:    4 messages
I (15362) QUEUE_SETS:   Network: 7 messages
I (15362) QUEUE_SETS:   Timer:   1 events
I (15362) QUEUE_SETS: ═══════════════════════
```

## ตารางผลการทดลอง
| ทดลอง | Sensor | User | Network | Timer | Total | สังเกต |
|------:|------:|-----:|--------:|------:|------:|--------|
| **1 (ปกติ)** | 13 | 7 | 15 | 4 | **39** | โหลดกระจายตัวดี ทุกแหล่งยิงเหตุการณ์เข้ามาสม่ำเสมอ |
| **2 (ไม่มี Sensor)** | 0 | 2 | 3 | 1 | **6** | ไม่มีข้อมูลจาก Sensor ตัวประมวลผลทำงานเฉพาะ User/Network/Timer |
| **3 (Network เร็ว)** | 0 | 4 | 7 | 1 | **12** | Network เด่น มีข้อความ priority สูง (แจ้งเตือน) โผล่หลายครั้ง |

---

## คำถามสำหรับการทดลอง

### 1) Processor Task รู้ได้อย่างไรว่าข้อมูลมาจาก Queue ไหน?
- ใช้ `xQueueSelectFromSet(queueSet, timeout)` จะ **คืนค่า “แฮนด์เดิลของสมาชิกคิว/เซมาฯ”** ที่ปลุกเรา  
- จากนั้นเทียบแฮนด์เดิลกับ `sensorQueue / userQueue / networkQueue / timerQueue` เพื่อรู้แหล่งที่มา แล้วค่อย `xQueueReceive()` จากคิวนั้น  
- (เสริม) ใส่ **tag/enum** ใน payload ด้วยก็ช่วยยืนยันแหล่ง/ชนิดข้อความได้

### 2) เมื่อหลาย Queue มีข้อมูลพร้อมกัน เลือกประมวลผลอันไหนก่อน?
- มาตรฐานคือ **ตัวแรกที่พร้อม/ปลุกเราได้** (ไม่การันตีลำดับระหว่างสมาชิกใน set)  
- แนวปฏิบัติ:
  - หลังถูกปลุก ให้ทำลูป **ดึงให้หมด** ด้วย `xQueueSelectFromSet(queueSet, 0)` เพื่อเคลียร์คิวที่ยังรออยู่  
  - หากต้องการ “ลำดับความสำคัญ” ให้แยกเป็น **หลาย queue sets ตามระดับ priority** หรือทำ **priority scan** เช็คคิวสำคัญก่อนในโค้ด

### 3) Queue Sets ช่วยประหยัด CPU อย่างไร?
- แทนที่จะ **poll หลายคิว** ทีละตัว เรา **block แค่ตัวเดียว (queue set)**  
- ลด **context switch** และ **wake-ups** ที่ไม่จำเป็น → ประหยัดพลังงาน/CPU time  
- โค้ดง่ายขึ้น: N-source → 1-wait point (multiplex) แล้วค่อยแตกไปยังคิวที่ตรงเหตุการณ์

---