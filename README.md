PCB Module based on STM32G491RET6 acting as a water sensor just for tests purposes. Nominal working voltage is 12V.
It is designed to receive commands either by UART or LIN-BUS containing info about:
  1. How many voltage between 0-3.3V to put in a connector A. 
     DAC_OUT1 from the STM32 is used for this purpose.
  2. How many current between 0-20mA to put in a connector B.
     DAC_OUT2 from the STM32 is used for this purpose. An equivalent voltage is generated from the DAC that will go through a phase of voltage-current conversion with the Improved Howland Current Pump achieving an outside current from 0mA to 20mA with 0V-3.3V.
  3. Toggle between 0V & 12V that must reach a connector C.
     This phase is achieved with high side switching topology to toggle 4 different pins of 2 separate connectores to toggle between 0V and 12V.
