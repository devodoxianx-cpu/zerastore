# 🎮 ZeraStore — Modern Game Top-Up Website

> **"Top Up Cepat, Push Rank Tanpa Batas."**  
> Platform katalog top-up game terpercaya, responsif, dan berestetika premium (*deep black & electric cyan*) yang dirancang khusus untuk kenyamanan para gamer di Indonesia.

---

## 🌟 Fitur Utama

- **Identitas Visual Premium**: Mengusung tema *cyberpunk/gaming marketplace* dengan palet warna hitam pekat (`#080B10`), dark charcoal (`#101720`), aksen electric cyan (`#00E5FF`), soft blue (`#168BFF`), serta efek glow futuristik.
- **Logo Eksklusif ZeraStore**: Dibuat dari bentuk geometris huruf **Z** futuristik berekstensi SVG dengan animasi glow & refleksi high-tech.
- **Katalog 10+ Game Terpopuler**:
  1. *Mobile Legends: Bang Bang* (MOBA)
  2. *Free Fire* (Battle Royale)
  3. *PUBG Mobile* (Battle Royale)
  4. *Honor of Kings* (MOBA)
  5. *Genshin Impact* (RPG)
  6. *Roblox* (Casual)
  7. *Call of Duty: Mobile* (FPS)
  8. *Valorant* (FPS)
  9. *Wuthering Waves* (RPG)
  10. *Zenless Zone Zero* (RPG)
- **Pencarian & Filter Kategori Instan**: Filter instan berdasarkan kategori (*Semua Game, MOBA, Battle Royale, RPG, FPS, Casual*) dan pencarian nama game secara client-side tanpa reload halaman.
- **Pemilihan Nominal & Harga Transparan**: Daftar paket lengkap dalam mata uang Rupiah (IDR) seperti Diamond, UC, Robux, Genesis Crystals, VP, dll.
- **Validasi Data Akun Pemain**:
  - Kolom khusus untuk game dengan format ganda (contoh: **User ID + Zone ID** untuk Mobile Legends, **UID + Server** untuk Genshin Impact/WuWa/ZZZ, **Riot ID + Tag** untuk Valorant).
  - Pesan peringatan real-time jika kolom wajib belum diisi atau salah format.
  - **Jaminan Keamanan**: Tidak pernah meminta password atau kode OTP.
- **Integrasi Pemesanan WhatsApp (Tanpa Biaya Gateway)**:
  - Otomatis membuat nomor referensi pesanan unik (contoh: `ZR-829103`).
  - Format pesan WhatsApp rapi, terstruktur, dan di-*encode* secara aman via tautan resmi `https://wa.me/`.
  - Dilengkapi jendela konfirmasi pesanan, fitur salin pesan, serta pemberitahuan status operasional toko.
- **Bagian Promo & Edukasi**:
  - Banner diskon dan event khusus.
  - 4 Kartu keunggulan ZeraStore (*Why Choose Us*).
  - 3 Langkah mudah panduan top-up (*How to Top Up*).
  - Akordeon FAQ interaktif untuk pertanyaan umum pembeli.
  - Modal Kebijakan Layanan (*Terms of Service*) & Kebijakan Privasi (*Privacy Policy*).
- **Desain Mobile-First 100% Responsif**:
  - Dioptimalkan khusus untuk layar smartphone Android & iOS.
  - Grid fleksibel (2 kolom pada layar kecil ponsel, 3–4 kolom pada tablet & desktop).
  - Navigasi drawer mobile yang mulus dengan *comfortable touch targets*.

---

## 🛠️ Teknologi yang Digunakan

- **React 18** (Komponen modular, hook reaktif)
- **TypeScript 5** (Ketik data ketat & type-safe)
- **Vite 6** (Build tool ultra-cepat & HMR)
- **Tailwind CSS 3** (Styling fleksibel, utility dark gaming theme)
- **Lucide React** (Ikon SVG ringan & modern)

---

## 📁 Struktur Proyek

```text
src/
├── components/
│   ├── Logo.tsx               # Logo ZeraStore geometris Z futuristik
│   ├── Navbar.tsx             # Navigasi sticky desktop & drawer mobile
│   ├── Hero.tsx               # Headline, pencarian cepat, trust badge, promo banner
│   ├── GameCard.tsx           # Kartu game interaktif dengan fallback gambar
│   ├── GameCatalog.tsx        # Filter kategori & grid responsif
│   ├── GameDetailModal.tsx    # Modal detail game, form User ID & pilih nominal
│   ├── WhatsAppSetupModal.tsx # Konfirmasi pesanan WhatsApp & petunjuk nomor
│   ├── Promotions.tsx         # Banner promo & kode voucher
│   ├── WhyChooseUs.tsx        # 4 Kartu keunggulan layanan
│   ├── HowToTopUp.tsx         # 3 Langkah mudah pemesanan & catatan keamanan
│   ├── FAQ.tsx                # Akordeon pertanyaan yang sering diajukan
│   ├── Footer.tsx             # Info toko, navigasi cepat, kontak, copyright
│   └── TermsPrivacyModal.tsx  # Syarat & ketentuan dan kebijakan privasi
├── data/
│   ├── settings.ts            # Konfigurasi toko, nomor WhatsApp & info CS
│   ├── games.ts               # Data 10 game populer & spesifikasi input ID
│   ├── packages.ts            # Daftar nominal & harga paket (IDR)
│   ├── promotions.ts          # Data banner promo
│   └── faqs.ts                # Pertanyaan & jawaban FAQ
├── types/
│   └── index.ts               # Interface TypeScript
├── utils/
│   ├── whatsapp.ts            # Generator pesan wa.me & format Rupiah (IDR)
│   └── validation.ts          # Validasi formulir User ID
├── App.tsx                    # Komponen utama aplikasi
├── main.tsx                   # Entry point React
└── index.css                  # Tema Tailwind & efek cybernetic glow
```

---

## 🚀 Panduan Menjalankan Proyek

### 1. Menjalankan di Mode Pengembangan (Local Dev Server)

Jalankan perintah berikut pada terminal:

```bash
npm run dev
```

Aplikasi akan berjalan di `http://localhost:5173/`. Buka alamat tersebut di browser favorit Anda.

### 2. Membangun Proyek untuk Produksi (Production Build)

```bash
npm run build
```

Hasil build yang dioptimalkan akan tersedia di folder `dist/` dan siap di-*deploy* ke hosting statis gratis seperti Vercel, Netlify, Cloudflare Pages, atau GitHub Pages.

---

## ⚙️ Panduan Kustomisasi untuk Pemilik Toko

### 1. Mengganti Nomor WhatsApp Bisnis
Buka file [`src/data/settings.ts`](file:///c:/Users/Achmad/Documents/ZStore%20Pjct/src/data/settings.ts):
```typescript
export const STORE_SETTINGS: StoreSettings = {
  storeName: "ZeraStore",
  tagline: "Top Up Cepat, Push Rank Tanpa Batas.",
  whatsappNumber: "6281234567890", // Ganti dengan nomor WhatsApp aktif (gunakan format 62...)
  isWhatsAppConfigured: true,      // Ubah ke true setelah nomor diisi
  currency: "IDR",
  operatingHours: "24/7 Transaksi Cepat • Konfirmasi Admin 08:00 - 23:00 WIB",
  ...
};
```

### 2. Menambah / Mengubah Harga Paket Top Up
Buka file [`src/data/packages.ts`](file:///c:/Users/Achmad/Documents/ZStore%20Pjct/src/data/packages.ts):
```typescript
{
  id: "ml-86",
  gameId: "mlbb",
  name: "86 Diamonds",
  amount: "78 + 8 Bonus",
  price: 21500,           // Harga jual dalam Rupiah (IDR)
  originalPrice: 24000,   // Harga sebelum diskon (opsional)
  popular: true,          // Tambahkan badge 'POPULER' jika diinginkan
  categoryGroup: "Diamonds"
}
```

### 3. Menambah Game Baru ke Katalog
Buka file [`src/data/games.ts`](file:///c:/Users/Achmad/Documents/ZStore%20Pjct/src/data/games.ts) dan tambahkan objek game baru sesuai struktur `GameItem`.

---

## 🔒 Kebijakan & Keamanan Data
- Seluruh komunikasi transaksi dilakukan langsung melalui platform WhatsApp resmi.
- Sistem tidak pernah meminta kata sandi (*password*) akun game maupun kode OTP pembeli.
- Seluruh harga awal adalah harga katalog estimasi yang akan dikonfirmasi kembali oleh admin sebelum transfer dilakukan.
