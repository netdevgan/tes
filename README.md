# Digital Time Store - Landing Page

Landing page untuk jualan ebook dengan desain modern seperti Linktree + Admin Dashboard.

## 📁 File Structure

```
.
├── index.html       # Landing page utama (halaman publik)
├── admin.html       # Dashboard admin (untuk edit konten)
├── config.json      # Konfigurasi (opsional, untuk referensi)
├── profile.jpeg     # Foto profil
├── digital product.png  # Cover ebook 1
├── diet.jpeg        # Cover ebook 2
└── README.md        # Dokumentasi ini
```

## 🎨 Cara Edit Konten

### Cara Paling Mudah: Edit data.json di GitHub

1. **Buka repository GitHub**
2. **Klik file `data.json`**
3. **Klik icon pensil (Edit)**
4. **Edit konten** (nama, bio, produk, link, dll)
5. **Commit changes**
6. **Tunggu 1-2 menit** - Vercel auto-deploy
7. **Refresh website**

📖 **Panduan lengkap:** Lihat file `ADMIN-GUIDE.md`

### Struktur data.json:

```json
{
  "profile": {
    "name": "Your Name",
    "bio": "Your bio",
    "image": "profile.jpeg"
  },
  "products": [...],
  "links": [...],
  "social": [...]
}
```

## 🚀 Deploy ke Vercel

### Cara 1: Via GitHub

1. **Upload ke GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/username/repo.git
   git push -u origin main
   ```

2. **Import ke Vercel:**
   - Buka vercel.com/new
   - Import repository
   - Deploy

3. **Custom Domain:**
   - Settings → Domains
   - Tambah: `link.digitaltime.store`
   - Tambah CNAME di DNS panel:
     ```
     Type: CNAME
     Name: link
     Target: cname.vercel-dns.com
     ```

### Cara 2: Drag & Drop

1. Zip semua file
2. Buka vercel.com/new
3. Drag & drop folder
4. Deploy

## 🔒 Keamanan Dashboard

**PENTING:** Dashboard (`admin.html`) bisa diakses siapa saja yang tahu URL-nya.

### Cara Proteksi:

**Opsi 1: Rename File**
- Rename `admin.html` menjadi nama random: `admin-xyz123.html`
- Hanya Anda yang tahu URL-nya

**Opsi 2: Vercel Password Protection**
- Upgrade ke Vercel Pro
- Set password protection untuk `/admin.html`

**Opsi 3: Jangan Deploy Admin**
- Hanya deploy `index.html`
- Edit konten di lokal, lalu push ke GitHub

## 📝 Edit Manual (Tanpa Dashboard)

Jika tidak mau pakai dashboard, edit langsung di `index.html`:

- **Foto profil:** Baris ~150
- **Nama:** Baris ~151
- **Bio:** Baris ~152
- **Product 1:** Baris ~158-163
- **Product 2:** Baris ~166-171
- **Links:** Baris ~175-195
- **Social:** Baris ~198-225

## 🎯 Fitur

✅ Landing page modern & responsive
✅ Admin dashboard untuk edit konten
✅ Tambah/hapus produk dinamis
✅ Tambah/hapus link & social media
✅ Upload gambar via dashboard
✅ Preview real-time
✅ Data tersimpan di localStorage

## 💡 Tips

- Gunakan gambar berkualitas tinggi (min 1000px width)
- Compress gambar sebelum upload (tinypng.com)
- Test di mobile browser
- Backup data sebelum edit besar-besaran
- Gunakan URL pendek untuk link produk

## 🆘 Troubleshooting

**Q: Perubahan tidak muncul di landing page?**
- Clear cache browser (Ctrl + Shift + R)
- Pastikan sudah klik "Save Changes"

**Q: Gambar tidak muncul setelah deploy?**
- Upload gambar ke hosting (imgur.com, imgbb.com)
- Gunakan URL absolut di dashboard

**Q: Dashboard tidak bisa diakses?**
- Pastikan file `admin.html` sudah ter-upload
- Cek URL: `https://domain.com/admin.html`

## 📞 Support

Butuh bantuan? Edit file ini atau hubungi developer.

---

Made with ❤️ for Digital Time Store
