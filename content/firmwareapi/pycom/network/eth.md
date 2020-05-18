---
title: "Ethernet"
aliases:
    - firmwareapi/pycom/network/eth.html
    - firmwareapi/pycom/network/eth.md
    - chapter/firmwareapi/pycom/network/eth
---

The ETH class enables the use of an ethernet connection via the PyEthernet board plugged into a Pygate.

---
*NOTE* :
Ethernet support is only available in special Gpy or WiPy firmware builds where this feature has been enabled.

---

## Constructors

### class network.ETH(id=0, ...)

Create and configure an ETH object. See init for params of configuration.

```python
from network import ETH
eth = ETH()
```

## Methods


### eth.init(hostname=None)

This function starts the Ethernet interface and enables the ethernet adapter.

`hostname`: set the interface hostname

### eth.ifconfig(config=\['dhcp' or configtuple\])

With no parameters given, this returns a 4-tuple of (ip, subnet mask, gateway, DNS server).

Optionally specify the configuration parameter:

- `config='dhcp'`  

If 'dhcp' is passed as a parameter, then the DHCP client is enabled and the IP parameters are negotiated with the DHCP server.

- `config=(ip, nm, gw, dns)`

If the 4-tuple config is given then a static IP is configured. For example: `eth.ifconfig(config=('192.168.0.4', '255.255.255.0', '192.168.0.1', '8.8.8.8'))`.

### eth.hostname(string)

Set the interface host name.

### eth.mac()

Get the ethernet interface mac address.

### eth.deinit()

Shuts down the ethernet interface.

### eth.isconnected()

Returns `True` if the ethernet link is up and IP is accquired, `False` otherwise.
