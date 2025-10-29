### Lab 1
# lab 1-1
ทดสอบ Single Task:

สังเกตการทำงานของ LED
กดปุ่มและสังเกตเวลาตอบสนอง
บันทึกเวลาตอบสนองเมื่อกดปุ่ม
```c
I (8043) SINGLE_TASK: Controlling actuator...
W (8643) SINGLE_TASK: Button pressed! (Delayed response)
I (8643) SINGLE_TASK: Reading sensor...
I (9643) SINGLE_TASK: Processing data...
I (9713) SINGLE_TASK: Controlling actuator...
I (10313) SINGLE_TASK: Reading sensor...
I (11313) SINGLE_TASK: Processing data...
I (11383) SINGLE_TASK: Controlling actuator...
I (11983) SINGLE_TASK: Reading sensor...
I (12983) SINGLE_TASK: Processing data...
I (13053) SINGLE_TASK: Controlling actuator...
W (13653) SINGLE_TASK: Button pressed! (Delayed response)
I (13653) SINGLE_TASK: Reading sensor...
I (14653) SINGLE_TASK: Processing data...
I (14723) SINGLE_TASK: Controlling actuator...
I (15323) SINGLE_TASK: Reading sensor...
I (16323) SINGLE_TASK: Processing data...
I (16393) SINGLE_TASK: Controlling actuator...
I (16993) SINGLE_TASK: Reading sensor...
I (17993) SINGLE_TASK: Processing data...
I (18063) SINGLE_TASK: Controlling actuator...
I (18663) SINGLE_TASK: Reading sensor...
I (19663) SINGLE_TASK: Processing data...
I (19733) SINGLE_TASK: Controlling actuator...
```

# lab 1-2
ทดสอบ MULTITASK Task:

สังเกตการทำงานของ LED
กดปุ่มและสังเกตเวลาตอบสนอง
บันทึกเวลาตอบสนองเมื่อกดปุ่ม
```c
I (8043) MULTITASK: Controlling actuator...
W (8643) MULTITASK: Button pressed! (Delayed response)
I (8643) MULTITASK: Reading sensor...
I (9643) MULTITASK: Processing data...
I (9713) MULTITASK: Controlling actuator...
I (10313) MULTITASK Reading sensor...

```


### คำถามสำหรับวิเคราะห์
ความแตกต่างในการตอบสนองปุ่มระหว่างทั้งสองระบบคืออะไร?
- Single Task System: การตอบสนองของปุ่มจะล่าช้า เพราะโปรแกรมวนทำงานแต่ละงาน (Blink LED, คำนวณ, ควบคุม LED) แบบลำดับขั้น เมื่อปุ่มถูกกด ระบบจะตรวจสอบเฉพาะเมื่อวนถึงโค้ดเช็คปุ่ม → การตอบสนองไม่ทันที
- Multitasking System: แต่ละงานถูกแยกเป็น Task อิสระ ทำงานพร้อมกัน (โดย Scheduler ของ FreeRTOS) ดังนั้น Task ที่คอยอ่านปุ่มจะสามารถตรวจจับได้แทบจะทันที → การตอบสนองเร็วขึ้นและเสถียรกว่า
ใน Single Task System งานไหนที่ทำให้การตอบสนองล่าช้า?
- งาน Processing data (heavy computation) ซึ่งใช้ลูป for (int i=0; i<1000000; i++) ทำให้ CPU ถูกใช้เต็มช่วงเวลานั้น → ไม่มีเวลาไปตรวจสอบปุ่มจนกว่างานนี้จะเสร็จ → กดปุ่มแล้วตอบสนองช้า
ข้อดีของ Multitasking System ที่สังเกตได้คืออะไร?
- การตอบสนองทันที: Task ที่เกี่ยวกับปุ่มหรือเหตุฉุกเฉินทำงานได้ทันที โดยไม่ต้องรอให้ Task อื่นจบ
- ความเป็นระเบียบ: การแบ่งงานออกเป็น Task ทำให้โค้ดอ่านง่าย ดูแยกหน้าที่ชัดเจน
- เพิ่มความน่าเชื่อถือ: ระบบไม่พลาดเหตุการณ์สำคัญ (เช่น การกดปุ่ม Emergency)
มีข้อเสียของ Multitasking System ที่สังเกตได้หรือไม่?
- การจัดการซับซ้อนกว่า: ต้องคำนึงถึง Priority, Synchronization, และการใช้ Shared Resource
- Overhead ของ Scheduler: มีการสลับ Task ตลอดเวลา ทำให้สิ้นเปลืองบางส่วนเมื่อเทียบกับ Single Task
- ถ้าออกแบบ Priority ไม่ดี: อาจเกิดปัญหา Task starvation (บางงานไม่ได้รันเลย)
### lab2
# 2-1.1
ANS
```c
I (282) main_task: Started on CPU0
I (292) main_task: Calling app_main()
I (292) TIME_SHARING: Time-Sharing System Started
I (292) TIME_SHARING: Time slice: 50 ms
I (292) TIME_SHARING: Sensor Task 0
I (342) TIME_SHARING: Processing Task 0
I (392) TIME_SHARING: Actuator Task 0
I (442) TIME_SHARING: Display Task 0
I (492) TIME_SHARING: Sensor Task 1
I (542) TIME_SHARING: Processing Task 1
I (592) TIME_SHARING: Actuator Task 1
I (642) TIME_SHARING: Display Task 1
I (692) TIME_SHARING: Sensor Task 2
I (742) TIME_SHARING: Processing Task 2
I (792) TIME_SHARING: Actuator Task 2
I (842) TIME_SHARING: Display Task 2
I (892) TIME_SHARING: Sensor Task 3
I (942) TIME_SHARING: Processing Task 3
I (992) TIME_SHARING: Actuator Task 3
I (1042) TIME_SHARING: Display Task 3
I (1092) TIME_SHARING: Sensor Task 4
I (1142) TIME_SHARING: Processing Task 4
I (1192) TIME_SHARING: Actuator Task 4
I (1242) TIME_SHARING: Display Task 4
I (1292) TIME_SHARING: === Round 1 Statistics ===
I (1292) TIME_SHARING: Context switches: 20
I (1292) TIME_SHARING: Total time: 996068 us
I (1292) TIME_SHARING: Task execution time: 75546 us
I (1292) TIME_SHARING: CPU utilization: 7.6%
I (1302) TIME_SHARING: Overhead: 92.4%
I (1302) TIME_SHARING: Avg time per task: 3777 us
I (1302) TIME_SHARING: Sensor Task 5
I (1362) TIME_SHARING: Processing Task 5
I (1412) TIME_SHARING: Actuator Task 5
I (1462) TIME_SHARING: Display Task 5
I (1512) TIME_SHARING: Sensor Task 6
I (1562) TIME_SHARING: Processing Task 6
I (1612) TIME_SHARING: Actuator Task 6
I (1662) TIME_SHARING: Display Task 6
I (1712) TIME_SHARING: Sensor Task 7
I (1762) TIME_SHARING: Processing Task 7
I (1812) TIME_SHARING: Actuator Task 7
I (1862) TIME_SHARING: Display Task 7
I (1912) TIME_SHARING: Sensor Task 8
I (1962) TIME_SHARING: Processing Task 8
I (2012) TIME_SHARING: Actuator Task 8
I (2062) TIME_SHARING: Display Task 8
I (2112) TIME_SHARING: Sensor Task 9
I (2162) TIME_SHARING: Processing Task 9
I (2212) TIME_SHARING: Actuator Task 9
```
# 2-1.2
ANS
```c
I (262) spi_flash: detected chip: generic
I (266) spi_flash: flash io: dio
W (269) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (282) main_task: Started on CPU0
I (292) main_task: Calling app_main()
I (292) TIME_SHARING: Time-Sharing System Started
I (292) TIME_SHARING: Time slice: 50 ms
I (292) TIME_SHARING: Sensor Task 0
I (342) TIME_SHARING: Processing Task 0
I (392) TIME_SHARING: Actuator Task 0
I (442) TIME_SHARING: Display Task 0
I (492) TIME_SHARING: Sensor Task 1
I (542) TIME_SHARING: Processing Task 1
I (592) TIME_SHARING: Actuator Task 1
I (642) TIME_SHARING: Display Task 1
I (692) TIME_SHARING: Sensor Task 2
I (742) TIME_SHARING: Processing Task 2
I (792) TIME_SHARING: Actuator Task 2
I (842) TIME_SHARING: Display Task 2
I (892) TIME_SHARING: Sensor Task 3
I (942) TIME_SHARING: Processing Task 3
I (992) TIME_SHARING: Actuator Task 3
I (1042) TIME_SHARING: Display Task 3
I (1092) TIME_SHARING: Sensor Task 4
I (1142) TIME_SHARING: Processing Task 4
I (1192) TIME_SHARING: Actuator Task 4
I (1242) TIME_SHARING: Display Task 4
I (1292) TIME_SHARING: === Round 1 Statistics ===
I (1292) TIME_SHARING: Context switches: 20
I (1292) TIME_SHARING: Total time: 996067 us
I (1292) TIME_SHARING: Task execution time: 75530 us
I (1292) TIME_SHARING: CPU utilization: 7.6%
I (1302) TIME_SHARING: Overhead: 92.4%
I (1302) TIME_SHARING: Avg time per task: 3776 us
I (1302) TIME_SHARING: Sensor Task 5
I (1362) TIME_SHARING: Processing Task 5
I (1412) TIME_SHARING: Actuator Task 5
I (1462) TIME_SHARING: Display Task 5
I (1512) TIME_SHARING: Sensor Task 6
I (1562) TIME_SHARING: Processing Task 6
I (1612) TIME_SHARING: Actuator Task 6
I (1662) TIME_SHARING: Display Task 6
I (1712) TIME_SHARING: Sensor Task 7
I (1762) TIME_SHARING: Processing Task 7
I (1812) TIME_SHARING: Actuator Task 7
I (1862) TIME_SHARING: Display Task 7
I (1912) TIME_SHARING: Sensor Task 8
I (1962) TIME_SHARING: Processing Task 8
I (2012) TIME_SHARING: Actuator Task 8
I (2062) TIME_SHARING: Display Task 8
I (2112) TIME_SHARING: Sensor Task 9
I (2162) TIME_SHARING: Processing Task 9
I (2212) TIME_SHARING: Actuator Task 9
I (2262) TIME_SHARING: Display Task 9
I (2312) TIME_SHARING: === Round 2 Statistics ===
```
# 2-1.3
ANS
```c
I (8182) TIME_SHARING: Display Task 38
I (8232) TIME_SHARING: Sensor Task 39
I (8282) TIME_SHARING: Processing Task 39
I (8332) TIME_SHARING: Actuator Task 39
I (8382) TIME_SHARING: Display Task 39
I (8432) TIME_SHARING: === Round 8 Statistics ===
I (8432) TIME_SHARING: Context switches: 160
I (8432) TIME_SHARING: Total time: 8136068 us
I (8432) TIME_SHARING: Task execution time: 605749 us
I (8432) TIME_SHARING: CPU utilization: 7.4%
I (8442) TIME_SHARING: Overhead: 92.6%
I (8442) TIME_SHARING: Avg time per task: 3785 us
I (8442) TIME_SHARING: Sensor Task 40
I (8502) TIME_SHARING: Processing Task 40
I (8552) TIME_SHARING: Actuator Task 40
I (8602) TIME_SHARING: Display Task 40
I (8652) TIME_SHARING: Sensor Task 41
I (8702) TIME_SHARING: Processing Task 41
I (8752) TIME_SHARING: Actuator Task 41
I (8802) TIME_SHARING: Display Task 41
I (8852) TIME_SHARING: Sensor Task 42
I (8902) TIME_SHARING: Processing Task 42
I (8952) TIME_SHARING: Actuator Task 42
I (9002) TIME_SHARING: Display Task 42
I (9052) TIME_SHARING: Sensor Task 43
I (9102) TIME_SHARING: Processing Task 43
I (9152) TIME_SHARING: Actuator Task 43
I (9202) TIME_SHARING: Display Task 43
I (9252) TIME_SHARING: Sensor Task 44
I (9302) TIME_SHARING: Processing Task 44
I (9352) TIME_SHARING: Actuator Task 44
I (9402) TIME_SHARING: Display Task 44
I (9452) TIME_SHARING: === Round 9 Statistics ===
I (9452) TIME_SHARING: Context switches: 180
I (9452) TIME_SHARING: Total time: 9156068 us
I (9452) TIME_SHARING: Task execution time: 681514 us
I (9452) TIME_SHARING: CPU utilization: 7.4%
I (9462) TIME_SHARING: Overhead: 92.6%
I (9462) TIME_SHARING: Avg time per task: 3786 us
I (9462) TIME_SHARING: Sensor Task 45
I (9522) TIME_SHARING: Processing Task 45
```
## คำถามสำหรับวิเคราะห์

1. Time slice ขนาดไหนให้ประสิทธิภาพดีที่สุด? เพราะอะไร?
- ขนาดของ time slice ที่ดีที่สุดคือค่าที่สมดุลระหว่าง context switching overhead และ response time — โดยทั่วไปจะอยู่ในช่วง 10–100 ms
2. ปัญหาอะไรที่เกิดขึ้นเมื่อ time slice สั้นเกินไป?
- จะเกิด context switching บ่อยเกินไป
3. ปัญหาอะไรที่เกิดขึ้นเมื่อ time slice ยาวเกินไป?
- งานที่ใช้เวลาสั้นหรือ interactive (เช่น UI, การป้อนข้อมูล) จะต้องรอนาน
4. Context switching overhead คิดเป็นกี่เปอร์เซ็นต์ของเวลาทั้งหมด?
- โดยทั่วไปอยู่ที่ประมาณ 1–5% ของเวลาการทำงาน CPU ทั้งหมด
5. งานไหนที่ได้รับผลกระทบมากที่สุดจากการ time-sharing?
- งานที่ ต้องการเวลาประมวลผลต่อเนื่องนาน (CPU-bound tasks)
### Lab3
# 3-1
```c
I (1741) COOPERATIVE: Coop Task1 running: 8
I (1801) COOPERATIVE: Coop Task2 running: 8
I (1921) COOPERATIVE: Coop Task1 running: 9
I (1981) COOPERATIVE: Coop Task2 running: 9
I (2101) COOPERATIVE: Coop Task1 running: 10
I (2161) COOPERATIVE: Coop Task2 running: 10
I (2281) COOPERATIVE: Coop Task1 running: 11
I (2341) COOPERATIVE: Coop Task2 running: 11
I (2461) COOPERATIVE: Coop Task1 running: 12
I (2521) COOPERATIVE: Coop Task2 running: 12
I (2641) COOPERATIVE: Coop Task1 running: 13
I (2701) COOPERATIVE: Coop Task2 running: 13
I (2821) COOPERATIVE: Coop Task1 running: 14
I (2881) COOPERATIVE: Coop Task2 running: 14
I (3001) COOPERATIVE: Coop Task1 running: 15
I (3061) COOPERATIVE: Coop Task2 running: 15
I (3181) COOPERATIVE: Coop Task1 running: 16
I (3241) COOPERATIVE: Coop Task2 running: 16
I (3361) COOPERATIVE: Coop Task1 running: 17
I (3421) COOPERATIVE: Coop Task2 running: 17
I (3541) COOPERATIVE: Coop Task1 running: 18
I (3601) COOPERATIVE: Coop Task2 running: 18
I (3721) COOPERATIVE: Coop Task1 running: 19
I (3781) COOPERATIVE: Coop Task2 running: 19
I (3901) COOPERATIVE: Coop Task1 running: 20
I (3961) COOPERATIVE: Coop Task2 running: 20
I (4081) COOPERATIVE: Coop Task1 running: 21
I (4141) COOPERATIVE: Coop Task2 running: 21
I (4261) COOPERATIVE: Coop Task1 running: 22
I (4321) COOPERATIVE: Coop Task2 running: 22
I (4441) COOPERATIVE: Coop Task1 running: 23
I (4501) COOPERATIVE: Coop Task2 running: 23
I (4621) COOPERATIVE: Coop Task1 running: 24
I (4681) COOPERATIVE: Coop Task2 running: 24
I (4801) COOPERATIVE: Coop Task1 running: 25
I (4861) COOPERATIVE: Coop Task2 running: 25
I (4981) COOPERATIVE: Coop Task1 running: 26
I (5041) COOPERATIVE: Coop Task2 running: 26
I (5161) COOPERATIVE: Coop Task1 running: 27
I (5221) COOPERATIVE: Coop Task2 running: 27
I (5341) COOPERATIVE: Coop Task1 running: 28
I (5401) COOPERATIVE: Coop Task2 running: 28
I (5521) COOPERATIVE: Coop Task1 running: 29
I (5581) COOPERATIVE: Coop Task2 running: 29
I (5701) COOPERATIVE: Coop Task1 running: 30
I (5761) COOPERATIVE: Coop Task2 running: 30
I (5881) COOPERATIVE: Coop Task1 running: 31
I (5941) COOPERATIVE: Coop Task2 running: 31
I (6061) COOPERATIVE: Coop Task1 running: 32
I (6121) COOPERATIVE: Coop Task2 running: 32
I (6241) COOPERATIVE: Coop Task1 running: 33
I (6301) COOPERATIVE: Coop Task2 running: 33
I (6421) COOPERATIVE: Coop Task1 running: 34
I (6481) COOPERATIVE: Coop Task2 running: 34
I (6601) COOPERATIVE: Coop Task1 running: 35
```
# 3-2
```c
I (10392) PREEMPTIVE: Preempt Task1: 84
I (10502) PREEMPTIVE: Preempt Task2: 45
I (10512) PREEMPTIVE: Preempt Task1: 85
I (10632) PREEMPTIVE: Preempt Task1: 86
I (10732) PREEMPTIVE: Preempt Task2: 46
I (10752) PREEMPTIVE: Preempt Task1: 87
I (10872) PREEMPTIVE: Preempt Task1: 88
I (10962) PREEMPTIVE: Preempt Task2: 47
I (10992) PREEMPTIVE: Preempt Task1: 89
I (11112) PREEMPTIVE: Preempt Task1: 90
I (11192) PREEMPTIVE: Preempt Task2: 48
I (11232) PREEMPTIVE: Preempt Task1: 91
I (11352) PREEMPTIVE: Preempt Task1: 92
I (11422) PREEMPTIVE: Preempt Task2: 49
I (11472) PREEMPTIVE: Preempt Task1: 93
I (11592) PREEMPTIVE: Preempt Task1: 94
I (11652) PREEMPTIVE: Preempt Task2: 50
I (11712) PREEMPTIVE: Preempt Task1: 95
I (11832) PREEMPTIVE: Preempt Task1: 96
I (11882) PREEMPTIVE: Preempt Task2: 51
I (11952) PREEMPTIVE: Preempt Task1: 97
I (12072) PREEMPTIVE: Preempt Task1: 98
I (12092) PREEMPTIVE: Preempt Task2: 52
I (12192) PREEMPTIVE: Preempt Task1: 99
I (12302) PREEMPTIVE: Preempt Task2: 53
I (12312) PREEMPTIVE: Preempt Task1: 100
I (12432) PREEMPTIVE: Preempt Task1: 101
I (12532) PREEMPTIVE: Preempt Task2: 54
I (12552) PREEMPTIVE: Preempt Task1: 102
I (12672) PREEMPTIVE: Preempt Task1: 103
I (12762) PREEMPTIVE: Preempt Task2: 55
I (12792) PREEMPTIVE: Preempt Task1: 104
I (12912) PREEMPTIVE: Preempt Task1: 105
I (12992) PREEMPTIVE: Preempt Task2: 56
I (13032) PREEMPTIVE: Preempt Task1: 106
I (13152) PREEMPTIVE: Preempt Task1: 107
I (13222) PREEMPTIVE: Preempt Task2: 57
I (13272) PREEMPTIVE: Preempt Task1: 108
I (13392) PREEMPTIVE: Preempt Task1: 109
I (13452) PREEMPTIVE: Preempt Task2: 58
I (13512) PREEMPTIVE: Preempt Task1: 110
I (13632) PREEMPTIVE: Preempt Task1: 111
```
