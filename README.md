# openclash adblock
Ini adalah adblock untuk openclash, source list diambil dari **Energized Blu** yang digabung dengan **Xtreme Extension Pack**. Source list diupdate setiap hari secara otomatis oleh bot github.

Untuk menggunakan, modifikasi `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  adblock:
    type: http
    behavior: classical
    path: "./rule_provider/energized_blu_adblock.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/energized_blu_adblock.yaml
    interval: 14400 # Update rules every 4 hours
rules:
# Block ads
- RULE-SET,adblock,REJECT
```

**Sumber: [Energized Protection](https://github.com/EnergizedProtection/block)**
