# LedCube 20x20x20 PET Project

This is my Hobby Project (LED CUBE 20x20x20 public repository)

## Roadmap

- [X] Buy all required components  
- [X] Created schematic ( used schema where cathodes by columns and anodes for layers)
- [X] Created a wooden template for soldering 1x20Led line using a CNC machine (16mm between via)
- [X] Created a wooden template for soldering 5x Lines using a CNC machine
- [X] Created a wooden stand with bottom vias using a CNC machine
- [X] Cathode cascade PCB schematic (In Production)
- [X] Anode cascade PCB schematic (In Production)
- [X] Setup project and write BLINK project used I2C and shift registers to the microcontroller
- [ ] 6000x8000 Soldering
- [ ] 3/20 Installing 20x20 sides to stand
- [ ] Connect anode  cascade and tests it (delivery )
- [ ] Connect cathode  cascade and tests it (delivery )
- [ ] Create or adopt LCD font for 20x20 dimension  (Glyph fonts required) write Python script to convert  ASCII fonts  to binary matrix format
- [ ] Write test snowfall program 
- [ ] Animations
- [ ] Add WiFi module and write mobile App for device control


---- 

## Components:
 - 1x STM32F103 Microcontroller
 - 1x 220v -5V8A AC/DC power supply
 - 8000x 3.3V 50mA Blue LED 
 - 53x 74HC595 Shift Registers (Placed at 11PCB connected successively)
 - 400x 220Om registers
 
---- 

## Notes

### About Cathode Shift registers PCB cascade

![3D View](https://github.com/iborysenko/LedCube/blob/main/LED_cube%20cathode%20cascade%203D%20view.png?raw=true)
![Schematic](https://github.com/iborysenko/LedCube/blob/main/LED_cude%20cathode_cascade.png?raw=true)

This is led cube cathode shift registers cascade schematic

We need 10pts connected successively to shift the I2C signal from the microcontroller.

PCB has 40data out PINs to connect 2x20 Led Columns SHIFT side must be connected to the INPUT side of another PCB to perform data SHIFT

I will use a +5V8A power supply therefore I will use 220 Om registers to save my Led-rows

Why PCB has a 100x50mm size?

because my stand has 220x220x70mm size and I need a place to contain Microcontroller and AC/DC power supply
