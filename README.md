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


### 🧠 How It Works

    The server sends a message like:

    The nearest minecraft:crimson_forest is at [123, 64, 789] (422 blocks away).

    Node-RED parses the biome name, distance, and attaches the dimension (nether/overworld/end).

    The dashboard shows:

        Biome name (e.g. crimson forest)

        Distance (422 blocks)

        Last scanned time

    If the dimension changes, all prior biome data is cleared to avoid stale readings.

    LED strip updates based on the closest biome with unique effects and colors.

## 🎨 Example Biome Colors
**Biome**	        **LED Color**
warped_forest	    #00ffff	
crimson_forest	  #ff0033	
nether_wastes	    #ff6600	
basalt_deltas	    #999999	
soul_sand_valley	#c9b79c	
