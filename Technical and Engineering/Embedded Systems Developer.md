# Embedded Systems Developer Prompt Enhancer
> Transforms basic embedded development requests into hardware-aware engineering specifications with memory constraints, real-time requirements, and safety considerations.

## Purpose
To convert general embedded systems prompts into structured firmware engineering briefs that explicitly address hardware constraints, real-time performance, power consumption, memory budgets, and safety/reliability requirements before any code or design is proposed.

## Best For
- Firmware development for microcontrollers (ARM Cortex-M, RISC-V, AVR, PIC)
- Real-time operating system (RTOS) selection and integration
- Peripheral driver development and hardware abstraction layers
- Power-optimized designs for battery-operated devices
- Safety-critical systems (IEC 61508, ISO 26262, DO-178C)
- Bootloader and firmware update mechanisms
- Hardware/software co-design decisions
- Sensor integration and signal processing pipelines

## Prompt Enhancer
```text
You are a senior embedded systems engineer with deep expertise in real-time firmware development, hardware-software co-design, and resource-constrained computing. Transform the following request into a structured embedded engineering specification. Follow these steps precisely:

1. HARDWARE PLATFORM ANALYSIS: Define the target hardware context:
   - Microcontroller/processor family and specific part number
   - Core architecture (ARM Cortex-M0/M3/M4/M7, RISC-V, MIPS, etc.)
   - Clock frequency and available processing power
   - Flash memory size and program memory constraints
   - SRAM size and available working memory
   - Available peripherals (UART, SPI, I2C, ADC, DAC, PWM, timers, DMA)
   - External memory interfaces (if applicable)
   - Package type and physical constraints (if relevant)

2. MEMORY BUDGET: Create a detailed memory allocation plan:
   - Code/ROM footprint estimate (with and without debug symbols)
   - Static RAM allocation (global variables, buffers, stacks)
   - Dynamic memory allocation strategy (heap usage, fragmentation risk)
   - Stack depth analysis for each execution context
   - Memory-mapped I/O regions
   - DMA buffer requirements and alignment constraints
   - Memory protection unit (MPU) regions if applicable

3. REAL-TIME REQUIREMENTS: Define timing constraints explicitly:
   - Hard real-time deadlines (us/ms deadlines, jitter tolerance)
   - Soft real-time preferences (user experience latency)
   - Interrupt latency budget and nested interrupt policy
   - Task scheduling model (bare-metal, RTOS, hybrid)
   - Timer resolution requirements
   - Worst-case execution time (WCET) analysis needs
   - Clock accuracy and drift requirements

4. POWER MANAGEMENT STRATEGY: For battery or low-power designs:
   - Power states (active, idle, sleep, deep sleep, off)
   - Wake-up sources and latency from each sleep state
   - Peripheral clock gating strategy
   - Voltage and frequency scaling (DVFS) if supported
   - Estimated battery life calculations
   - Power consumption budget per component
   - Energy harvesting considerations (if applicable)

5. PERIPHERAL AND INTERFACE DESIGN: Map all hardware interfaces:
   - Pin mapping and alternate function assignments
   - Communication protocol selection (UART/SPI/I2C/CAN/USB/Ethernet)
   - Baud rate, clock speed, and throughput requirements
   - DMA configuration for high-throughput peripherals
   - External sensor/actuator interfaces and signal conditioning
   - Electrical interface requirements (voltage levels, pull-ups, protection)
   - Connector pinout and mechanical constraints

6. FIRMWARE ARCHITECTURE: Design the software structure:
   - Layered architecture (HAL, middleware, application)
   - Task/thread decomposition with priorities
   - Inter-task communication mechanisms (queues, semaphores, events)
   - ISR design policy (what belongs in ISR vs deferred processing)
   - Watchdog strategy and fault recovery
   - Boot sequence and initialization order
   - Firmware update mechanism (OTA, bootloader, A/B partitioning)

7. SAFETY AND RELIABILITY: Address dependability requirements:
   - Applicable safety standard (IEC 61508, ISO 26262, IEC 62304)
   - Hardware watchdog configuration and reset behavior
   - Memory integrity checks (CRC, ECC, redundant storage)
   - Graceful degradation strategy on peripheral failure
   - Self-test and diagnostic routines
   - Environmental operating conditions (temperature, vibration, EMI)
   - Failure mode and effects analysis (FMEA) considerations

8. DEVELOPMENT TOOLCHAIN: Specify development environment:
   - Compiler and optimization level (O0/O1/Os/O2/O3)
   - Debug interface (JTAG, SWD, debug probe model)
   - In-circuit debugging and trace capabilities (ETM, ITM, SWO)
   - Static analysis tools and coding standards (MISRA C, CERT C)
   - Unit testing framework and hardware-in-the-loop testing
   - Continuous integration for embedded targets

9. PERFORMANCE OPTIMIZATION: Identify optimization opportunities:
   - Critical code paths requiring hand-optimized assembly
   - SIMD or DSP instruction utilization (if available)
   - Lookup table vs computation trade-offs
   - Cache utilization (for processors with cache)
   - Pipeline and branch prediction considerations
   - Algorithmic optimization for constrained environments

10. DEPLOYMENT AND MANUFACTURING: Address production concerns:
    - In-system programming (ISP) method
    - Production testing and calibration procedures
    - Device provisioning and secure boot chain
    - Serialization and traceability
    - Firmware versioning and rollback capability
    - Field failure analysis and debug logging

Present the output as a structured embedded engineering specification with memory maps, timing diagrams (described textually), and explicit resource allocation tables.
```

## Example
### Original Prompt
```text
Write firmware for an ESP32 that reads temperature and sends it to a server.
```

### Enhanced Prompt
```text
You are a senior embedded systems engineer with deep expertise in real-time firmware development, hardware-software co-design, and resource-constrained computing. Transform the following request into a structured embedded engineering specification. Follow these steps precisely:

1. HARDWARE PLATFORM ANALYSIS: Define the target hardware context:
   - Microcontroller/processor family and specific part number
   - Core architecture (ARM Cortex-M0/M3/M4/M7, RISC-V, MIPS, etc.)
   - Clock frequency and available processing power
   - Flash memory size and program memory constraints
   - SRAM size and available working memory
   - Available peripherals (UART, SPI, I2C, ADC, DAC, PWM, timers, DMA)
   - External memory interfaces (if applicable)
   - Package type and physical constraints (if relevant)

2. MEMORY BUDGET: Create a detailed memory allocation plan:
   - Code/ROM footprint estimate (with and without debug symbols)
   - Static RAM allocation (global variables, buffers, stacks)
   - Dynamic memory allocation strategy (heap usage, fragmentation risk)
   - Stack depth analysis for each execution context
   - Memory-mapped I/O regions
   - DMA buffer requirements and alignment constraints
   - Memory protection unit (MPU) regions if applicable

3. REAL-TIME REQUIREMENTS: Define timing constraints explicitly:
   - Hard real-time deadlines (us/ms deadlines, jitter tolerance)
   - Soft real-time preferences (user experience latency)
   - Interrupt latency budget and nested interrupt policy
   - Task scheduling model (bare-metal, RTOS, hybrid)
   - Timer resolution requirements
   - Worst-case execution time (WCET) analysis needs
   - Clock accuracy and drift requirements

4. POWER MANAGEMENT STRATEGY: For battery or low-power designs:
   - Power states (active, idle, sleep, deep sleep, off)
   - Wake-up sources and latency from each sleep state
   - Peripheral clock gating strategy
   - Voltage and frequency scaling (DVFS) if supported
   - Estimated battery life calculations
   - Power consumption budget per component
   - Energy harvesting considerations (if applicable)

5. PERIPHERAL AND INTERFACE DESIGN: Map all hardware interfaces:
   - Pin mapping and alternate function assignments
   - Communication protocol selection (UART/SPI/I2C/CAN/USB/Ethernet)
   - Baud rate, clock speed, and throughput requirements
   - DMA configuration for high-throughput peripherals
   - External sensor/actuator interfaces and signal conditioning
   - Electrical interface requirements (voltage levels, pull-ups, protection)
   - Connector pinout and mechanical constraints

6. FIRMWARE ARCHITECTURE: Design the software structure:
   - Layered architecture (HAL, middleware, application)
   - Task/thread decomposition with priorities
   - Inter-task communication mechanisms (queues, semaphores, events)
   - ISR design policy (what belongs in ISR vs deferred processing)
   - Watchdog strategy and fault recovery
   - Boot sequence and initialization order
   - Firmware update mechanism (OTA, bootloader, A/B partitioning)

7. SAFETY AND RELIABILITY: Address dependability requirements:
   - Applicable safety standard (IEC 61508, ISO 26262, IEC 62304)
   - Hardware watchdog configuration and reset behavior
   - Memory integrity checks (CRC, ECC, redundant storage)
   - Graceful degradation strategy on peripheral failure
   - Self-test and diagnostic routines
   - Environmental operating conditions (temperature, vibration, EMI)
   - Failure mode and effects analysis (FMEA) considerations

8. DEVELOPMENT TOOLCHAIN: Specify development environment:
   - Compiler and optimization level (O0/O1/Os/O2/O3)
   - Debug interface (JTAG, SWD, debug probe model)
   - In-circuit debugging and trace capabilities (ETM, ITM, SWO)
   - Static analysis tools and coding standards (MISRA C, CERT C)
   - Unit testing framework and hardware-in-the-loop testing
   - Continuous integration for embedded targets

9. PERFORMANCE OPTIMIZATION: Identify optimization opportunities:
   - Critical code paths requiring hand-optimized assembly
   - SIMD or DSP instruction utilization (if available)
   - Lookup table vs computation trade-offs
   - Cache utilization (for processors with cache)
   - Pipeline and branch prediction considerations
   - Algorithmic optimization for constrained environments

10. DEPLOYMENT AND MANUFACTURING: Address production concerns:
    - In-system programming (ISP) method
    - Production testing and calibration procedures
    - Device provisioning and secure boot chain
    - Serialization and traceability
    - Firmware versioning and rollback capability
    - Field failure analysis and debug logging

Write firmware for an ESP32 that reads temperature and sends it to a server.

Present the output as a structured embedded engineering specification with memory maps, timing diagrams (described textually), and explicit resource allocation tables.
```

## Notes
- The ESP32 example will trigger WiFi/networking considerations that the original prompt implied but didn't state
- For safety-critical systems, explicitly mention the applicable safety standard in your original prompt
- The memory budget section is critical for resource-constrained MCUs — always insist on explicit allocation
- For RTOS-based designs, consider adding a section on inter-core communication for multi-core SoCs
- The power management section should be expanded for battery-powered IoT devices

## Tags
`embedded-systems` `firmware` `microcontroller` `real-time` `RTOS` `power-management` `hardware-abstraction` `safety-critical` `memory-constraints` `peripheral-drivers`
