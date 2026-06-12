# Dashboard Kinerja Saham Indonesia

> Dashboard interaktif untuk menganalisis dan memvisualisasikan performa kumulatif, tren harga, dan momentum 9 saham blue-chip Indonesia (Magnificent 7 + ASII & ANTM) terhadap IHSG dengan data historis nyata yang bersumber dari Yahoo Finance.

🌐 Demo: https://indonesia-market-dashboard.vercel.app

## Isi Dashboard

- **Chart 1: Performa Relatif Saham terhadap IHSG** — Menampilkan grafik multiline persentase keuntungan akumulatif seluruh 9 saham dan IHSG (benchmark) yang telah direbase ke 100% untuk perbandingan kinerja yang adil sejak awal periode.
- **Chart 2: Analisis Tren Harga Saham** — Grafik Candlestick harga harian saham terpilih yang dilengkapi dengan garis rata-rata pergerakan MA20 (tren jangka pendek) dan MA50 (tren jangka menengah) untuk membaca tren pasar.
- **Chart 3: Analisis Momentum MACD** — Grafik Moving Average Convergence Divergence (MACD Line, Signal Line, dan MACD Histogram) untuk mendeteksi kekuatan dorongan arah pergerakan harga.
- **Chart 4: Arah Tren Pasar (IHSG)** — Grafik garis pergerakan indeks IHSG terhadap garis MA50 untuk menentukan status pasar terkini (Bullish/Bearish).
- **Fitur interaktif**:
  - *Tooltip hover interaktif*: Menampilkan data harga penutupan eksak dan indikator secara detail saat disorot.
  - *Ruler Tool*: Pengukur rentang tanggal, persentase selisih harga, jumlah bar, dan volume perdagangan secara dinamis pada grafik tren.
  - *Dropdown Filter Saham*: Memilih dan memuat visualisasi saham tertentu secara instan.
  - *Timeframe Switcher*: Tombol interaktif untuk merubah periode pengelompokan data (Daily, Weekly, Monthly, Yearly).
  - *Sinkronisasi Zoom & Pan*: Geser (drag-pan) dan perbesar (scroll-zoom) sumbu X yang tersinkronisasi otomatis antara grafik tren dan volume/MACD.
- **Animasi**:
  - *Chart.js Entrance Animation*: Visualisasi grafik muncul perlahan dengan transisi ease-out saat halaman selesai dimuat.
  - *KPI Count-Up Number*: Angka counter pada 4 kartu KPI utama (Nilai IHSG, Status Pasar, Outperformer, Underperformer) terhitung naik secara dinamis dari 0 ke nilai target.
  - *CSS Fade-in / Sliding Entrance*: Elemen kartu dashboard dan peta heatmap masuk dengan animasi transisi yang halus.

## Sumber Data

- Nama dataset: **Yahoo Finance Historical Stock Market Prices**
- URL sumber: [https://finance.yahoo.com/](https://finance.yahoo.com/)
- Script pengambilan data otomatis: [scripts/fetch_data.py](file:///c:/Semester/Semester%206/Visualisasi%20Data/TUBES%20DASHBOARD%20SAHAM%20INDO%20MAGNIFIENT%207/indonesia-market-dashboard/scripts/fetch_data.py) (mengunduh data real-time, menyelaraskan tanggal perdagangan, dan menghitung MA20/MA50 secara backend).

## Cara Jalankan di Lokal

### Jalur A (Server Lokal dengan Python - Direkomendasikan):
Karena beberapa browser memblokir pembacaan file JSON lokal (`data/prices.json`) secara langsung karena kebijakan keamanan CORS, gunakan server HTTP sederhana bawaan Python:
1. Pastikan Python 3 sudah terinstal pada komputer Anda.
2. Buka terminal/command prompt di dalam direktori project.
3. Jalankan perintah berikut:
   ```bash
   python -m http.server 8000
   ```
4. Buka browser Anda dan akses: [http://localhost:8000](http://localhost:8000)

### Jalur B (Static):
Buka file `index.html` secara langsung di browser Anda (atau klik kanan -> *Open with Live Server* di VS Code).

### Langkah Pembaruan Data Historis (Opsional):
Jika Anda ingin mendownload ulang data pasar terbaru dari Yahoo Finance:
1. Instal dependensi python yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
2. Jalankan script fetch data:
   ```bash
   python scripts/fetch_data.py
   ```

## Teknologi

- **Chart.js** (Visualisasi grafik utama & candlestick)
- **Hammer.js & chartjs-plugin-zoom** (Kontrol interaksi geser dan perbesar sumbu X)
- **Luxon & chartjs-adapter-luxon** (Adapter pengolahan format tanggal)
- **yfinance, pandas, numpy** (Python library untuk scraping dan kalkulasi indikator)
- **HTML5, CSS3 (CSS Grid & Flexbox), dan Vanilla JavaScript (ES6)**
- **Vercel** (Platform deployment online static)

## Anggota Kelompok

- Mentheng Paskahbuana T (103012300128)
- Nama Anggota 2 (NIM)
- Nama Anggota 3 (NIM)
- Nama Anggota 4 (NIM)
- Nama Anggota 5 (NIM)
