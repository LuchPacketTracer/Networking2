# Packet Tracer Configuration

## PC 1-6

> Just assign IP Addresses from the **same network** for all the PC's. For example, pick anything from _192.168.1.1 - 192.168.1.254_. The **subnet mask** for the example would be _255.255.255.0_ or **CIDR** of _/30_.

## Switch 0

> Assign VLAN ID to interface ranges

```
S0(config)#interface range f0/1-f0/5
S0(config-if)#switchport access VLAN 100
S0(config)#interface range f0/6-f0/10
S0(config-if)#switchport access VLAN 200
S0(config)#interface range f0/11-f0/15
S0(config-if)#switchport access VLAN 300
```

## Switch 1

> Assign VLAN ID to interface ranges

```
S1(config)#interface range f0/1-f0/5
S1(config-if)#switchport access VLAN 100
S1(config)#interface range f0/6-f0/10
S1(config-if)#switchport access VLAN 200
S1(config)#interface range f0/11-f0/15
S1(config-if)#switchport access VLAN 300
```

---

## Finished Product

### Logical View

<p align="center">
  <img src="./Images/LogicalView.png" />
</p>

### List of VLAN's

> Command

```
S0#show VLAN brief
```

| VLAN | Name     | Status | Ports                                                                                  |
| ---- | -------- | ------ | -------------------------------------------------------------------------------------- |
| 1    | default  | active | Fa0/16, Fa0/17, Fa0/18, Fa0/19, Fa0/20, Fa0/21, Fa0/22, Fa0/23, Fa0/24, Gig0/1, Gig0/2 |
| 100  | VLAN0100 | active | Fa0/1, Fa0/2, Fa0/3, Fa0/4, Fa0/5                                                      |
| 200  | VLAN0200 | active | Fa0/6, Fa0/7, Fa0/8, Fa0/9, Fa0/10                                                     |
| 300  | VLAN0300 | active | Fa0/11, Fa0/12, Fa0/13, Fa0/14, Fa0/15                                                 |
