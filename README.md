# Ants vs Bees: Tower Defense Game

[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)]() [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]()

A Python implementation of an ant-colony tower defense game: place different ant types to defend against waves of invading bees, with turn-based simulation and simple enemy AI.

> **Academic Integrity / Original Source Note**
>
> This project was completed in Fall 2021 at **UC Berkeley** for CS 61A: The Structure and Interpretation of Computer Programs. It is published for portfolio/educational purposes only — please do not reuse in active coursework.
---

## 🐜 Overview

Two sides: an **ant colony** defends a path of connected places, while **bees** spawn from the hive and march toward the colony base.
* Each turn:
  * You spend available **food** to place new ants on empty tiles.
  * All ants act once (e.g., generate food, throw leaves at bees, block damage, support other ants).
  * All bees then move one step forward, or sting an ant if they are blocked.
* Win / Lose conditions:
  * You **win** if all bees are defeated before any of them reach the colony base.
  * You **lose** immediately if a bee makes it all the way to the colony base.
* Key mechanics:
  * Each ant type has a **food cost**, **health**, and a unique **action** each turn.
  * Some ants generate food, some attack at range, some act as tanks or protect other ants in the same place.
  * Bees constantly spawn and advance, so you must choose **which ants to buy** and **where to place them** to survive later waves.

---

## 📁 Repository Layout & Naming

```
./ants.py        # Core game logic (GameState, Place, Insect/Ant/Bee, turn rules)  
./ants_gui.py    # Legacy GUI entry point (older interface, optional)  
./gui.py         # Main GUI entry point (browser-based GUI)  
./graphics.py    # Simple 2D graphics utilities for the GUI  
./state.py       # Game state wrapper used by gui.py  
./utils.py       # General helper/utility functions  
./ucb.py         # Small utility helpers (logging, argument parsing, etc.)  
./assets/        # Images & other assets used by gui.py  
./img/           # Images used by ants_gui.py  
```
---

## ▶️ Quick Start

```
Text-based version (depending on how you keep the entrypoint):

    python3 ants.py

Graphical version (recommended):

    python3 gui.py

Then open the link shown in the terminal (if it doesn’t open automatically) and start placing ants to defend against the bees.
```
---
