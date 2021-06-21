# warabilba-network

Assumptions

- NBN conected to main house
  - Shed could be connected earlier during build, but then would be the "master" location
- Wired connections preferred over wireless, but not overdone
- PoE preferred over mains+data
- Shed connected for work/backup
- Dedicated network segments or configuration for [trusted|IoT|guests|kids]

Roles:

| House | Shed |
| ----- | ---- |
| - NBN/Internet<br>- Router<br>- Switch + PoE<br>- WiFi<br>- Cameras?<br>- NAS/Server | - Switch+PoE<br>- Wifi<br>- Cameras<br>- NAS/Server |

[**TP-Link Omada**](https://www.tp-link.com/uk/omada-sdn/)

- Business-grade software-defined-network suite of products
  - Exapandable over time
  - Dedicated APs where they are needed to provide full internal/external signal
  - Seamless handover between APs
  - Mesh network for long-range external connectivity
  - Dedicated network configuration for IoT, kids, guests
- [Controller](https://www.tp-link.com/au/business-networking/omada-sdn-controller/)
  - Hardware or software application that manages & monitors other devices 
  - Software preferred if an internal always-on machine exists
- [Router](https://www.tp-link.com/au/business-networking/omada-sdn-router/)  
  - Dedicated router enables segmentation of devices/networks, monitoring & control
- [Switch + PoE](https://www.tp-link.com/au/business-networking/omada-sdn-switch/?filterby=5984%7C5985%7C4993%2C5996)
  - Fast interconnectivity, expandable as wired network grows
  - PoE to support cameras/APs
- [Wifi Access Point](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/)
  - Ceiling Mount
    - _Provides large area internal WiFi in living area or between rooms_
    - [EAP620-HD-v1](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/eap620-hd/v1/)
      - AX1800
      - $160
    - [EAP660-HD-v1](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/eap660-hd/v1/)
      - AX3600
      - 2.5G uplink
      - $300
  - External
    - _Long-range external wifi_
    - [EAP225-OUTDOOR-v1](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/eap225-outdoor/v1/)
      - AC1200
      - $130 (umart)
  - Wall Mount
    - _Short-range room-level wifi_
    - [EAP235-WALL-v1](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/eap235-wall/v1/)
      - AC1200
      - 3x LAN ports, including 1x PoE
      - $130 (kogan, mwave)

## House

### Minimal
 



