---
name: "Tambah Konsep Baru Sakernas"
description: "Prosedur standar (SOP) untuk menambahkan konsep ketenagakerjaan baru dari modul BPS mentah ke dalam Obsidian Vault dan Quartz Website dengan metode Lossless + Parafrase."
---

# Konteks
Koleksi ini menggunakan metode **"Best of Both Worlds"**: Setiap catatan konsep harus memiliki kutipan murni 100% tanpa pengubahan makna dari dokumen sumber (untuk dasar hukum), yang disandingkan dengan ringkasan/parafrase buatan AI (untuk keterbacaan), serta tautan (wikilink) langsung ke dokumen sumber BPS.

# Instruksi Langkah-demi-Langkah untuk AI

Jika USER meminta Anda untuk menambahkan konsep baru (misalnya: "Tolong tambahkan konsep X"):

## 1. Pencarian Data Mentah (Lossless)
- Gunakan alat pencarian (misal: `grep_search`) untuk mencari kemunculan konsep "X" di dalam folder *workspace* utama yang berisi modul-modul asli (`.md`).
- Temukan dokumen dan *heading* yang memuat definisi atau aturan paling komprehensif mengenai konsep tersebut.
- **ATURAN MUTLAK:** Salin teks/paragraf definisi tersebut **persis huruf-per-huruf (100% verbatim)**. Jangan ubah strukturnya, jangan gabungkan kalimatnya.

## 2. Pembuatan File Markdown
- Buat file baru bernama `Nama Konsep.md` di dalam direktori `Obsidian_Notes\`.
- Gunakan *template* persis seperti di bawah ini:

```markdown
---
title: [Nama Konsep]
tags: [indikator, sakernas]
---

# Definisi Asli (Kutipan Resmi)
> [Masukkan teks 100% kutipan murni dari langkah 1 di sini. Sisipkan kurung siku ganda [[ ]] pada kata-kata yang sekiranya merujuk ke konsep lain]

# Ringkasan (Parafrase AI)
* [Tuliskan penjelasan/parafrase yang sangat lugas, mudah dipahami, dan menggunakan poin-poin jika perlu, berdasarkan kutipan asli di atas.] *

# Tautan ke Dokumen Modul (Klik untuk membaca teks asli)
- **File Sumber**: [[Nama File Modul Asli Beserta Ekstensinya.md]]
- **Heading Spesifik**: `Nama Heading Tempat Kutipan Berada`
```

## 3. Registrasi ke MOC (Map of Content)
- Buka file MOC yang sesuai di direktori `Obsidian_Notes\` (misalnya `MOC - Indikator Ketenagakerjaan.md` atau `MOC - Metodologi & Instrumen.md`).
- Tambahkan tautan baru ke konsep tersebut dalam bentuk list: `- [[Nama Konsep]]`.

## 4. Sinkronisasi ke Web Quartz
- Karena *Vault* ini juga dipublikasikan ke web melalui Quartz, Anda wajib menyalin *file* yang baru saja dibuat tersebut ke dalam folder rilis web.
- Salin `Obsidian_Notes\Nama Konsep.md` ke direktori `quartz_site\content\Nama Konsep.md`.
- Jika Anda mengedit file MOC di langkah 3, pastikan Anda juga menimpanya ke `quartz_site\content\`.

## 5. Konfirmasi ke USER
- Beri tahu USER bahwa file telah dibuat, MOC telah diperbarui, dan direktori Quartz telah disinkronisasikan sehingga siap untuk di-*push* ke GitHub kapan saja.
