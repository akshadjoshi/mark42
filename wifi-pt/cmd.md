
```bash
apt install aircrack-ng 
```


```bash
ip a
```

`check mode default is manage `
```bash
iwconfig
```

`check the mode default `
```bash
airmon-ng
```

> THE MODE WILL CHANGE AUTOMATICALLY WHEN YOU START THE INTERFACE VIA `airmon-ng`
> The mode should change from manage to monitor

```bash
airmon-ng start wlan0
```



`to stop the interface`
```bash
airmon-ng stop wlan0mon
```

`command to capture packets`

```bash
airodump-ng wlan0mon
```
