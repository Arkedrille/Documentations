# Configurer Port Série Putty sous Ubuntu 20.04.1 LTS



## Dans le terminal

**Commande**

```bash
// Retirer câble usb/série
lsub
```

**Sortie**

```bash
Bus 005 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 004 Device 004: ID 13d3:56a6 IMC Networks 
Bus 004 Device 003: ID 05e3:0610 Genesys Logic, Inc. 4-port hub
Bus 004 Device 002: ID 8087:0025 Intel Corp. 
Bus 004 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 003 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```



**Commande**

```bash
// Brancher câble
lsub
```

**Sortie**

```bash
Bus 005 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 004 Device 004: ID 13d3:56a6 IMC Networks 
Bus 004 Device 003: ID 05e3:0610 Genesys Logic, Inc. 4-port hub
Bus 004 Device 002: ID 8087:0025 Intel Corp. 
Bus 004 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 003 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
// Noter 067b et 2303
Bus 002 Device 008: ID 067b:2303 Prolific Technology, Inc. PL2303 Serial Port
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```



**Commande**

```bash
modprobe usbserial vendor=0x067b product=0x2303
```

**Sortie**

```bash
Bus 002 Device 008: ID 067b:2303 Prolific Technology, Inc. PL2303 Serial Port
```



**Commande**

```bash
dmesg | grep 'ttyUSB'
```

**Sortie**

```bash
[  168.482337] usb 2-3: pl2303 converter now attached to ttyUSB0
[  334.347250] pl2303 ttyUSB0: pl2303 converter now disconnected from ttyUSB0
[  353.431623] usb 2-3: pl2303 converter now attached to ttyUSB0
```



## Note

Sous Putty : sélectionner Serial et dans le champ "Serial Line", renseigner 'ttyUSB0' et dans "Speed" renseigner la vitesse de votre switch

