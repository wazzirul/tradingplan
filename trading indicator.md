# Dokumentasi Indikator Trading

Dokumen ini menjelaskan dua indikator kustom untuk platform trading, yaitu "HMA Swing Levels" dan "Volumatic VIDYA + OrderFlow Sentiment SwiftEdge". Penjelasan mencakup deskripsi, komponen, kalkulasi, serta manfaat dan kegunaannya dalam analisis teknikal.

---

## 1. HMA Swing Levels [BigBeluga]

### Nama dan Deskripsi
*   **Nama:** `HMA Swing Levels [BigBeluga]`
*   **Deskripsi:** Indikator ini dirancang untuk mengidentifikasi level-level *swing high* dan *swing low* secara otomatis berdasarkan pergerakan harga dalam periode tertentu. Indikator ini juga menggunakan *Hull Moving Average* (HMA) untuk membantu mengkonfirmasi arah tren.

### Komponen, Tampilan, dan Kalkulasi
*   **Komponen Utama:**
    1.  **Swing Levels:** Garis horizontal yang ditarik dari titik harga tertinggi (swing high) dan terendah (swing low) dalam rentang `len2` (default 50 bar).
    2.  **Hull Moving Average (HMA):** Sebuah garis moving average (default periode 50) yang warnanya berubah sesuai arah tren. Hijau limau untuk tren naik dan merah untuk tren turun.
*   **Tampilan pada Chart:**
    *   Garis horizontal berwarna merah untuk level *resistance* (swing high).
    *   Garis horizontal berwarna hijau untuk level *support* (swing low).
    *   Garis HMA yang mengikuti pergerakan harga.
    *   Label harga pada setiap garis swing yang terbentuk.
*   **Kalkulasi:**
    *   Indikator mencari harga `high` tertinggi dan `low` terendah dalam `len2` bar terakhir.
    *   Sebuah *swing high* teridentifikasi jika harga saat ini lebih rendah dari `high` sebelumnya dan HMA menunjukkan sinyal positif (`change > 0`).
    *   Sebuah *swing low* teridentifikasi jika harga saat ini lebih tinggi dari `low` sebelumnya dan HMA menunjukkan sinyal negatif (`change < 0`).
    *   Garis akan diperpanjang hingga harga berhasil menembus level tersebut, di mana garis akan berubah menjadi putus-putus.

### Manfaat dan Kegunaan dalam Analisa

#### a. Menentukan Market Structure
Level *swing high* dan *swing low* yang digambarkan oleh indikator ini adalah fondasi dari struktur pasar.
*   **Uptrend:** Terbentuknya rangkaian *higher highs* (puncak yang lebih tinggi) dan *higher lows* (lembah yang lebih tinggi). Garis-garis hijau akan terbentuk di level yang semakin tinggi.
*   **Downtrend:** Terbentuknya rangkaian *lower highs* (puncak yang lebih rendah) dan *lower lows* (lembah yang lebih rendah). Garis-garis merah akan terbentuk di level yang semakin rendah.
*   **Range/Konsolidasi:** Harga bergerak di antara level support (garis hijau) dan resistance (garis merah) yang relatif sejajar.

#### b. Mengkonfirmasi Pola Candlestick
Level support dan resistance yang dihasilkan sangat berguna untuk memvalidasi sinyal dari pola candlestick.
*   **Sinyal Beli:** Jika muncul pola *bullish* (misalnya, Bullish Engulfing, Hammer, Pin Bar) tepat di atas atau saat memantul dari garis support (hijau), ini memperkuat sinyal untuk membuka posisi *buy*.
*   **Sinyal Jual:** Jika muncul pola *bearish* (misalnya, Bearish Engulfing, Shooting Star) tepat di bawah atau saat tertolak oleh garis resistance (merah), ini memperkuat sinyal untuk membuka posisi *sell*.

#### c. Mengidentifikasi Arah Tren
Selain dari struktur pasar, arah tren juga dapat dilihat secara langsung dari indikator HMA.
*   **Tren Naik:** Garis HMA berwarna hijau dan bergerak di bawah harga.
*   **Tren Turun:** Garis HMA berwarna merah dan bergerak di atas harga.

#### d. Strategi Entry, SL, dan TP
*   **Entry:**
    *   **Buy:** Lakukan entry saat harga melakukan *pullback* dan memantul dari garis support (hijau), idealnya dikonfirmasi dengan HMA yang berwarna hijau dan pola candle *bullish*.
    *   **Sell:** Lakukan entry saat harga melakukan *pullback* dan tertolak oleh garis resistance (merah), idealnya dikonfirmasi dengan HMA yang berwarna merah dan pola candle *bearish*.
*   **Stop Loss (SL):**
    *   Untuk posisi *buy*, letakkan SL beberapa pips di bawah garis support (hijau) yang menjadi dasar entry.
    *   Untuk posisi *sell*, letakkan SL beberapa pips di atas garis resistance (merah) yang menjadi dasar entry.
*   **Take Profit (TP):**
    *   **TP 1:** Level swing terdekat yang berlawanan. Untuk posisi *buy*, TP 1 adalah garis resistance (merah) terdekat. Untuk posisi *sell*, TP 1 adalah garis support (hijau) terdekat.
    *   **TP 2 & TP 3:** Level-level swing berikutnya yang lebih jauh.

---

## 2. Volumatic VIDYA + OrderFlow Sentiment SwiftEdge

### Nama dan Deskripsi
*   **Nama:** `Volumatic VIDYA + OrderFlow Sentiment SwiftEdge`
*   **Deskripsi:** Ini adalah indikator multifungsi yang menggabungkan beberapa alat analisis: VIDYA untuk tren dinamis, deteksi level likuiditas berbasis pivot, dan tabel sentimen pasar berdasarkan simulasi *order flow*.

### Komponen, Tampilan, dan Kalkulasi
*   **Komponen Utama:**
    1.  **VIDYA (Variable Index Dynamic Average):** Sebuah *moving average* adaptif yang kecepatannya disesuaikan dengan volatilitas pasar. Digunakan sebagai penentu tren utama dan level support/resistance dinamis.
    2.  **Liquidity Levels:** Garis horizontal yang ditarik dari titik *pivot high* dan *pivot low*. Garis ini merepresentasikan zona likuiditas atau support/resistance.
    3.  **OrderFlow & Sentiment Table:** Sebuah tabel yang menampilkan:
        *   Persentase sentimen *buy* vs *sell*.
        *   Simulasi volume beli dan jual pada berbagai level harga di dalam candle saat ini.
*   **Tampilan pada Chart:**
    *   Garis VIDYA yang warnanya berubah sesuai tren (hijau untuk naik, merah untuk turun).
    *   Garis-garis likuiditas dari titik pivot.
    *   Tanda panah (▲▼) saat terjadi perubahan tren.
    *   Tabel sentimen di pojok kanan chart.
*   **Kalkulasi:**
    *   **VIDYA:** Dihitung berdasarkan perubahan momentum harga, sehingga lebih responsif di pasar yang aktif dan lebih halus di pasar yang tenang.
    *   **Liquidity Levels:** Menggunakan fungsi `ta.pivothigh` dan `ta.pivotlow` untuk mendeteksi titik balik harga, lalu menarik garis dari sana.
    *   **Sentiment:** Mensimulasikan volume beli dan jual berdasarkan pergerakan harga (open, high, low, close) dan volume total dari candle saat ini. Ini adalah estimasi, bukan data order book riil.

### Manfaat dan Kegunaan dalam Analisa

#### a. Menentukan Market Structure
Level likuiditas yang berbasis pivot berfungsi sebagai level support dan resistance yang signifikan, membantu memetakan struktur pasar. Pergerakan harga di antara level-level ini akan membentuk struktur tren atau konsolidasi.

#### b. Mengkonfirmasi Pola Candlestick
Tabel sentimen memberikan konfirmasi tambahan yang kuat untuk pola candlestick.
*   **Contoh:** Sebuah pola *Bullish Engulfing* yang muncul di dekat level support (pivot low) akan jauh lebih valid jika tabel sentimen juga menunjukkan sentimen *buy* yang dominan (> 60%). Sebaliknya, jika sentimen *sell* yang dominan, pola tersebut kemungkinan adalah *fakeout* atau sinyal yang lemah.

#### c. Mengidentifikasi Arah Tren
*   **VIDYA:** Warna dan posisi garis VIDYA adalah indikator tren utama. Jika harga berada di atas VIDYA yang berwarna hijau, tren kuat naik. Jika harga di bawah VIDYA yang berwarna merah, tren kuat turun.
*   **Panah Sinyal:** Panah hijau (▲) menandakan awal tren naik, dan panah merah (▼) menandakan awal tren turun.

#### d. Strategi Entry, SL, dan TP
*   **Entry:**
    *   **Buy (High Probability):** Cari momen di mana **semua kondisi terpenuhi**:
        1. Harga melakukan *pullback* ke garis VIDYA atau ke level likuiditas (pivot low).
        2. Muncul pola candle *bullish*.
        3. Tabel sentimen menunjukkan dominasi *buyer*.
        4. Idealnya, sinyal panah ▲ baru saja muncul.
    *   **Sell (High Probability):** Cari momen di mana **semua kondisi terpenuhi**:
        1. Harga *pullback* ke garis VIDYA atau ke level likuiditas (pivot high).
        2. Muncul pola candle *bearish*.
        3. Tabel sentimen menunjukkan dominasi *seller*.
        4. Idealnya, sinyal panah ▼ baru saja muncul.
*   **Stop Loss (SL):**
    *   Untuk posisi *buy*, letakkan SL di bawah level pivot low terakhir.
    *   Untuk posisi *sell*, letakkan SL di atas level pivot high terakhir.
*   **Take Profit (TP):**
    *   **TP 1, TP 2, TP 3:** Gunakan level-level likuiditas (pivot) yang berlawanan sebagai target profit. Untuk posisi *buy*, setiap level pivot high di atas harga entry bisa menjadi target TP1, TP2, dan seterusnya.
