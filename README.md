
# Aplikasi Statistik Sukan Sekolah (Live)

Aplikasi mudah untuk merekod keputusan acara dan memaparkan papan skor langsung (auto-refresh) untuk rumah sukan sekolah.

## Ciri-ciri
- Tambah rumah sukan (Merah/Biru/Hijau/Kuning dsb).
- Tetapkan acara (kategori, jantina, sistem mata custom).
- Catat keputusan (kedudukan 1–3, catatan masa/jarak/markah).
- Papan skor langsung: mata + kiraan pingat.
- Import/Export pangkalan data SQLite (fail `sports.db`).

## Cara Jalankan (Laptop/PC)
1. Pastikan ada **Python 3.9+**.
2. Buka terminal dalam folder projek ini.
3. Pasang kebergantungan:
   ```bash
   pip install -r requirements.txt
   ```
4. Jalankan aplikasi:
   ```bash
   streamlit run app.py
   ```
5. Buka pautan yang dipaparkan (contoh: `http://localhost:8501`).
6. Gunakan menu **Admin** untuk tambah rumah/acara, dan **Papan Skor** untuk paparan langsung.

> Tip: Buka **Papan Skor** di projector/TV; buka **Admin** di telefon/laptop untuk kemaskini — paparan akan auto-refresh.

## Deploy (Pilihan)
- **Streamlit Community Cloud**: Upload repo ini ke GitHub, set app file `app.py`, dan jalankan.
- **Lain-lain**: Boleh host di server sekolah yang ada Python.

## Struktur Data
- **houses**: rumah sukan.
- **events**: acara (dengan `points_json` untuk aturan mata).
- **results**: keputusan (unik untuk setiap *acara + kedudukan*).

## Tukar Sistem Mata
Dalam borang tambah acara, ubah `points_json`, contoh:
```json
{"1": 10, "2": 7, "3": 5, "4": 3, "5": 1}
```
