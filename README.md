# Planner
https://github.com/users/Katukiii/projects/3

# Minecraft Biome Lights
A minecraft project that make an LED glow different colors depending on where your player resides!

# How it works:
This project runs on a nodered server. It uses minecraft nodes (see https://flows.nodered.org/node/@tomsith/node-red-contrib-minecraft/ for all the different nodes used for this project) to pin-point what biome the player is currently in.

Moving around different biomes in Minecraft will set different color values onto the LED strip.
All biomes are affected and have different color values.


# 🌍 Minecraft Biome Distance Dashboard & LED Visualizer

A Node-RED dashboard that visualizes distances to Minecraft biomes in real-time and synchronizes biome proximity with LED strip animations. Designed for RCON-connected Minecraft servers.

---

## 🧭 Features

- 📊 **Dashboard Display**  
  Interactive UI with biome-specific distance data, updated in real-time per dimension.

- 🎨 **Biome-Themed LED Strip**  
  LED strip reacts dynamically to the nearest biome, using colors and effects unique to each environment.

- 🔄 **Automatic Dimension Switching**  
  Clears old biome data and resets visuals when switching dimensions (e.g., Overworld → Nether).

- ❌ **Per-Biome Removal**  
  Easily remove any biome from the dashboard via in-line buttons.

- 🧹 **Clean and Sorted UI**  
  Biomes are listed in order of distance for a clearer view of proximity priorities.

---

## 💡 Example Output

![Dashboard Example](example-dashboard.png)

---

## 🛠 Requirements

- Minecraft Java Edition server with **RCON** enabled
- [Node-RED](https://nodered.org/) installed and running
- Node-RED dashboard nodes installed
- Optional: LED strip controlled via MQTT, ESP8266/ESP32 or Raspberry Pi
- Biome scan commands (e.g. `/locate biome`) triggered via Node-RED inject or automation

---

## 🔧 Setup Instructions

### 1. Install Node-RED Dashboard Nodes

Make sure the dashboard nodes are installed in Node-RED:

```bash
cd ~/.node-red
npm install node-red-dashboard


