# AnonProj

- Hacklog 1
- Hacklog 2

## MUST
1. Mac Spoofing
2. Non usare la rete di casa
3. **NO Proxy**
4. **NO Google**, e.g. use DuckDuckGo
5. FingerPrint
6. HTTPS, plugin to force https
7. [VPN](#vpn) e pagamento in cripto
  - **Attento ai DNS**, use DNS Leak Prevent
    - DNS Leak (Proxy DNS trasparenti, switch che leggono le richieste DNS...)
  - **VPN con criptomonete** (bitcoin, litecoin, ...)
  - OpenVPN
8. [Tor](#tor) (Deepweb != Darknet)
  - scaricarlo dalla repo officiale
  - scaricare le chiavi gpg per i certificati

## Distros

- [Tails](https://tails.boum.org/)

## To Check

https://wedevs.com/164817/make-search-anonymous-with-duckduckgo/

## Altro

- ```ToS, Terms of Service```
- ```Privacy Policy```
  - Logs
  - [dlapiperdataprotection](https://www.dlapiperdataprotection.com/)
- ```MAC```
  - Chi conosce il tuo MAC?
    - log files
    - ISP
  - $apt-get install macchanger
- ```Hostname```
- ```DNS```
  - chi ha un server DNS?
    - ISP
      - il pc prende gli indirizzi dall'ISP
  - dove trovare un nuovo DNS?
    - www.opendns.com
    - www.opennicproject.org
  - **cache DNS**
    - nscd per pulire la cache DNS
- proxychains-ng

# VPN

### [vpndienste](http://www.vpndienste.com/)

### Test the VPN

- TorGuard
- IPLeak.net
- ipMagnet

### DNS Leak Prevent

- VPN Provider
  - Mullvad
  - TorGuard
  - LimeVPN
  - PureVPN
- Software
  - VPN Watcher
  - VPN Check
  - VPN Lifeguard
  - TunnelRat
  - VPNetMon

### Protocolli

- Protocollo L2TP/IPSEC (non proprio sicuro)
  - Multithreading
- **Protocollo OpenVPN (THIS)
  - lento, non multithreading nel 2017
- Protocollo PPTP (insicuro)
  - buono per gaming online, torrent, streaming

### Altro

- VPN Multi-Hop
- Kill Switch (usarla ad esempio se si deve andare afk)
- Tipi di VPN
  - Trusted VPN (devono garantire l'arrivo dei dati senza errori)
  - Secure VPN (le piu' utilizzate)
  - Hybrid VPN (trusted + secure)

# Tor

TorProject.org riceve soldi dal dipartimento degli stati uniti d'America per sviluppo e ricerca.
- ```I server Tor agiscono da router per costruire una rete privata virtuale a strati```
  - LV1: Client
  - LV2: Middleman
    - Server di rimbalzo dei dati
  - LV3: Exit Router
    - Server finali della rete Tor
  - LV4: Bridge Router
    - simili agli exit router (LV3)
    - sono server con identificatore privato per bypassare il blocco della rete Tor se viene applicata dagli ISP, o dallo stato, o altro
 
```
service tor status
service tor stop/start/restart
```
## Settare il sistema

Installato e avviato Tor esso funzionera' come un **proxy locale in ascolto sulla porta 9050 tramite socks4 (nel 2017)** e **porta 9150 per Tor Browser**.

> Arch Linux has deprecated net-tools in favor of iproute2
```
Deprecated command 	Replacement commands
netstat 	          ss
```
```
netstat -tanp | grep tor
```

> **Settare il proxy per farlo lavorare sulla porta di tor**
















# Arch Linux Configuration

[Network configuration](https://wiki.archlinux.org/index.php/Network_configuration)

```
net-tools

Arch Linux has deprecated net-tools in favor of iproute2

Deprecated command 	Replacement commands
arp 	              ip neighbor
ifconfig 	          ip address, ip link
netstat 	          ss
route 	            ip route

$ ss
216.58.198.46     Google
52.12.8.165
40.114.177.156    DuckDuckGo
151.101.240.133   GitHub
140.82.112.26
138.201.81.199
40.114.178.124    DuckDuckGo
```
