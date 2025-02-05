git commit -m "Initial commit"
```

3. Tambahkan remote repository:
```bash
git remote add origin https://github.com/username/repository-name.git
git branch -M main
git push -u origin main
```

## Cara Instalasi Lokal

1. Clone repository:
```bash
git clone https://github.com/username/repository-name.git
cd repository-name
```

2. Install dependencies:
```bash
npm install
```

3. Setup environment variables dalam file `.env`:
```env
DATABASE_URL=postgresql://username:password@host:port/database
```

4. Jalankan migrasi database:
```bash
npm run db:push
```

5. Jalankan aplikasi:
```bash
npm run dev
```

Aplikasi akan berjalan di `http://localhost:5000`

## Environment Variables yang Dibutuhkan

- `DATABASE_URL`: URL koneksi PostgreSQL database
- `PORT`: Port untuk menjalankan aplikasi (default: 5000)

## Opsi Deployment

### 1. Vercel
1. Push proyek ke GitHub
2. Buat akun di Vercel
3. Import repository dari GitHub
4. Setup environment variables di dashboard Vercel
5. Deploy

### 2. Railway
1. Buat akun di Railway
2. Connect dengan GitHub repository
3. Setup PostgreSQL service
4. Add environment variables
5. Deploy

### 3. Heroku
1. Install Heroku CLI
2. Login ke Heroku:
```bash
heroku login
```
3. Buat aplikasi baru:
```bash
heroku create nama-aplikasi
```
4. Add PostgreSQL addon:
```bash
heroku addons:create heroku-postgresql:hobby-dev
```
5. Push ke Heroku:
```bash
git push heroku main
