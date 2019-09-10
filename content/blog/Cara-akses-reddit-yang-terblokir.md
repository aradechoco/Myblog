---
title: 'Cara akses reddit yang terblokir'
date: 2019-9-9 10:21:13
category: 'Article'
---

![](./images/reddit.png)

Mengakses [Reddit](https://en.wikipedia.org/wiki/Reddit) dari Indonesia bisa dengan VPN, bypass situs web yang diblokir melalui berkas hosts, atau memakai DNSCrypt.

Reddit sendiri merupakan sebuah situs komunitas yang menurut saya sangat bermanfaat, karena sebelum itu saya sering mengunjungi situs reddit hanya untuk mecari sebuah informasi terbaru mengenai teknologi.

Bagaimana cara agar saya tetap dapat mengakses situs reddit walaupun sudah di blokir oleh provider indonesia.

## Dengan VPN
VPN yang bagus sampai saat ini adalah ProtonVPN (Gratis) dan Private Internet Access (Berbayar). Mereka mempunyai kebijakan privasi yang bagus. Kamu harus membuat dan mendaftar akun dahulu untuk menggunakannya.

## Melalui hosts

# Windows 
Cara ini mudah tanpa harus terkoneksi ke layanan lain, seperti VPN. Tetapi kamu harus mempunyai hak akses ke Sistem Operasimu.

Hal yang cukup sulit adalah menyunting berkas hosts di ponsel. Kamu tidak mempunyai hak akses root di Sistem Operasi Android atau iOS bawaan dari pabrik, kamu harus me-root atau jailbreak ponselmu.

Jika kamu berada di desktop dan menggunakan Sistem Operasi Linux, macOS, atau Windows hal ini cukup mudah.

Di Linux, macOS, Android, atau iOS silakan sunting `/etc/hosts` dengan akses root.
Di Windows, silakan sunting `C:\Windows\System32\drivers\etc\hostsdengan` akses administrator
Copas script dibawah ini, tepat dibawah tulisan `127.0.0.1 localhost`

```
## Reddit
151.101.129.140  redd.it
54.172.97.229    redd.it
151.101.129.140  i.redd.it

151.101.129.140  reddit.com
151.101.129.140  4x.reddit.com
151.101.129.140  api.reddit.com
151.101.129.140  about.reddit.com
151.101.129.140  blog.reddit.com
151.101.129.140  bt.reddit.com
151.101.129.140  e.reddit.com
151.101.129.140  en.reddit.com
151.101.129.140  en-us.reddit.com
151.101.129.140  forum.reddit.com
151.101.129.140  gateway.reddit.com
151.101.129.140  help.reddit.com
151.101.129.140  i.reddit.com
151.101.129.140  m.reddit.com
151.101.85.140   m.reddit.com
151.101.129.140  nm.reddit.com
151.101.129.140  np.reddit.com
151.101.129.140  nsfw.reddit.com
151.101.129.140  oauth.reddit.com
151.101.129.140  out.reddit.com
54.174.14.76     out.reddit.com
151.101.129.140  pay.reddit.com
151.101.129.140  ssl.reddit.com
151.101.129.140  test.reddit.com
151.101.129.140  ww.reddit.com
151.101.129.140  www.reddit.com

192.0.79.33      redditblog.com
192.0.79.33      www.redditblog.com

151.101.129.140  redditgifts.com
151.101.129.140  www.redditgifts.com

151.101.129.140  redditmedia.com
151.101.129.140  events.redditmedia.com
151.101.129.140  g.redditmedia.com
151.101.129.140  i.redditmedia.com
151.101.129.140  pixel.redditmedia.com
151.101.129.140  stats.redditmedia.com
151.101.129.140  www.redditmedia.com
151.101.129.140  a.thumbs.redditmedia.com
151.101.129.140  b.thumbs.redditmedia.com

151.101.129.140  redditstatic.com
151.101.129.140  www.redditstatic.com

151.101.129.140  reddituploads.com
151.101.129.140  i.reddituploads.com
151.101.129.140  www.reddituploads.com
##---
```
# Android
Pastikan android anda sudah diroot.
Download aplikasi root explorer apk.
Setelah itu anda cari file hosts di folder `system/etc/`
Anda Edit file tersebut dengan text di bawah ini, dan letakkan tepat dibawah `127.0.0.1 localhost`

```
## Reddit
151.101.129.140  redd.it
54.172.97.229    redd.it
151.101.129.140  i.redd.it

151.101.129.140  reddit.com
151.101.129.140  4x.reddit.com
151.101.129.140  api.reddit.com
151.101.129.140  about.reddit.com
151.101.129.140  blog.reddit.com
151.101.129.140  bt.reddit.com
151.101.129.140  e.reddit.com
151.101.129.140  en.reddit.com
151.101.129.140  en-us.reddit.com
151.101.129.140  forum.reddit.com
151.101.129.140  gateway.reddit.com
151.101.129.140  help.reddit.com
151.101.129.140  i.reddit.com
151.101.129.140  m.reddit.com
151.101.85.140   m.reddit.com
151.101.129.140  nm.reddit.com
151.101.129.140  np.reddit.com
151.101.129.140  nsfw.reddit.com
151.101.129.140  oauth.reddit.com
151.101.129.140  out.reddit.com
54.174.14.76     out.reddit.com
151.101.129.140  pay.reddit.com
151.101.129.140  ssl.reddit.com
151.101.129.140  test.reddit.com
151.101.129.140  ww.reddit.com
151.101.129.140  www.reddit.com

192.0.79.33      redditblog.com
192.0.79.33      www.redditblog.com

151.101.129.140  redditgifts.com
151.101.129.140  www.redditgifts.com

151.101.129.140  redditmedia.com
151.101.129.140  events.redditmedia.com
151.101.129.140  g.redditmedia.com
151.101.129.140  i.redditmedia.com
151.101.129.140  pixel.redditmedia.com
151.101.129.140  stats.redditmedia.com
151.101.129.140  www.redditmedia.com
151.101.129.140  a.thumbs.redditmedia.com
151.101.129.140  b.thumbs.redditmedia.com

151.101.129.140  redditstatic.com
151.101.129.140  www.redditstatic.com

151.101.129.140  reddituploads.com
151.101.129.140  i.reddituploads.com
151.101.129.140  www.reddituploads.com
##---
```

#Linux
Anda buka terminal, dan edit file hosts yang ada di dalam etc caranya dengan memasukkan command ini. `$ sudo nano /etc/hosts`
Lalu copy dan paste teks dibawah ini tepat di bawah atau sesudah teks `127.0.0.1 localhost`

```
## Reddit
151.101.129.140  redd.it
54.172.97.229    redd.it
151.101.129.140  i.redd.it

151.101.129.140  reddit.com
151.101.129.140  4x.reddit.com
151.101.129.140  api.reddit.com
151.101.129.140  about.reddit.com
151.101.129.140  blog.reddit.com
151.101.129.140  bt.reddit.com
151.101.129.140  e.reddit.com
151.101.129.140  en.reddit.com
151.101.129.140  en-us.reddit.com
151.101.129.140  forum.reddit.com
151.101.129.140  gateway.reddit.com
151.101.129.140  help.reddit.com
151.101.129.140  i.reddit.com
151.101.129.140  m.reddit.com
151.101.85.140   m.reddit.com
151.101.129.140  nm.reddit.com
151.101.129.140  np.reddit.com
151.101.129.140  nsfw.reddit.com
151.101.129.140  oauth.reddit.com
151.101.129.140  out.reddit.com
54.174.14.76     out.reddit.com
151.101.129.140  pay.reddit.com
151.101.129.140  ssl.reddit.com
151.101.129.140  test.reddit.com
151.101.129.140  ww.reddit.com
151.101.129.140  www.reddit.com

192.0.79.33      redditblog.com
192.0.79.33      www.redditblog.com

151.101.129.140  redditgifts.com
151.101.129.140  www.redditgifts.com

151.101.129.140  redditmedia.com
151.101.129.140  events.redditmedia.com
151.101.129.140  g.redditmedia.com
151.101.129.140  i.redditmedia.com
151.101.129.140  pixel.redditmedia.com
151.101.129.140  stats.redditmedia.com
151.101.129.140  www.redditmedia.com
151.101.129.140  a.thumbs.redditmedia.com
151.101.129.140  b.thumbs.redditmedia.com

151.101.129.140  redditstatic.com
151.101.129.140  www.redditstatic.com

151.101.129.140  reddituploads.com
151.101.129.140  i.reddituploads.com
151.101.129.140  www.reddituploads.com
##---
```

## Dengan DNSCrypt
DNSCrypt juga adalah pilihan yang bagus. Ia akan mengenkripsi lalu lintas DNS antara pengguna dan DNS Resolver. Ini akan mengurangi pelacakan dari ISP. Tetapi kamu harus menggunakan hak akses root untuk menjalankan ini.
Opsi yang pertama dan ketiga yang membuat jaringan menjadi lebih aman adalah nilai tambah. Opsi yang kedua adalah cara yang cukup mudah untuk mengakses Reddit untuk penggunaan sehari-hari.