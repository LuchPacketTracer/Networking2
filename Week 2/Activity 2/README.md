# Packet Tracer Configuration

## Router 1

> Assign IP Address to FastEthernet0/0

```
R1(config)#in f0/0
R1(config-if)#ip add 192.168.1.1 255.255.255.0
R1(config-if)#no shut
```

> Assign IP Address to Serial0/0

```
R1(config)#in s0/0
R1(config-if)#ip add 10.0.0.1 255.255.255.0
R1(config-if)#no shut
```

> Configure Frame Relay and DLCI's

```
R1(config-if)#encapsulation frame-relay
R1(config-if)#frame-relay interface-dlci 102
R1(config-if)#frame-relay interface-dlci 103
```

> Configure RIP Routes

```
R1(config)#router rip
R1(config-router)#net 192.168.1.0
R1(config-router)#net 10.0.0.0
```

> Display RIP routes

```
R1#show ip route rip
     10.0.0.0/24 is subnetted, 1 subnets
R    192.168.2.0/24 [120/1] via 10.0.0.2, 00:00:22, Serial0/0
R    192.168.3.0/24 [120/1] via 10.0.0.3, 00:00:17, Serial0/0
R    192.168.4.0/24 [120/1] via 10.0.0.3, 00:00:17, Serial0/0
```

---

## Router 2

> Assign IP Address to FastEthernet0/0

```
R2(config)#in f0/0
R2(config-if)#ip add 192.168.2.1 255.255.255.0
R2(config-if)#no shut
```

> Assign IP Address to Serial0/0

```
R2(config)#in s0/0
R2(config-if)#ip add 10.0.0.2 255.255.255.0
R2(config-if)#no shut
```

> Configure Frame Relay and DLCI's

```
R2(config-if)#encapsulation frame-relay
R2(config-if)#frame-relay interface-dlci 201
R2(config-if)#frame-relay interface-dlci 203
```

> Configure RIP Routes

```
R2(config)#router rip
R2(config-router)#net 192.168.2.0
R2(config-router)#net 10.0.0.0
```

> Display RIP routes

```
R2#show ip route rip
     10.0.0.0/24 is subnetted, 1 subnets
R    192.168.1.0/24 [120/1] via 10.0.0.1, 00:00:11, Serial0/0
R    192.168.3.0/24 [120/1] via 10.0.0.3, 00:00:26, Serial0/0
R    192.168.4.0/24 [120/1] via 10.0.0.3, 00:00:26, Serial0/0
```

---

## Router 3

> Assign IP Address to FastEthernet0/0

```
R3(config)#in f0/0
R3(config-if)#ip add 192.168.3.1 255.255.255.0
R3(config-if)#no shut
```

> Assign IP Address to FastEthernet1/0

```
R3(config)#in f1/0
R3(config-if)#ip add 192.168.4.1 255.255.255.0
R3(config-if)#no shut
```

> Assign IP Address to Serial0/0

```
R3(config)#in s0/0
R3(config-if)#ip add 10.0.0.3 255.255.255.0
R3(config-if)#no shut
```

> Configure Frame Relay and DLCI's

```
R3(config-if)#encapsulation frame-relay
R3(config-if)#frame-relay interface-dlci 301
R3(config-if)#frame-relay interface-dlci 302
```

> Configure RIP Routes

```
R3(config)#router rip
R3(config-router)#net 192.168.3.0
R3(config-router)#net 192.168.4.0
R3(config-router)#net 10.0.0.0
```

> Display RIP routes

```
R3#show ip route rip
     10.0.0.0/24 is subnetted, 1 subnets
R    192.168.1.0/24 [120/1] via 10.0.0.1, 00:00:19, Serial0/0
R    192.168.2.0/24 [120/1] via 10.0.0.2, 00:00:07, Serial0/0
```

---

## Finished Product

### Logical View

<p align="center">
  <img src="./Images/LogicalView.png" />
</p>

### Webserver viewed via PC A Web Browser

<p align="center">
  <img src="./Images/Webserver.png" />
</p>
