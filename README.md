# AIoT-HealthMonitoringSystem_Grey2White
Edge-Based Non-Intrusive Behavioural Modelling for Patient Support Systems

## Team Name
Grey2White

##  Team Members
  Team Leader: V R Sridevi
  Member 2: Diya Prakash

## Track
AIoT (Artificial Intelligence of Things)

## Problem Statement
Design intelligent bedside and ambient monitoring systems using audio, motion, and physiological signals to continuously assess patient well-being without intrusive devices.

## Project Overview
This project presents an AIoT-based, non-intrusive patient support framework that passively observes patient behaviour using ambient audio, motion, and contact-less physiological signals. Instead of relying on wearables, cameras, or manual inputs, the system integrates edge-based artificial intelligence with IoT sensing to infer patient intent—such as comfort, discomfort, or distress—and autonomously provides assistance through healthcare equipment like smart beds or wheelchairs.

The solution moves beyond traditional monitoring systems by introducing intent-aware intelligence and autonomous decision-making at the edge, reducing caregiver workload while preserving patient privacy and dignity.

## Key Objectives
- Enable continuous non-intrusive monitoring
- Integrate AI-driven behavioural modelling at the edge
- Infer patient intent, not just sensor values
- Provide autonomous assistance before escalation
- Ensure low-latency, privacy-preserving AIoT operation
- Support device-agnostic deployment across healthcare equipment

## Key Features
- Non-intrusive ambient sensing (no wearables, no cameras)
- Motion and micro-movement analysis
- Audio-based distress pattern sensing (non-recording)
- Contact-less physiological trend inference
- Edge-based AI intent inference
- Autonomous assistance actions
- Multi-level alerting (visual and audible)
- Explainable system behaviour via logs
- Scalable to beds, wheelchairs, and assistive devices

## AI Layer: Edge-Based Behavioural Intelligence (Core Contribution)

The AI component of this system is implemented as an edge-based behavioural intelligence layer, which differentiates the solution from conventional IoT monitoring setups.

### AI Capabilities
- Multi-sensor behavioural feature interpretation
  Sensor inputs are treated as behavioural indicators rather than raw values, enabling higher-level understanding of patient state.

- Context-aware intent inference
  The AI logic analyses combined patterns from motion, audio, and physiological trends to infer patient intent, such as:
  - Comfortable state
  - Discomfort requiring assistance
  - Distress requiring caregiver intervention

- Lightweight decision modelling at the edge
  Intent inference is performed locally on the ESP32 using lightweight decision models, ensuring:
  - Low latency response
  - Continuous operation without cloud dependency
  - Privacy-preserving data handling

- Agentic action selection
  Based on inferred intent, the system autonomously selects and executes appropriate actions:
  - Monitor (no action)
  - Assist (bed or device adjustment)
  - Escalate (caregiver alert)

This AI-driven behavioural modelling enables proactive, intent-aware patient support, fulfilling the core objective of AIoT.

## IoT Layer: Sensing and Actuation

The IoT layer provides the physical interface for intelligence execution:

- Embedded sensors for motion, audio, and physiological signals
- ESP32 microcontroller for edge computation
- Actuators for bed or wheelchair adjustment
- Visual and audible alert components

The AI and IoT layers operate together as a closed-loop intelligent system.

## System Workflow
1. Patient naturally interacts with healthcare equipment.
2. Non-intrusive sensors capture behavioural signals.
3. Edge AI preprocesses and interprets sensor patterns.
4. Patient intent is inferred using behavioural modelling.
5. Autonomous assistance or alerting action is executed.
6. Patient response is monitored for continuous feedback.

## System Architecture
The system follows a layered AIoT architecture:

- Sensing Layer
  Ambient and embedded sensors capture patient behaviour.

- Edge Intelligence Layer (AI Core)
  Bbehavioural feature extraction and intent inference logic.

- Decision & Action Layer 
  Autonomous actuation and alert generation.

- Interface Layer (Optional)  
  Serial output and future caregiver dashboards.

Only the actuation layer changes across devices, making the system device-agnostic.

## Wokwi Simulation (Edge AI Demonstration)

To demonstrate feasibility within hackathon constraints, the system is implemented and simulated using Wokwi with an ESP32.

### Simulated Components
- Potentiometer 1 → Motion / restlessness signal
- Potentiometer 2 → Audio / distress signal
- Potentiometer 3 → Physiological trend signal
- Servo motor → Bed position adjustment
- LEDs (Green, Yellow, Red) → Patient state indicators
- Buzzer → Caregiver alert

### AI-Driven Intent Mapping
- Normal State  
  - Low combined sensor values  
  - Green LED ON  
  - Bed remains neutral  

- Discomfort State 
  - Elevated motion pattern  
  - Yellow LED ON  
  - Autonomous bed adjustment  

- Distress State  
  - Elevated audio or physiological pattern  
  - Red LED + Buzzer ON  
  - Caregiver alert triggered  

The simulation demonstrates edge-based AI decision logic and intent inference, focusing on system behaviour rather than medical-grade signal accuracy.

## Wokwi Simulation link
https://wokwi.com/projects/451761882501678081

## To Run the Simulation
1. Open the Wokwi project link
2. Start the simulation.
3. Adjust potentiometer values to simulate patient behaviour.
4. Observe:
   - AI-driven state inference
   - Autonomous actions
   - Serial monitor explanations

## Why This is an AIoT Solution
- IoT provides sensing and actuation
- AI provides behavioural modelling and intent inference
- Intelligence runs at the edge
- Decisions are autonomous and explainable
- The system closes the loop from sensing → thinking → acting

## Future Scope
- Advanced ML-based intent prediction
- Patient-specific learning models
- Integration with hospital information systems
- Federated learning across wards
- Optional EEG-based extensions for locked-in patients

## Disclaimer
This project is a conceptual and simulation-based implementation developed for academic and hackathon purposes. It is not intended for direct clinical deployment without further validation.
