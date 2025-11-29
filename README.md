# Start-Wash-Go-

# Start-Wash Go! - Landing Page React

Implementasi landing page Start-Wash Go! (AI Penjadwalan Laundry) menggunakan React + Vite + Bootstrap 5.

## 📁 Struktur Project

```
src/
├── components/
│   ├── Navigation.jsx      # Navigation bar dengan logo dan menu
│   ├── Hero.jsx            # Hero section dengan call-to-action
│   ├── Features.jsx        # Fitur-fitur utama platform
│   ├── HowItWorks.jsx      # Cara kerja sistem dalam 3 langkah
│   ├── Contact.jsx         # Informasi kontak (telepon & email)
│   └── Footer.jsx          # Footer dengan copyright
├── App.jsx                 # Main app component dengan config state
├── App.css                 # Styling untuk animasi dan layout
├── index.css               # Global styling
└── main.jsx                # Entry point React

public/                      # Static assets
```

## 🎨 Sistem Styling

Landing page menggunakan sistem styling dinamis dengan **Tailwind CSS** dan **inline styles** untuk:

- **Colors**: Primary, Secondary, Text, Accent, Background
- **Typography**: Font family, font size yang dapat dikonfigurasi
- **Animations**: Fade-in, hover-lift, pulse effects

### Default Configuration

```javascript
{
  background_color: "#f8fafc",
  primary_color: "#6366f1",
  secondary_color: "#ffffff",
  text_color: "#1e293b",
  accent_color: "#8b5cf6",
  font_family: "system-ui",
  font_size: 16,
  company_name: "CucianPintar",
  tagline: "🤖 AI Penjadwalan untuk Laundry UMKM",
  // ... dan banyak text content lainnya
}
```

## 🚀 Fitur-Fitur

### 1. Navigation Component
- Fixed navigation bar dengan branding
- Menu navigasi (Beranda, Fitur, Cara Kerja, Kontak)
- Logo SVG yang dinamis

### 2. Hero Section
- Gradient background yang eye-catching
- Call-to-action buttons (Coba Sekarang, Lihat Demo)
- Tagline dan deskripsi yang customizable

### 3. Features Section
- Grid 3 kolom (responsive)
- Icon-based feature cards
- Hover lift effect pada cards

### 4. How It Works Section
- 3-step process visualization
- Input form example
- AI processing visualization
- Priority table dan machine status
- Progress bars

### 5. Contact Section
- Phone dan email contact cards
- Clickable links (href untuk tel: dan mailto:)
- Icon backgrounds dengan custom colors

### 6. Footer
- Copyright information
- Customizable footer text

## 🎯 Cara Menggunakan

### Development
```bash
npm run dev
```
Server akan berjalan di `http://localhost:5173/` (atau port lain jika sedang digunakan)

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 🎨 Customization

### Mengubah Color Scheme
Edit file `App.jsx` dan ubah nilai di `defaultConfig`:

```javascript
const [config, setConfig] = useState({
  primary_color: "#6366f1",      // Warna utama
  secondary_color: "#ffffff",    // Warna background cards
  accent_color: "#8b5cf6",       // Warna highlight
  background_color: "#f8fafc",   // Background halaman
  text_color: "#1e293b",         // Warna text
  // ... config lainnya
})
```

### Mengubah Content
Semua text dapat diubah melalui `config` object:
- `company_name`: Nama perusahaan
- `hero_title`: Judul hero section
- `hero_description`: Deskripsi hero
- `features_title`: Judul fitur section
- `contact_title`: Judul kontak section
- `phone_number`: Nomor telepon
- `email_address`: Alamat email
- Dan lainnya...

### Mengubah Font
```javascript
font_family: "system-ui",  // Atau: "Arial", "Georgia", dll
font_size: 16              // Base font size
```

## 📱 Responsive Design

Semua komponen menggunakan **Tailwind CSS** responsive classes:
- `hidden md:flex` - Tersembunyi di mobile, muncul di desktop
- `grid-cols-1 md:grid-cols-3` - 1 kolom mobile, 3 kolom desktop
- `flex-col sm:flex-row` - Vertical mobile, horizontal desktop

## ✨ Animasi

### Fade-in Animation
Semua section menggunakan CSS animation `.fade-in` untuk efek smooth entrance.

### Hover Effects
- `.hover-lift` - Efek lift dan shadow saat hover
- Transition effects pada buttons dan links

### Pulse Animation
AI processing circle menggunakan `.pulse-dot` animation

## 🔧 Dependencies

- **React 19.2.0** - UI library
- **Vite 7.2.4** - Build tool & dev server
- **Tailwind CSS** - Utility-first CSS framework (via CDN)

## 📦 Build Output

Production build akan generate optimized files di folder `dist/`:
```bash
npm run build
# Output ke: dist/
```

## 🐛 Troubleshooting

**Port sudah digunakan?**
- Vite otomatis menggunakan port berikutnya (5174, 5175, dst)
- Atau kill process yang menggunakan port 5173

**Styling tidak muncul?**
- Pastikan Tailwind CSS CDN sudah ter-load (di index.html)
- Clear cache browser (Ctrl+Shift+Delete)

**Komponen tidak render?**
- Periksa console browser untuk error messages
- Pastikan semua imports sudah benar

## 📄 License

Digunakan untuk project Start-Wash Go!

---

**Created**: 30 November 2024  
**Framework**: React 19 + Vite 7 + Bootstrap 5

