# Tutorial Install COPS
COPS itu apa ya ? Silahkan kunjungi http://blog.slucas.fr/en/oss/calibre-opds-php-server

## Instalasi
```bash
   opkg update; opkg install php5-mod-dom php5-mod-gd php5-mod-json php5-mod-pdo php5-mod-pdo-sqlite php5-mod-sqlite php5-mod-sqlite3 php5-mod-xml php5-mod-xmlreader php5-mod-xmlwriter php5-mod-zip
```

## Konfigurasi
- Edit file **/etc/php.ini** di bagian:
```bash
   ; Dynamic Extensions
   extension=dom.so
   extension=pdo.so
   extension=pdo_sqlite.so
   extension=sqlite.so
   extension=sqlite3.so
   extension=xml.so
   extension=xmlreader.so
   extension=xmlwriter.so
```

- Buat folder web-nya:
```bash
   mkdir -p /www/cops 
```

- Buat folder nampung buku-bukunya:
```bash
   mkdir -p /mnt/usb/books
```

- Download file berikut:
```bash
   https://docs.google.com/file/d/0B8uKhOOykTAteWNKYTF6SFd4emc/edit?pli=1
   Ekstrak isinya ke folder /www/cops
```


- Edit **/www/cops/configlocal.php** di bagian directorynya:
```bash
   $config['calibre_directory'] = '/mnt/usb/books/';
```

- Perbaiki *symlink* dari **/www/cops/books** dengan cara pakai PuTTY edit link nya arahkan ke **/mnt/usb/books**
- Copy - kan isi dari folder Calibre Library dari komputer ke folder/mnt/usb/books, **pastikan metadata.db juga tercopy semuanya**
- Buka browser arahkan ke **http://192.168.1.1/cops**

- Selesai dan terimakasih kepada yang telah buat aplikasi ini
- Supaya bisa terintegrasi dengan Aldiko dan semacamnya, tinggal edit catalog dan arahkan URL nya ke **http://192.168.1.1/cops/feed.php**
- Alhasil buku-buku anda tersusun rapi dan bisa di search dengan Aldiko.

Kontribusi:
- Terima Kasih kepada (Johan Rusli)[https://www.facebook.com/johan.rusli]
- Terima Kasih kepada (OpenWrt Indonesia)[http://www.facebook.com/groups/openwrt]

Referensi:
- https://www.facebook.com/notes/openwrt-indonesia/tutorial-install-cops/840685975972428/
