# ESP32 Garage Control

## Intended use

This project is intended to add smarts to existing, traditional garage door openers operating on a DC motor. It is not intended to replace the existing garage door opener, as it doesn't include any provisions for motor control or safety. 

It is designed to be used with ESPHome, but the hardware part can equally well be used with classic Arduino or IDF-ESP code.

It was designed to be used with a Novoferm 413 drive, but it can probably be adapted to other drives quite readily.

The parts list provided is intended to mount it in a din rail enclosure, for other means of mounting it, you will have to adjust your shopping list accordingly

## Features

### Inputs

#### Native GPIO inputs

- Endstop closed
- Endstop open
- Action close
- Action open
- Action single-button

#### Isolated Inputs

Several inputs require isolation and/or level shifting, achieved by means of solid state relays

- Motor closing
- Motor opening
- "Door not closed" output of garage door opener

### Outputs

- Control output relay: Connect to single potential free control input of garage door opener

## Possibilty for expansion

Following ideas are currently not implemented, but would be possible

- Interdict output: If you have existing manual control switches connected in parallel, you may want to use one of the spare relays to operate the movement interdiction input of the garage door motor if external sensors indicate that the door should not move
