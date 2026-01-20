# 4D Three-Target Challenge

A browser-based 4D navigation game where players explore a four-dimensional space and capture three target points located along different axes.

## Overview

This is an interactive visualization of 4D space rendered onto a 2D screen using linear projection. Players navigate using first-person controls and must reach three targets positioned at coordinates along the X, Z, and W axes.

## Features

- **4D Space Navigation**: Move through X, Z, and W dimensions with intuitive controls
- **Linear 4D Projection**: Mathematically accurate projection from 4D to 2D using additive depth calculation
- **Touch Controls**: Dual virtual joysticks optimized for mobile devices
  - Left joystick: Movement (X/Z plane)
  - Right joystick: Camera rotation (Yaw and 4D Pitch)
  - W+/W- buttons: Movement along the fourth dimension
- **Collision System**: Boundary walls and obstacle cubes with collision detection
- **Target Tracking**: Real-time distance display to each of the three objectives
- **Visual Feedback**: Screen edge glow effect when hitting boundaries

## Controls

| Control | Action |
|---------|--------|
| Left Joystick | Move forward/backward and strafe |
| Right Joystick | Rotate camera (Yaw) and 4D view angle (Pitch4D) |
| W+ Button | Move in positive W direction |
| W- Button | Move in negative W direction |
| Wall Toggle | Enable/disable wall obstacles |
| Reset | Return to starting position |

## Game Objective

Capture all three targets by moving within 0.8 units of each:

1. **TARGET X** (Red) - Located at X=5.0
2. **TARGET Z** (Yellow) - Located at Z=5.0
3. **TARGET W** (Cyan) - Located at W=5.0

## Technical Details

- Pure HTML5/CSS/JavaScript implementation (no dependencies)
- Canvas-based rendering with device pixel ratio support
- Linear depth projection formula: `Depth = Z' + W' + offset`
- 4D rotation using combined Yaw (XZ) and Pitch4D (ZW) transformations
- Grid-based floor with 0.5 unit spacing in XZ and 1.5 unit spacing in W
- Boundary limits: -6.0 to +6.0 on all navigable axes

## Usage

Open `index.html` in any modern web browser. Works best on mobile devices with touch support, but also functions with mouse input on desktop.

## License

MIT
