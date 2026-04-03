# Automotive Turn Signals - FPGA

A finite state machine (FSM) implemented in VHDL on a Basys 3 FPGA board, simulating an automotive turn signal system.

## Description

The project models the behavior of car turn signals using a synchronous FSM. The system takes switch inputs and drives LED outputs to simulate left turn, right turn, hazard lights, and upper signals.

## Features

- Left and right turn signals with sequential LED activation
- Hazard lights with 3-stage animation
- Upper left and upper right signal modes
- Frequency divider for timing control
- Reset functionality

## States

| State | Description |
|-------|-------------|
| idle | No signal active |
| LAon / LALBon / LALBLCon | Left turn signal stages |
| RAon / RARBon / RARBRCon | Right turn signal stages |
| HAZARD1 / HAZARD2 / HAZARD3 | Hazard light stages |
| LEFT_UP_SIG / RIGHT_UP_SIG | Upper signal modes |

## State Transition Diagram

The following diagram illustrates the finite state machine transitions between the idle state, turn signal states, and hazard light stages.

<p align="center">
  <img src="transitions-diagram.jpg" width="650">
</p>

## Inputs

| Switch | Function |
|--------|----------|
| sw(0) | Hazard lights |
| sw(1) | Left turn signal |
| sw(2) | Right turn signal |
| sw(3) | Upper left signal |
| sw(4) | Upper right signal |

## Technologies

- VHDL
- Vivado Design Suite
- Basys 3 FPGA board

## Authors

- Fit Nicolae
- Vultur Cristian
