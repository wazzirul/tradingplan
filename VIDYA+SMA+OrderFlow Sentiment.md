# Dokumentasi Indikator: Volumatic VIDYA + SMA + OrderFlow Sentiment SwiftEdge

Dokumen ini menjelaskan secara rinci mengenai indikator multifungsi `Volumatic VIDYA + SMA + OrderFlow Sentiment SwiftEdge`. Penjelasan mencakup deskripsi umum, detail setiap komponen, serta panduan strategi trading menggunakan indikator ini.

---

## 1. Deskripsi Indikator

`Volumatic VIDYA + SMA + OrderFlow Sentiment SwiftEdge` adalah sebuah indikator teknikal yang dirancang untuk memberikan pandangan komprehensif mengenai kondisi pasar. Indikator ini menggabungkan empat alat analisis utama dalam satu tampilan untuk membantu trader mengambil keputusan yang lebih baik.

Kombinasi ini bertujuan untuk mengidentifikasi arah tren, mengukur kekuatan tren, menemukan level support/resistance yang signifikan, serta mengkonfirmasi sentimen pasar sesaat sebelum melakukan transaksi.

---

## 2. Detail Fungsi dan Komponen Indikator

Indikator ini terdiri dari beberapa komponen utama yang bekerja secara sinergis.

#### a. VIDYA (Variable Index Dynamic Average)
*   **Fungsi:** Sebagai garis *moving average* yang adaptif. Kecepatan VIDYA akan menyesuaikan diri dengan tingkat volatilitas pasar.
*   **Tampilan:** Garis yang warnanya berubah sesuai arah tren (misalnya, hijau untuk tren naik dan merah untuk tren turun). Garis ini berfungsi sebagai *support* dinamis saat tren naik dan *resistance* dinamis saat tren turun.

#### b. SMA (Simple Moving Average)
*   **Fungsi:** Sebagai *moving average* standar yang digunakan untuk konfirmasi tren jangka pendek atau menengah atau panjang (tergantung periode yang diatur, default 8).
*   **Tampilan:** Garis tunggal (default berwarna putih) yang bergerak lebih halus dibandingkan pergerakan harga. Posisi harga terhadap SMA membantu mengkonfirmasi kekuatan tren.

#### c. Liquidity Levels (Level Likuiditas Berbasis Pivot)
*   **Fungsi:** Mengidentifikasi dan menandai level *support* dan *resistance* statis yang signifikan.
*   **Tampilan:** Garis-garis horizontal yang ditarik dari titik *pivot high* (puncak harga) dan *pivot low* (lembah harga) sebelumnya. Level ini seringkali menjadi area di mana harga akan bereaksi (memantul atau menembus).

#### d. OrderFlow & Sentiment Table
*   **Fungsi:** Memberikan gambaran sentimen pasar pada *candle* saat ini melalui simulasi *order flow*.
*   **Tampilan:** Sebuah tabel di pojok chart yang berisi:
    *   **Persentase Sentimen:** Perbandingan kekuatan antara pembeli (Buy) dan penjual (Sell).
    *   **Volume Beli/Jual:** Simulasi distribusi volume pada berbagai level harga.
    *   **Informasi ini sangat berguna untuk konfirmasi akhir sebelum entry.**

---

## 3. Manfaat dan Strategi Trading

Indikator ini dirancang untuk memberikan sinyal trading dengan probabilitas tinggi dengan cara menggabungkan konfirmasi dari semua komponennya.

### a. Strategi Posisi BUY (Beli)

#### **Kondisi Entry (Masuk Pasar):**
Cari momen di mana **semua atau sebagian besar kondisi berikut terpenuhi** untuk mendapatkan sinyal beli dengan probabilitas tinggi:
1.  **Konfirmasi Tren:**
    *   Harga berada di atas garis VIDYA, dan garis VIDYA berwarna hijau (menandakan tren naik).
    *   Harga juga berada di atas garis SMA (menandakan konfirmasi tren naik jangka menengah/panjang).
2.  **Area Entry Ideal:**
    *   Harga melakukan *pullback* (koreksi turun) dan mendekati atau menyentuh garis VIDYA atau SMA.
    *   ATAU, harga memantul dari salah satu garis *Liquidity Level* (pivot low) yang berfungsi sebagai support.
3.  **Sinyal Pemicu (Trigger):**
    *   Muncul pola *candlestick bullish* (misalnya, Hammer, Bullish Engulfing, Pin Bar) di area entry ideal tersebut.
4.  **Konfirmasi Akhir (Sentimen):**
    *   Tabel *OrderFlow & Sentiment* menunjukkan sentimen **BUY dominan** (misalnya, di atas 60%). Ini menandakan bahwa pada saat itu, tekanan beli lebih kuat.

#### **Stop Loss (SL):**
*   Letakkan SL beberapa pips **di bawah** level support terdekat, yaitu:
    *   Di bawah garis *Liquidity Level* (pivot low) yang menjadi dasar pantulan.
    *   Atau di bawah swing low terakhir.

#### **Take Profit (TP):**
*   Gunakan level-level likuiditas (pivot high) yang berada di atas harga entry sebagai target profit.
    *   **TP 1:** Pada level pivot high terdekat.
    *   **TP 2:** Pada level pivot high berikutnya, dan seterusnya.

### b. Strategi Posisi SELL (Jual)

#### **Kondisi Entry (Masuk Pasar):**
Cari momen di mana **semua atau sebagian besar kondisi berikut terpenuhi** untuk sinyal jual dengan probabilitas tinggi:
1.  **Konfirmasi Tren:**
    *   Harga berada di bawah garis VIDYA, dan garis VIDYA berwarna merah (menandakan tren turun).
    *   Harga juga berada di bawah garis SMA (menandakan konfirmasi tren turun jangka menengah/panjang).
2.  **Area Entry Ideal:**
    *   Harga melakukan *pullback* (koreksi naik) dan mendekati atau menyentuh garis VIDYA atau SMA.
    *   ATAU, harga tertolak oleh salah satu garis *Liquidity Level* (pivot high) yang berfungsi sebagai resistance.
3.  **Sinyal Pemicu (Trigger):**
    *   Muncul pola *candlestick bearish* (misalnya, Shooting Star, Bearish Engulfing) di area entry ideal tersebut.
4.  **Konfirmasi Akhir (Sentimen):**
    *   Tabel *OrderFlow & Sentiment* menunjukkan sentimen **SELL dominan** (misalnya, di atas 60%). Ini menandakan tekanan jual sedang menguat.

#### **Stop Loss (SL):**
*   Letakkan SL beberapa pips **di atas** level resistance terdekat, yaitu:
    *   Di atas garis *Liquidity Level* (pivot high) yang menjadi dasar penolakan.
    *   Atau di atas swing high terakhir.

#### **Take Profit (TP):**
*   Gunakan level-level likuiditas (pivot low) yang berada di bawah harga entry sebagai target profit.
    *   **TP 1:** Pada level pivot low terdekat.
    *   **TP 2:** Pada level pivot low berikutnya, dan seterusnya.
