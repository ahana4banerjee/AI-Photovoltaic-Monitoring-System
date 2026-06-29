# Dashboard Documentation

## Overview

The project uses **FlowFuse Dashboard 2** to provide a real-time industrial monitoring interface for the simulated photovoltaic plant.

The dashboard receives telemetry from the MQTT broker through Node-RED and visualizes the current operating condition of the plant.

---

# Dashboard Structure

## Page

Overview

---

## Group 1 – Electrical

Monitored Parameters:

- Voltage (V)
- Current (A)
- Output Power (W)

Visual Components:

- Voltage Gauge
- Current Gauge
- Power Gauge
- Voltage Trend Chart
- Current Trend Chart
- Power Trend Chart

Purpose:

Provides real-time visualization of electrical characteristics of the photovoltaic array.

---

## Group 2 – Environmental

Monitored Parameters:

- Panel Temperature (°C)

Visual Components:

- Temperature Gauge
- Temperature Trend Chart

Purpose:

Tracks environmental conditions affecting panel performance.

---

## Group 3 – Performance

Monitored Parameters:

- Efficiency (%)

Visual Components:

- Efficiency Gauge
- Efficiency Trend Chart

Purpose:

Displays the operational efficiency of the simulated photovoltaic system.

---

## Live Updates

Dashboard values update automatically whenever new telemetry is published to the MQTT topic:

```

solar/full_data

```

---

## Features Implemented

- Real-time MQTT visualization
- Live gauges
- Time-series trend charts
- Industrial dashboard layout
- Automatic refresh
- Responsive interface

---

## Future Dashboard Enhancements

- Fault history table
- Alert log
- Plant health indicator
- Daily energy generation statistics
- AI prediction panel
- Predictive maintenance recommendations