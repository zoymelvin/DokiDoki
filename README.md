# DokiDoki — Anime Explorer 🎌

Aplikasi katalog anime dengan UI modern berbasis Flutter, terintegrasi API Jikan v4. Jelajahi anime berdasarkan genre, trending, rilis musim ini, lakukan pencarian, lihat detail, dan simpan ke Watchlist.

> Built for **NusaCode Flutter Bootcamp** — final project.

---

## 🖼️ Screenshots

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d11eee9f-2ad5-45cd-b04b-07b9502fd834" alt="Home Screen" width="200"/>
      <br/>
      <b>Home</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d2914e32-972a-40d9-a1a0-7b6026f84751" alt="Genre Action" width="200"/>
      <br/>
      <b>Genre (Action)</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/7b212d43-bcae-4ac2-89c7-2fd211831562" alt="Watchlist" width="200"/>
      <br/>
      <b>Watchlist</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c3967a42-e1dc-496d-85e9-d896b85050ef" alt="Settings" width="200"/>
      <br/>
      <b>Settings</b>
    </td>
  </tr>
</table>

---

## ✨ Fitur Utama

### 🏠 Home
- Hero carousel (highlight anime)
- Explore Genres (kartu ikon berwarna, horizontal)
- Daftar horizontal: Recommended, Trending Now, This Season, Top Movies

### 🔍 Search
Pencarian judul anime dengan hasil real-time

### 📺 Detail Anime
- Overview lengkap
- Episodes (dengan pagination)
- Characters & voice actors

### ⭐ Watchlist
Simpan anime favorit untuk ditonton nanti

### ⚙️ Settings
- **Theme:** System / Light / Dark (dengan preview cards)
- **Safe Mode (SFW):** Filter konten dewasa
- **Prefer English Titles:** Tampilkan judul dalam bahasa Inggris

### 🚀 Performa
- Cache gambar (CachedNetworkImage)
- State management dengan Provider
- Optimasi loading dan smooth scrolling

---

## 🧱 Arsitektur & Teknologi

### Tech Stack
- **Framework:** Flutter 3+
- **Language:** Dart
- **HTTP Client:** Dio
- **State Management:** Provider
- **Local Storage:** SharedPreferences
- **Image Caching:** CachedNetworkImage
- **Typography:** Google Fonts
- **Utilities:** url_launcher, Hive (optional), flutter_launcher_icons

### Struktur Direktori
```
lib/
├── core/
│   └── anime_api.dart          # Client Jikan v4 (sfw param, search, genre, season)
├── models/
│   └── anime.dart              # Model utama + JSON parser
├── providers/
│   ├── anime_provider.dart     # State home & list
│   └── watchlist_provider.dart # State watchlist (local)
└── features/
    ├── home/                   # Home + widgets (carousel, horizontal lists, genres)
    ├── search/                 # Search page
    ├── genre/                  # Genre list page (grid)
    ├── detail/                 # Detail page (overview/episodes/characters)
    ├── watchlist/              # Watchlist page
    └── settings/               # Settings page + provider
```

---

## 📦 Prasyarat

- Flutter SDK 3.x
- Android Studio / VS Code
- (Opsional) Postman/Insomnia untuk eksplorasi API

---

## 🔑 Integrasi API

Menggunakan **Jikan v4** (public, read-only API untuk MyAnimeList)

- **Base URL:** `https://api.jikan.moe/v4`
- **Endpoints:**
  - `/anime` - List anime dengan filter
  - `/anime/{id}/full` - Detail lengkap anime
  - `/genres/anime` - Daftar genre
  - `/seasons/now` - Anime musim ini
  - `/top/anime` - Top anime by ranking

> ⚠️ **Note:** Rate limit Jikan dapat memicu `429 Too Many Requests`. Gunakan debounce, batasi refresh, dan tunggu sesuai `Retry-After` header jika diperlukan.

---

## 🚀 Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/zoymelvin/DokiDoki.git
cd DokiDoki
```

### 2. Install Dependencies
```bash
flutter pub get
```

### 3. Run the App
```bash
flutter run
```

---


## 👨‍💻 Author

**Joy Melvin Ginting**  
*Flutter Developer | Anime Enthusiast*

- 📧 Email: zoymelvin04@gmail.com
- 🔗 GitHub: [@zoymelvin](https://github.com/zoymelvin)
- 💼 Repository: [DokiDoki](https://github.com/zoymelvin/DokiDoki)

> "Anime is not just a hobby, it's a lifestyle!" 🎌


## 🙏 Acknowledgments

- [Jikan API](https://jikan.moe/) for providing free MyAnimeList data
- [Flutter](https://flutter.dev/) for the amazing framework
- **NusaCode Flutter Bootcamp** for the learning opportunity
