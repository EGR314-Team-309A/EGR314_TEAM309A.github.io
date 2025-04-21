---
title: Block/Process Diagrams & Message Structure
---

## Block Diagram

### General Diagram

![Image](https://github.com/user-attachments/assets/0c77f48d-81e9-4630-be1a-b01ad48d87c3)

### Connector Diagram

![Image](https://github.com/user-attachments/assets/5181d0f3-c607-4b25-8f0b-ecfba9d1c3aa)

## Process Diagram

![Image](https://github.com/user-attachments/assets/f9f6a9df-799b-4281-8727-621961ece887)

## Message Structure

### IDs

Each user has been assigned a user ID to make communication easier between users. Any messages sent will contain the sender and reciever ID to identify where its coming from and where its going to. Below is a list of IDs for each user in our project

| ID | User |
|---|---|
| M | Bruce |
| B | Baron |
| A | Aadish |
| S | Shaurya |

### Message Types

The message types are defined by the Process Diagram. Our Process Diagram only has 3 types of messages that are send between users, so below are those messages and their functions.

| Message Type | Description |
|---|---|
| 1 | Change Motor Direction |
| 2 | Update Motor Speed |
| 3 | Rotational Velocity |

### Message Variations

While message types are meant to define each message in the Process Diagram, there can be multiple variations within a message type. A motor direction message can mean to move the motor forward or reverse, so below is a breakdown of each message variation in each type and its ID.

| Message Type | Variations | ID |
|---|---|---|
| 1 | Motor Direction Forward | 0x0040 |
| 1 | Motor Direction Reverse | 0x0041 |
| 2 | Motor Speed Increase | 0x0042 |
| 2 | Motor Speed Decrease | 0x0043 |
| 3 | Rotational Velocity | Varies |

### Messages Structure

This is a breakdown of how serial messages will be sent. It shows each byte in a message and what its use is.

- Any messages sent to Bruce will be sent to Baron through UART and then sent to Bruce through MQTT server.
- Any messages sent from Bruce will be sent to Baron through MQTT server and then sent to there respective user through UART.

| Message Type | Byte 1-2 (Prefix)<br>(uint16_t) | Byte 3 (Sender ID)<br>(uint8_t) | Byte 4 (Reciever ID)<br>(uint8_t) | Byte 5-6 (Data)<br>(uint16_t) | Byte 7-8 (Suffix)<br>(uint16_t) |
|---|---|---|---|---|---|
| 1 | AZ | Bruce | Aadish | Motor Direction X | YB |
| 2 | AZ | Shaurya | Aadish | Motor Speed X | YB |
| 3 | AZ | Shaurya | Bruce | Rotational Velocity | YB |
