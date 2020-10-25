<h1 align="center">AnonProj</h1>

### MUST

1. Mac Spoofing
2. Non usare la rete di casa
3. **NO Proxy**
4. **NO Google**, e.g. use DuckDuckGo
5. [VPN](https://github.com/Jakkins/AnonProj/blob/master/VPN.md) **a pagamento in criptovalute
    - **Attento ai DNS**, use DNS Leak Prevent
      - DNS Leak (Proxy DNS trasparenti, switch che leggono le richieste DNS...)
    - OpenVPN
6. [TOR](https://github.com/Jakkins/AnonProj/blob/master/TOR.md) (Deepweb != Darknet)
    - scaricarlo dalla repo officiale
    - scaricare le chiavi gpg per i certificati
    - test TOR
    - [TorCheck.xenobite.ue](https://torcheck.xenobite.eu/)
7. Risorse Locali
    - FingerPrint, Canvas Blocker
        - [panopticlick](https://panopticlick.eff.org/)
        - Firegloves (firefox)
    - HTTPS, plugin to force https
    - Cookie (file di testo)
        - I cookie di terze parti possono condividere informazioni sui siti web visitati
        - Cookie Manager
        - Usare la modalita' incognito (non salva i cookie)
    - NoScript, uMatrix
    - Disable Web RTC
    - [browserspy](http://browserspy.dk/)

### MUST pt. 2

- Email
    - icedove (client di posta) + enigmail
- Veracrypt
- [Tails OS](https://tails.boum.org/) OR [**Subgraph OS**](https://subgraph.com/) OR Qubes OS

### Smartphone

- Browser
    - https://www.orchid.com/
    
### Cryptovalute

- Wallet
    - Tipi di wallet
        - Software
        - Web Based
        - Oppure installi il client in locale
- LocalBitcoin.com, Inforge (dove comprarli)
- blockchain.info (vedere tutte le transazioni mondiali)
- Mixing Service
- Coinjoin
- Ethereum

### Mixing Service

- Helix by Grams
- bitcoinblender.net
- bitcoinmix.org
- payshield
- bitcoin-for.org
- conmixer.se
- coinmixer.net
- spacechain.io

Modalità:
``` 
3 wallet.
Creiamo un wallet1 (tramite tor) dove arrivano i bitcoin.
Da questo wallet1 li inviamo al mixer.
Facciamo inviare i bitcoin dal mixer al wallet2 (creato sempre su tor).
A questo punto inviare i bitcoin dal wallet2 al wallet3 (creato sulla clearnet).
```

## Altro

- ```ToS, Terms of Service```
- ```Privacy Policy```
  - Logs
  - [dlapiperdataprotection](https://www.dlapiperdataprotection.com/)
- ```MAC```
  - Chi conosce il tuo MAC?
    - log files
    - ISP
- ```Hostname```
- ```DNS```
  - chi ha un server DNS?
    - ISP
      - il pc prende gli indirizzi DNS dall'ISP
  - dove trovare un nuovo DNS?
    - www.opendns.com
    - www.opennicproject.org
  - **cache DNS**
    - nscd per pulire la cache DNS
- proxychains-ng
- Metadata, EXIF data
- Data Shredding (DBAN)
- ASLR PAX (Grsecurity)
- codice interpretato > codice compilato (il codice interpretato non è soggetto ad attacchi di tipo memory)

### TODO

- email
- numero cell

### To Check

- Hacklog 1
    - [HACKLOG 1x25 - Guida alle Cryptovalute e al Bitcoin](https://www.youtube.com/watch?v=ERwv2Q_F0LA&list=PLYkvirnokewhbPaVM8Ykaj1JVnTPfdMzE&index=27)
- Hacklog 2
- https://wedevs.com/164817/make-search-anonymous-with-duckduckgo/
- DarkWebNews
- [Psychonautwiki](https://psychonautwiki.org/wiki/Main_Page)
- [Grams](https://grams-search.com/)















# Arch Linux Configuration

- [Network configuration](https://wiki.archlinux.org/index.php/Network_configuration)

```diff
- Arch Linux has deprecated net-tools in favor of iproute2

Deprecated command 	Replacement commands
netstat 	        ss

netstat -tanp | grep tor
```
- Rsync per il backup, anche in ssh

