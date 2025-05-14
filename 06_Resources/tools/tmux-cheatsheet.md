---
source: https://tmuxcheatsheet.com/
tags:
  - resource
  - tmux
  - cli
  - cheatsheet
---

# Tmux Cheatsheet

> Catatan: Gunakan `Ctrl + b` sebagai prefix sebelum menekan tombol berikutnya.

## Manajemen Sesi

```bash
tmux                            # Mulai sesi baru
tmux new -s mysession           # Mulai sesi baru bernama 'mysession'
tmux ls                         # Daftar semua sesi
tmux a -t mysession             # Gabung ke sesi 'mysession'
tmux kill-session -t mysession  # Hapus sesi 'mysession'
```

**Shortcut**:
- `Ctrl + b d` : Detach dari sesi saat ini
- `Ctrl + b s` : Tampilkan daftar sesi
- `Ctrl + b $` : Ganti nama sesi
- `Ctrl + b ( / )` : Pindah ke sesi sebelumnya / berikutnya

## Manajemen Jendela

```bash
tmux new -s mysession -n mywindow  # Sesi baru dengan jendela bernama 'mywindow'
```

**Shortcut**:
- `Ctrl + b c` : Buat jendela baru
- `Ctrl + b ,` : Ganti nama jendela saat ini
- `Ctrl + b &` : Tutup jendela saat ini
- `Ctrl + b p / n` : Jendela sebelumnya / berikutnya
- `Ctrl + b 0–9` : Pindah ke jendela nomor tertentu
- `Ctrl + b l` : Pindah ke jendela terakhir yang aktif

## Manajemen Panel

**Membagi Panel**:
- `Ctrl + b "` : Bagi horizontal (atas–bawah)
- `Ctrl + b %` : Bagi vertikal (kiri–kanan)

**Navigasi Panel**:
- `Ctrl + b o` : Pindah ke panel berikutnya
- `Ctrl + b ;` : Pindah ke panel terakhir yang aktif
- `Ctrl + b q` : Tampilkan nomor panel
- `Ctrl + b q 0–9` : Pindah ke panel nomor tertentu
- `Ctrl + b z` : Zoom panel aktif

**Mengatur Pane**l:
- `Ctrl + b { / }` : Pindah panel ke kiri / kanan
- `Ctrl + b Space` : Ubah tata letak panel
- `Ctrl + b !` : Ubah panel menjadi jendela
- `Ctrl + b x` : Tutup panel saat ini

**Sinkronisasi Panel**:
```bash
:setw synchronize-panes   # Kirim input ke semua panel
```

## Mode Salin (Copy Mode)

**Masuk Mode Salin**:
- `Ctrl + b [` : Masuk ke copy mode
- `Ctrl + b PgUp` : Masuk ke copy mode dan scroll satu halaman ke atas

**Navigasi**:
- `h / j / k / l` : Kiri / bawah / atas / kanan
- `w / b` : Maju / mundur satu kata
- `g / G` : Awal / akhir buffer
- `/ / ?` : Cari maju / mundur
- `n / N` : Hasil pencarian berikutnya / sebelumnya

**Menyalin dan Menempel**:
- `Space` : Mulai seleksi
- `Enter` : Salin seleksi
- `Ctrl + b ]` : Tempel isi buffer

**Perintah Buffer**:
```bash
:show-buffer              # Tampilkan isi buffer
:list-buffers             # Daftar semua buffer
:save-buffer buf.txt      # Simpan buffer ke file
:delete-buffer -b 1       # Hapus buffer nomor 1
```
## Perintah Lain
- `Ctrl + b` : : Masuk ke prompt perintah tmux
- `tmux source-file ~/.tmux.conf` : Muat ulang konfigurasi
