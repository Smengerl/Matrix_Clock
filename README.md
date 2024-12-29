# LED Matrix Retro Clock

A retro style clock with matrix LED display using an ESP32 microcontroller with automatic NTP time sync.

Renderings / Prototype:
| Front                                                | Back                                                 | Isometric |
| ---------------------------------------------------- | ---------------------------------------------------- | --------- |
| <img src="./print/rendering/fully_assembled_front.png" alt="front"/> | <img src="./print/rendering/fully_assembled_back.png" alt="back"/>   | <img src="./print/rendering/fully_assembled_iso.png" alt="iso"/> |


## Features

- Displays the current time in HH:MM format
- 4 Digit LED matrix display (8x8 pixel)
- Customizable animations, dimming and 
- Automatic time synchronization using NTP

## Hardware Requirements

- ESP32 (housing designed for USB C version)
- 4 digit 8x8 LED matrix display based on MAX7219 (FC16)

## Software Requirements

- PlatformIO
- MD_Parola (via PIO)
- ESPDateTime (via PIO) 
- WiFiManager (via PIO)

## Mechanics

The only mechanical part required is the housing which consists of a front and a back piece.

You can optionally ad

### 3D-Printed Parts

| Filename                     | Thumbnail                                                           | Required | Notes |
| ---------------------------- | --------------------------------------------------------------------| -------- | ------|
| `./print/front.stl`          | <img src="./print/rendering/front.png" alt="front" width="300"/>    | 1        | |
| `./print/back.stl`           | <img src="./print/rendering/back.png" alt="back" width="300"/>      | 1        | |

Printer settings:
- All printed parts designed for PETG. 
- Best experience on my printer was to print the front upside down (the actual front of the case facing the print bed) as this does not require any supports. For a cleaner look you can consider to print it reversed with ironing enabled but note that this requires a lot of support material. 
- Using fuzzy skin for all outside walls creates a nice touch
- No rafts/brim etc. reguired for any model.

### Required parts

| Name              | Spec                          | Required | Notes |
| ----------------- | ----------------------------- | -------- | ------|
| countersunk screw | M3 5mm, e.g. DIN EN ISO 4762  | 4        | To attach ESP to back of housing |
| countersunk screw | M3 10mm, e.g. DIN EN ISO 4762 | 4        | To attach display to back of housing |
| countersunk screw | M3 10mm, e.g. DIN EN ISO 4762 | 4        | To fix back and front of housing |
| semi-transparent acrylic board | max 2mm, 140-150mm * 33-35mm | 1        | Optional, for cleaner look |

### Assembly

- All electronics are screwed to the back of the housing.
- The acrylic plate is glued to the front.
- Finally the front of the housing is snapped into the back and tightened via the screws from the back.

![assembly](./print/rendering/assembly.gif)



## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/Matrix_Clock.git
2. Open the project in PlatformIO.
3. Wait for PIO to configure and download the required libraries
4. Compile and upload the project to your ESP32 microcontroller.


## Usage
- Power on the ESP32.
- On first usage only: Configure the ESP to your local WiFi. For this, connect to the ESP's access point and use the default configuration page to enter your WLAN SSID and password 
- Wait for NTP sync
- The current time will be displayed on the LED matrix.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
MD_Parola library by MajicDesigns
