---
parent: Harmony 3 peripheral library application examples for SAM D21/DA1 family
title: TCC PWM generation 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# TCC PWM generation

This example application shows how to use the TCC to generate a 2 or 3 phase PWM signals for motor control with dead time.

## Description

TCC module is configured to generate synchronous 2 or 3 phase PWM signals with dead time. The duty cycle of the PWM signals is updated in the period interrupt handler.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_sam_d21_da1) and then click **Clone** button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/tcc/tcc_synchronous_pwm_channels/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| sam_d21_xpro.X | MPLABX project for [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) |
| sam_da1_xpro.X | MPLABX project for [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| sam_d21_xpro.X | [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro)
| sam_da1_xpro.X | [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO)
|||

### Setting up [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro)

- Connect the Debug USB port on the board to the computer using a micro USB cable

### Setting up [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO)

- Connect the Debug USB port on the board to the computer using a micro USB cable

## Running the Application

1. Build and Program the application using its IDE
2. Observe the high-side and low-side PWM waveforms on oscilloscope
3. Observe the dead time between the high side and the low side
4. Observe the pwm frequency to be 10 KHz

Output waveforms:

  ![output](images/output_tcc_synchronous_pwm_channels.png)

[SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) pin details:

|Signal Name| Pad   | Pin |
|-----------|-------|-----|
| CH0-PWMH  | PA08  | Pin 11 of EXT2 connector |
| CH0-PWML  | PB10  | Pin 14 of EXT2 connector  |
| CH1-PWMH  | PA09  | Pin 12 of EXT2 connector |
| CH1-PWML  | PB11  | Pin 13 of EXT2 connector |
| CH2-PWMH  | PA10  | Pin 3 of EXT2 connector |
| CH2-PWML  | PB12  | Pin 7 of EXT2 connector |
||||

[SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) pin details:

|Signal Name| Pad   | Pin |
|-----------|-------|-----|
| CH0-PWMH  | PA08  | Pin 11 of EXT2 connector |
| CH0-PWML  | PB10  | Pin 14 of EXT2 connector  |
| CH1-PWMH  | PA09  | Pin 12 of EXT2 connector |
| CH1-PWML  | PB11  | Pin 13 of EXT2 connector |
| CH2-PWMH  | PA10  | Pin 3 of EXT2 connector |
| CH2-PWML  | PB12  | Pin 7 of EXT2 connector |
||||
