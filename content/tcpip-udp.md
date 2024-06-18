+++
title = 'Tcp/Ip Udp | Intro to TCP/IP'
date = 2024-06-17T20:41:14+05:45
draft = false
description="Intro to TCP/IP"
image ="/images/tcpudp1.png"
imageBig ="/images/tcpipprotocol.png"
categories= ["general"]
authors= ["Saurab Poudel"]
avatar = "/images/avatar.webp"
+++

The TCP/IP model (Transmission Control Protocol/ Internet Protocol Model) is a part of network domain designed specially for achieving efficient and error-free transmission of data.

## History of TCP/IP

- developed during the Cold war as a way for U.S. Department of Defence to connect computers within their networks and with each other across national boundaries.
- first version of TCP/IP was ARPANET (Advanced Research Projects Administration Network). Then in 1983, name changed to TCP/IP
- to give researchers access to each other's equipment, they needed to send message quickly over long distances without having them re-transmitted by any intermediate nodes along the way. This necessity led to the development of TCP/IP.

## Features of the TCP/IP Model

- comprises four layer:
  - the network access layer
  - the internet layer
  - the transport layer
  - the application layer
    (going bottom to top)
- implemented during network and communication related issues
- communication between different modes of network devices is possible through the application of various layers
- layer in the mode provide maintenance of communication channels, flow control, and reliability check format, among other application in the form of protocols.

## Layers of the TCP/IP Model

- Application layer
- Transport layer
- Internet Layer
- Network Access Layer
  (Top to bottom)

### Application Layer

- top most layer which indicates the application and programs that utilize the TCP/IP mode for communicating with the user through application and various tasks performed by the layer, including data representation for the application executed by the user and forward it to transport layer
- maintains a smooth connection between the application and user for data exchange and offers various features as remote handling of the system, email services etc.

- Some protocol used in this layer are: HTTP, SMTP and FTP

### Transport Layer

- responsible for establishing the connection between the sender and the receiver device and also performs the tasks of dividing the data from the application layer into packets, which are then used to create sequences.
- maintaining of data (to be transmitted without error), and controls the data flow rate over the communication channel for smooth transmission of data.

#### The protocols used in this layer are:

- TCP (Transmission Control Protocol): responsible for the proper transmission of segments over the communication channel. establishes a network connection between the source and destination system.
- UDP: responsible for identifying errors, and other tasks during the transmission for information. (more about UDP in next blog...)

### Internet Layer

- controls the transmission of the data over the network modes and enacts protocols related to the various steps related to the transmission of data over the channel, which is in the form of packets sent by the previous layer
- responsible for specifying the path that the data packets will use for transmission
- responsible for providing IP addresses to the system for the identification matters over the network channel

### Network Access Layer

- last layer
- combination of data-link and physical layer where it is responsible for maintaining the task of sending and receiving data in raw bits
- uses the physical address of the system for mapping the path of transmission over the network channel

(on upcomming blog , I will write about how does TCP/IP work, OSI vs TCP/IP model, intro to UDP and many more...)
