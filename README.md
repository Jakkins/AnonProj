# AnonProj

## To Check

- Hacklog 1
    - [HACKLOG 1x25 - Guida alle Cryptovalute e al Bitcoin](https://www.youtube.com/watch?v=ERwv2Q_F0LA&list=PLYkvirnokewhbPaVM8Ykaj1JVnTPfdMzE&index=27)
- Hacklog 2
- https://wedevs.com/164817/make-search-anonymous-with-duckduckgo/
- DarkWebNews
- [Psychonautwiki](https://psychonautwiki.org/wiki/Main_Page)
- [Grams](https://grams-search.com/)

## MUST

1. Mac Spoofing
2. Non usare la rete di casa
3. **NO Proxy**
4. **NO Google**, e.g. use DuckDuckGo
5. [VPN](#vpn) e pagamento in cripto
    - **Attento ai DNS**, use DNS Leak Prevent
      - DNS Leak (Proxy DNS trasparenti, switch che leggono le richieste DNS...)
    - **VPN con criptomonete** (bitcoin, litecoin, ...)
    - OpenVPN
6. [TOR](#tor) (Deepweb != Darknet)
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

## MUST pt. 2

- Email
    - icedove (client di posta) + enigmail
- Veracrypt
- [Tails OS](https://tails.boum.org/)
- [**Subgraph OS**](https://subgraph.com/)
- Qubes OS

## Smartphone

- Browser
    - https://www.orchid.com/
    
## Cryptovalute

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


# VPN

### [VPN List](http://www.vpndienste.com/)

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
  - LV5: Tor Relay
    - ogni utente puo' essere un relay, puoi decidere se essere un middleman o un exit node
    - i middleman e gli exit node (LV3), anche loro sono relay
  - LV6: Pluggable Transports (PT)
    - Hanno il compito di transformare il flusso del traffico tor in traffico pulito tra il client e il bridge che altrimenti potrebbe essere intercettato dall'ISP con una tecnica chiamata DPI (deep packet inspection)
    - Chiamati anche **Bridge offuscati**
    - Protocolli
      - obfs2 (**NO**)
      - obfs3 (WAT)
      - obfs4 (Simile a ScrambleSuite) [**Presente di default su Tor Browser**]
 
```
service tor status
service tor stop/start/restart
```
## Settare il sistema

Installato e avviato Tor esso funzionera' come un **proxy locale in ascolto sulla porta 9050 tramite socks4 (nel 2017)** e **porta 9150 per Tor Browser**.

### Settare il proxy per farlo lavorare sulla porta di tor

### Tor Bundle, Tor Expert Bundle

- Firefox ESR -> Tor Browser -> Proxyserver SOCKS (9150)
  - Plugin gia' inseriti
    - TorLauncher
    - TorButton
    - NoScript
    - HTTPS Everywhere
  - Da inserire
    - qualcosa per fare un fake FingerPrint
      - CanvasBlocker
- TorChat
  - decentralizzato
- bridges.torproject.org/bridges
  - possono essere blacklistati

## Surf 

- The Hidden Wiki
- Exit Node Compromessi? Cripta tutto il traffico (HTTPS)
- I2P
- Freenet
- PGP asimmetrica = Diffie–Hellman
- GPG (GNU Provacy Guard) suite di tools alternativa a PGP
















# Arch Linux Configuration

- [Network configuration](https://wiki.archlinux.org/index.php/Network_configuration)

```diff
- Arch Linux has deprecated net-tools in favor of iproute2

Deprecated command 	Replacement commands
netstat 	        ss

netstat -tanp | grep tor
```
- Rsync per il backup, anche in ssh

