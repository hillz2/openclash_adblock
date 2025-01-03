# OpenClash AdBlock
<div align="center"><h3>Hunter x Hunter - Ohayou (Cover by kena yokie x miyuki)</h3>
  
<a href="https://youtu.be/oaTRssMI66c" target=”_blank”>
 <img src="http://img.youtube.com/vi/oaTRssMI66c/mqdefault.jpg" alt="Watch the video" width="400" height="400" border="10" />
</a><br />
<i>(Mari mengenang masa lalu dulu. Click on the image above)</i><br /><br />
</div>

Ini adalah adblock untuk openclash, source list diambil dari `oisd.nl`. Source list diupdate setiap hari secara otomatis oleh bot github.

| PACK NAME | DESCRIPTION | SOURCES |
|---------|:-------:|:-----:|
oisd big | Blocks Ads, (Mobile) App Ads, Phishing, Malvertising, Malware, Spyware, Ransomware, CryptoJacking, Scam, ... Telemetry/Analytics/Tracking (Where not needed for proper functionality) | https://big.oisd.nl/domainswild |
oisd small | Mainly focusses on blocking ads | https://small.oisd.nl/domainswild |
adaway | Blocklist suitable for android / iOS, it focuses on blocking mobile ad providers. | https://adaway.org/hosts.txt |

Untuk menggunakan, edit `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  oisd_big:
    type: http
    behavior: classical
    path: "./rule_provider/oisd_big.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/oisd_big.yaml
    interval: 28800 # Update rules every 8 hours
    
rules:
# AdBlock
- RULE-SET,oisd_big,REJECT
```

Setelah di test dengan situs [Adblock Test](https://d3ward.github.io/toolz/adblock.html) hasilnya:

![2022-06-08-213555-1920x986-scrot.png](https://i.ibb.co/HVxLfYz/2024-01-13-185840-1920x973-scrot.png)

Hasil di situs adblock test bisa berbeda beda karena source list diupdate setiap hari.
