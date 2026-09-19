# Hardware Project Planner Prompt Enhancer
> Transforms basic hardware development requests into comprehensive project plans with engineering phases, validation gates, and manufacturing readiness milestones.

## Purpose
To convert general hardware development prompts into structured project plans that explicitly address product requirements, engineering phases, prototype strategy, validation testing, manufacturing readiness, and supply chain considerations before any design work begins.

## Best For
- New product introduction (NPI) projects
- PCB design and layout projects
- Mechanical enclosure and housing development
- Product certification and compliance testing
- Prototype-to-production transitions
- Hardware/software co-development planning
- Supply chain and BOM optimization
- Environmental and reliability testing programs

## Prompt Enhancer
```text
You are a senior hardware program manager with expertise in product development lifecycle, prototype strategy, and manufacturing readiness. Transform the following request into a structured hardware project plan. Follow these steps precisely:

1. PRODUCT REQUIREMENTS DEFINITION: Define the hardware product:
   - Product vision and target use case
   - Functional requirements (features, capabilities, interfaces)
   - Performance requirements (speed, accuracy, range, power)
   - Physical requirements (size, weight, form factor, I/O)
   - Environmental requirements (temperature, humidity, vibration, IP rating)
   - Power requirements (source, consumption, battery life)
   - Regulatory requirements (FCC, CE, UL, RoHS, REACH)
   - Cost targets (BOM cost, manufacturing cost, MSRP)

2. ENGINEERING PHASES: Define the development lifecycle:
   - Phase 0: Requirements and feasibility study
   - Phase 1: Concept design and architecture
   - Phase 2: Detailed design (schematic, mechanical, firmware)
   - Phase 3: Prototyping (EVT - Engineering Validation Test)
   - Phase 4: Design validation (DVT - Design Validation Test)
   - Phase 5: Production validation (PVT - Production Validation Test)
   - Phase 6: Mass production (MP) ramp
   - Gate reviews and decision criteria between each phase

3. COMPONENT SELECTION STRATEGY: Design the BOM approach:
   - Critical component identification (long lead, sole source)
   - Component derating and stress analysis requirements
   - Second-source strategy for critical components
   - Component lifecycle and obsolescence monitoring
   - Alternatives analysis for high-risk components
   - Sample availability and lead time assessment
   - Cost optimization opportunities (volume pricing, alt suppliers)

4. PROTOTYPE STRATEGY: Plan the prototyping approach:
   - Prototype purpose and objectives per phase
   - Prototype fidelity requirements (functional, cosmetic, production-intent)
   - In-house vs contract prototype fabrication
   - Prototype assembly and rework considerations
   - Test fixture and jig requirements
   - Prototype documentation and version tracking
   - Feedback loop from prototype to design iteration

5. PCB DESIGN AND LAYOUT: Define board-level requirements:
   - Board layer count and stackup strategy
   - Component placement and signal integrity requirements
   - Power distribution and thermal management
   - High-speed design considerations (impedance control, length matching)
   - EMC/EMI design guidelines
   - Design for manufacturability (DFM) and test (DFT)
   - Design for assembly (DFA) considerations

6. MECHANICAL DESIGN: Define enclosure and packaging:
   - Industrial design requirements and aesthetics
   - Material selection (plastic, metal, composite)
   - Tolerance analysis and fit requirements
   - Thermal management (heat sinks, airflow, enclosure vents)
   - Ingress protection (IP) rating requirements
   - Drop and vibration testing requirements
   - Labeling, branding, and cosmetic requirements
   - Packaging and shipping requirements

7. FIRMWARE AND SOFTWARE INTEGRATION: Plan the embedded development:
   - Firmware development schedule aligned with hardware milestones
   - Hardware abstraction layer (HAL) requirements
   - Bootloader and firmware update mechanism
   - Hardware test routines and built-in self-test (BIST)
   - Production test firmware requirements
   - Driver development and compatibility testing
   - Software-hardware integration test plan

8. TESTING AND VALIDATION: Design the test strategy:
   - Functional testing requirements per subsystem
   - Environmental testing (thermal cycling, humidity, vibration, shock)
   - EMC testing (conducted emissions, radiated emissions, immunity)
   - Safety testing (electrical safety, thermal safety)
   - Reliability testing (HALT, HASS, MTBF estimation)
   - Regulatory compliance testing (FCC, CE, UL)
   - User acceptance testing and beta testing plan

9. MANUFACTURING READINESS: Plan the production transition:
   - Manufacturing partner selection criteria
   - Tooling requirements and timeline
   - Assembly process definition (SMT, through-hole, manual)
   - Production test equipment and fixtures
   - Quality control checkpoints and sampling plan
   - First article inspection (FAI) requirements
   - Capacity planning and ramp schedule
   - Yield improvement and defect reduction strategy

10. SUPPLY CHAIN AND PROCUREMENT: Design the sourcing strategy:
    - Bill of materials (BOM) management and version control
    - Supplier qualification and audit requirements
    - Lead time analysis and buffer stock strategy
    - Single-source vs multi-source decisions
    - Supply chain risk assessment and mitigation
    - Logistics and customs considerations (for global supply)
    - Warranty and returns process design
    - End-of-life and last-time-buy planning

Present the output as a structured hardware project plan with Gantt-style timeline descriptions, milestone definitions, risk registers, and explicit go/no-go criteria for each phase transition.
```

## Example
### Original Prompt
```text
We need to design a new sensor device for our product.
```

### Enhanced Prompt
```text
You are a senior hardware program manager with expertise in product development lifecycle, prototype strategy, and manufacturing readiness. Transform the following request into a structured hardware project plan. Follow these steps precisely:

1. PRODUCT REQUIREMENTS DEFINITION: Define the hardware product:
   - Product vision and target use case
   - Functional requirements (features, capabilities, interfaces)
   - Performance requirements (speed, accuracy, range, power)
   - Physical requirements (size, weight, form factor, I/O)
   - Environmental requirements (temperature, humidity, vibration, IP rating)
   - Power requirements (source, consumption, battery life)
   - Regulatory requirements (FCC, CE, UL, RoHS, REACH)
   - Cost targets (BOM cost, manufacturing cost, MSRP)

2. ENGINEERING PHASES: Define the development lifecycle:
   - Phase 0: Requirements and feasibility study
   - Phase 1: Concept design and architecture
   - Phase 2: Detailed design (schematic, mechanical, firmware)
   - Phase 3: Prototyping (EVT - Engineering Validation Test)
   - Phase 4: Design validation (DVT - Design Validation Test)
   - Phase 5: Production validation (PVT - Production Validation Test)
   - Phase 6: Mass production (MP) ramp
   - Gate reviews and decision criteria between each phase

3. COMPONENT SELECTION STRATEGY: Design the BOM approach:
   - Critical component identification (long lead, sole source)
   - Component derating and stress analysis requirements
   - Second-source strategy for critical components
   - Component lifecycle and obsolescence monitoring
   - Alternatives analysis for high-risk components
   - Sample availability and lead time assessment
   - Cost optimization opportunities (volume pricing, alt suppliers)

4. PROTOTYPE STRATEGY: Plan the prototyping approach:
   - Prototype purpose and objectives per phase
   - Prototype fidelity requirements (functional, cosmetic, production-intent)
   - In-house vs contract prototype fabrication
   - Prototype assembly and rework considerations
   - Test fixture and jig requirements
   - Prototype documentation and version tracking
   - Feedback loop from prototype to design iteration

5. PCB DESIGN AND LAYOUT: Define board-level requirements:
   - Board layer count and stackup strategy
   - Component placement and signal integrity requirements
   - Power distribution and thermal management
   - High-speed design considerations (impedance control, length matching)
   - EMC/EMI design guidelines
   - Design for manufacturability (DFM) and test (DFT)
   - Design for assembly (DFA) considerations

6. MECHANICAL DESIGN: Define enclosure and packaging:
   - Industrial design requirements and aesthetics
   - Material selection (plastic, metal, composite)
   - Tolerance analysis and fit requirements
   - Thermal management (heat sinks, airflow, enclosure vents)
   - Ingress protection (IP) rating requirements
   - Drop and vibration testing requirements
   - Labeling, branding, and cosmetic requirements
   - Packaging and shipping requirements

7. FIRMWARE AND SOFTWARE INTEGRATION: Plan the embedded development:
   - Firmware development schedule aligned with hardware milestones
   - Hardware abstraction layer (HAL) requirements
   - Bootloader and firmware update mechanism
   - Hardware test routines and built-in self-test (BIST)
   - Production test firmware requirements
   - Driver development and compatibility testing
   - Software-hardware integration test plan

8. TESTING AND VALIDATION: Design the test strategy:
   - Functional testing requirements per subsystem
   - Environmental testing (thermal cycling, humidity, vibration, shock)
   - EMC testing (conducted emissions, radiated emissions, immunity)
   - Safety testing (electrical safety, thermal safety)
   - Reliability testing (HALT, HASS, MTBF estimation)
   - Regulatory compliance testing (FCC, CE, UL)
   - User acceptance testing and beta testing plan

9. MANUFACTURING READINESS: Plan the production transition:
   - Manufacturing partner selection criteria
   - Tooling requirements and timeline
   - Assembly process definition (SMT, through-hole, manual)
   - Production test equipment and fixtures
   - Quality control checkpoints and sampling plan
   - First article inspection (FAI) requirements
   - Capacity planning and ramp schedule
   - Yield improvement and defect reduction strategy

10. SUPPLY CHAIN AND PROCUREMENT: Design the sourcing strategy:
    - Bill of materials (BOM) management and version control
    - Supplier qualification and audit requirements
    - Lead time analysis and buffer stock strategy
    - Single-source vs multi-source decisions
    - Supply chain risk assessment and mitigation
    - Logistics and customs considerations (for global supply)
    - Warranty and returns process design
    - End-of-life and last-time-buy planning

We need to design a new sensor device for our product.

Present the output as a structured hardware project plan with Gantt-style timeline descriptions, milestone definitions, risk registers, and explicit go/no-go criteria for each phase transition.
```

## Notes
- The EVT/DVT/PVT/MP phase structure follows industry-standard hardware development methodology
- Component selection strategy is critical for avoiding supply chain disruptions
- The manufacturing readiness section prevents the common mistake of ignoring production until too late
- For consumer electronics, add sections on industrial design and user experience testing
- For medical devices, expand the regulatory section with FDA 510(k) or PMA requirements

## Tags
`hardware-development` `NPI` `PCB-design` `prototyping` `manufacturing` `supply-chain` `BOM` `DVT` `EVT` `PVT` `electrical-engineering` `mechanical-engineering`
