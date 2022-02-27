---
layout: post
title:  "S2. OSI Model Basics"
date:   2022-02-26 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# OSI Model Basics

![osi-model](/images/osi-model.png)

 OSI stands for `Open Systems Interconnection Model` and this system allows for  systems to work reliably with other systems in terms of their communication systems and creating a set of startardized commununication protocols. With the creation of computer networking, a need reliably connnect with each other had begun to form during the 1970s to 1980s.

This model is split into seven abstract parts that are refered to as layers. The layered organization is used in order to represent the functionality that each layer provides to the layers both immediately above and immediatly below it. 

![osi-model-2](/images/osi-model-2.png)

> The top 4 layers (application, presentation, session, and transport) are part of the Host Layers and pertain to data, connection, software and application functionality and issues. the bottom 3 layers (network, data link, and physical) are a part of the Media Layers and pertain to the application's physical hardware and its transportation of data. 

## 7. Application Layer

The application layer performs closest to the end user because it is this user that begins a communciation request between themselves and the application. The web interface that is provided at this stage allows for the user to begin network requests such as a website on the Internet, viewing an e-mail, or messaging other people electronically. 

## 6. Presentation Layer

The presentation layer essentially takes the requested data and reformats that into a machine-readable language. This new presentation of data translates data that was meant for humans and turns it into data that can be efficently fed into the network. 

## 5. Session Layer

The session layer takes the previously translated data and manages the transfer of that data to its destination. This process is safeguarded by protocols such as authentification, permissions, checkpoints, , recovery, restoration, etc. 
authentification permission session restoration

## 4. Transport Layer

The transport layer essentially is an extra layer of security and reliability during the connection and delivery process. 

> This layer can be seen as seperated from the "Host Layers" because it provides an intermieditary service between the software functionalities of the Upper Layers and the hardware functionalities of the lower layers. 

## 3. Network Layer

The network layer deals with the transferring of data ater the transl;ation/ conversion done in prevous layers. The operations that are seen in this process pertain to subnets and the path that the requested data should follow.

## 2. Data Link Layer

The data Link layer takes the previous data that was translated into machine-readable bits - and turn them into frames. These frames are delivered to its respected network according to a set list of protocols that pertain to things such as error detection, correction, etc.

## 1. Physical Layer

The physical layer deals with raw bits of data and the physical hardware that i sused to interpret that data. 
bits

# References

Wiki [https://en.wikipedia.org/wiki/OSI_model](https://en.wikipedia.org/wiki/OSI_model)

Cisco [https://learningnetwork.cisco.com/s/article/osi-model-reference-chart](https://learningnetwork.cisco.com/s/article/osi-model-reference-chart)

OSI [https://osi-model.com/] (https://osi-model.com/)