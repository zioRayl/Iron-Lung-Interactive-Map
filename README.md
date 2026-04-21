# Iron Lung Navigator - AT-5 Trench

A lightweight interactive web page for navigating the **AT-5 Trench** map from **Iron Lung**.

This tool lets you open the map in a browser, set your current position, choose a destination directly on the map, and get the heading you need to steer toward that point.

It is designed to work entirely **offline** as a local HTML file, and it can also be uploaded to simple static hosting services such as **Altervista**.

## What this page is

This project is a browser-based navigation helper for the **AT-5 Trench** area.

It was made for players who want a practical way to:

- track their current coordinates
- place a destination on the map
- calculate the angle needed to move toward that destination
- use everything locally without requiring a server or installation

## Main features

- Interactive map
- Manual input for current **X** and **Y** coordinates
- Visual marker for the current position
- Destination selection by clicking on the map
- Heading / angle calculation toward the selected point
- Optional comparison with the current heading
- Multilingual interface:
  - Italian
  - English
  - French
  - Spanish
  - German
  - Russian
  - Chinese
- Fully usable offline
- Suitable for static hosting

## How it works

### Set your current position
You can set your current position in two ways:

1. Type your **X** and **Y** coordinates manually
2. Use **Right Click (R Click)** on the map to place your current position

Once set, your position is shown directly on the map.

### Select a destination
Use **Left Click (L Click)** on the map to choose the point you want to reach.

The selected destination is marked visually.

### Read the navigation data
After both points are set, the page calculates:

- destination coordinates
- direction from the current point to the target
- required heading / angle
- difference between your current heading and the required heading, if a current heading is provided

## Usage

### Run locally
No installation is required.

Just open the HTML file in any modern browser.

### Upload online
You can upload the HTML file directly to a static hosting service such as Altervista.

No backend, build step, or database is needed.

## Project files

Example structure:

```text
/
├── iron_lung_navigator_multilang_de.html
└── README_EN.md
```

## Important notes

- The current version calculates navigation in a **straight line** between the current position and the selected point.
- It does **not** currently perform pathfinding through trench corridors.
- It is intended as a navigation aid, not as an in-game automation tool.
