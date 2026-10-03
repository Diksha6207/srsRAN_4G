# srsRAN 4G LTE Project

## Project Overview

This project demonstrates a software-based 4G LTE network using srsRAN.

The LTE network is simulated without physical USRP hardware by using ZeroMQ (ZMQ) as the RF interface.

## Components

- srsENB - LTE eNodeB
- srsEPC - Evolved Packet Core
- srsUE - LTE User Equipment
- ZeroMQ - Software RF interface
- HSS - Subscriber database
- MME - Mobility Management Entity
- SPGW - Serving and Packet Gateway

## Practical Result

The LTE network was successfully started using ZMQ-based RF simulation.

The UE successfully:

1. Detected the LTE cell.
2. Established an RRC connection.
3. Completed random access.
4. Successfully attached to the network.
5. Received IP address 172.16.0.2.
6. Passed the connectivity test.

## Connectivity Test

Command:

    ping -c 4 172.16.0.2

Result:

    4 packets transmitted, 4 received, 0% packet loss

This confirms successful connectivity in the simulated LTE environment.

## Configuration Files

### srsENB

- srsenb/enb.conf
- srsenb/sib.conf
- srsenb/rr.conf
- srsenb/rb.conf

### srsEPC

- srsepc/epc.conf
- srsepc/user_db.csv

### srsUE

- srsue/ue.conf

## Environment

- Linux / WSL2
- srsRAN 4G
- CMake
- GCC / G++
- ZeroMQ
- UHD support
- LTE EPC, eNB and UE

## Hardware

This practical uses ZeroMQ for RF simulation, so physical USRP hardware is not required.

