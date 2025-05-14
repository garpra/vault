---
tags:
  - experience
created: 2025-05-07
---

# Wine Error freetype2 Not Found

## Cerita & Konteks
Saat saya mau menginstall winetricks `vcrun2019`, floating window dari instalasi vcrun2019 malah hitam, dan muncul error

```bash

Wine cannot find the FreeType font library.  To enable Wine to
use TrueType fonts please install a version of FreeType greater than
or equal to 2.0.5.
http://www.freetype.org
Wine cannot find the FreeType font library.  To enable Wine to
use TrueType fonts please install a version of FreeType greater than
or equal to 2.0.5.
http://www.freetype.org

```

Hal yang harus dilakukan adalah menginstal freetype2 agar floating windownya tidak hitam, untuk menginstallnya bisa dengan

```bash
sudo pacman -S lib32-freetype2
```

## Hasil
Dapat menginstall `vcrun2019` tanpa error pada **winetricks**, dan melanjutkan instalasi game saya yang menggunakan `vcrun2019` atau package yang membutuhkan **freetype2**  lainnya.

## Refleksi
Troubleshooting dalam linux merupakan hal yang biasa, ini juga dapat membantu kita memahami linux secara mendalam dan membantu dalam problem solving pada programming

## Terkait
- [[aagl-tidak-ada-pembaruan]]