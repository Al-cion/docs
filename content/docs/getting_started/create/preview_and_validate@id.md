---
$title: Pratinjau dan Validasi
---

Pratinjau halaman AMP seperti Anda ingin mem-pratinjau situs HTML statis lainnya. Tidak ada langkah pembangunan atau prapemrosesan yang diperlukan. Gunakan salah satu cara berikut:

  - **Membukanya secara langsung dalam browser dari sistem file** (elemen tertentu mungkin tidak berfungsi karena gagalnya XMLHttpRequests).
  - **Menggunakan server web lokal seperti Apache 2 atau Nginx**.
    *(Tip: Untuk server web yang cepat, jalankan `python -m SimpleHTTPServer`.)*

Berikutnya, pastikan bahwa halaman AMP Anda **benar-benar merupakan halaman AMP yang valid**, jika tidak maka halaman tidak akan ditemukan dan didistribusikan oleh platform pihak ketiga seperti Google Penelusuran. Untuk memvalidasi:

  1. Buka halaman Anda di browser.
  1. Tambahkan "`#development=1`" ke URL, misalnya, `http://localhost:8000/released.amp.html#development=1`.
  1. Buka [konsol Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/debug/console/) dan periksa kesalahan validasi.

[Ketahui selengkapnya mengenai validasi](/id/docs/fundamentals/validate.html), dan tindakan yang harus Anda lakukan jika menjumpai kesalahan.

<div class="prev-next-buttons">
  <a class="button prev-button" href="/id/docs/getting_started/create/presentation_layout.html"><span class="arrow-prev">Sebelumnya</span></a>
  <a class="button next-button" href="/id/docs/getting_started/create/prepare_for_discovery.html"><span class="arrow-next">Berikutnya</span></a>
</div>
