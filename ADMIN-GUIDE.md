# 🎨 Admin Guide - Cara Edit Konten

Karena website ini static HTML, cara paling mudah untuk edit konten adalah **edit file `data.json`** langsung.

## 📝 Cara Edit via GitHub (Recommended)

### 1. Buka Repository GitHub
- Login ke GitHub
- Buka repository project ini

### 2. Edit File data.json
- Klik file `data.json`
- Klik icon **pensil (Edit)** di kanan atas
- Edit konten sesuai kebutuhan

### 3. Format JSON

```json
{
  "profile": {
    "name": "Nama Anda",
    "bio": "Deskripsi singkat Anda",
    "image": "profile.jpeg"
  },
  "products": [
    {
      "title": "Judul Produk 1",
      "price": "$67",
      "image": "cover-ebook-1.png",
      "link": "https://gumroad.com/..."
    },
    {
      "title": "Judul Produk 2",
      "price": "$47",
      "image": "cover-ebook-2.png",
      "link": "https://gumroad.com/..."
    }
  ],
  "links": [
    {
      "icon": "📚",
      "title": "View All Ebooks",
      "url": "https://..."
    },
    {
      "icon": "💬",
      "title": "Contact via WhatsApp",
      "url": "https://wa.me/628..."
    }
  ],
  "social": [
    {
      "name": "Facebook",
      "icon": "facebook",
      "url": "https://facebook.com/..."
    }
  ]
}
```

### 4. Commit Changes
- Scroll ke bawah
- Klik **"Commit changes"**
- Tunggu 1-2 menit
- Vercel akan auto-deploy

## 🖼️ Cara Ganti Gambar

### 1. Upload Gambar Baru ke GitHub
- Di repository, klik **"Add file"** → **"Upload files"**
- Drag gambar baru (misal: `new-product.png`)
- Commit

### 2. Update data.json
- Edit `data.json`
- Ganti nama file gambar:
  ```json
  "image": "new-product.png"
  ```
- Commit

## ➕ Cara Tambah Produk Baru

Edit `data.json`, tambahkan di array `products`:

```json
"products": [
  {
    "title": "Produk 1",
    "price": "$67",
    "image": "product1.png",
    "link": "https://..."
  },
  {
    "title": "Produk 2",
    "price": "$47",
    "image": "product2.png",
    "link": "https://..."
  },
  {
    "title": "Produk Baru",
    "price": "$99",
    "image": "product3.png",
    "link": "https://..."
  }
]
```

## 🗑️ Cara Hapus Produk

Hapus block produk di `data.json`:

```json
"products": [
  {
    "title": "Produk 1",
    ...
  }
  // Produk 2 dihapus
]
```

## 🔗 Cara Edit Link & Social Media

Edit bagian `links` dan `social` di `data.json`:

```json
"links": [
  {
    "icon": "🔗",
    "title": "Link Baru",
    "url": "https://..."
  }
],
"social": [
  {
    "name": "TikTok",
    "icon": "tiktok",
    "url": "https://tiktok.com/@..."
  }
]
```

## 💡 Tips

- **Validasi JSON:** Paste ke https://jsonlint.com untuk cek error
- **Backup:** Copy isi `data.json` sebelum edit besar
- **Test:** Setelah commit, tunggu 2 menit lalu refresh website
- **Emoji:** Copy emoji dari https://emojipedia.org

## 🚀 Quick Edit Workflow

1. Buka GitHub → `data.json`
2. Klik Edit (pensil icon)
3. Ubah konten
4. Commit changes
5. Tunggu auto-deploy (1-2 menit)
6. Refresh website

## ⚠️ Common Errors

**Error: JSON Parse Error**
- Cek koma terakhir (jangan ada koma di item terakhir)
- Cek kurung kurawal `{}` dan bracket `[]` harus balance
- Gunakan https://jsonlint.com untuk validasi

**Gambar tidak muncul:**
- Pastikan nama file gambar sama persis (case-sensitive)
- Pastikan gambar sudah ter-upload ke GitHub

**Perubahan tidak muncul:**
- Clear cache browser (Ctrl + Shift + R)
- Tunggu 2-3 menit untuk deploy selesai
- Cek di Vercel dashboard apakah deploy success

---

Lebih mudah dari dashboard admin karena:
✅ Tidak perlu login
✅ Edit langsung di GitHub
✅ Auto-deploy ke Vercel
✅ Version control (bisa rollback)
