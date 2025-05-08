If you have a flipper zero you can simply download this app: https://lab.flipper.net/apps/avr_isp
Then drop in your SD card into folder: apps_data/avr_isp
- Craft_pcb.avr
- Craft_pcb_eeprom.hex
- Craft_pcb_flash.hex

Connect your flipper zero gpio to the SPI bus on the PCB and flash the ATMega88 using the app.



       FLIPPER ZERO --- PCB ---               PCB --- FLIPPER ZERO
                                  ______
          PIN 11  --  GND -----  | x  x |  ----> RST  -- PIN 06
          PIN 02  --  MOSI <---  | x  x    ----> SCK  -- PIN 05
          PIN 09  --  VCC -----  | x  x |  <---- MISO -- PIN 03
                                  ------

                                .---__---.     
                          RESET |        | PC5 
                                |        |     
                            PD0 |        | PC4 
                                |        |     
                            PD1 |        | PC3 
                                |        |     
                            PD2 |        | PC2 
                                |        |     
                           OC2B |        | PC1 
                                |        |     
                            PD4 |        | PC0 
                                |        |     
                            VCC |        | GND 
                                |        |     
                            GND |        | AREF
                                |        |     
                          XTAL1 |        | AVCC
                                |        |     
                          XTAL2 |        | SCK 
                                |        |     
                            PD5 |        | MISO
                                |        |     
                            PD6 |        | MOSI
                                |        |
                            PD7 |        | OC1B
                                |        |
                            PB0 |        | PB1 
                                `--------'