# 06-1-1
```c
I (286) main_task: Started on CPU0
I (296) main_task: Calling app_main()
I (296) EVENT_GROUPS: 🚀 Basic Event Groups Lab Starting...
I (296) EVENT_GROUPS: Event group created successfully
I (296) EVENT_GROUPS: 🌐 Network initialization started
I (306) EVENT_GROUPS: Initializing WiFi driver...
I (306) EVENT_GROUPS: 🌡️ Sensor initialization started
I (316) EVENT_GROUPS: Initializing I2C bus...
I (316) EVENT_GROUPS: ⚙️ Configuration loading started
I (326) EVENT_GROUPS: Reading device configuration...
I (326) EVENT_GROUPS: 💾 Storage initialization started
I (336) EVENT_GROUPS: Mounting filesystem...
I (336) EVENT_GROUPS: 🎛️ System coordinator started - waiting for subsystems...
I (346) EVENT_GROUPS: 📋 Phase 1: Waiting for basic subsystems (Network + Config)...
I (346) EVENT_GROUPS: 👁️ Event monitor started
I (356) EVENT_GROUPS: 🔍 Monitoring events...
I (356) EVENT_GROUPS: Waiting for ANY subsystem event (5 second timeout)...
I (366) EVENT_GROUPS: All tasks created successfully
I (366) EVENT_GROUPS: 
🎯 LED Indicators:
I (376) EVENT_GROUPS:   GPIO2  - Network Ready
I (376) EVENT_GROUPS:   GPIO4  - Sensor Ready
I (386) EVENT_GROUPS:   GPIO5  - Config Ready
I (386) EVENT_GROUPS:   GPIO18 - Storage Ready
I (396) EVENT_GROUPS:   GPIO19 - System Ready
I (396) EVENT_GROUPS:
🔄 Watch the serial output for event synchronization!
I (406) EVENT_GROUPS: Basic Event Groups system operational!
I (406) main_task: Returned from app_main()
I (816) EVENT_GROUPS: Detecting sensors...
I (926) EVENT_GROUPS: Loading network settings...
I (1106) EVENT_GROUPS: Connecting to WiFi...
I (1326) EVENT_GROUPS: Loading sensor parameters...
I (1336) EVENT_GROUPS: Checking filesystem integrity...
I (1626) EVENT_GROUPS: Validating configuration...
I (2016) EVENT_GROUPS: Calibrating sensors...
I (2126) EVENT_GROUPS: ✅ Configuration loaded! (took 1800 ms)
I (2126) EVENT_GROUPS: 📢 Event detected: 0x00000004
I (2126) EVENT_GROUPS: ⚙️ Configuration monitoring - checking integrity
I (2126) EVENT_GROUPS:   ⚙️ Config event active
I (2136) EVENT_GROUPS: Waiting for FULL system ready...
I (2836) EVENT_GROUPS: Creating directories...
I (3106) EVENT_GROUPS: Getting IP address...
I (3136) EVENT_GROUPS: Initializing database...
I (3936) EVENT_GROUPS: ✅ Storage ready! (took 3600 ms)
I (3936) EVENT_GROUPS: 💾 Storage maintenance - checking space and health
I (3936) EVENT_GROUPS: Storage free space: 9637 MB
I (4016) EVENT_GROUPS: Running self-tests...
I (4106) EVENT_GROUPS: ✅ Phase 1 complete - basic system ready!
I (4106) EVENT_GROUPS: 📋 Phase 2: Waiting for all subsystems...
I (4106) EVENT_GROUPS: ✅ Network ready! (took 3800 ms)
I (4106) EVENT_GROUPS: 📡 Network heartbeat - checking connectivity
I (4816) EVENT_GROUPS: ✅ Phase 2 complete - all subsystems ready!
I (4816) EVENT_GROUPS: 🎉 SYSTEM FULLY OPERATIONAL! 🎉
I (4816) EVENT_GROUPS: ═══ INITIALIZATION COMPLETE ═══
I (4816) EVENT_GROUPS: ✅ Sensors ready! (took 4500 ms)
I (4816) EVENT_GROUPS: Total initialization time: 4470 ms
I (4826) EVENT_GROUPS: Network init:  3800 ms
I (4836) EVENT_GROUPS: 🌡️ Sensor readings: 34.9°C, 70.4% RH
I (4836) EVENT_GROUPS: Sensor init:   4500 ms
I (4846) EVENT_GROUPS: Config init:   1800 ms
I (4846) EVENT_GROUPS: Storage init:  3600 ms
I (4846) EVENT_GROUPS: ══════════════════════════════════
I (4856) EVENT_GROUPS: 🔄 System health check...
I (4866) EVENT_GROUPS: Current system status: 0x0000001F
I (4866) EVENT_GROUPS:   Network:  ✅
I (4876) EVENT_GROUPS:   Sensor:   ✅
I (4876) EVENT_GROUPS:   Config:   ✅
I (4876) EVENT_GROUPS:   Storage:  ✅
I (4886) EVENT_GROUPS:   System:   ✅
I (7846) EVENT_GROUPS: 🌡️ Sensor readings: 38.1°C, 46.2% RH
I (9116) EVENT_GROUPS: 📡 Network heartbeat - checking connectivity
```

# 06-2-1
```c
I (292) main_task: Started on CPU0
I (302) main_task: Calling app_main()
I (302) EVENT_SYNC: 🚀 Event Synchronization Lab Starting...
I (302) EVENT_SYNC: Event groups and queues created successfully
I (302) EVENT_SYNC: Creating barrier synchronization tasks...
I (312) EVENT_SYNC: 🏃 Barrier Worker 0 started
I (312) EVENT_SYNC: 👷 Worker 0: Cycle 1 - Independent work (3519 ms)
I (322) EVENT_SYNC: 🏃 Barrier Worker 1 started
I (322) EVENT_SYNC: 👷 Worker 1: Cycle 1 - Independent work (3527 ms)
I (332) EVENT_SYNC: 🏃 Barrier Worker 2 started
I (332) EVENT_SYNC: 👷 Worker 2: Cycle 1 - Independent work (2469 ms)
I (342) EVENT_SYNC: 🏃 Barrier Worker 3 started
I (342) EVENT_SYNC: 👷 Worker 3: Cycle 1 - Independent work (1192 ms)
I (352) EVENT_SYNC: Creating pipeline processing tasks...
I (362) EVENT_SYNC: 🏭 Pipeline Stage 0 (Input) started
I (362) EVENT_SYNC: ⏳ Stage 0: Waiting for input...
I (372) EVENT_SYNC: 🏭 Pipeline Stage 1 (Processing) started
I (372) EVENT_SYNC: ⏳ Stage 1: Waiting for input...
I (382) EVENT_SYNC: 🏭 Pipeline Stage 2 (Filtering) started
I (382) EVENT_SYNC: ⏳ Stage 2: Waiting for input...
I (392) EVENT_SYNC: 🏭 Pipeline Stage 3 (Output) started
I (392) EVENT_SYNC: ⏳ Stage 3: Waiting for input...
I (402) EVENT_SYNC: 🏭 Pipeline data generator started
I (402) EVENT_SYNC: 🚀 Generating pipeline data ID: 1
I (412) EVENT_SYNC: 📦 Stage 0: Processing pipeline ID 1
I (412) EVENT_SYNC: 📥 Stage 0: Data input and validation
I (422) EVENT_SYNC: ✅ Pipeline data 1 injected
I (422) EVENT_SYNC: Creating workflow management tasks...
I (432) EVENT_SYNC: 📋 Workflow manager started
I (432) EVENT_SYNC: 👨‍💼 Approval task started
I (442) EVENT_SYNC: 🏗️ Resource manager started
I (442) EVENT_SYNC: 🟢 Resources available
I (442) EVENT_SYNC: 📋 Workflow generator started
I (452) EVENT_SYNC: 🚀 Generated workflow: Security Scan (ID: 1, Priority: 3, Approval: Not Required)  
I (462) EVENT_SYNC: 📝 New workflow: ID 1 - Security Scan (Priority: 3)
I (462) EVENT_SYNC: ⏳ Waiting for workflow requirements (0x00000004)...
I (462) EVENT_SYNC: 📋 Approval process initiated...
I (472) EVENT_SYNC: ✅ Workflow 1: Requirements met, starting execution
I (482) EVENT_SYNC: ⚙️ Executing workflow 1 (2705 ms estimated)
I (472) EVENT_SYNC: 📊 Statistics monitor started
I (472) EVENT_SYNC: All tasks created successfully
I (502) EVENT_SYNC:
🎯 LED Indicators:
I (502) EVENT_SYNC:   GPIO2  - Barrier Synchronization
I (512) EVENT_SYNC:   GPIO4  - Pipeline Stage 1
I (512) EVENT_SYNC:   GPIO5  - Pipeline Stage 2
I (512) EVENT_SYNC:   GPIO18 - Pipeline Stage 3
I (522) EVENT_SYNC:   GPIO19 - Workflow Active
I (522) EVENT_SYNC:
🔄 System Features:
I (532) EVENT_SYNC:   • Barrier Synchronization (4 workers)
I (532) EVENT_SYNC:   • Pipeline Processing (4 stages)
I (542) EVENT_SYNC:   • Workflow Management (approval & resources)
I (542) EVENT_SYNC:   • Real-time Statistics Monitoring
I (552) EVENT_SYNC: Event Synchronization System operational!
I (552) main_task: Returned from app_main()
I (1442) EVENT_SYNC: ➡️ Stage 0: Data passed to next stage
I (1442) EVENT_SYNC: 📦 Stage 1: Processing pipeline ID 1
I (1442) EVENT_SYNC: ⏳ Stage 0: Waiting for input...
I (1442) EVENT_SYNC: ⚙️ Stage 1: Data processing and transformation
I (1542) EVENT_SYNC: 🚧 Worker 3: Ready for barrier (cycle 1)
I (2032) EVENT_SYNC: ✅ Approval granted (took 1552 ms)
I (2802) EVENT_SYNC: 🚧 Worker 2: Ready for barrier (cycle 1)
I (2882) EVENT_SYNC: ➡️ Stage 1: Data passed to next stage
I (2882) EVENT_SYNC: 📦 Stage 2: Processing pipeline ID 1
I (2882) EVENT_SYNC: ⏳ Stage 1: Waiting for input...
I (2882) EVENT_SYNC: 🔍 Stage 2: Data filtering and validation
I (2892) EVENT_SYNC: Average value: 53.85, Quality: 87
W (3192) EVENT_SYNC: ⚠️ Workflow 1 quality check failed (71%), retrying...
I (3192) EVENT_SYNC: 📝 New workflow: ID 1 - Security Scan (Priority: 3)
I (3192) EVENT_SYNC: ⏳ Waiting for workflow requirements (0x00000004)...
I (3192) EVENT_SYNC: ✅ Workflow 1: Requirements met, starting execution
I (3202) EVENT_SYNC: ⚙️ Executing workflow 1 (3295 ms estimated)
I (3602) EVENT_SYNC: ➡️ Stage 2: Data passed to next stage
I (3602) EVENT_SYNC: 📦 Stage 3: Processing pipeline ID 1
I (3602) EVENT_SYNC: ⏳ Stage 2: Waiting for input...
I (3602) EVENT_SYNC: 📤 Stage 3: Data output and delivery
I (3612) EVENT_SYNC: ✅ Pipeline 1 completed in 3194 ms (Quality: 87)
I (3832) EVENT_SYNC: 🚧 Worker 0: Ready for barrier (cycle 1)
I (3852) EVENT_SYNC: 🚧 Worker 1: Ready for barrier (cycle 1)
I (3852) EVENT_SYNC: 🎯 Worker 0: Barrier passed! (waited 20 ms)
I (3852) EVENT_SYNC: 🎯 Worker 3: Barrier passed! (waited 2310 ms)
I (3852) EVENT_SYNC: 🎯 Worker 2: Barrier passed! (waited 1050 ms)
I (3852) EVENT_SYNC: 🤝 Worker 3: Synchronized work phase
I (3862) EVENT_SYNC: 🤝 Worker 2: Synchronized work phase
I (4052) EVENT_SYNC: 🤝 Worker 0: Synchronized work phase
I (4232) EVENT_SYNC: ⏳ Stage 3: Waiting for input...
I (5842) EVENT_SYNC: 🔴 Resources temporarily unavailable
I (5842) EVENT_SYNC: ⏳ Waiting for resources to become available...
```

# 06-3-1
```c
I (287) main_task: Started on CPU0
I (297) main_task: Calling app_main()
I (297) COMPLEX_EVENTS: 🚀 Complex Event Patterns - Smart Home System Starting...
I (297) COMPLEX_EVENTS: Event groups created successfully
I (297) COMPLEX_EVENTS: 🏠 State changed: Idle → Idle
I (307) COMPLEX_EVENTS: Creating system tasks...
I (307) COMPLEX_EVENTS: 🧠 Pattern recognition engine started
I (317) COMPLEX_EVENTS: 🏠 Home state machine started
I (317) COMPLEX_EVENTS: 🔄 System event: 0x00000001
I (327) COMPLEX_EVENTS: 🧠 Adaptive learning system started
I (327) COMPLEX_EVENTS: 📊 Status monitor started
I (337) COMPLEX_EVENTS: 🏃 Motion sensor simulation started
I (337) COMPLEX_EVENTS: 🚪 Door sensor simulation started
I (347) COMPLEX_EVENTS: 💡 Light control system started
I (347) COMPLEX_EVENTS: 🌡️ Environmental sensors started
I (357) COMPLEX_EVENTS: 🔥 High temperature detected: 32°C
I (367) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (367) COMPLEX_EVENTS: All tasks created successfully
I (377) COMPLEX_EVENTS:
🎯 Smart Home LED Indicators:
I (377) COMPLEX_EVENTS:   GPIO2  - Living Room Light
I (387) COMPLEX_EVENTS:   GPIO4  - Kitchen Light
I (387) COMPLEX_EVENTS:   GPIO5  - Bedroom Light
I (387) COMPLEX_EVENTS:   GPIO18 - Security System
I (397) COMPLEX_EVENTS:   GPIO19 - Emergency Mode
I (397) COMPLEX_EVENTS:
🤖 System Features:
I (407) COMPLEX_EVENTS:   • Event-driven State Machine
I (407) COMPLEX_EVENTS:   • Pattern Recognition Engine
I (417) COMPLEX_EVENTS:   • Adaptive Learning System
I (417) COMPLEX_EVENTS:   • Smart Home Automation
I (427) COMPLEX_EVENTS:   • Complex Event Correlation
I (427) COMPLEX_EVENTS:
🔍 Monitored Patterns:
I (437) COMPLEX_EVENTS:   • Normal Entry
I (437) COMPLEX_EVENTS:   • Break-in Attempt
I (437) COMPLEX_EVENTS:   • Goodnight Routine
I (447) COMPLEX_EVENTS:   • Wake-up Routine
I (447) COMPLEX_EVENTS:   • Leaving Home
I (457) COMPLEX_EVENTS:   • Returning Home
I (457) COMPLEX_EVENTS: Complex Event Pattern System operational!
I (467) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (467) main_task: Returned from app_main()
I (567) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (667) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (767) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (867) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
```
# 06-3-2
```c
I (287) main_task: Started on CPU0
I (297) main_task: Calling app_main()
I (297) COMPLEX_EVENTS: 🚀 Complex Event Patterns - Smart Home System Starting...
I (297) COMPLEX_EVENTS: Event groups created successfully
I (297) COMPLEX_EVENTS: 🏠 State changed: Idle → Idle
I (307) COMPLEX_EVENTS: Creating system tasks...
I (307) COMPLEX_EVENTS: 🧠 Pattern recognition engine started
I (317) COMPLEX_EVENTS: 🏠 Home state machine started
I (317) COMPLEX_EVENTS: 🔄 System event: 0x00000001
I (327) COMPLEX_EVENTS: 🧠 Adaptive learning system started
I (327) COMPLEX_EVENTS: 📊 Status monitor started
I (337) COMPLEX_EVENTS: 🏃 Motion sensor simulation started
I (337) COMPLEX_EVENTS: 🚪 Door sensor simulation started
I (347) COMPLEX_EVENTS: 💡 Light control system started
I (347) COMPLEX_EVENTS: 🌡️ Environmental sensors started
I (357) COMPLEX_EVENTS: 🔥 High temperature detected: 34°C
I (367) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (367) COMPLEX_EVENTS: All tasks created successfully
I (377) COMPLEX_EVENTS:
🎯 Smart Home LED Indicators:
I (377) COMPLEX_EVENTS:   GPIO2  - Living Room Light
I (387) COMPLEX_EVENTS:   GPIO4  - Kitchen Light
I (387) COMPLEX_EVENTS:   GPIO5  - Bedroom Light
I (387) COMPLEX_EVENTS:   GPIO18 - Security System
I (397) COMPLEX_EVENTS:   GPIO19 - Emergency Mode
I (397) COMPLEX_EVENTS:
🤖 System Features:
I (407) COMPLEX_EVENTS:   • Event-driven State Machine
I (407) COMPLEX_EVENTS:   • Pattern Recognition Engine
I (417) COMPLEX_EVENTS:   • Adaptive Learning System
I (417) COMPLEX_EVENTS:   • Smart Home Automation
I (427) COMPLEX_EVENTS:   • Complex Event Correlation
I (427) COMPLEX_EVENTS:
🔍 Monitored Patterns:
I (437) COMPLEX_EVENTS:   • Normal Entry
I (437) COMPLEX_EVENTS:   • Break-in Attempt
I (437) COMPLEX_EVENTS:   • Goodnight Routine
I (447) COMPLEX_EVENTS:   • Wake-up Routine
I (447) COMPLEX_EVENTS:   • Leaving Home
I (457) COMPLEX_EVENTS:   • Returning Home
I (457) COMPLEX_EVENTS: Complex Event Pattern System operational!
I (467) COMPLEX_EVENTS: 🔍 Sensor event detected: 0x00000020
I (467) main_task: Returned from app_main()
```