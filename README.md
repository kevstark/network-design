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
  - _Hardware or software application that manages & monitors other devices_
  - Software preferred if an internal always-on machine exists
  - [OC200](https://www.tp-link.com/au/business-networking/omada-sdn-controller/oc200/)
    - $120
- [Router](https://www.tp-link.com/au/business-networking/omada-sdn-router/)  
  - _Dedicated router enables segmentation of devices/networks, monitoring & control_
  - [R605](https://www.tp-link.com/au/business-networking/omada-sdn-router/tl-r605/)
    - ~$90 (amazon)
- [Switch + PoE](https://www.tp-link.com/au/business-networking/omada-sdn-switch/?filterby=5984%7C5985%7C4993%2C5996)
  - _Fast interconnectivity, expandable as wired network grows_
  - _PoE to support cameras/APs_
  - [SG3210XHP-M2-v1](https://www.tp-link.com/au/business-networking/omada-sdn-switch/tl-sg3210xhp-m2/v1/)
    - 8xLAN+PoE @ 2.5G + 2xSFP @ 10G
    - 240W PoE budget
    - ~$630 (pcbyte)
  - [SG2210MP-v1](https://www.tp-link.com/au/business-networking/omada-sdn-switch/tl-sg2210mp/v1/)
    - 8xLAN @ 1G + 2xSFP @ 1G
    - 150W PoE budget
    - $230 (mwave)
  - [SG2218-v1](https://www.tp-link.com/au/business-networking/omada-sdn-switch/tl-sg2218/v1/)
    - 16xLAN @ 1G + 2xSFP @ 1G
    - $210 (pcbyte au)
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
 



