# Cara Memulai Bug Bounty untuk Pemula (Tanpa Modal)

> Oleh Tulungagung Black Hat - uchil404 | Tulungagung, Jawa Timur

Bug Bounty = cari celah keamanan di website/app dengan izin, lalu dapat reward.

## 1. Mindset
- **Legal dulu**: hanya test di scope yang diizinkan (baca program di HackerOne/Bugcrowd)
- **Defensive**: tujuan melindungi, bukan merusak
- **Tulisan > Video**: laporan yang jelas lebih penting dari video

## 2. Tools Gratis TBH (Termux Friendly)
- **TBH-Recon** - `python3 main.py -u https://target.com --ports` untuk cek header & port
- **TBH-PhishDetector** - cek URL phising sebelum klik
- **TBH-PortScanner** - scan port dengan CVE hints
- **TBH-PassStrength** - cek password kamu sendiri

Semua ada di: `https://github.com/TulungagungBlackHat/TBH-Toolkit` (1 klik install)

## 3. Langkah Praktis Minggu Pertama
1. Daftar HackerOne, pilih program **VDP** (tidak ada reward uang tapi aman untuk pemula)
2. Baca scope, pilih 1 domain saja
3. Jalankan `TBH-Recon` → catat missing headers (contoh: `Content-Security-Policy` hilang)
4. Laporan: jelaskan dampak + cara fix, bukan cuma "ketemu"

## 4. Contoh Laporan Sederhana
**Title**: Missing Security Header - CSP
**Severity**: Low
**Impact**: Rentan XSS
**Fix**: Tambah `Content-Security-Policy: default-src 'self'`

## 5. Tips Tanpa Video
- Tulis di GitHub README/Gist
- Screenshot + penjelasan langkah
- Konsisten 1 tulisan/minggu di `awesome-tulungagung`

---
*Always Smile :) - Tulungagung Black Hat*
