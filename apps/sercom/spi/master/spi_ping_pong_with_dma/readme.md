---
parent: Harmony 3 peripheral library application examples for SAM D21/DA1 family
title: SERCOM SPI ping pong with DMA 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# SERCOM SPI ping pong with DMA

This example demonstrates how to continuously transmit and receive data over a SPI interface using ping pong buffers with DMA.

## Description

The DMA peripheral provides support to implement the ping-pong buffering. The DMA transmits and receives data from one pair of buffers, when the CPU works on the second pair.

When the DMA is transmitting data from the ping buffer, the CPU works on the pong buffer. When the DMA completes the transfer, it generates interrupt to indicate transfer completion from the ping buffer. DMA channel is automatically re-initialized to transmit data from the pong buffer while the CPU works on the ping buffer.

When the DMA is receiving data to the ping buffer, the CPU works on the the pong buffer.When DMA completes the transfer, it generates interrupt to indicate the availability of the data in the ping buffer. DMA channel is automatically re-initialized to receive data in the pong buffer while the CPU works on the ping buffer.

Application transmits an array of values and verifies the value transmitted by receiving the values back with loop back and comparing it to the value transmitted. This application requires that the MOSI output pin to be connected to the MISO input pin so that anything
transmitted will also be received.

## Downloading and building the application

To download or clone this application from Github, go to the [top level of the repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_sam_d21_da1) and click

![clone](../../../../../docs/images/clone.png)

Path of the application within the repository is **apps/sercom/spi/spi_ping_pong_with_dma/firmware** .

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

- Use a jumper wire to short pin 16 and pin 17 of the EXT2 header
- Connect the Debug USB port on the board to the computer using a micro USB cable

### Setting up [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO)

- Use a jumper wire to short pin 16 and pin 17 of the EXT2 header
- Connect the Debug USB port on the board to the computer using a micro USB cable

## Running the Application

1. Build and Program the application project using its IDE
2. LED indicates the success or failure:
    - The LED is turned ON when the value received matched with the transmitted value
    - The LED is turned OFF when the value received did not match with the transmitted value

Following table provides the LED name:

| Board      | LED Name |
| ---------- | ---------------- |
| [SAM D21 Xplained Pro Evaluation Kit](https://www.microchip.com/developmenttools/ProductDetails/atsamd21-xpro) | LED0 |
| [SAM DA1 Xplained Pro Evaluation Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMDA1-XPRO) | LED0 |
|||
