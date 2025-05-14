---
tags:
  - project
  - linux
  - browser
---

# Konfigurasi Floorp

## Konfigurasi Floorp Browser

1. Install Floorp dengan pacman
	```bash
	sudo pacman -S floorp-bin
	```
2. Pergi ke setting
3. Bagian General matikan
	- Open previous window and tab
	- Enable Floorp Notes Sync
4. Bagian Design ubah Theme Mode dan Website Appearance ke Dark
5. Bagian Workspace matikan "Enable Workspaces"
6. Bagian Home ubah Floorp Home Background ke "Disable Background" dan matikan Shortcut pada Firefox Home Content
7. Bagian Privacy & Security ubah DNS over HTTPS ke Max Protection
8. Instal Extension yang saya gunakan:
	- **Tokyo Night by Milav**
	  Menyesuaikan dengan dotfiles saya dimana menggunakan tema Tokyo Night
	- **uBlock Origin by Raymond Hill**
	  Menghilangkan ads/iklan yang ada dalam website

## Log - 7 Mei 2025
- Instalasi Floorp menggunakan pacman
- Setup dan konfigurasi beberapa pengaturan bawaan dari Floorp
- Install extension yang dibutuhkan 
- Styling css pada homepage untuk menghilangkan link

## Masalah Solusi

Untuk dapat menghilangkan link pada pojok kanan bawah buka halaman `about: support` dan cari Profile Directory pilih Open Directory, Buka folder chrome/ dan edit file userContent.css

Tambahkan code ini pada bagian bawa file
```css
@-moz-document url-prefix(about:home), url-prefix(about:newtab) {
/* CSS code goes here */
  #floorp {
    display: none;
  }
}
```

## Catatan & Refleksi 

Tambahkan insight, hal menarik selama proses, atau ide untuk video selanjutnya.

## Terkait
- [...]