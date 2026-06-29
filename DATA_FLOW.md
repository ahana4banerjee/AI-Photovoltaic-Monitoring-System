# System Data Flow

## Overview

The project follows a modular Industrial IoT architecture where telemetry flows sequentially through multiple processing stages before reaching the end user.

---

# Complete Pipeline

Virtual PV Sensors

↓

Simulated UCT DAMS

↓

MQTT Publisher

↓

Mosquitto MQTT Broker

↓

Node-RED Subscriber

↓

┌───────────────────────────────┐
│                               │
│ Dashboard Visualization        │
│                               │
├───────────────────────────────┤
│                               │
│ SQLite Historical Database     │
│                               │
├───────────────────────────────┤
│                               │
│ Rule-Based Fault Detection     │
│                               │
└───────────────────────────────┘

---

# Step 1 – Sensor Simulation

The photovoltaic plant is simulated using Node-RED function nodes.

Generated parameters include:

- Voltage
- Current
- Power
- Temperature
- Irradiance
- Efficiency
- Health Score
- Status
- Fault Type

---

# Step 2 – MQTT Communication

Telemetry is published through:

Topic

```

solar/full_data

```

Each MQTT message contains the complete plant telemetry as a JSON object.

---

# Step 3 – Dashboard

The dashboard receives MQTT telemetry and updates:

- Gauges
- Trend Charts
- Status Indicators

---

# Step 4 – Historical Storage

The same telemetry packet is simultaneously stored inside SQLite.

This creates a historical dataset for future analysis.

---

# Step 5 – Fault Monitoring

Incoming telemetry is evaluated against predefined thresholds.

Possible outputs include:

- Normal
- Warning
- Critical

These alerts are displayed on the dashboard in real time.

---

# Current Architecture

Virtual Sensors

↓

MQTT

↓

Node-RED

↓

Dashboard

↓

SQLite

↓

Rule-Based Alerts

---

# Future Architecture

Week 4

↓

AI Fault Detection

↓

Fault Classification

↓

Predictive Maintenance

↓

Business Intelligence