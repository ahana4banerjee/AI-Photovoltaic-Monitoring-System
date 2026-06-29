**Weekly Progress Report**

Name: **Ahana Banerjee**

Domain: **Embedded Systems & IoT**

Date of submission: **30/06/2026**

**Week Ending:** **03**

**I. Overview:**

During Week 3, the primary objective was to transform the existing MQTT-based photovoltaic monitoring system into a complete industrial monitoring platform by developing a real-time visualization dashboard, implementing historical data storage, and integrating a rule-based fault monitoring system. The work focused on enhancing system usability through live dashboards, telemetry visualization, persistent database storage, and real-time alert generation.

**II. Achievements:**

**1\. Industrial Dashboard Development**

- Successfully developed a professional monitoring dashboard using FlowFuse Dashboard 2.
- Designed a structured dashboard layout with dedicated sections for:
  - Electrical Parameters
  - Environmental Parameters
  - Performance Parameters
- Integrated live gauges for:
  - Panel Voltage
  - Current
  - Output Power
  - Temperature
  - Efficiency
- Configured dashboard widgets to display live MQTT telemetry updates in real time.

**2\. Real-Time Trend Visualization**

- Added live trend charts for continuous monitoring of system behaviour.
- Implemented individual line charts for:
  - Voltage
  - Current
  - Power
  - Temperature
  - Efficiency
- Configured time-series visualization for continuous monitoring of parameter variations.
- Improved dashboard usability by allowing operators to observe system trends instead of only instantaneous values.

**3\. Historical Database Integration**

**Project:** AI-Enabled Photovoltaic Monitoring and Fault Detection System

- Integrated SQLite as the historical telemetry database.
- Created the telemetry database schema for storing sensor information.
- Configured Node-RED to automatically insert every incoming MQTT packet into the database.
- Stored the following telemetry fields:
  - Timestamp
  - Voltage
  - Current
  - Power
  - Temperature
  - Irradiance
  - Efficiency
  - Health Score
  - System Status
  - Fault Type
- Verified successful data persistence through SQL queries.

**4\. Rule-Based Fault Monitoring**

- Developed a threshold-based monitoring module using Node-RED Function nodes.
- Implemented real-time detection for abnormal operating conditions including:
  - Panel Overheating
  - High Voltage
  - Low Voltage
  - Efficiency Degradation
  - Poor Health Score
- Displayed system operating status dynamically as:
  - Normal
  - Warning
  - Critical
- Established the initial fault monitoring pipeline that will later be extended using AI models.

**III. Challenges:**

**1\. FlowFuse Dashboard Configuration**

- Faced initial challenges while configuring FlowFuse Dashboard 2 due to its architecture being different from the legacy Node-RED Dashboard.
- Resolved widget configuration, dashboard layout, and chart visualization issues through experimentation and iterative testing.

**2\. SQLite Integration**

- Encountered database insertion errors caused by missing table initialization and SQL query validation.
- Successfully created the telemetry schema and verified reliable insertion of live MQTT telemetry into the database.

**3\. Live Data Processing**

- Managed structured JSON telemetry packets by extracting individual parameters for dashboard visualization while simultaneously storing complete packets in SQLite.
- Optimized Node-RED flow design using parallel branches for visualization and database storage.

**IV. Learning Resources:**

**1\. FlowFuse Dashboard Documentation**

- Learned FlowFuse Dashboard 2 architecture.
- Explored dashboard widgets including gauges, charts, text widgets, and layout management.
- Understood dashboard organization using Pages and Groups.

**2\. SQLite Documentation**

- Studied SQLite database creation and schema design.
- Learned SQL operations including:
  - CREATE TABLE
  - INSERT
  - SELECT
- Understood persistent telemetry storage for Industrial IoT applications.

**3\. Node-RED Development**

- Improved understanding of:
  - Function nodes
  - MQTT message handling
  - JSON payload processing
  - Dashboard integration
  - Database connectivity
  - Rule-based automation

**V. Next Week's Goals:**

**1\. AI-Based Fault Detection**

- Generate and prepare datasets for machine learning.
- Train an AI model capable of identifying photovoltaic system faults.
- Integrate AI predictions into the existing monitoring pipeline.

**2\. Intelligent Monitoring Features**

- Replace rule-based fault monitoring with AI-assisted fault detection.
- Display predicted fault categories and confidence levels on the dashboard.
- Begin implementing historical fault analysis and alert logging using the stored SQLite telemetry.

**VI. Additional Comments**

Week 3 significantly improved the project by evolving it from a basic MQTT communication prototype into an industrial-style monitoring platform. The system now supports live visualization, persistent telemetry storage, and real-time operational monitoring, providing a strong foundation for AI-based analytics and predictive fault detection in the following development phase.