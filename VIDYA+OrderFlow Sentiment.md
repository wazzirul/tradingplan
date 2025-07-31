# Indikator Volumatic VIDYA + OrderFlow Sentiment SwiftEdge

## 1. Deskripsi
Indikator ini menggabungkan algoritma Variable Index Dynamic Average (VIDYA) dengan analisis OrderFlow dan Sentiment berbasis SwiftEdge. Tujuannya adalah memberikan gambaran tren harga, zona likuiditas, serta sentimen pasar secara visual dan interaktif pada chart trading.

## 2. Detail yang Ditampilkan
- **VIDYA Trend Line**: Menampilkan garis tren dinamis berdasarkan pergerakan harga dan momentum, dengan warna berbeda untuk uptrend dan downtrend.
- **Upper/Lower Bands**: Batas atas dan bawah berdasarkan VIDYA dan ATR (Average True Range) untuk mendeteksi breakout atau reversal.
- **OrderFlow & Sentiment Table**: Tabel di chart yang menampilkan:
  - Persentase sentimen beli/jual
  - Total volume beli dan jual
  - Distribusi volume pada 10 level harga (orderbook simulasi)
  - Highlight pada level harga saat ini
- **Zona Likuiditas**: Garis horizontal pada pivot high/low yang menandai area support/resistance penting, lengkap dengan label volume.
- **Delta Volume**: Statistik perbandingan volume tren naik dan turun.
- **Marker Trend Change**: Tanda panah pada chart saat terjadi perubahan tren.

## 3. Manfaat & Panduan Penggunaan untuk Trader
- **Entry**: 
  - Entry buy saat harga menembus upper band VIDYA dan sentimen didominasi volume beli (>50%).
  - Entry sell saat harga menembus lower band VIDYA dan sentimen didominasi volume jual (>50%).
  - Konfirmasi tambahan jika harga mendekati zona likuiditas (support/resistance) dan terjadi perubahan sentimen.
- **Stop Loss (SL)**:
  - Letakkan SL di bawah zona support (untuk buy) atau di atas zona resistance (untuk sell) yang ditandai oleh garis likuiditas.
  - Alternatif: gunakan band VIDYA sebagai acuan SL dinamis.
- **Take Profit (TP)**:
  - TP dapat ditempatkan pada zona likuiditas berikutnya atau saat sentimen mulai berbalik arah.
  - Perhatikan perubahan delta volume dan marker trend change sebagai sinyal exit.

Indikator ini membantu trader memahami kekuatan tren, area penting likuiditas, serta sentimen pasar secara real-time untuk pengambilan keputusan entry, SL, dan TP yang lebih presisi.
