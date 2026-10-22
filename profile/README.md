# <div align="center">🏪 Aronium POS Community Extensions</div>
### <div align="center"><i>Suite Ekstensi Mandiri, Installer Otomatis & Alat Integrasi Aronium POS</i></div>

<div align="center">

![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Framework](https://img.shields.io/badge/.NET%20Framework-4.7.1-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Installer](https://img.shields.io/badge/Installer-Inno%20Setup%206-2563EB?style=for-the-badge)
![Access](https://img.shields.io/badge/Access-Private%20%2F%20Member%20Only-DC2626?style=for-the-badge&logo=github&logoColor=white)
![Aronium POS](https://img.shields.io/badge/Compatibility-Aronium%20POS-10B981?style=for-the-badge)

</div>

---

## 📌 Tentang Organisasi

**Aronium-Unofficial-Extensions** adalah hub privat untuk pengembangan, pemeliharaan, dan distribusi modul ekstensi pihak ketiga (*third-party community plugins*) untuk aplikasi kasir **Aronium POS**. 

Setiap modul dioptimalkan dengan:
- **Standalone Windows Installer (`.exe`)**: Pengguna cukup klik ganda untuk instalasi; modul otomatis mendeteksi lokasi Aronium POS tanpa perlu salin-tempel manual.
- **Deteksi Proses Aktif**: Installer otomatis memverifikasi agar Aronium POS ditutup terlebih dahulu demi mencegah *file locking* saat upgrade.
- **Keamanan Data**: Menggunakan metode *clean in-place upgrade* yang menjaga keutuhan basis data (`pos.db`) dan riwayat penjualan Anda.
- **Multi-Language Support**: Dukungan antarmuka dwibahasa (Bahasa Indonesia & Bahasa Inggris).

---

## 📂 Katalog Modul Resmi Komunitas

Seluruh modul di bawah ini berstatus privat dan dapat diakses oleh anggota terdaftar:

| Modul | Repositori | Status Rilis | Deskripsi Fungsionalitas |
| :--- | :--- | :---: | :--- |
| **📱 WhatsApp Notifier** | [Aronium-WhatsApp-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-WhatsApp-Modul-Unofficial) | `v1.0.0` | Integrasi pengiriman struk digital & notifikasi transaksi otomatis ke WhatsApp pelanggan via gateway API. |
| **🏷️ Price Lists & Promo** | [Aronium-PriceLists-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-PriceLists-Modul-Unofficial) | `v1.4.0.1` | Manajemen daftar harga bertingkat, harga grosir per pelanggan/grup, dengan pelokalan Bahasa Indonesia (`id.lang`). |
| **📦 Multi-Unit Measurement** | [Aronium-MultiUnit-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-MultiUnit-Modul-Unofficial) | `v1.0.0` | Konversi multi-satuan (Pcs, Lusin, Box, Karton), barcode per satuan, dan template struk FastReport (`.frx`). |
| **🎁 Gift Promotions** | [Aronium-GiftPromotions-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-GiftPromotions-Modul-Unofficial) | `v1.0.0` | Engine promosi Beli X Gratis Y, diskon bersyarat nominal belanja, dan prompt hadiah otomatis pada kasir. |
| **🔄 Mobile Sync** | [Aronium-MobileSync-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-MobileSync-Modul-Unofficial) | `v1.0.0` | Sinkronisasi nirkabel lokal LAN, integrasi Supabase Cloud, auto-discovery UDP, dan pairing via QR Code. |
| **⚡ PPOB Digital Services** | [Aronium-PPOB-Modul-Unofficial](https://github.com/Aronium-Unofficial-Extensions/Aronium-PPOB-Modul-Unofficial) | `v1.0.0` | Layanan penjualan produk digital langsung dari kasir (Pulsa, Paket Data, Token PLN, Topup E-Wallet). |

---

## 🚀 Panduan Instalasi Bagi Pengguna / Member

1. **Akses Rilis**: Buka tab **Releases** pada repositori modul yang Anda butuhkan.
2. **Unduh Installer**: Pilih file `Aronium.Pos.[NamaModul].Unofficial.Setup.exe`.
3. **Tutup Aronium POS**: Pastikan aplikasi Aronium POS sedang tidak berjalan di komputer kasir.
4. **Jalankan Installer**: Ikuti panduan wizard instalasi:
   - Installer akan otomatis mendeteksi folder instalasi Aronium (`C:\Program Files\Aronium` atau `D:\DATA\Aronium`).
   - Tekan **Next** hingga selesai.
5. **Buka Kembali Aronium**: Modul akan langsung aktif dan muncul pada menu pengaturan atau antarmuka kasir Aronium POS Anda.

---

## 🛠️ Standar Pengembangan & Build

Bagi pengembang yang telah diberikan hak akses kolaborator:

```bash
# Clone repositori modul
git clone https://github.com/Aronium-Unofficial-Extensions/[Nama-Modul].git

# Build biner modul
dotnet build -c Release

# Kompilasi paket installer mandiri (.exe)
powershell -ExecutionPolicy Bypass -File .\Build-Installer.ps1
```

> Seluruh repositori mengadopsi file `Directory.Build.props` terpusat sehingga dependensi SDK Aronium akan di-*resolve* otomatis di komputer pengembang mana pun tanpa perlu konfigurasi path manual.

---

## 🔒 Kebijakan Hak Akses & Privasi

- **Akses Organisasi**: Organisasi ini dikelola secara privat. Seluruh kode sumber, rilis biner, dan dokumentasi teknis hanya dapat diakses oleh member dan kolaborator yang diundang langsung oleh pemilik organisasi (*Owner*).
- **Undangan Member**: Untuk menambahkan kasir cabang, teknisi, atau pengembang baru, Owner dapat mengundang via menu **Organization Settings > People > Invite member**.

---

## ⚖️ Penafian Hukum & Komunitas (Disclaimer)

1. **Status Komunitas**: Seluruh perangkat lunak dalam organisasi ini merupakan proyek komunitas independen (*Unofficial Community Edition*).
2. **Independensi Resmi**: Organisasi dan repositori ini **BUKAN** merupakan bagian resmi dari **Aronium d.o.o.**, serta tidak terafiliasi, didukung, atau disponsori oleh Aronium d.o.o.
3. **Merek Dagang**: Nama "Aronium" serta logo terkait adalah merek dagang milik Aronium d.o.o. Penyebutan nama semata-mata bertujuan untuk kejelasan identifikasi teknis kompatibilitas platform.
4. **Garansi**: Modul disediakan "sebagaimana adanya" (*AS-IS*) tanpa jaminan komersial. Selalu lakukan pencadangan (*backup*) data secara berkala sebelum pembaruan sistem kasir.

---
<div align="center">
  <sub>Dikurasi dengan standar profesional oleh Komunitas Pengembang Aronium POS</sub>
</div>
