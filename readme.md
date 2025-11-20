# Zendesk Voice Widget — Demo Static

Repo ini berisi contoh sederhana tombol untuk membuka Zendesk Messenger pada mode *voice*.

## Opsi deployment

### Opsi A — Simpel (cepat)
1. Edit `index.html`:
   - Ganti `SNIPPET_KEY` dengan snippet key Zendesk Anda.
   - Ganti `VOICE_LINE_ID` dengan voice line id Anda.
2. Commit & push ke GitHub.
3. Aktifkan **GitHub Pages** dari branch `main` (Settings → Pages) dan pilih folder `/ (root)` atau `/docs` sesuai struktur.
4. Situs akan tersedia di `https://<username>.github.io/<repo>/` dalam beberapa menit.

**PERINGATAN:** cara ini menyimpan key di file publik — siapa pun bisa melihat snippet key & line_id.

### Opsi B — Lebih aman (direkomendasikan)
Gunakan GitHub Actions untuk memasukkan secrets saat build dan deploy otomatis.
- Simpan secret di GitHub repo Settings → Secrets: `ZENDESK_SNIPPET_KEY` dan `ZENDESK_VOICE_LINE_ID`.
- Buat workflow yang menggantikan placeholder `SNIPPET_KEY` dan `VOICE_LINE_ID` pada `index.html` dengan nilai secret, lalu deploy ke GitHub Pages.
- Contoh workflow disediakan di `.github/workflows/deploy-pages.yml`.

_Lihat contoh workflow di folder `.github` (opsional)._

## Lisensi
Gunakan sesuai kebutuhan. Hati-hati dengan credential.
