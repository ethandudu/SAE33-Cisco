# Topologie

## Index

- [VLANs](#vlans)
- [Routeurs](#routeurs)
  - [RB11](#rb11)
  - [RB12](#rb12)
- [Switchs L3](#switchs-l3)
  - [SWB31](#swb31)
  - [SWB32](#swb32)
  - [SWB33](#swb33)
  - [SWB34](#swb34)
- [Switchs L2](#switchs-l2)
  - [SWB21](#swb21)
  - [SWB22](#swb22)
  - [SWB23](#swb23)
  - [SWB24](#swb24)
- [ASAB](#asab)
- [WLCB](#wlcb)

## VLANs

| VLAN | Nom |
| ---- | --- |
| 2 | 2-Collab |
| 3 | 3-Admins |
| 4 | 4-VoIP |
| 6 | 6-WiFi |
| 7 | 7-Gestion |

## Routeurs

### RB11

**🔌Port USB** : `ttyUSB15`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/0 |  | SWB31 | Trunk VLAN 3-4-7 |
| Fa0/1 |  | SWB32 | Trunk VLAN 2-6 |
| Fa1/0 | 10.10.10.11/28 | ASA | ASA-RB11 |

#### SVI

| Interface | IP | VLAN | Description |
| --------- | -- | ---- | ----------- |
| Fa0/0.3 | 192.168.168.1/24 | 3 | VLAN 3 |
| Fa0/0.4 | 192.168.169.1/24 | 4 | VLAN 4 |
| Fa0/0.7 | 192.168.174.1/27 | 7 | VLAN 7 |
| Fa0/1.2 | 192.168.172.1/23 | 2 | VLAN 2 |
| Fa0/1.6 | 192.168.170.1/23 | 6 | VLAN 6 |

### RB12

**🔌Port USB** : `ttyUSB14`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/0 |  | SWB32 | Trunk VLAN 2-6 |
| Eth1/0 |  | SWB31 | Trunk VLAN 3-4-7 |
| Eth1/1 | 10.10.10.12/28 | ASA | ASA-RB12 |

#### SVI

| Interface | IP | VLAN | Description |
| --------- | -- | ---- | ----------- |
| Fa0/0.2 | 192.168.172.2/23 | 2 | VLAN 2 |
| Fa0/0.6 | 192.168.170.2/23 | 6 | VLAN 6 |
| Eth1/0.3 | 192.168.168.2/24 | 3 | VLAN 3 |
| Eth1/0.4 | 192.168.169.2/24 | 4 | VLAN 4 |
| Eth1/0.7 | 192.168.174.2/27 | 7 | VLAN 7 |

## Switchs L3

### SWB31

**🔌Port USB** : `ttyUSB20`

**🌐IP Gestion** : `192.168.174.3`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/2 |  | SWB32 |  |
| Fa0/3 |  | SWB33 |  |
| Fa0/4 |  | SWB34 |  |
| Fa0/9 |  | RB11 |  |
| Fa0/10 |  | RB12 |  |
| Fa0/12 |  | SWB21 |  |

### SWB32

**🔌Port USB** : `ttyUSB21`

**🌐IP Gestion** : `192.168.174.4`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/1 |  | SWB31 |  |
| Fa0/3 |  | SWB33 |  |
| Fa0/4 |  | SWB34 |  |
| Fa0/9 |  | RB11 |  |
| Fa0/10 |  | RB12 |  |
| Fa0/12 |  | SWB22 | ?? 24 |

### SWB33

**🔌Port USB** : `ttyUSB22`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/1 |  | SWB31 |  |
| Fa0/2 |  | SWB32 |  |
| Fa0/3 |  | SWB34 |  |
| Fa0/12 |  | SWB23 |  |

### SWB34

**🔌Port USB** : `ttyUSB23`

#### Interfaces

| Interface | IP | Destination | Description |
| --------- | -- | ----------- | ----------- |
| Fa0/1 |  | SWB31 |  |
| Fa0/2 |  | SWB32 |  |
| Fa0/3 |  | SWB33 |  |
| Fa0/12 |  | SWB24 | ?? 22 |

## Switchs L2

### SWB21

**🔌Port USB** : `ttyUSB16`

### SWB22

**🔌Port USB** : `ttyUSB17`

### SWB23

**🔌Port USB** : `ttyUSB18`

### SWB24

**🔌Port USB** : `ttyUSB19`

## ASAB

**🔌Port USB** : `ttyUSB13`

## WLCB

**🔌Port USB** : `ttyUSB12`
