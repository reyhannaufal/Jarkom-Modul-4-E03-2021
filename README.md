# Jarkom Modul 4 E03 2021

Daftar Kelompok:

1. Reyhan Naufal Rahman - 05111940000171
2. Vicky Thirdian - 05111940000211
3. Fiodhy Ardito Narawangsa - 05111940000218

## Subnetting & Routing

- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.
  ![subnetting](https://user-images.githubusercontent.com/59334824/143676710-2e52860a-6c85-4afc-a68a-3121538685bf.png)

## Perhitungan VLSM

1. Pembagian subnet terhadap topologi.
   ![praktikum_modul4 - Frame 10](https://user-images.githubusercontent.com/59334824/143676704-bfe3ce3f-ddbf-47f6-95f5-70d90a866a69.jpg)
2. Menghitung pembagian IP berdasarkan NID dan netmask menggunakan pohon dibawah.
   ![praktikum_modul4 - Frame 11](https://user-images.githubusercontent.com/59334824/143676684-2a39e8af-fc41-4b2f-814b-7317c758fd80.jpg)
3. Hasil VLSM menggunakan Cisco Packet Tracer
   ![image](https://user-images.githubusercontent.com/59334824/143676925-5226966f-3540-4785-8209-5fb310856c07.png)

## Perhitungan CIDR

### Subnetting

a. ![subnetting (1)](https://user-images.githubusercontent.com/54606856/143683525-ce7680e3-f1d1-49f4-a917-5b282e9121f7.jpg) </br>

b. ![subnetting (2)](https://user-images.githubusercontent.com/54606856/143683559-3898af86-d24b-40f7-af2d-b2321b7d7f60.jpg) </br>

c. ![subnetting (3)](https://user-images.githubusercontent.com/54606856/143683590-2ac592f9-be29-4d7a-9a5a-b92da6d82c3a.jpg)</br>

d. ![subnetting (4)](https://user-images.githubusercontent.com/54606856/143683637-e2e10b42-3cd1-4965-820d-cb172918291c.jpg) </br>

e. ![subnetting (5)](https://user-images.githubusercontent.com/54606856/143683667-7fcfd75a-cef5-4fd2-9a5a-f5ba9ffd335c.jpg) </br>

### CIDR TREE

![CIDRTree](https://user-images.githubusercontent.com/54606856/143683777-01d20c4b-fc14-4087-b972-7dfbfce38579.jpg)

### Setting Konfigurasi

**FOOSHA (ROUTER)**

```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.210.64.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.210.192.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.210.32.1
	netmask 255.255.255.252
```

**BLUENO (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.64.2
	netmask 255.255.252.0
	gateway 192.210.64.1
```

**WATER7 (ROUTER)**

```

auto eth0
iface eth0 inet static
	address 192.210.192.2
	netmask 255.255.255.252
	gateway 192.210.192.1

auto eth1
iface eth1 inet static
	address 192.210.160.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.210.144.1
	netmask 255.255.255.252

```

**CIPHER (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.160.2
	netmask 255.255.252.0
	gateway 192.210.160.1

```

**COURTYARD (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.128.3
	netmask 255.255.248.0
	gateway 192.210.128.1

```

**CALMBELT (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.128.2
	netmask 255.255.248.0
	gateway 192.210.128.1
```

**PUCCI (ROUTER)**

```
auto eth0
iface eth0 inet static
	address 192.210.144.2
	netmask 255.255.255.252
	gateway 192.210.144.1

auto eth1
iface eth1 inet static
	address 192.210.128.1
	netmask 255.255.240.0

auto eth2
iface eth2 inet static
	address 192.210.136.1
	netmask 255.255.255.128
```

**JIPANGU (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.136.2
	netmask 255.255.255.128
	gateway 192.210.136.1
```

**GUANHAO (ROUTER)**

```
auto eth0
iface eth0 inet static
	address 192.210.32.2
	netmask 255.255.255.252
        gateway 192.210.32.1

auto eth1
iface eth1 inet static
	address 192.210.20.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.210.16.1
	netmask 255.255.254.0

auto eth3
iface eth3 inet static
	address 192.210.8.1
	netmask 255.255.255.252
```

**JABRA (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.20.2
	netmask 255.255.252.0
	gateway 192.210.20.1
```

**MAINGATE (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.16.2
	netmask 255.255.254.0
	gateway 192.210.16.1
```

**ALABASTA (ROUTER)**

```
auto eth0
iface eth0 inet static
	address 192.210.16.3
	netmask 255.255.254.0
	gateway 192.210.16.1

auto eth1
iface eth1 inet static
	address 192.210.18.1
	netmask 255.255.255.240
```

**JORGE (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.18.2
	netmask 255.255.255.240
	gateway 192.210.18.1
```

**OIMO (ROUTER)**

```
auto eth0
iface eth0 inet static
	address 192.210.8.2
	netmask 255.255.255.0
	gateway 192.210.8.1

auto eth2
iface eth2 inet static
	address 192.210.4.1
	netmask 255.255.255.0
```

**ENIESLOBBY (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.4.2
	netmask 255.255.255.0
	gateway 192.210.4.1
```

**SEASTONE (ROUTER)**

```
auto eth0
iface eth0 inet static
	address 192.210.4.3
	netmask 255.255.255.0
	gateway 192.210.4.1

auto eth1
iface eth1 inet static
	address 192.210.0.1
	netmask 255.255.252.0
```

**ELENA (CLIENT)**

```
auto eth0
iface eth0 inet static
	address 192.210.0.2
	netmask 255.255.252.0
	gateway 192.210.0.1
```

### ROUTING

**FOOSHA**

```
route add -net 192.210.128.0 netmask 255.255.128.0 gw 192.210.192.2

route add -net 192.210.0.0 netmask 255.255.128.0 gw 192.210.32.2
```

**WATER7**

```
route add -net 192.210.128.0 netmask 255.255.192.0 gw 192.210.144.2
```

**GUANHAO**

```
route add -net 192.210.0.0 netmask 255.255.240.0 gw 192.210.8.2

route add -net 192.210.16.0 netmask 255.255.248.0 gw 192.210.16.3
```

**OIMO**

```
route add -net 192.210.0.0 netmask 255.255.252.0 gw 192.210.4.3
```

Setelah itu jangan lupa untuk melakukan `iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.210.0.0/16` pada FOOSHA. Dan `echo nameserver 192.168.122.1 > /etc/resolv.conf` pada node client dan router.
