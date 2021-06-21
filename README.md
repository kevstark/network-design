# Network Design

Objectives:

- Complete wireless coverage within and around house and gardens
  - Enable work-from-home video conferencing on the move anywhere in/around house
  - Enable media devices anywhere (focus on living/master initially?)
- Strong wifi in/around shed to enable calls/stocktake/invoicing immediately when home
  - Computer/tablet device dedicated for business in shed
  - Security cameras on shed give exceptional view/coverage

Assumptions

- NBN conected to main house
  - Shed could be connected earlier during build, but then would be the "master" location for NBN/router
- Wired connections in house preferred over wireless, but at a build budget
- Option for remote shed to serve as work/backup location
- Dedicated network segments or configuration for [trusted|IoT|guests|kids]
- Fully-offsite backup via cloud services (or remote family/business property)


Roles:

| House | Shed |
| ----- | ---- |
| - NBN/Internet<br>- Router<br>- Switch + PoE<br>- WiFi<br>- Cameras?<br>- NAS/Server | - Switch+PoE<br>- Wifi<br>- Cameras<br>- Backup NAS/Server |

Comparison:

- High-spec consumer-grade single devices cost ~$600-800 and are not easily expandable (or iteratively upgradeable)
- [Ubiquity UniFi](https://www.ubnt.com.au/unifi/) devices have a larger range of integrated devices and capabilities, but at a +2x price

## Minimal

> Minimal data wiring - barebones for initial wifi coverage across house with expectation that cameras/external wifi can be run through roof later. 

- Run all data lines and 2+ power-points to a large cupboard in cool room such as office.
- Network cabinet, mounted low or high in office built-in cupboard
  - This will ensure its kept tidy, locked, screen & fan for dust.
  - Biggest one you are willing to dedicate space to.
  - Initially contain NBN, router, switch & powerboard
  - Future uses would be UPS, media/automation server, network storage, camera recorder, etc
  - [6U, 450d](https://www.selby.com.au/brands/raxx/6u-wall-cabinet-530-450.html) ~$140
  - [8U, 450d](https://www.selby.com.au/brands/raxx/8u-wall-cabinet-530-450.html) ~$150
  - [11U, 500d](https://www.selby.com.au/brands/raxx/11u-19in-wall-mount-network-server-rack-cabinet-11ru.html) ~$180
- CAT6
  - Roof in kitchen (Wifi AP for kitchen/living/entertaining
  - Ceiling in hallway (to serve kids bedrooms)
  - Wall point low behind TV area (to serve wired and wireless tv/games/media devices)
  - Wall of office (to serve office dedicate wifi point + wired devices)
  - Wall of master bedroom (to serve dedicated AP in future)
- ~$460 [OC200 network controller](#controller), [R605 router](#router) + [SG2210MP 8-port switch + PoE](#switch)
- $160 [EAP620](#wifi-access-points) on roof of kitchen area
- $130 (optional) [EAP225-WALL](#wifi-access-points) in the office or master bedroom.
- $130 (optional) [EAP225-OUTDOOR](#wifi-access-points) in/on the shed to provide external coverage and shed coverage.

## Expanded

> All of [minimal](#minimal) wiring and devices, plus increased wiring for additional room points and external wifi/cameras

- CAT6
  - Single/double runs to all wall points (behind TV, office, bedrooms etc)
  - Run wall points to kids/spare bedrooms
  - Spare lines to corners of house under eaves (for cameras and/or external wifi points)
- Wifi access points
  - Wall points in office, master bedroom or behind living TV as needed
  - Roof point in hallway for kids as needed  
- [SG2210MP 8-port switch + PoE](#switch) in shed (to run multiple cameras or wifi points)
- Additional [SG2218 16-port switch](#switch) in office to interconnect wired (non-PoE) points (as needed)
- ~$200-400 [UPS](https://www.umart.com.au/UPS---Power-Protection_C.html?id=57&price_min=&price_max=&filter=0&filter_attr=0.0.0.15223-15116-15039.0.0.0.0.0.0.0.0.0) backup power supply
- ~$800+ [NAS](https://www.umart.com.au/NAS---Network-Storage_C.html?id=126&brand=271&price_min=&price_max=&filter=0&filter_attr=10126-111094-112003.0.0.0.0.0.0.0.0.0.0) network storage

## TP-Link Omada

[**TP-Link Omada**](https://www.tp-link.com/uk/omada-sdn/)

- Business-grade software-defined-network suite of products
- Exapandable over time
- Dedicated APs where they are needed to provide full internal/external signal
- Seamless handover between APs
- Mesh network for long-range external connectivity
- Dedicated network configuration for IoT, kids, guests

### [Controller](https://www.tp-link.com/au/business-networking/omada-sdn-controller/)
- _Hardware or software application that manages & monitors other devices_
- Software preferred if an internal always-on machine exists
- [OC200](https://www.tp-link.com/au/business-networking/omada-sdn-controller/oc200/)
  - $120

### [Router](https://www.tp-link.com/au/business-networking/omada-sdn-router/)  
- _Dedicated router enables segmentation of devices/networks, monitoring & control_
- [R605](https://www.tp-link.com/au/business-networking/omada-sdn-router/tl-r605/)
  - ~$90 (amazon)

### [Switch](https://www.tp-link.com/au/business-networking/omada-sdn-switch/?filterby=5984%7C5985%7C4993%2C5996)
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

### [Wifi Access Points](https://www.tp-link.com/au/business-networking/omada-sdn-access-point/)
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
