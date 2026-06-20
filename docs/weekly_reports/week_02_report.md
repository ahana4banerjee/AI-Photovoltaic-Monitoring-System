# Weekly Progress Report

**Name:** Ahana Banerjee

**Domain:** Embedded Systems & IoT

**Date of Submission:** 21/06/2026

**Week Ending:** 02

## I. Overview

This week focused on developing the communication and data acquisition layer of the AI-Enabled Photovoltaic Monitoring and Fault Detection System using Simulated UCT DAMS, MQTT, and Node-RED.

The primary objectives were to set up the Industrial IoT development environment, learn Node-RED fundamentals, create virtual photovoltaic sensors, simulate the functionality of a UCT DAMS platform, and establish MQTT-based communication between system components. Additionally, project documentation and version control practices were maintained through GitHub.

## II. Achievements

### 1. Development Environment Setup

- Successfully installed and configured Node-RED for Industrial IoT application development.
- Verified Mosquitto MQTT Broker configuration and connectivity.
- Organized the project repository structure on GitHub for systematic development and documentation.
- Added project README and Week 1 documentation to the repository.

### 2. Node-RED Familiarization

- Learned the functionality of core Node-RED nodes including:
  - Inject Nodes
  - Function Nodes
  - Debug Nodes
  - MQTT In Nodes
  - MQTT Out Nodes
- Developed and tested multiple introductory flows to understand event-driven data processing.
- Explored Node-RED deployment, debugging, and flow export mechanisms.

### 3. Virtual Photovoltaic Sensor Development

- Developed a photovoltaic sensor simulator using Node-RED Function Nodes.
- Implemented realistic generation of solar plant parameters including:
  - Panel Voltage
  - Panel Current
  - Output Power
  - Panel Temperature
  - Solar Irradiance
  - Efficiency
- Configured automatic sensor data generation at regular intervals to simulate real-time photovoltaic system operation.
- Generated structured JSON-based sensor payloads for downstream processing.

### 4. Simulated UCT DAMS Implementation

- Designed and implemented a software-based simulation of a UCT DAMS platform.
- Developed a DAMS Processing Layer responsible for:
  - Data acquisition
  - Data validation
  - Data formatting
  - Health score calculation
  - Status monitoring
  - Fault classification
- Implemented system health assessment logic using operational parameters.
- Generated industrial-style monitoring messages containing:
  - Plant identifiers
  - Sensor identifiers
  - Health scores
  - Operational status
  - Fault information

### 5. MQTT Communication Integration

- Configured MQTT Publisher and Subscriber flows within Node-RED.
- Established successful communication using Mosquitto MQTT Broker.
- Created and tested MQTT topic architecture for photovoltaic monitoring.
- Published processed DAMS data to MQTT topics.
- Verified end-to-end data transfer between publishers and subscribers.
- Successfully demonstrated real-time industrial data communication using the MQTT publish-subscribe model.

### 6. GitHub Documentation and Version Control

- Maintained project progress using GitHub.
- Structured project directories for documentation, Node-RED flows, MQTT configurations, screenshots, and future AI modules.
- Exported and version-controlled Node-RED flow files.
- Documented MQTT topic structures and communication architecture.
- Uploaded screenshots and supporting materials for future reporting and presentations.

## III. Challenges

### 1. Understanding Industrial IoT Architecture

- Initially required additional study to understand the interaction between virtual sensors, DAMS platforms, MQTT brokers, and monitoring applications.
- Addressed the challenge through experimentation and incremental flow development.

### 2. Node-RED Flow Design

- Encountered challenges while organizing data flow between sensor simulation, processing, and communication modules.
- Improved understanding of message handling and payload management within Node-RED.

### 3. MQTT Configuration and Testing

- Required multiple iterations to verify successful message publishing and subscription.
- Learned MQTT topic management and communication debugging techniques.

## IV. Learning Resources

### 1. Node-RED Resources

- Official Node-RED Documentation
- Node-RED Community Examples
- Node-RED Dashboard Tutorials

### 2. MQTT Resources

- Mosquitto MQTT Documentation
- MQTT Publish-Subscribe Architecture Guides
- Industrial IoT Communication Tutorials

### 3. Photovoltaic Monitoring Resources

- Solar Plant Monitoring Concepts
- Industrial DAMS Architecture References
- IoT-Based Energy Monitoring Case Studies

## V. Next Week's Goals

### 1. Dashboard Development

- Develop a real-time photovoltaic monitoring dashboard using Node-RED Dashboard.
- Create gauges, charts, and status indicators for key plant parameters.

### 2. Historical Data Storage

- Implement data storage using JSON or SQLite databases.
- Store timestamped sensor records for future analysis and AI model training.

### 3. Alert and Threshold Monitoring

- Create threshold-based alert mechanisms.
- Generate warnings for:
  - Overheating
  - Low efficiency
  - Abnormal operating conditions

### 4. Visualization and Reporting

- Design graphical visualizations for voltage, current, power, and temperature trends.
- Develop an operator-friendly monitoring interface.

## VI. Additional Comments

This week marked the successful implementation of the core Industrial IoT communication framework for the project. The system can now generate realistic photovoltaic sensor data, process it through a simulated UCT DAMS layer, and transmit information using MQTT communication protocols.

The completed architecture successfully demonstrates the workflow of a modern industrial monitoring system and establishes a strong foundation for dashboard development, data storage, fault detection, AI analytics, and predictive maintenance modules planned for upcoming weeks.

**Current Working Architecture:**

```
Virtual PV Sensors
        ↓
Simulated UCT DAMS
        ↓
   MQTT Broker
        ↓
 MQTT Subscriber
        ↓
Real-Time Monitoring
```