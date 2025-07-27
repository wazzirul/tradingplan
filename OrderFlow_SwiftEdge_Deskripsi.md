# OrderFlow & Sentiment SwiftEdge

## Deskripsi
OrderFlow & Sentiment SwiftEdge adalah indikator analisis teknikal berbasis Pine Script yang menggabungkan data order flow, sentimen pasar, serta indikator MACD dan RSI untuk memberikan gambaran komprehensif tentang kekuatan pembeli dan penjual pada setiap candlestick. Indikator ini mensimulasikan distribusi volume pada berbagai level harga, menampilkan sentimen pasar, dan membantu trader dalam pengambilan keputusan entry, stop loss (SL), dan take profit (TP).

## Fitur Utama
- **Simulasi Orderbook:** Membagi rentang harga candlestick menjadi 10 level dan mengestimasi volume beli/jual di setiap level.
- **Sentimen Pasar:** Menghitung persentase kekuatan buyer dan seller berdasarkan distribusi volume.
- **Visualisasi MACD & RSI:** Menampilkan nilai MACD, Signal, dan RSI untuk konfirmasi momentum dan overbought/oversold.
- **Tabel Interaktif:** Menampilkan data orderbook, sentimen, dan indikator dalam satu tabel yang mudah dibaca.
- **Highlight Harga Terkini:** Menandai level harga saat ini pada tabel untuk memudahkan identifikasi area penting.

## Cara Kerja
1. **Orderbook Simulation:** Indikator membagi rentang harga candlestick menjadi 10 level, lalu mengestimasi volume beli dan jual di setiap level dengan mempertimbangkan aktivitas harga dan variasi acak.
2. **Sentiment Calculation:** Total volume beli dan jual dihitung, lalu persentase sentimen buyer/seller ditampilkan.
3. **MACD & RSI:** Nilai MACD, Signal, dan RSI dihitung untuk setiap candlestick dan ditampilkan pada tabel.
4. **Visualisasi:** Semua data ditampilkan dalam tabel di chart, dengan warna yang membedakan kekuatan buyer/seller dan menyorot harga terkini.

## Kegunaan untuk Analisa, Entry, SL, TP
- **Analisa:** Memudahkan identifikasi area harga dengan volume dominan, serta sentimen pasar secara real-time.
- **Entry:** Entry dapat dilakukan pada level harga dengan dominasi volume beli/jual dan konfirmasi dari MACD/RSI.
- **Stop Loss (SL):** SL dapat ditempatkan di bawah/atas level harga dengan volume besar yang berlawanan dengan arah entry.
- **Take Profit (TP):** TP dapat ditargetkan pada level harga berikutnya dengan volume besar atau saat sentimen mulai berbalik.

Indikator ini sangat cocok untuk trader yang ingin menggabungkan analisa order flow, sentimen, dan momentum dalam satu alat visual yang praktis.
