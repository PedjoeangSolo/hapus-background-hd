# Hapus Background HD — Pro

Website untuk menghapus latar belakang foto dengan AI yang berjalan langsung di browser Android maupun desktop. **Tidak menggunakan Python, Gradio, API key, atau server pemrosesan milik sendiri.** GitHub Pages dapat meng-host berkas statis secara gratis.

## Fitur
- Model AI dari IMG.LY dengan pilihan **Medium** (seimbang antara kualitas dan kecepatan) serta **Small** (lebih ringan).
- Pratinjau dengan latar kotak-kotak, putih, hitam, atau abu-abu.
- Kuas manual untuk memulihkan bagian subjek yang terpotong atau menghapus sisa background.
- Pengaturan kelembutan tepi.
- Ekspor PNG transparan pada dimensi foto sumber.
- Pengaman unggahan: maksimal 20 MB dan 20 megapiksel untuk mengurangi risiko kehabisan memori pada HP.

## Cara menggunakan
1. Buka website dari browser HP atau PC.
2. Pilih foto yang ingin diedit.
3. Tekan **Hapus background AI** dan tunggu proses selesai.
4. Pada pemakaian pertama, library/model AI perlu diunduh melalui internet; proses pertama bisa lebih lama.
5. Periksa hasil dengan latar pratinjau berbeda.
6. Gunakan **Pulihkan bagian subjek** atau **Hapus bagian background** untuk koreksi manual.
7. Atur kelembutan tepi jika diperlukan, lalu tekan **Simpan PNG transparan**.

## Deploy gratis melalui GitHub Pages
1. Buka repositori GitHub ini.
2. Pilih **Settings → Pages**.
3. Pada **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch **main**, folder **/(root)**, lalu tekan **Save**.
5. Tunggu beberapa menit. Alamat website yang diharapkan: https://pedjoeangsolo.github.io/hapus-background-hd/

## Biaya, privasi, dan keterbatasan
- Hosting statis GitHub Pages gratis untuk repositori publik yang memenuhi ketentuan GitHub Pages.
- Inferensi AI berlangsung pada perangkat pengguna, sehingga tidak memerlukan compute server atau langganan hosting Python.
- Library dan model AI dimuat dari CDN, sehingga internet diperlukan. Unduhan model bisa cukup besar dan penggunaan data berbeda menurut model.
- Foto diproses di browser dan tidak diunggah ke server pemrosesan aplikasi oleh kode ini. Browser tetap mengunduh library/model dari CDN.
- Model **Medium** direkomendasikan sebagai titik awal; pilih **Small** bila HP terasa lambat atau kekurangan memori.
- Rambut halus, kaca, jaring, bayangan, atau subjek yang warnanya mirip latar mungkin perlu koreksi manual. Hasil tidak dijamin sempurna untuk semua gambar.
- Pada HP dengan RAM terbatas, foto besar dapat membuat browser melambat. Batas 20 megapiksel adalah pengaman, bukan jaminan semua perangkat dapat memproses setiap gambar di bawah batas itu.
- Model dan library pihak ketiga tunduk pada lisensi masing-masing; periksa ketentuannya untuk penggunaan komersial.

## Catatan teknis
Aplikasi memakai JavaScript module dari `@imgly/background-removal@1.7.0` yang dimuat dari jsDelivr. Tidak ada build step atau dependensi Python. Jika CDN atau unduhan model diblokir jaringan, pemrosesan tidak akan berjalan.

