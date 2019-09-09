---
title: 'Blogging mudah dengan Gatsby + Netlify'
date: 2019-8-8 16:21:13
category: 'Article'
---

## Gatsby?

Gatsby adalah framework open source yang gratis berdasar React yang membantu developer membangun situs web dan aplikasi yang sangat cepat - Gatsby 

## Kenapa Gatsby?

Ada [banyak generator situs statis](https://www.staticgen.com/) untuk dipilih. Jekyll, Hugo, Next, dan Hexo adalah beberapa yang terkenal dan beberapa yang menarik seperti Eleventy juga. Pada awalnya, saya hanya ingin membuat sesuatu yang dapat menghasilkan HTML secara langsung dan JavaScript app yang berat tidak mungkin lebih baik daripada HTML dan CSS sederhana.

Namun, saya sadari bahwa SSG seperti Gatsby memanfaatkan kekuatan pemisahan kode / data, pra-load, pra-cache, pengoptimalan gambar, dan segala macam peningkatan kinerja yang akan sulit atau tidak mungkin dilakukan dengan HTML biasa.

## Hal yang saya sukai dari Gatsby

- No page reloads  - situs ini sekarang menjadi SPA (single page app), dan ketika mengklik halaman internal apa pun dari dalam situs web tidak perlu lagi memuat semua page.
- Image optimization - semua gambar secara otomatis dihapus dari metadata, optimized, resized, lazy-loaded, dan compressed
- Pre-fetch resources - Gatsby mendeteksi tautan apa yang tersedia pada halaman tertentu dan memuat data itu ke dalam cache
- Bundling and minification - kode diperkecil, dibundel, dan disajikan.
- Server side ditampilkan pada waktu pembuatan

Gatsby juga menggunakan [GraphQL](https://graphql.org/) untuk mengimpor data secara default, bahkan jika Anda tidak tahu tata bahasanya, Anda dapat secara intuitif memahami kueri terstruktur sehingga Anda dapat mengembangkannya tanpa belajar. Halaman dapat dikembangkan seperti komponen, dan pada dasarnya memberikan kemampuan untuk memasukkan data ke dalam komponen.

Tunggu apa lagi, ayo buat!. Klik [tautan ini](https://www.gatsbyjs.org/starters/?v=2)

# Getting Started 😎

##  Create a Gatsby site.

💻 Buka Commant Prom 💻

```sh
# create a new Gatsby site using the blog starter
$ npx gatsby new my-blog-starter https://github.com/gatsbyjs/gatsby-starter-blog
```

> Jika kamu tidak menggunakan `npx`, following [Gatsby Getting Started](https://www.gatsbyjs.org/docs/quick-start)

```sh
$ npm install -g gatsby-cli
$ gatsby new my-blog-starter https://github.com/gatsbyjs/gatsby-starter-blog
```

##  Start developing.

```sh
$ cd my-blog-starter/
$ gatsby develop
```

Buka source code dan mulai mengedit!

Situs Anda sekarang berjalan di http: // localhost: 8000!

Catatan: Kamu akan melihat tautan kedua: http: // localhost: 8000 / ___ graphql. Ini adalah tools yang dapat kamu gunakan untuk bereksperimen dengan menanyakan data kamu. Pelajari lebih lanjut tentang menggunakan tools ini di [tutorial Gatsby](https://www.gatsbyjs.org/tutorial/part-five/#introducing-graphiql).

Buka direktori my-blog-starter di editor kode favorit kamu saya menggunakan [Visual Studio Code](https://code.visualstudio.com/) dan edit src / pages / index.js. Simpan perubahan dan reaload browser kamu! Viola! Situs Kamu sudah bisa di akses 😎

## 5. Publish with [netlify](https://netlify.com)

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gatsbyjs/gatsby-starter-blog)

:bulb: jika Kamu ingin menggunakan halaman github, tambahkan skrip berikut ke package.json

```json
"scripts": {
    "deploy": "gatsby build && gh-pages -d public -b master -r 'git@github.com:${your github id}/${github page name}.github.io.git'"
}
```
