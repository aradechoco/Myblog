---
title: 'Migrasi Dari Wordpress ke Gatsby'
date: 2019-8-8 09:17:13
category: 'Gatsby'
---


## Kenapa Gatsby?

Ada [banyak generator situs statis] (https://www.staticgen.com/) untuk dipilih. Jekyll, Hugo, Next, dan Hexo adalah beberapa yang besar, dan aku pernah mendengar beberapa yang menarik seperti Eleventy juga. Pada awalnya, saya pikir saya hanya ingin sesuatu yang menghasilkan HTML langsung, dan aplikasi JavaScript yang berat tidak mungkin lebih baik daripada HTML dan CSS sederhana.

Namun, saya menyadari bahwa SSG seperti Gatsby memanfaatkan kekuatan pemisahan kode / data, pra-pemuatan, pra-cache, pengoptimalan gambar, dan segala macam peningkatan kinerja yang akan sulit atau tidak mungkin dilakukan dengan HTML lurus.

Karena saya terutama menulis JavaScript hari ini, saya pasti menginginkan SSG yang berjalan di Node.js, dan jika menggunakan React, bahkan lebih baik. Saya menguji beberapa situs yang berjalan di Gatsby dan ya - mereka cepat. Sangat cepat.

Beberapa hal yang saya sukai dari Gatsby:

- Tidak ada ulang halaman - situs ini sekarang menjadi SPA (aplikasi satu halaman), dan mengklik halaman internal apa pun dari dalam situs web tidak perlu memuat sumber yang sama sekali baru
- Optimalisasi gambar - semua gambar secara otomatis dihapus dari metadata, dioptimalkan, diubah ukurannya, malas dimuat, dan dikompresi
- Pra-pengambilan sumber daya - Gatsby mendeteksi tautan apa yang tersedia pada halaman tertentu dan memuat data itu ke dalam cache
- Bundling dan minifikasi - kode diperkecil, dibundel, dan disajikan
- Sisi server ditampilkan pada waktu pembuatan
- Siapa pun dapat mengedit posting saya! Jika Anda melihat kesalahan ketik atau kesalahan, cukup garpu repo dan lakukan perubahan!
- Setiap kali saya mendorong ke repo, situs akan secara otomatis digunakan.

Sangat sedikit kode boilerplate diperlukan untuk memulai dengan Gatsby. Saya baru saja memotong [Gatsby Advanced Starter] (https://github.com/vagr9k/gatsby-advanced-starter/), sebuah yayasan yang sangat sederhana, minimalis, sepenuhnya bebas-UI menurut hati saya sendiri, dan mulai bekerja dengannya.

Sejauh ini, satu-satunya hal yang saya tidak suka adalah bahwa Gatsby tampaknya mengubah zoom situs setelah membangun entah bagaimana, jadi gaya saya tidak sama persis.

Saya harus menyebutkan bahwa saya memindahkan host saya dari NearlyFreeSpeech.net ke [Netlify] (https://www.netlify.com/), yang luar biasa. Saya benar-benar tidak bisa mengatakan cukup tentang mereka. Saya sangat terkesan dengan betapa cepat dan mudahnya mengatur apa pun yang saya inginkan.

## Proses migrasi 

Saya telah menunda bermigrasi ke situs statis selama berbulan-bulan, karena saya tahu itu akan menjadi waktu yang sangat lama, obsesi, dan banyak pekerjaan. Tetapi pada akhirnya, saya bisa memindahkan semuanya dalam 10 hari, jadi itu benar-benar bukan akhir dari dunia. Saya akan memberi Anda dasar-dasar apa yang saya lakukan jika Anda juga ingin beralih:

- Pertama, saya mengunduh XML dari WordPress di bagian Alat -> Ekspor.
- Kemudian saya menggunakan alat [ExitWP] (https://github.com/thomasf/exitwp) untuk mengubah XML menjadi Markdown. Ini melakukan sekitar 50% dari pekerjaan mengubah posting.
- Saya harus melalui dan menggunakan [HTML to Markdown Table Converter] (https://jmalarcon.github.io/markdowntables/) secara individual, secara manual indent semua blok kode, secara manual mengkonversi semua blok kode empat-indent spasi ke gaya GitHub kode kunci berpagar, dan memperbaiki semua daftar yang rusak.
- Saya menggunakan Prettier pada semua file penurunan harga untuk mencoba membuatnya konsisten.

Berikut kode yang saya gunakan untuk menjalankan:

```bash
cd content/posts
prettier
  --print-width 100
  --no-semi
  --single-quote
  --jsx-single-quote
  --trailing-comma es5
  --arrow-parens avoid
  --parser "markdown"  "*.md"
```
- Saya pada dasarnya harus melakukan ulang semua gaya, menggunakan [Primitive] (https://taniarascia.github.io/primitive) sebagai dasar dari sistem style karena saya belum tertarik pada ide menggunakan CSS- di-JS belum.
- Saya `scp`'d gambar dari server ke folder` gambar`.
- Saya menggunakan beberapa regex untuk menghapus semua thumbnail WordPress, mis. semua gambar yang berakhiran `150x150`,` 300x300` dan `1024px1024px` atau variasi apa pun darinya, kemudian lakukan pencarian / ganti semua untuk memastikan semua file terhubung ke` ../ images / file.ext` alih-alih `wp -content / uploads / file.ext`, lalu hapus nama url thumbnail dari semua posting.
- Saya secara manual menyimpan semua thumbnail saya dan memindahkannya ke folder thumbnail sehingga saya dapat menggunakannya kembali dengan mudah di beberapa posting.
- Terapkan kembali mode malam dan buat mode malam baru menggunakan [React Context API] (https://www.gatsbyjs.org/blog/2019-01-31-using-react-context-api-with-gatsby/) sebagai pembungkus.
- Bermain-main dengan banyak kencan sampai aku bisa bekerja dengan benar.
- Bermain-main dengan Disqus banyak sampai saya berfungsi dengan benar - gunakan komponen Disqus yang berbeda dari yang ada di Advanced Starter.

Dari sana itu hanya masalah membangun semua halaman, belajar cukup GraphQL untuk membuat pertanyaan yang tepat, membuat beberapa array statis untuk podcast saya, berbicara, dan menerbitkan data artikel, dan kemudian banyak pembersihan kecil dan tweaker.

Saya cukup lelah karena sudah lewat tengah malam sekarang, tetapi saya terlalu bersemangat untuk tidak membuat posting kecil merayakan langkah selanjutnya dalam perjalanan situs web ini. Saya merasa senang bahwa semua posting saya sekarang disimpan dengan aman di kontrol versi dan penurunan harga. Sebenarnya sangat melegakan bagi saya untuk mengetahui bahwa mereka tidak berantakan di dalam beberapa database MySQL yang kikuk, tetapi mudah dibaca, ditulis, diedit, dan berbagi file penurunan harga. Sekarang jika saya ingin pindah ke SSG lain di masa depan, itu akan sangat mudah.

Saya dapat menulis lebih banyak tentang ini di masa depan jika ada yang memiliki pertanyaan lebih spesifik tentang Gatsby, React, atau Netlify. Jika Anda melihat ada yang rusak tentang situs baru, beri tahu saya!

Source : https://www.taniarascia.com/migrating-from-wordpress-to-gatsby/
