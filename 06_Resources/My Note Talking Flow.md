---
tags:
  - resource
  - core
  - system
created: 2025-05-09
---

# Sistem Produktivitas Obsidian

## Struktur Folder Utama

```
📁 00 Inbox          → Catatan cepat, ide mentah, fleeting notes
📁 01 Zettels        → Catatan atomic, insight pribadi dengan ID 
📁 02 Articles       → Ringkasan artikel, bacaan, materi penting 
📁 03 Projects       → Semua proyek aktif (coding, konten YouTube, dll)
📁 04 Daily Journal  → Jurnal harian dan refleksi diri
📁 05 Logs           → Personal log: pengalaman, eksperimen, catatan lapangan 
📁 06 Resources      → Referensi berguna, rujukan tetap (tools, panduan, cheatsheet) 
📁 Templates         → Semua template Templater
```

---

## Alur Kerja Harian

1. **Pagi**: Buka `04_Daily_Journal`, isi agenda dan niat hari itu.
2. **Saat belajar atau bekerja**:
   - Jika menemukan ide → catat cepat di `00_Inbox`.
   - Jika membaca artikel → simpan di `02_Articles` + buat ringkasan.
   - Jika ada insight → ubah jadi Zettel di `01_Zettels`.
   - Jika bereksperimen (misal install Arch, debug error) → catat di `05_Logs`.
   - Jika mengerjakan proyek → dokumentasikan di `03_Projects`.

3. **Malam**:
   - Refleksi di `04_Daily_Journal`
   - Review Inbox → sortir ke folder tujuan

---

## Tips Penggunaan

- **Gunakan Templater** untuk membuat catatan harian, artikel, zettel, log, dst.
- **Jangan biarkan Inbox penuh**. Review setiap malam atau pagi.
- **Zettels cukup 1 ide per file**, jangan terlalu panjang.
- **Gunakan tag dan backlink antar catatan** untuk membangun jaringan pemikiran (knowledge graph).
- Tambahkan metadata (`created`, `tags`, `source`) agar rapi dan mudah dicari.

---

## Kapan Gunakan Folder Ini?

| Kegiatan                                 | Simpan di Folder           |
|------------------------------------------|-----------------------------|
| Ide mentah, fleeting note                | `00 Inbox`                  |
| Ringkasan artikel, blog                  | `01 Articles`               |
| Catatan hasil pemahaman sendiri          | `02 Zettelkasten`           |
| Catatan pengalaman (debug, eksperimen)   | `03 Logs`                   |
| Proyek coding, YouTube, dsb              | `04 Projects`               |
| Jurnal, agenda, refleksi harian          | `05 Daily`                  |
| Panduan, sumber belajar, referensi tetap | `06 Resources`              |

---

## Contoh Alur: Dari Artikel ke Zettel

1. Kamu membaca artikel → Buat ringkasan di `01 Articles` (pakai template `article-summary.md`)
2. Setelah membaca, kamu punya ide penting → Buka artikel → Gunakan Templater `zettel-from-article.md`
3. Selesai → Catatan masuk ke `02 Zettelkasten` dan siap kamu hubungkan dengan ide lain

---

## Plugin Wajib

- **Templater**: Otomatisasi template
- **Calendar**: Navigasi jurnal harian
- **Dataview**: Query jurnal, log, zettels
- **Hotkeys++ / QuickAdd** *(opsional)*: Untuk efisiensi workflow

---
