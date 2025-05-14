---
tags:
  - experience
  - javascript
  - programming
  - unit-test
created: 2025-05-07
---

# Mocha Chai Unit Test Javascript

## Cerita & Konteks
Saat saya mengerjakan coding challenge di codewars saya bingung code pada bagian **Sample Test** itu code javascript apa, dan saya cari tahu melalui chtgpt, saya menemukan bahwa code itu adalah code unit test untuk javascript, unit test yang biasa digunakan oleh codewars adalah mocha dan chai

Saya pun ingin mencoba menggunakannya, dan saya berpikir untuk menginstal unit testnya melalui pnpm bukan npm karena sekalian belajar pnpm, dan juga katanya pnpm ukuran node_module lebih kecil, dan saya menginstal pnpm terlebih dahulu 

```bash
npm install -g pnpm

# Jangan lupa setup agar pnpm bisa digunakan
pnpm setup
```

Saya pun membuat project node dengan pnpm dengan pergi ke folder project saya dan melakukan

```bash
pnpm init

# dan install package mocha dan chai
pnpm add --save-dev mocha chai
```

Akhir, unit test bisa digunakan
```
pnpm mocha nama_file.js
```

Di unit test saya belum belajar sama cara penggunaannya, Saya cuma mencoba menjalankan unit test saja, mungkin kedepannya saya coba belajar tentang unit test ini

## Hasil
Berhasil menjalankan unit test Javascript dengan mocha chai `pnpm mocha nama_file.js` dan melihat output test. Walapun belum belajar sama sekali syntaxnya, tapi saya tertarik untuk mencoba dan belajar unit test

## Refleksi
Ternyata unit test sangat berguna daripada saya menggunakan `console.log` disetiap baris code saya bisa gunakan unit test ini, Ini akan membantu saya dalam proyek kedepannya.

## Terkait
- [[highest-lowest-javascript]]