---
title: 'Whack-A-Mole-Game with VHDL on Basys3 Board'
collection: projects
date: 2021-01-01
permalink: /projects/whack-a-mole-game/
---

The primary goal of this project is to develop a digital game, Whack-A-Mole, using a VGA connector and a BASYS3 FPGA. The project aims to enhance digital design abilities, focusing on debugging, glitch removal, and the implementation of sequential and combinatorial design elements to create a glitch-free game.

## Design Specifications:

- Components used: BASYS3 FPGA, VGA monitor, VGA cable, mini-breadboard, buzzer, jumper cables.
- Game concept: Adaptation of the classic arcade game Whack-A-Mole, where players hit moles (represented by colored squares) to score points.
- Game mechanics: Players gain points by hitting moles and lose points for errors. The game features two difficulty levels (easy and hard), sound effects using a buzzer, and a game clock.

## Methodology:

- VGA_TOP: Main module connecting all submodules, setting the screen saver using a multiplexer.
- Clock Divider and Random Clock Divider: Generate desired clocks from the BASYS3’s built-in clock.
- VGA_640x480: Creates horizontal and vertical count signals and sync signals for the monitor.
- Game Buzzer: Generates a beep sound when buttons are pressed.
- Whack-A-Mole Module: Controls the game process using a Moore FSM with states for game start, gameplay, and game over.
- Push Release: Detects changes in button states to avoid repetition errors.
- Main Game Screen: Draws squares on the display and handles their blinking effect.
- Game Clock: Displays the time elapsed since the start of the game using FSMs.
- Game Mode: Displays the game mode and score on the screen.
- Character Placer and Alnum: Place alphanumeric characters and symbols on the screen.
- Game Sounds: Displays the audio status on the screen.
- Score Count: Manages the game score and determines game over conditions.
- LFSR4: Generates random numbers for the game.
- Game End/Begin: Displays the start and end screens using word selectors and multiplexers.


[Github Repository of the Project](https://github.com/tarhanefe/bilkent-ee102?tab=readme-ov-file#project)
