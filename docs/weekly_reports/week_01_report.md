# Weekly Progress Report

**Name:** Ahana Banerjee
**Domain:** Embedded Systems & IoT
**Date of Submission:** 12/06/2026
**Week Ending:** 01

## I. Overview

This week, the primary focus was on understanding the requirements of the project **"AI-Enabled Photovoltaic Monitoring and Fault Detection System using Simulated UCT DAMS, MQTT and Node-RED."** The work mainly involved conducting a literature survey, studying photovoltaic monitoring systems, understanding the concept of Industrial DAMS, and designing the overall system architecture.

## II. Achievements

### 1. Project Research and Planning

- Studied the working principles of photovoltaic (PV) monitoring systems.
- Understood the role of Industrial IoT in renewable energy applications.
- Explored the concept of UCT DAMS and its industrial use cases.
- Defined the project objectives and identified the major system components.

### 2. System Architecture Design

**Project Name:** AI-Enabled Photovoltaic Monitoring and Fault Detection System

- Designed the high-level architecture of the complete system.
- Identified the flow of data from virtual sensors to MQTT, Node-RED, database, AI analytics, and dashboard.
- Finalized the software stack:
  - Node-RED
  - Mosquitto MQTT Broker
  - Python
  - SQLite/JSON Database
  - Node-RED Dashboard
  - GitHub

### 3. Literature Survey and Parameter Identification

- Identified the important parameters to be monitored:
  - Voltage
  - Current
  - Power
  - Panel Temperature
  - Efficiency
  - Solar Irradiance
- Studied common photovoltaic faults such as:
  - Panel overheating
  - Dust accumulation
  - Partial shading
  - Electrical faults
  - Performance degradation

## III. Challenges

### 1. Understanding UCT DAMS Architecture

- Since actual UCT DAMS hardware and documentation are not available, understanding its industrial workflow was challenging.
- A software-based simulation approach was planned to replicate its functionality.

### 2. Defining the Overall System Design

- Integrating multiple technologies such as Node-RED, MQTT, AI, and database management into a single workflow required careful planning.
- Additional research was performed to ensure proper communication between each module.

## IV. Learning Resources

### 1. Industrial IoT and Photovoltaic Systems

- Studied online resources related to solar monitoring systems and Industrial IoT architecture.
- Reviewed industrial dashboard and SCADA concepts for inspiration.

### 2. Node-RED and MQTT

- Began learning the basics of Node-RED flow programming.
- Studied MQTT publish-subscribe communication and its applications in IoT.

### 3. AI-Based Fault Detection

- Explored introductory resources on machine learning applications for predictive maintenance and fault classification.

## V. Next Week's Goals

### 1. Node-RED and MQTT Implementation

- Install and configure Node-RED.
- Install Mosquitto MQTT Broker.
- Create virtual photovoltaic sensor nodes.
- Establish MQTT communication between publisher and subscriber.

### 2. Simulated DAMS Development

- Develop the initial simulated DAMS workflow.
- Test data transmission using sample sensor values.

### 3. Documentation

- Update project documentation.
- Record implementation progress and prepare the Week 2 report.

## VI. Additional Comments

The first week was primarily dedicated to planning and building a strong foundation for the project. A clear understanding of the system requirements, architecture, and technologies has been established. This preparation is expected to simplify the implementation stages and ensure systematic progress in the upcoming weeks.