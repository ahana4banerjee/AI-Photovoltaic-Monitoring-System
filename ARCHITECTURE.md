# System Architecture

# AI-Enabled Photovoltaic Monitoring and Fault Detection System

### Using Simulated UCT DAMS, MQTT and Node-RED

---

# 1. Architecture Overview

The AI-Enabled Photovoltaic Monitoring and Fault Detection System is designed as a software-based Industrial IoT platform that simulates the functionality of a real-world UCT DAMS (Data Acquisition and Monitoring System).

The architecture follows a layered Industrial IoT approach consisting of:

1. Data Generation Layer
2. Data Acquisition Layer
3. Communication Layer
4. Monitoring and Visualization Layer
5. Data Storage Layer
6. AI Analytics Layer
7. Alerting and Reporting Layer

The system continuously generates photovoltaic plant data, processes it through a simulated DAMS platform, transmits it using MQTT communication protocols, stores historical records, and performs intelligent fault detection and predictive maintenance analysis.

---

# 2. High-Level System Architecture

```text
┌──────────────────────────────┐
│      Virtual PV Sensors      │
│------------------------------│
│ Voltage                      │
│ Current                      │
│ Power                         │
│ Temperature                  │
│ Irradiance                   │
│ Efficiency                   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      Simulated UCT DAMS      │
│------------------------------│
│ Data Acquisition             │
│ Data Validation              │
│ Health Score Calculation     │
│ Fault Classification         │
│ Data Formatting              │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        MQTT Broker           │
│------------------------------│
│ Mosquitto MQTT               │
│ Publish/Subscribe Engine     │
└──────────────┬───────────────┘
               │
      ┌────────┴────────┐
      ▼                 ▼

┌───────────────┐   ┌───────────────┐
│ Node-RED      │   │ Data Storage  │
│ Dashboard     │   │ Layer         │
│ Visualization │   │ SQLite / JSON │
└───────┬───────┘   └───────┬───────┘
        │                   │
        └────────┬──────────┘
                 ▼

┌──────────────────────────────┐
│      AI Analytics Engine     │
│------------------------------│
│ Fault Detection              │
│ Health Assessment            │
│ Predictive Maintenance       │
│ Performance Analysis         │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│ Alerting & Reporting Layer   │
│------------------------------│
│ Dashboard Alerts             │
│ Fault Reports                │
│ Maintenance Suggestions      │
│ Business Intelligence        │
└──────────────────────────────┘
```

---

# 3. Layer-Wise Architecture

## Layer 1: Data Generation Layer

### Purpose

Simulates a photovoltaic power plant by generating realistic operating parameters.

### Parameters Generated

| Parameter    | Typical Range   |
| ------------ | --------------- |
| Voltage      | 420 – 470 V     |
| Current      | 8 – 15 A        |
| Temperature  | 30 – 65 °C      |
| Irradiance   | 200 – 1000 W/m² |
| Efficiency   | 80 – 98 %       |
| Power Output | Calculated      |

### Implementation

* Node-RED Function Nodes
* Periodic sensor simulation
* JSON payload generation
* Real-time data stream creation

---

## Layer 2: Simulated UCT DAMS Layer

### Purpose

Acts as a software replica of an industrial DAMS platform.

### Responsibilities

* Sensor data acquisition
* Data validation
* Timestamp management
* Health score generation
* Fault classification
* Data aggregation
* Message formatting

### Generated Metadata

```json
{
  "plant_id": "PV_PLANT_001",
  "sensor_id": "PV_ARRAY_01",
  "health_score": 95,
  "status": "Normal",
  "fault_type": "None"
}
```

---

## Layer 3: MQTT Communication Layer

### Purpose

Provides lightweight industrial communication between system components.

### Protocol

MQTT Publish/Subscribe

### Broker

Mosquitto MQTT

### Topics

```text
solar/full_data
solar/voltage
solar/current
solar/power
solar/temperature
solar/efficiency
```

### Advantages

* Low bandwidth
* Scalable architecture
* Real-time communication
* Industrial IoT standard

---

## Layer 4: Monitoring and Visualization Layer

### Purpose

Provides real-time operational visibility.

### Dashboard Components

* Voltage Gauge
* Current Gauge
* Temperature Gauge
* Power Monitoring
* Efficiency Tracking
* Health Status Indicator
* Fault Status Panel

### Technology

* Node-RED Dashboard

---

## Layer 5: Data Storage Layer

### Purpose

Stores historical plant data for analytics and machine learning.

### Stored Parameters

* Timestamp
* Voltage
* Current
* Power
* Temperature
* Irradiance
* Efficiency
* Health Score
* Fault Status

### Technologies

* SQLite
* JSON Storage

---

## Layer 6: AI Analytics Layer

### Purpose

Performs intelligent monitoring and fault detection.

### Input Features

* Voltage
* Current
* Power
* Temperature
* Irradiance
* Efficiency

### AI Tasks

* Fault Detection
* Health Assessment
* Performance Degradation Analysis
* Predictive Maintenance

### Target Fault Classes

| Fault Type             | Description                    |
| ---------------------- | ------------------------------ |
| Normal                 | Healthy Operation              |
| Overheating            | Excessive Temperature          |
| Efficiency Degradation | Reduced Performance            |
| Partial Shading        | Irradiance Loss                |
| Electrical Fault       | Abnormal Electrical Conditions |

### Technology

* Python
* Scikit-Learn
* Pandas
* NumPy

---

# 4. Data Flow Architecture

```text
Sensor Generation
        │
        ▼
Virtual PV Sensors
        │
        ▼
Simulated UCT DAMS
        │
        ▼
MQTT Publisher
        │
        ▼
Mosquitto Broker
        │
        ▼
MQTT Subscriber
        │
        ▼
Dashboard & Database
        │
        ▼
AI Analytics
        │
        ▼
Alerts & Reports
```

---

# 5. Fault Detection Workflow

```text
Sensor Data
      │
      ▼
Feature Extraction
      │
      ▼
Health Assessment
      │
      ▼
Fault Classification
      │
      ▼
Alert Generation
      │
      ▼
Maintenance Recommendation
```

---

# 6. Repository Architecture

```text
AI-Photovoltaic-Monitoring-System/
│
├── docs/
│   ├── architecture/
│   ├── weekly_reports/
│   └── screenshots/
│
├── node_red/
│   ├── basic_learning_flow.json
│   ├── pv_sensor_simulator.json
│   ├── simulated_dams_flow.json
│   ├── mqtt_publish_flow.json
│   └── mqtt_subscribe_flow.json
│
├── mqtt/
│   └── topic_structure.md
│
├── dashboard/
│
├── database/
│
├── datasets/
│
├── ai_model/
│
├── presentation/
│
└── README.md
```

---

# 7. Future Architecture Enhancements

## Cloud Integration

* AWS IoT Core
* Azure IoT Hub
* Google Cloud IoT

## Advanced Analytics

* Deep Learning Models
* Time-Series Forecasting
* Remaining Useful Life Prediction

## Notifications

* Email Alerts
* Telegram Alerts
* SMS Notifications

## Digital Twin

* Virtual Solar Farm Replica
* Real-Time Asset Simulation

## Multi-Plant Monitoring

* Centralized Monitoring of Multiple PV Sites

---

# 8. Expected Outcome

The completed system will function as a fully software-based Industrial IoT photovoltaic monitoring platform capable of real-time sensor simulation, DAMS-based data acquisition, MQTT communication, dashboard visualization, historical data management, AI-powered fault detection, predictive maintenance analysis, and operational decision support.
