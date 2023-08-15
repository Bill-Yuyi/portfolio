+++
draft = false
date = 2023-08-14
title = "Network basics"
description = ""
tags = ["System Design","Computer Networking"]
+++

## Basics

* IP Addresss(Unique Identifier on Internet)
    * IPV4(32-bit) which owns 4.5 billion unique IP address
    * IPV6(128-bit) became popular since internet growth

* IP and Data Packets
    * data packet
        * header
            * source
            * destination
        * data(payload)
        * trailer
    * data is sent by dividing into multiple data packets

* TCP(Transmission Control Protocol)
    * Since data is divided into multiple data packets, TCP is used to ensure data packets are arrived in right sequence and reassembled correctly
    * IP ensures data is sent to right destination

* Application Data
    * HTTP request(POST,GET)

* Network Layer
    * IP - Network layer (Physical)
    * TCP - Transport layer
    * HTTP operates - Application layer

* Public and Private IP
    * Public IP is able to be accessed globally
    * Private IP is only reachable within LAN(Local Area Network)

* Static and Dynamic IP
    * Static IP is used by server side (Imagine your local file server),manually configured
    * Dynamic IP is often used by client side which is auto-configured

* Port
    * Port is used to distinguish multiple application or service that running on single device(Like database port, backend port, React.js port)
