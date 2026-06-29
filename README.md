# AI-Enabled Photovoltaic Monitoring and Fault Detection System

A software-based Industrial IoT project that simulates a UCT DAMS-style photovoltaic monitoring system using Node-RED, MQTT, a database layer, dashboard visualization, and AI-based fault detection. 

## Overview

This project simulates a solar plant monitoring environment without requiring physical DAMS hardware. It generates virtual sensor data, transmits it through MQTT, stores historical records, visualizes live plant status, and applies AI analytics for fault detection and maintenance insights. 

## Problem Statement

Solar farms face performance loss and maintenance challenges due to environmental effects, equipment faults, and delayed manual monitoring. This project addresses those issues with a real-time software monitoring and analytics pipeline. 

## Objectives

- Simulate an industrial DAMS platform for photovoltaic monitoring. 
- Generate virtual solar sensor data. 
- Implement MQTT-based data communication. 
- Build a Node-RED dashboard for live monitoring. 
- Store historical data for analysis. 
- Detect system faults using AI. 

## Features

- Virtual sensor simulation for voltage, current, power, temperature, and efficiency. 
- Simulated DAMS data acquisition and processing. 
- MQTT publish/subscribe communication flow. 
- Live dashboard with gauges, charts, status indicators, and alerts. 
- Historical data storage for analytics and model training. 
- AI-based detection of dust accumulation, shading, overheating, degradation, and electrical faults. 
- Alert generation for abnormal operating conditions. 

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

Architecture adapted from the project plan. 

## Parameters Monitored

### Electrical
- Panel voltage 
- Panel current 
- Output power 
- Energy generated 

### Environmental
- Panel temperature 
- Ambient temperature 
- Solar irradiance 
- Humidity 

### Performance
- Efficiency 
- Performance ratio 
- Energy loss 
- Plant utilization 

### AI Metrics
- Fault probability 
- Maintenance score 
- Health index 
- Predicted failure time 

## Tech Stack

| Component | Purpose |
|---|---|
| Node-RED | Sensor simulation and workflow logic  |
| Mosquitto MQTT | Device communication  |
| SQLite / JSON | Data storage  |
| Python | AI model development  |
| Node-RED Dashboard | Visualization  |
| GitHub | Project hosting and submission  |

## Workflow

1. Generate realistic virtual sensor readings. 
2. Process the readings through a simulated UCT DAMS layer. 
3. Publish data to MQTT topics. 
4. Store sensor values for historical analysis. 
5. Display live system metrics and alerts on the dashboard. 
6. Run AI models to identify probable faults and maintenance needs. 

## Fault Detection Targets

The AI module is intended to classify system conditions such as:

- Normal operation 
- Dust accumulation 
- Partial shading 
- Overheating 
- Electrical fault 

## Expected Output

The final system is expected to provide real-time monitoring, dashboard visualization, MQTT-based communication, historical data storage, AI-driven fault detection, predictive maintenance support, and business intelligence style reporting in a fully software-simulated environment. 

## Future Enhancements

- Cloud integration with platforms such as AWS IoT, Azure IoT, or Google Cloud IoT. 
- Mobile-based remote monitoring. 
- Email, Telegram, or SMS alerts. 
- Weather API integration. 
- Digital twin implementation. 
- Advanced AI and multi-plant monitoring. 

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