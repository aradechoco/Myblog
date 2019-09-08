---
title: 'Blogging mudah dengan Gatsby + Netlify'
date: 2019-8-8 09:17:13
category: 'Gatsby'
---

## Gatsby?

Gatsby adalah kerangka kerja sumber terbuka dan gratis berdasarkan React yang membantu pengembang membangun situs web dan aplikasi yang sangat cepat - Gatsby 

## Kenapa Gatsby?

Ada [banyak generator situs statis] (https://www.staticgen.com/) untuk dipilih. Jekyll, Hugo, Next, dan Hexo adalah beberapa yang besar, dan beberapa yang menarik seperti Eleventy juga. Pada awalnya, saya pikir hanya ingin sesuatu yang dapat menghasilkan HTML secara langsung dan aplikasi JavaScript yang berat tidak mungkin lebih baik daripada HTML dan CSS sederhana.

Namun, saya sadari bahwa SSG seperti Gatsby memanfaatkan kekuatan pemisahan kode / data, pra-load, pra-cache, pengoptimalan gambar, dan segala macam peningkatan kinerja yang akan sulit atau tidak mungkin dilakukan dengan HTML biasa.

## Hal yang saya sukai dari Gatsby

- No page reloads  - situs ini sekarang menjadi SPA (single page app), dan ketika mengklik halaman internal apa pun dari dalam situs web tidak perlu lagi memuat semua page.
- Image optimization - semua gambar secara otomatis dihapus dari metadata, optimized, resized, lazy-loaded, dan compressed
- Pre-fetch resources - Gatsby mendeteksi tautan apa yang tersedia pada halaman tertentu dan memuat data itu ke dalam cache
- Bundling and minification - kode diperkecil, dibundel, dan disajikan.
- Server side ditampilkan pada waktu pembuatan

Gatsby juga menggunakan GraphQL untuk mengimpor data secara default, bahkan jika Anda tidak tahu tata bahasanya, Anda dapat secara intuitif memahami kueri terstruktur sehingga Anda dapat mengembangkannya tanpa belajar. Halaman dapat dikembangkan seperti komponen, dan pada dasarnya memberikan kemampuan untuk memasukkan data ke dalam komponen.

Jika masih terlihat rumit, ayo buat! Gatsby adalah tempat bagi pengembang. Klik tautan ini https://www.gatsbyjs.org/starters/?v=2
