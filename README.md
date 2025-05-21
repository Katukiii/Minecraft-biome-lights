# 🌍 Minecraft Biome Distance Dashboard & LED Visualizer

A Node-RED dashboard that visualizes distances to Minecraft biomes in real-time and synchronizes biome proximity with LED strip animations. Designed for RCON-connected Minecraft servers.

---

## 🧭 Features

- 📊 **Dashboard Display**  
  Interactive UI with biome-specific distance data, updated in real-time per dimension.

- 🎨 **Biome-Themed LED Strip**  
  LED strip reacts dynamically to the nearest biome, using colors and effects unique to each environment.
  
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
- Optional: LED strip controlled via MQTT
- Biome scan commands (e.g. `/locate biome`) triggered via Node-RED inject or automation

---

## 🔧 Setup Instructions

### 1. Install Node-RED Dashboard Nodes

Make sure the dashboard nodes are installed in Node-RED:

```bash
cd ~/.node-red
npm install node-red-dashboard
```

### 2. Install the required flow

Make sure to donwload the flow. The flow is called 'BiomeLightsFlow'.
![{7E23CCC2-8958-48E2-8C47-D40DCD002F7F}](https://github.com/user-attachments/assets/93a833b9-51b5-4356-9cdf-96b6c7b7148d)



