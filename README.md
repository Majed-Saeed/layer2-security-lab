# layer2-security-lab
Cisco Packet Tracer lab demonstrating Layer 2 security: STP root bridge configuration, STP attack protection, port security, and disabling unused ports.

# Packet Tracer – Layer 2 Security

## About this Lab
This lab demonstrates configuration of Layer 2 security in Cisco Packet Tracer.  
It covers securing Spanning Tree Protocol (STP), configuring root/secondary bridges, enabling port security, and disabling unused ports to protect against common LAN attacks.

## Objectives
- Assign Central switch as the **root bridge**.  
- Configure **secondary root bridge** on SW-1.  
- Secure STP parameters to prevent manipulation attacks.  
- Enable **PortFast**, **BPDU Guard**, and **Root Guard**.  
- Configure **port security** to protect against CAM table overflow.  
- Disable all unused ports.  

## Skills Shown
- Cisco IOS CLI configuration  
- Spanning Tree Protocol (STP) hardening  
- Port security (MAC address limits, violation modes)  
- LAN security best practices  

## Devices
- 3 Switches (3560 Central, SW-1, SW-2)  
- 2 Access Switches (SW-A, SW-B)  
- End devices (PCs and Servers)  

## Files
- `Layer2-Security.pkt` → Cisco Packet Tracer lab file  
- `README.md` → Documentation  

## Topology Overview

| Device   | Role              | VLAN | Ports Secured | Notes                  |
|----------|------------------|------|---------------|------------------------|
| Central  | Root Bridge       | 1    | -             | Primary root bridge    |
| SW-1     | Secondary Root    | 1    | F0/23-24 RG   | Root Guard enabled     |
| SW-2     | Distribution      | 1    | F0/23-24 RG   | Root Guard enabled     |
| SW-A     | Access Switch     | 10   | F0/1-12 PS    | Port security enabled  |
| SW-B     | Access Switch     | 20   | F0/1-12 PS    | Port security enabled  |
