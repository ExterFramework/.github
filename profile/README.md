# 🎮 ExterFramework

[![GitHub Organization](https://img.shields.io/badge/GitHub-ExterFramework-181717?style=for-the-badge&logo=github)](https://github.com/ExterFramework)
[![License](https://img.shields.io/badge/License-GPL%20v3.0-blue?style=for-the-badge)](https://www.gnu.org/licenses/gpl-3.0)
[![Repositories](https://img.shields.io/badge/Repositories-25-green?style=for-the-badge)]()
[![Platform](https://img.shields.io/badge/Platform-FiveM-orange?style=for-the-badge)]()

---

## 📖 Profil Institusional

**ExterFramework** merupakan entitas pengembangan perangkat lunak berbasis komunitas yang berfokus pada orkestrasi ekosistem resource **FiveM** untuk framework **QBCore**. Secara konseptual, ExterFramework tidak semata-mata menawarkan kumpulan script, melainkan menyediakan _interoperable module stack_ yang dirancang untuk menyederhanakan integrasi, menjaga koherensi antarmuka, dan meningkatkan determinisme pengalaman roleplay pada skenario produksi server.

Dengan pendekatan desain yang terinspirasi ekosistem **NoPixel 4.0**, setiap modul diorientasikan pada tiga aksentuasi utama: **konsistensi visual**, **efisiensi runtime**, dan **skalabilitas operasional**.

---

## 🏛️ Statement Arsitektural

| Domain | Implementasi |
|--------|---------------|
| **Server Runtime** | Lua (FiveM server-side execution model) |
| **Client Runtime** | Lua (event-driven client pipeline) |
| **NUI Layer** | HTML, CSS, JavaScript |
| **Framework Basis** | QBCore |
| **Design Paradigm** | NoPixel 4.0-inspired modern interface |
| **License Governance** | GNU GPL v3.0 |

---

## 🌐 Kanal Resmi

- **GitHub Organization**: <https://github.com/ExterFramework>
- **Website Resmi/Portal Informasi**: <https://exterframeworked.gt.tc>
- **Lisensi**: <https://www.gnu.org/licenses/gpl-3.0>

> Seluruh komunikasi teknis, pembaruan modular, dan dokumentasi tambahan direkomendasikan merujuk pada kanal resmi di atas agar terhindar dari artefak informasi yang tidak terverifikasi.

---

## 📦 Struktur Repository (25 Modul)

### 🔧 Core & Library

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-lib**](https://github.com/ExterFramework/exter-lib) | Lua | Lapisan utilitas inti (notify, progressbar, table info, info bar, dan komponen interoperabilitas UI) |

### 🖥️ UI & HUD

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-hud**](https://github.com/ExterFramework/exter-hud) | CSS | Modul telemetri visual pemain (health, armor, hunger, thirst, dan parameter vital lain) |
| [**exter-menu**](https://github.com/ExterFramework/exter-menu) | CSS | Sistem menu modular untuk interaksi multi-konteks |
| [**exter-radialmenu**](https://github.com/ExterFramework/exter-radialmenu) | Lua | Akses aksi cepat berbasis radial command surface |
| [**exter-textui**](https://github.com/ExterFramework/exter-textui) | CSS | Notifikasi interaksi kontekstual berbasis text overlay |

### 🎒 Inventory & Itemization

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**ox_inventory**](https://github.com/ExterFramework/ox_inventory) | Lua | Fork/kustomisasi sistem inventory untuk kebutuhan implementasi spesifik |
| [**exter-shop**](https://github.com/ExterFramework/exter-shop) | Lua | Infrastruktur transaksi item dan komoditas in-game |
| [**exter-books**](https://github.com/ExterFramework/exter-books) | Lua | Mekanisme dokumen-baca berbentuk buku interaktif |
| [**exter-documents**](https://github.com/ExterFramework/exter-documents) | Lua | Sistem dokumen legal/administratif (ID, SIM, dan varian surat lainnya) |

### 🚗 Vehicular Ecosystem

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-vehicleshop**](https://github.com/ExterFramework/exter-vehicleshop) | Lua | Modul showroom dan pembelian kendaraan |
| [**exter-garage**](https://github.com/ExterFramework/exter-garage) | Lua | Lifecycle penyimpanan, retrieval, dan state kendaraan |
| [**exter-carcontrol**](https://github.com/ExterFramework/exter-carcontrol) | JavaScript | Kontrol perangkat kendaraan (engine, lock, lights, dsb.) |
| [**exter_radar**](https://github.com/ExterFramework/exter_radar) | JavaScript | Instrumentasi radar kecepatan untuk kebutuhan law enforcement |

### 👮 Roleplay Service Layer

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-dispatch**](https://github.com/ExterFramework/exter-dispatch) | CSS | Sistem dispatch untuk kanal darurat kepolisian/medis |
| [**exter-report**](https://github.com/ExterFramework/exter-report) | Lua | Manajemen pelaporan pemain dan eskalasi administratif |
| [**exter-billing**](https://github.com/ExterFramework/exter-billing) | CSS | Transaksi billing antar entitas pemain/bisnis |
| [**exter-moneywash**](https://github.com/ExterFramework/exter-moneywash) | Lua | Simulasi ekonomi ilegal untuk skenario criminal RP |

### 🎮 Gameplay & Interaction Suite

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-racingapp**](https://github.com/ExterFramework/exter-racingapp) | HTML | Aplikasi balap jalanan dengan antarmuka kompetitif |
| [**exter-lockpick**](https://github.com/ExterFramework/exter-lockpick) | JavaScript | Minigame lockpick berbasis interaksi real-time |
| [**exter-emotemenu**](https://github.com/ExterFramework/exter-emotemenu) | Lua | Orkestrasi emote dan animasi karakter |
| [**exter-radio**](https://github.com/ExterFramework/exter-radio) | Lua | Komunikasi radio in-game multi-channel |
| [**exter-chat**](https://github.com/ExterFramework/exter-chat) | Lua | Sistem percakapan custom berorientasi RP |
| [**exter-scenes**](https://github.com/ExterFramework/exter-scenes) | CSS | Penempatan scene/teks 3D sebagai artefak naratif dunia |

### 💀 Auxiliary Systems

| Repository | Bahasa | Fokus Fungsional |
|------------|--------|------------------|
| [**exter-deathscreen**](https://github.com/ExterFramework/exter-deathscreen) | Lua | Death-state visual handling untuk fase incapacitated |
| [**exter-doorlock**](https://github.com/ExterFramework/exter-doorlock) | Lua | Kontrol akses properti melalui skema door authorization |

---

## 📊 Telemetri Ringkas

| Metrik | Nilai |
|--------|-------|
| **Total Repository** | 25 |
| **Distribusi Bahasa** | Lua (15), CSS (6), JavaScript (3), HTML (1) |
| **Lisensi** | GNU GPL v3.0 |
| **Basis Framework** | QBCore |
| **Pembaruan Dokumen** | 22 April 2026 |

---

## ⚙️ Protokol Implementasi Dasar

1. **Kloning modul** yang diperlukan ke direktori resource server:
   ```bash
   cd /path/to/your/fivem-server/resources/
   git clone https://github.com/ExterFramework/[nama-repo].git
   ```
2. **Registrasikan modul** pada `server.cfg`:
   ```cfg
   ensure [nama-repo]
   ```
3. **Verifikasi dependensi inti**:
   - QBCore telah terpasang dan aktif.
   - `exter-lib` direkomendasikan sebagai fondasi utilitas.
   - Dokumentasi repo masing-masing diutamakan untuk dependensi khusus.
4. **Muat ulang service**:
   ```bash
   refresh
   ensure [nama-repo]
   ```

---


## 👕 Panduan Instalasi Clothing System (Step-by-Step)

> Bagian ini ditambahkan khusus untuk kebutuhan implementasi script **clothing system** (mis. `exter-clothing`) agar proses setup lebih jelas dan berurutan.

1. **Siapkan prasyarat server**
   - Pastikan server FiveM sudah berjalan normal.
   - Pastikan **QBCore**, **oxmysql**, dan dependensi UI terkait sudah aktif.

2. **Dapatkan resource clothing**
   - Jika repository public:
     ```bash
     cd /path/to/your/fivem-server/resources/[local]
     git clone https://github.com/ExterFramework/exter-clothing.git
     ```
   - Jika repository private/restricted, minta akses terlebih dahulu ke tim ExterFramework.

3. **Konfigurasi folder resource**
   - Pastikan nama folder sesuai ekspektasi script (disarankan: `exter-clothing`).
   - Jangan menaruh resource di folder yang tidak di-ensure oleh server.

4. **Import SQL (jika disediakan oleh resource)**
   - Cek apakah ada file `.sql` di dalam repo clothing system.
   - Import ke database server (contoh via phpMyAdmin/Adminer/MySQL CLI).

5. **Atur dependensi pada `server.cfg`**
   - Pastikan urutan load benar (dependency lebih dulu):
     ```cfg
     ensure oxmysql
     ensure qb-core
     ensure exter-lib
     ensure exter-clothing
     ```

6. **Validasi file konfigurasi internal**
   - Buka file seperti `config.lua` / `shared.lua` (sesuai struktur repo).
   - Sesuaikan job restriction, target system, command, keybind, dan opsi pricing jika ada.

7. **Restart resource / server**
   ```bash
   refresh
   ensure exter-clothing
   ```
   - Atau restart penuh server untuk memastikan semua dependency terinisialisasi bersih.

8. **Uji fungsional di dalam game**
   - Masuk server dan buka menu clothing.
   - Coba ganti komponen pakaian, simpan outfit, dan reload karakter.
   - Verifikasi tidak ada error di console server/client.

9. **Troubleshooting cepat**
   - Jika menu tidak muncul: cek dependency belum aktif atau export tidak terbaca.
   - Jika outfit tidak tersimpan: cek koneksi database dan tabel terkait.
   - Jika ada konflik UI: cek apakah ada resource clothing lain yang berjalan bersamaan.

---

## 📋 Dependensi Referensial

- [**QBCore Framework**](https://github.com/qbcore-framework)
- [**oxmysql**](https://github.com/overextended/oxmysql)
- [**ox_lib**](https://github.com/overextended/ox_lib)
- **exter-lib** sebagai utility layer internal ExterFramework

---

## 👥 Credits & Atribusi

Pengembangan ExterFramework merupakan hasil kolaborasi komunitas open-source yang melibatkan maintainer, kontributor kode, penguji internal server, serta pengguna akhir yang menyuplai _feedback loop_ berkesinambungan.

Atribusi utama:
- Tim inti dan maintainer **ExterFramework**.
- Komunitas **QBCore** dan ekosistem dependensi pendukung.
- Kontributor independen melalui _issue tracking_, _pull request_, dan validasi fungsional.

> Demi menjaga integritas etika open-source, mohon tetap mencantumkan kredit ketika melakukan fork, redistribusi, atau modifikasi publik.

---

## 📌 Catatan Operasional

- Sebagian modul dapat bersifat **private/restricted** dan tidak selalu tersedia untuk publik.
- ExterFramework ditujukan secara primer untuk **QBCore**; penggunaan pada stack lain (mis. ESX/vRP) memerlukan rekayasa adaptif tambahan.
- Untuk klarifikasi legal, teknis, atau kolaborasi, prioritaskan kanal resmi yang telah dicantumkan.

---

<p align="center">
  <i>Dokumen ini disusun untuk representasi profesional organisasi ExterFramework.</i><br>
  <i>Revisi terakhir: 22 April 2026 (UTC)</i>
</p>
