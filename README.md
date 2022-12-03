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
AdAway | AdAway is an open source ad blocker for Android using the hosts file. | https://adaway.org/ |
Adguard DNS | Filter composed of several other filters (AdGuard Base filter, Social media filter, Tracking Protection filter, Mobile ads filter, EasyList, EasyPrivacy, etc) and simplified specifically to be better compatible with DNS-level ad blocking. | [Adguard DNS Github](https://github.com/AdguardTeam/AdGuardSDNSFilter) |

Untuk menggunakan, edit `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  adaway:
    type: http
    behavior: classical
    path: "./rule_provider/adaway.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/adaway.yaml
    interval: 14400 # Update rules every 4 hours
  adguard_dns:
    type: http
    behavior: classical
    path: "./rule_provider/AdguardDNS.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/AdguardDNS.yaml
    interval: 14400 # Update rules every 4 hours
  
rules:
# Block ads
- RULE-SET,adaway,REJECT
- RULE-SET,adguard_dns,REJECT
```

Setelah di test dengan situs [Adblock Test](https://d3ward.github.io/toolz/adblock.html) hasilnya:

[![2022-06-08-213555-1920x986-scrot.png](https://i.postimg.cc/0yCf9YQK/2022-06-08-213555-1920x986-scrot.png)](https://postimg.cc/CRzDNfbw)

Hasil di situs adblock test bisa berbeda beda karena source list diupdate setiap hari.
