# OpenClash AdBlock
<div align="center"><h3>Hunter x Hunter - Ohayou (Cover by kena yokie x miyuki)</h3>
  
<a href="https://youtu.be/oaTRssMI66c" target=”_blank”>
 <img src="http://img.youtube.com/vi/oaTRssMI66c/mqdefault.jpg" alt="Watch the video" width="400" height="400" border="10" />
</a><br />
<i>(Mari mengenang masa lalu dulu. Click on the image above)</i><br /><br />
</div>

Ini adalah adblock untuk openclash, source list diambil dari berbagai sumber. Source list diupdate setiap hari secara otomatis oleh bot github.

| PACK NAME | DESCRIPTION | SOURCES |
|---------|:-------:|:-----:|
OISD Full | It blocks: Ads, (Mobile) App Ads, Phishing, Malvertising, Malware, Spyware, Ransomware, CryptoJacking, Scam ... Telemetry/Analytics/Tracking (Where not needed for proper functionality) | https://oisd.nl/ |
ABPindo_annoyance | ABPindo merupakan filter tambahan untuk melengkapi filter internasional seperti EasyList atau AdGuard Base filter memblokir iklan mengganggu di situs berbahasa Indonesia dan Malaysia. ABPindo_annoyance memblokir situs iklan & situs judi di Indonesia dan Malaysia | [ABPindo](https://github.com/ABPindo/indonesianadblockrules) |

Untuk menggunakan, edit `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  oisd_dbl_full:
    type: http
    behavior: classical
    path: "./rule_provider/oisd_dbl_full.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/oisd_dbl_full.yaml
    interval: 14400 # Update rules every 4 hours
  abpindo_annoyance:
    type: http
    behavior: classical
    path: "./rule_provider/abpindo_annoyance_adblock.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/abpindo_annoyance_adblock.yaml
    interval: 14400 # Update rules every 4 hours
rules:
# Block ads
- RULE-SET,oisd_dbl_full,REJECT
- RULE-SET,adblock_abpindo_annoyance,REJECT
```

Setelah di test dengan situs [Adblock Test](https://d3ward.github.io/toolz/adblock.html) hasilnya:

[![2022-06-08-213555-1920x986-scrot.png](https://i.postimg.cc/0yCf9YQK/2022-06-08-213555-1920x986-scrot.png)](https://postimg.cc/CRzDNfbw)

Hasil di situs adblock test bisa berbeda beda karena source list diupdate setiap hari.
