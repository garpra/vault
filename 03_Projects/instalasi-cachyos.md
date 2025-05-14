---
tags:
  - project
  - linux
  - cachyos
---

# Instalasi CachyOS

## Tujuan Instalasi

- Lebih mudah di install dibandingkan Archlinux karena instalasi menggunakan GUI
- Performa gaming lebih baik dari Archlinux karena memiliki linux kernel dan scheduler yang sudah di optimasi
- Tidak perlu terlalu lama untuk konfigurasi karena sudah di setup dengan optimal

## Langkah-langkah

1. Buat bootable USB untuk cachyos iso
	```bash
	sudo dd if=cachyos.iso of=/dev/sda bs=4M status=progress
	```
2. Menghubungkan wifi dan "Manually Block" pada setting Power & Battery supaya layar tidak mati selama proses instalasi
3. Tekan Launch Installer dan tunggu sesaat
4. Pilih Bootloader: GRUB
5. Pilih bahasa: America English
6. Pilih Region & Zone: Asia Jakarta
7. Pilih Keyboard: English(US) Default
8. Bagian Lartition pilih **"Erase disk"** dengan filesystem **"Btrfs"**
9. Pilih DE atau WM, saya memilih Hyprland
10. Pilih package yang diperlukan --> [[#Package Pilihan]]
11. Isikan nama anda, nama komputer, dan password
12. Tunggu instalasi selesai, proses akan cukup lama tergantung koneksi internet
13. Shutdown CachyOS dan cabut flashdisk
14. Nyalakan Laptop dan login ke Akun yang sudah dibuat

## Package Pilihan

CachyOS Packages: 
- cachyos-ananicy-rules
- cachyos-hello
- cachyos-kernel-manager
- cachyos-packageinstaller
- cachyos-settings

Base-devel + Common Packages
- Matikan X-system jika menggunakan Wayland
- Network:
	- networkmanager
	- wpa_supplicant
	- wireless_regdb
- Matikan Firewall
- Matikan Bluetooth
- Packages Management
	- pacman-contrib
	- pkgfile
	- rebuild-detector
- Desktop Integration
	- gst-libav
	- gst-plugin-pipewire
	- libgsf
	- xdg-user-dirs
	- xdg-utils
- Filesystem
	- smartmontools
	- unrar
	- unzip
	- xz
- Fonts
	- noto-fonts
	- noto-fonts-emoji
- Audio
	- pipewire-pulse
	- wireplumber
	- rtkit
- Aktifkan seluruh Hardware
- Aktifkan seluruh Power
- Some application selection
	- duf
	- findutils
	- git
	- hwinfo
	- inxi
	- fastfetch
	- wget
	- ripgrep
	- openssh

CPU spesific Microcode updates packages: 
- intel-ucode

## Sesudah Instalasi

1. Ganti default shell ke bash terlebih dahulu untuk menghapus konfigurasi bawaan fish dari CachyOS
	```bash
	chsh -s /bin/bash
	```

2. Logout dengan command
	```bash
	exit
	```

3. Login ulang denga memasukkan username dan password

4. Menghubungkan wifi dengan command
	```bash
	nmcli d wifi connect <SSID> password <PASSWORD>
	```

5. Hapus package fish beserta dependency
	```bash
	sudo pacman -Rnsc fish
	```

6. Install package yang digunakan, yang terhapus setelah hapus package fish
	```bash
	sudo pacman -S eza fastfetch fzf pkgfile fish
	```

7. Hapus folder konfigurasi bawaan fish
	```bash
	rm -rf .config/fish
	```

8. Kembalikan shellnya menjadi fish
	```bash
	chsh -s /bin/fish
	```

9. Install AUR
	```bash
	sudo pacman -S yay
	```

10. Reboot Laptop

## Konfigurasi

### Rekomendasi
Buka CachyOS Hello dan pergi ke bagian **App/Tweaks** dan jalankan script: Clear packages cache, Remove orphans, dan Rank Mirror

### Setup sched_ext
Buka CachyOS Kernel Manager dan pergi ke bagian **sched-ext scheduler config** dan pilih schedulernya **scx_lavd** dan profilenya **Auto**

### Setup snapper
Berguna untuk membuat rollback sistem
Buka CachyOS Hello dan pergi ke bagian **App/Tweaks** dan jalankan script Install Snapper support, setelah selesai buka Btrfs Assistant dan ke Snapper Settings matikan Snapper cleanup enabled dan apply systemd changes

## Log - 6 Mei 2025
- Instalasi CachyOS menggunakan GUI Installer
- Menggunakan Filesystem Btrfs + subvolume default
- Setup hyprland dengan dotfile pada repository github
- Konfigurasi beberapa pengaturan bawaan dari CachyOS agar sesuai preferensi

## Catatan & Refleksi 

Tambahkan insight, hal menarik selama proses, atau ide untuk video selanjutnya.

## Terkait
- [...]