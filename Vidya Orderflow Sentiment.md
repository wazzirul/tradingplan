# Dokumentasi: Vidya Orderflow Sentiment

## 1. Deskripsi

Script ini merupakan indikator gabungan berbasis Pine Script (TradingView) yang mengombinasikan VIDYA (Variable Index Dynamic Average) dengan analisis OrderFlow dan Sentimen pasar. Indikator ini dirancang untuk membantu trader memahami arah tren, kekuatan volume, serta distribusi order di sekitar harga saat ini, sehingga dapat meningkatkan akurasi pengambilan keputusan trading.

## 2. Indikator yang Digunakan

- **VIDYA (Variable Index Dynamic Average):** Moving average adaptif yang menyesuaikan sensitivitasnya berdasarkan volatilitas dan momentum harga.
- **OrderFlow & Sentiment Table:** Simulasi distribusi volume beli/jual pada 10 level harga di setiap candle, menampilkan sentimen dominan (Buy/Sell) dan total volume.
- **ATR (Average True Range):** Digunakan untuk menentukan band atas/bawah sebagai zona breakout atau reversal.
- **Pivot High/Low:** Deteksi titik support/resistance dinamis berdasarkan pola harga lokal.
- **Trend Marker:** Penanda perubahan tren dengan panah naik/turun pada chart.
- **Volume Delta:** Akumulasi volume selama tren naik/turun untuk mengukur kekuatan buyer/seller.

## 3. Manfaat Indikator

- **Identifikasi Tren Dinamis:** VIDYA memberikan sinyal tren yang lebih responsif terhadap perubahan volatilitas dibanding MA konvensional.
- **Visualisasi Sentimen OrderFlow:** Tabel orderbook membantu melihat distribusi volume dan sentimen dominan pada setiap level harga.
- **Deteksi Zona Likuiditas:** Pivot dan garis likuiditas menandai area support/resistance potensial yang sering menjadi titik reaksi harga.
- **Konfirmasi Breakout/Reversal:** Band ATR dan marker tren membantu mengidentifikasi peluang breakout atau potensi pembalikan arah.
- **Analisis Kekuatan Volume:** Volume delta memperlihatkan dominasi buyer/seller selama tren berlangsung.

## 4. Kegunaan untuk Trader (Entry, Sell, TP)

- **Entry (Buy/Sell):**
  - Entry buy dapat dipertimbangkan saat harga menembus band atas VIDYA dengan sentimen orderflow dominan beli dan volume delta positif.
  - Entry sell dipertimbangkan saat harga breakdown band bawah VIDYA dengan sentimen dominan jual dan volume delta negatif.
- **Konfirmasi & Filter:**
  - Gunakan marker panah (▲/▼) sebagai konfirmasi perubahan tren.
  - Perhatikan zona likuiditas (pivot/garis) sebagai area validasi entry atau potensi rejection.
- **Take Profit (TP):**
  - TP dapat ditempatkan di zona resistance/support berikutnya (pivot high/low) atau saat sentimen orderflow mulai berbalik.
  - Pantau perubahan volume delta dan sentimen untuk mengantisipasi potensi reversal.

Indikator ini sangat membantu trader dalam membaca kekuatan tren, distribusi volume, dan sentimen pasar secara visual dan terstruktur, sehingga keputusan entry, exit, dan TP menjadi lebih objektif dan berbasis data.
