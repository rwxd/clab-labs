# Switches

## Lab 2

### leaf01

```bash
nv set interface lo ip address 10.255.255.2/32
nv set interface bond0 bond member swp49-50
nv set bridge domain br_default vlan 10,20
nv set interface bond0 bridge domain br_default
nv set interface swp1 bridge domain br_default access 10

nv set interface vlan10 ip address 10.0.10.2/24
nv set interface vlan10 ip vrr address 10.0.10.1/24
nv set interface vlan10 ip vrr mac-address 00:00:00:00:1a:10

nv set interface vlan20 ip address 10.0.20.2/24
nv set interface vlan20 ip vrr address 10.0.20.1/24
nv set interface vlan20 ip vrr mac-address 00:00:00:00:1a:20

nv config apply -y
```


### leaf02

```bash
nv set interface lo ip address 10.255.255.2/32
nv set interface bond0 bond member swp49-50
nv set bridge domain br_default vlan 10,20
nv set interface bond0 bridge domain br_default
nv set interface swp2 bridge domain br_default access 20

nv set interface vlan10 ip address 10.0.10.3/24
nv set interface vlan10 ip vrr address 10.0.10.1/24
nv set interface vlan10 ip vrr mac-address 00:00:00:00:1a:10

nv set interface vlan20 ip address 10.0.20.3/24
nv set interface vlan20 ip vrr address 10.0.20.1/24
nv set interface vlan20 ip vrr mac-address 00:00:00:00:1a:20


nv config apply -y
```

### spine01

```bash

```
