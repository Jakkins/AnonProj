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
  - **Attento ai DNS**
  - **VPN con criptomonete** (bitcoin, litecoin, ...)
  - OpenVPN

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
  - $hostnamectl
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

## VPN

### [vpndienste](http://www.vpndienste.com/)

### Test the VPN

- TorGuard
- IPLeak.net
- ipMagnet

### Protocolli

- Protocollo L2TP/IPSEC (non proprio sicuro)
  - Multithreading
- **Protocollo OpenVPN (THIS)
  - lento, non multithreading nel 2017
- Protocollo PPTP (insicuro)
  - buono per gaming online, torrent, streaming

### Altro

- VPN Multi-Hop
- Tipi di VPN
  - Trusted VPN (devono garantire l'arrivo dei dati senza errori)
  - Secure VPN (le piu' utilizzate)
  - Hybrid VPN (trusted + secure)























