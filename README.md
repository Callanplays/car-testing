# Car Testing

An experimental vehicle controller built entirely in Hypixel Housing with
[HTSW](https://legendarygames.dev/htsw/).

The project turns normal player movement into a small driving system with
acceleration, braking, steering, drifting, ramps, crash feedback, rendered
wheels, and an in-game HUD. It is also a practical experiment in building
real-time movement and physics-like behavior within Housing's action system.

## Features

- Speed-sensitive acceleration, drag, and engine braking
- View-directed steering with separate forward and lateral velocity
- Grip, drift entry, drift recovery, and braking behavior
- Ramp and airborne handling
- Collision detection with rebound and crash feedback
- Four-wheel visualization using dropped items
- HUD indicators for throttle, steering, grip, braking, speed, and crashes
- Debug readout for tuning the controller in game

## Controls

The import includes two custom items:

| Item | Action |
| --- | --- |
| **Toggle Car** | Right-click to enable or disable the vehicle controller |
| **Car Controls** | Right-click to accelerate; left-click repeatedly to brake |

Look where you want to steer while the controller is enabled.

## How it works

`Runner` is a repeating Housing function that advances the simulation in
several smaller steps. Each update calculates the player's desired heading,
applies throttle and braking, separates forward movement from sideways slip,
updates traction or drifting, detects ramps and collisions, and finally writes
the result back through player velocity.

Housing variables hold the vehicle's state between updates. The constants in
`functions/set_constants.htsl` are the main tuning surface for acceleration,
drag, grip, drift, ramp, and crash behavior.

## Project structure

```text
.
├── import.json             # Root HTSW import
├── functions/
│   ├── import.json         # Function declarations
│   ├── Runner.htsl         # Repeating simulation loop
│   ├── set_constants.htsl  # Handling and physics tuning
│   └── ...
└── items/
    ├── import.json         # Custom control items
    ├── *.snbt              # Item definitions
    └── *.htsl              # Click actions
```

## Importing

1. Install [HTSW](https://legendarygames.dev/htsw/) and its in-game module.
2. Clone this repository into your HTSW projects directory.
3. Validate the project from this directory:

   ```sh
   htsw check import.json
   ```

4. In Minecraft, stand in the Housing plot where you want the system and
   import the root `import.json` through HTSW.
5. Use the imported **Toggle Car** and **Car Controls** items to drive.

This is an experimental Housing project, so it is best imported into a test
house before being integrated into a larger game.
