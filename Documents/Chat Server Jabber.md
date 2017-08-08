# Chat Server Jabber

## Install package:
```bash
   opkg update; opkg install prosody libexpat
```

## Konfigurasi:
```bash
   nano /etc/prosody/prosody.cfg.lua
```

```lua
VirtualHost "localhost"
 
VirtualHost "openwrt-id"
	enable = true
--	ssl = { -- optional
--		key = "/etc/prosody/certs/example.com.key";
--		certificate = "/etc/prosody/certs/example.com.crt";
--		}
```

Permission:
```bash
   chmod 755 /etc/prosody/prosody.cfg.lua
   cd /etc/prosody && chown prosody:prosody $(find -type d)
```

Start prosody:
```bash
   /etc/init.d/prosody start
```

Adduser:
```bash
   prosodyctl adduser user1@openwrt-id
``

Jabber Client:
- Android
	Jtalk

- Windows
	Gajin

Kontribusi:
- Terima Kasih kepada [Tisaros Obengkumana](https://www.facebook.com/tisaros.obengkumana)
- Terima Kasih kepada [OpenWrt Indonesia](https://www.facebook.com/groups/openwrt)

Referensi:
- https://www.facebook.com/notes/openwrt-indonesia/chat-server-jabber/661327953908232/
- http://fekkyreviant.wordpress.com/2012/01/26/install-prosodyjabber-server-di-openwrt/
