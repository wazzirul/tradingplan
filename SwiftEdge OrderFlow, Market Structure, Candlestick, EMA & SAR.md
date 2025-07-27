# SwiftEdge OrderFlow, Struktur Pasar, Candlestick, EMA & SAR

## Gambaran Umum

**SwiftEdge OrderFlow, Struktur Pasar, Candlestick, EMA & SAR** adalah indikator Pine Script komprehensif untuk TradingView yang menggabungkan:
1. Visualisasi Orderflow & sentimen (tabel)
2. Struktur pasar (Higher High, Lower Low)
3. Pengenalan berbagai pola candlestick
4. EMA 4 & EMA 50
5. Parabolic SAR

Dioptimalkan untuk mode gelap dan kejelasan.

---

## Fitur Utama

### 1. Visualisasi Orderflow & Sentimen (Tabel)
- Membagi harga menjadi 10 rentang/zona per bar.
- Menghitung volume beli/jual dan sentimen untuk setiap rentang.
- Menampilkan tabel (kanan atas/tengah/bawah) dengan:
  - Harga, Volume Beli, Volume Jual, Volume Total
  - Menyorot rentang harga saat ini
  - Bar sentimen (% Beli / % Jual)

### 2. Struktur Pasar
- Mendeteksi dan menandai Higher Highs (segitiga biru ke atas) dan Lower Lows (segitiga oranye ke bawah).

### 3. Pengenalan Berbagai Pola Candlestick
- Mengenali dan menandai:
  - Bullish/Bearish Engulfing
  - Hammer, Inverted Hammer
  - Shooting Star, Hanging Man
  - Doji
  - Morning/Evening Star
  - Three White Soldiers/Black Crows
  - Piercing Line, Dark Cloud Cover
  - Tweezer Top/Bottom
- Setiap pola digambarkan dengan warna/bentuk unik untuk kejelasan.

### Penjelasan Pola Candlestick & Warnanya

Berikut adalah rincian bagaimana setiap pola candlestick ditandai pada grafik untuk identifikasi yang mudah:

#### Pola Bullish (Sinyal Potensi Kenaikan)
- **Bullish Engulfing**: Label **hijau limau (lime)** di bawah candle.
- **Hammer**: Segitiga ke atas berwarna **hijau limau transparan** di bawah candle.
- **Morning Star**: Segitiga ke atas berwarna **hijau solid** di bawah candle.
- **Three White Soldiers**: Segitiga ke atas berwarna **hijau solid** di bawah candle.
- **Piercing Line**: Label **hijau limau (lime)** di bawah candle.
- **Tweezer Bottom**: Segitiga ke atas berwarna **hijau limau (lime)** di bawah candle.

#### Pola Bearish (Sinyal Potensi Penurunan)
- **Bearish Engulfing**: Label **merah** di atas candle.
- **Shooting Star**: Segitiga ke bawah berwarna **oranye** di atas candle.
- **Hanging Man**: Segitiga ke atas berwarna **oranye transparan** di atas candle.
- **Evening Star**: Segitiga ke bawah berwarna **merah solid** di atas candle.
- **Three Black Crows**: Segitiga ke bawah berwarna **merah solid** di atas candle.
- **Dark Cloud Cover**: Label **merah** di atas candle.
- **Tweezer Top**: Segitiga ke bawah berwarna **merah solid** di atas candle.

#### Pola Netral / Keraguan
- **Doji**: Lingkaran **abu-abu** di atas candle.
- **Inverted Hammer**: Segitiga ke bawah berwarna **hijau limau transparan** di atas candle.

### 4. EMA Cross (4/50)
- Menampilkan **EMA 4** (garis hijau) dan **EMA 50** (garis putih).
- Ketika EMA 4 dan EMA 50 bersilangan, sebuah tanda silang (**kuning**) akan muncul pada titik persilangan di grafik.
- Teks "**4/50 X**" juga akan ditampilkan di bagian bawah grafik untuk menandakan terjadinya persilangan.

### 5. Parabolic SAR
- Menggambarkan titik-titik SAR untuk mengikuti tren.
- Parameter akselerasi yang dapat disesuaikan.

---

## Skema Warna & Visual
- Semua warna dipilih untuk kontras tinggi dalam mode gelap.
- Tabel dan label menggunakan latar belakang semi-transparan agar mudah dibaca.
- Penanda pola candlestick berukuran kecil dan tidak mengganggu.

---

## Tips Penggunaan
- Gunakan tabel sentimen untuk mengukur bias pasar secara sekilas.
- Gabungkan dengan analisis aksi harga (price action) Anda sendiri untuk hasil terbaik.

---

## Contoh Grafik

> Saat mengirim tangkapan layar untuk analisis AI, pastikan hal-hal berikut terlihat:
> - Tabel sentimen (kanan atas/tengah/bawah)
> - Penanda pola candlestick
> - Plot EMA dan SAR

Ini akan membantu AI memberikan umpan balik yang lebih akurat dan sesuai konteks.

---

## Versi
- Terakhir diperbarui: Juli 2025
- Pine Script v6

---

## Penulis
- Skrip dioptimalkan dan didokumentasikan oleh AI (GitHub Copilot)
- Asli oleh wazirul azzan
