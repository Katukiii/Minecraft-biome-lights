# 🌍 Minecraft Biome Distance Dashboard & LED Visualizer

A Node-RED project that visualizes distances to Minecraft biomes in real-time and synchronizes biome proximity with LED strip animations. Designed for RCON-connected Minecraft servers.

---

## 🧭 Features

- 📊 **Dashboard Display**  
  Interactive UI with biome-specific distance data, updated in real-time.

- 🎨 **Biome-Themed LED Strip**  
  LED strip reacts dynamically to the nearest biome, using colors unique to each environment.
  
- 🧹 **Clean and Sorted UI**  
  Biomes are listed in order of distance for a clearer view of proximity priorities.

---

## 💡 Example Output

![eeeoeoeo](https://github.com/user-attachments/assets/af344263-2b68-445a-8a7c-304e8d6be85e)


---

## 🛠 Requirements

- Minecraft Java Edition server with **RCON** enabled
- [Node-RED](https://nodered.org/) installed and running
- Node-RED dashboard nodes installed
- Node-RED minecraft nodes installed (see setup instructions for the download command OR do manually in NodeRed (@tomsith/node-red-contrib-minecraft))
- 16 Lights LED strip controlled via MQTT (see flow for MQTT node)

---

## 🔧 Setup Instructions

### 1. Install Node-RED Dashboard and Minecraft Nodes

Make sure the dashboard and minecraft nodes are installed in Node-RED:

```bash
cd ~/.node-red
npm install node-red-dashboard
npm install @tomsith/node-red-contrib-minecraft
```

### 2. Install the required flow

Make sure to donwload the flow. The flow is called 'BiomeLightsFlow'.

![{7E23CCC2-8958-48E2-8C47-D40DCD002F7F}](https://github.com/user-attachments/assets/93a833b9-51b5-4356-9cdf-96b6c7b7148d)

### 3. Import flow in your Raspberry Pi or PC Nodered

Import the BiomeLightsFlow in your NodeRed. 

#### IMPORTANT! Change Inject, RCON and MQTT node

Your username on minecraft needs to be inside of the inject node and your server should be in the RCON node. Your MQTT server should be set to your MQTT server aswell.
Note that you can customise which biomes the program can detect in the Overworld, Nether and End biomes nodes. Just put // before the biome name in order to remove that biomes' name from scanning.

---

## 🧠 How It Works

The server sends a message like:
The nearest minecraft:crimson_forest is at [123, 64, 789] (422 blocks away).
Node-RED parses the biome name and distance.
The dashboard shows:
  - Biome name (e.g. crimson forest)
  - Distance (422 blocks)
  - Last scanned time

LED strip updates based on the closest biome with colors.
Forest is green, desert is yellow, ocean is blue, and so on.

#### IMPORTANT!

This project ONLY works with an LED strip consisting of 16 Lights EXCEPT if you change the 'Biome to LED Lights' nodes' amount to your desired amount (line 146 inside the function node code).

---

## 🧾 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 📌 Credits

https://flows.nodered.org/node/@tomsith/node-red-contrib-minecraft/#configuration
Minecraft nodes used in this project.
