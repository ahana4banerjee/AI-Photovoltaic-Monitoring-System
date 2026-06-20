# AI-Enabled Photovoltaic Monitoring and Fault Detection System

A software-based Industrial IoT project that simulates a UCT DAMS-style photovoltaic monitoring system using Node-RED, MQTT, a database layer, dashboard visualization, and AI-based fault detection. [1]

## Overview

This project simulates a solar plant monitoring environment without requiring physical DAMS hardware. It generates virtual sensor data, transmits it through MQTT, stores historical records, visualizes live plant status, and applies AI analytics for fault detection and maintenance insights. [1]

## Problem Statement

Solar farms face performance loss and maintenance challenges due to environmental effects, equipment faults, and delayed manual monitoring. This project addresses those issues with a real-time software monitoring and analytics pipeline. [1]

## Objectives

- Simulate an industrial DAMS platform for photovoltaic monitoring. [1]
- Generate virtual solar sensor data. [1]
- Implement MQTT-based data communication. [1]
- Build a Node-RED dashboard for live monitoring. [1]
- Store historical data for analysis. [1]
- Detect system faults using AI. [1]

## Features

- Virtual sensor simulation for voltage, current, power, temperature, and efficiency. [1]
- Simulated DAMS data acquisition and processing. [1]
- MQTT publish/subscribe communication flow. [1]
- Live dashboard with gauges, charts, status indicators, and alerts. [1]
- Historical data storage for analytics and model training. [1]
- AI-based detection of dust accumulation, shading, overheating, degradation, and electrical faults. [1]
- Alert generation for abnormal operating conditions. [1]

## System Architecture

```text
Virtual Solar Sensors
        |
        v
Simulated UCT DAMS
        |
        v
   MQTT Broker
        |
        v
Node-RED Processing
    |         |
    v         v
Dashboard   Database
      \     /
       v   v
    AI Analytics
        |
        v
  Fault Detection
        |
        v
 Alert Generation
        |
        v
Business Intelligence
```

Architecture adapted from the project plan. [1]

## Parameters Monitored

### Electrical
- Panel voltage [1]
- Panel current [1]
- Output power [1]
- Energy generated [1]

### Environmental
- Panel temperature [1]
- Ambient temperature [1]
- Solar irradiance [1]
- Humidity [1]

### Performance
- Efficiency [1]
- Performance ratio [1]
- Energy loss [1]
- Plant utilization [1]

### AI Metrics
- Fault probability [1]
- Maintenance score [1]
- Health index [1]
- Predicted failure time [1]

## Tech Stack

| Component | Purpose |
|---|---|
| Node-RED | Sensor simulation and workflow logic [1] |
| Mosquitto MQTT | Device communication [1] |
| SQLite / JSON | Data storage [1] |
| Python | AI model development [1] |
| Node-RED Dashboard | Visualization [1] |
| GitHub | Project hosting and submission [1] |

## Workflow

1. Generate realistic virtual sensor readings. [1]
2. Process the readings through a simulated UCT DAMS layer. [1]
3. Publish data to MQTT topics. [1]
4. Store sensor values for historical analysis. [1]
5. Display live system metrics and alerts on the dashboard. [1]
6. Run AI models to identify probable faults and maintenance needs. [1]

## Fault Detection Targets

The AI module is intended to classify system conditions such as:

- Normal operation [1]
- Dust accumulation [1]
- Partial shading [1]
- Overheating [1]
- Electrical fault [1]

## Expected Output

The final system is expected to provide real-time monitoring, dashboard visualization, MQTT-based communication, historical data storage, AI-driven fault detection, predictive maintenance support, and business intelligence style reporting in a fully software-simulated environment. [1]

## Future Enhancements

- Cloud integration with platforms such as AWS IoT, Azure IoT, or Google Cloud IoT. [1]
- Mobile-based remote monitoring. [1]
- Email, Telegram, or SMS alerts. [1]
- Weather API integration. [1]
- Digital twin implementation. [1]
- Advanced AI and multi-plant monitoring. [1]

## Repository Structure

```text
AI-Photovoltaic-Monitoring-System/
├── NodeRED/
├── MQTT/
├── Dashboard/
├── Database/
├── AI_Model/
├── Dataset/
├── Documentation/
├── Weekly_Reports/
└── Final_Report/
```