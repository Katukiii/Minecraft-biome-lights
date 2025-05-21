# 🌍 Minecraft Biome Distance Dashboard & LED Visualizer

A Node-RED project that visualizes distances to Minecraft biomes in real-time and synchronizes biome proximity with LED strip animations. Designed for RCON-connected Minecraft servers.

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

---

## 🧠 How It Works

The server sends a message like:
The nearest minecraft:crimson_forest is at [123, 64, 789] (422 blocks away).
Node-RED parses the biome name, distance, and attaches the dimension (nether/overworld/end).
The dashboard shows:
  - Biome name (e.g. crimson forest)
  - Distance (422 blocks)
  - Last scanned time
LED strip updates based on the closest biome with colors.
Forest is green, desert is yellow, ocean is blue, and so on.

---

## License

MIT License

Copyright (c) 2025 Katuki

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
