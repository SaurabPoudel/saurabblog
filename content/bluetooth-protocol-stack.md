+++
title = 'Bluetooth Protocol Stack'
date = 2024-06-17T10:29:20+05:45
draft = false
description="brief description of different layers and protocols used in Bluetooth Protocol Stack"
image ="/images/bluetooth.avif"
imageBig ="/images/bluetoothprotocolstack.png"
categories= ["bluetooth","communication","wireless"]
authors= ["Saurab Poudel"]
avatar = "/images/avatar.webp"
+++
## Radio Layer

- critical for the physical communication between Bluetooth devices
- Ensures reliable and efficient data transmission by defining RF characteristics, modulation schemes, frequency bands, and error correction method
- uses frequency hopping and adaptive mechanisms that allows Bluetooth to coexist with other wireless technologies

## Baseband Layer

- Above the Radio Layer 
- Responsible for managing physical channels and links
- handles low-level operations of Bluetooth communication, such as packet formation, addressing, timing, and error correction

## Link Manager Protocol (LMP)

- responsible for managing the establishment, maintenance, and security of links between Bluetooth devices
- operates directly above the Baseband layer and handles various control functions to ensure proper link configuration and management

## Host Controller Interface (HCI)

- serves as an interface between the Host (typically the operating system or Bluetooth stack software ) and the Bluetooth Controller(the hardware responsible for handling the physical layer and baseband operations)
- defines standardized set of commands, events, and data structures for communication between the Host and the Controller, allowing the Host to control and configure the Bluetooth hardware

## Logical Link Control and Adaptation Protocol(L2CAP)

- operating above the Baseband layer and providing an abstraction layer for higher-layer protocols
- enables high-layer protocols to exchange data packets over Bluetooth connections, offering features such as segmentation and reassembly, multiplexing, and quality of service (Qos) negotitation
## RFCOMM (Radio Frequency Communication)

- provides emulation emulation of serial ports over Bluetooth
- enables serial communication betwen Bluetooth-enabled devices, allowing application to communication using a familiar serial port interface
- useful for legacy application that rely on serial port communication and need to migrate to Bluetooth without significant changes to their software architecture

##  Service Discovery Protocol(SDP)
- responsible for discovering and describing services offered by Bluetooth devices within a LAN
- enables Bluetooth devices to identify available services, determine their characteristics, and establish connections with compatible services for data exchange or interaction







