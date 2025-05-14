---
source: https://vim.rtorr.com/
tags:
  - resource
  - vim
  - text-editor
  - cheatsheet
---

# Vim Cheatsheet

## Global

- :help keyword — Buka bantuan untuk keyword
- :saveas file — Simpan file dengan nama baru
- :close — Tutup jendela saat ini
- :terminal — Buka jendela terminal
- K — Buka halaman manual untuk kata di bawah kursor

## Pergerakan Kursor

- h j k l — Gerak kiri, bawah, atas, kanan
- w / W — Lompat ke awal kata berikutnya
- e / E — Lompat ke akhir kata berikutnya
- b / B — Lompat ke awal kata sebelumnya
- ge / gE — Lompat ke akhir kata sebelumnya
- 0 / ^ / $ / g_ — Awal, awal non-spasi, akhir, akhir non-spasi baris
- gg / G — Awal / akhir dokumen
- % — Lompat ke pasangan tanda kurung
- fx / Fx — Lompat ke karakter x berikutnya / sebelumnya
- ; / , — Ulangi gerakan f/F sebelumnya maju / mundur
- } / { — Lompat ke paragraf berikutnya / sebelumnya
- zz / zt / zb — Posisikan kursor di tengah / atas / bawah layar
- Ctrl + d / Ctrl + u — Scroll setengah halaman ke bawah / atas
- Ctrl + f / Ctrl + b — Scroll satu halaman ke bawah / atas

## Mode Insert

- i / I — Masuk mode insert sebelum kursor / di awal baris
- a / A — Masuk mode insert setelah kursor / di akhir baris
- o / O — Buka baris baru di bawah / atas
- ea — Masuk mode insert di akhir kata
- Ctrl + h / Ctrl + w — Hapus karakter / kata sebelum kursor
- Ctrl + n / Ctrl + p — Auto-complete ke depan / belakang
- Ctrl + o — Jalankan satu perintah normal dari mode insert
- Esc / Ctrl + c — Keluar dari mode insert

## Pengeditan

- r / R — Ganti satu / beberapa karakter
- J / gJ — Gabungkan baris dengan / tanpa spasi
- cc / C — Ganti seluruh baris / dari kursor ke akhir baris
- ciw / cw / ce — Ganti kata saat ini / hingga akhir kata
- s / S — Hapus dan ganti karakter / baris
- xp — Tukar dua karakter
- u / Ctrl + r — Undo / redo
- . — Ulangi perintah terakhir

## Copy, Paste, dan Hapus

- yy / Y — Salin baris
- dd — Hapus baris
- p / P — Tempel setelah / sebelum kursor
- x / X — Hapus karakter di bawah / sebelum kursor
- d + gerakan — Hapus teks berdasarkan gerakan (misal: dw, d$)
- y + gerakan — Salin teks berdasarkan gerakan (misal: yw, y$)

## Pencarian

- /pattern — Cari ke depan
- ?pattern — Cari ke belakang
- n / N — Ulangi pencarian ke arah yang sama / berlawanan

## Penyimpanan dan Keluar

- :w — Simpan
- :q — Keluar
- :wq / :x — Simpan dan keluar
- :q! — Keluar tanpa menyimpan
- ZZ — Simpan dan keluar (shortcut)

