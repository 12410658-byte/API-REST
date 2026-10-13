# CRUD Posts - React + TypeScript

Aplikasi web sederhana untuk operasi **CRUD** (Create, Read, Update, Delete)
dengan mengonsumsi REST API [JSONPlaceholder](https://jsonplaceholder.typicode.com/posts).

## Teknologi
- React 18
- TypeScript
- Vite

## Fitur
| Operasi | HTTP Method | Keterangan |
|---------|-------------|------------|
| Read    | GET         | Menampilkan daftar post |
| Create  | POST        | Menambah post baru lewat form |
| Update  | PUT         | Mengubah post (tombol Edit) |
| Delete  | DELETE      | Menghapus post (tombol Hapus) |

## Struktur Folder
```
crud-posts-react/
├── index.html
├── package.json
├── tsconfig.json
├── vite.config.ts
└── src/
    ├── main.tsx                  # Entry point
    ├── App.tsx                   # Komponen utama + logika CRUD
    ├── App.css                   # Styling
    ├── types/Post.ts             # Tipe data TypeScript
    ├── services/postService.ts   # Fungsi fetch ke API (GET, POST, PUT, DELETE)
    └── components/
        ├── PostForm.tsx          # Form tambah / edit
        └── PostList.tsx          # Daftar post
```

## Cara Menjalankan
```bash
npm install
npm run dev
```
Buka alamat yang muncul di terminal (biasanya http://localhost:5173).

## Catatan
JSONPlaceholder adalah API palsu: data yang ditambah, diubah, atau dihapus
**tidak benar-benar tersimpan** di server. Aplikasi ini memperbarui tampilan
(state React) setelah request berhasil, sehingga perubahan terlihat selama
halaman belum di-refresh.
