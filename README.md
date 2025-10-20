# MATKUL-SIG-D4TI-ULBI-2025
Tugas Matakuliah Sistem Informasi Geografis 

# 🗺️ Peta Digital Jalan Sariasih, Sarijadi – Kota Bandung

## 📘 Deskripsi Proyek
Proyek ini dibuat untuk memenuhi **Tugas Praktik Mata Kuliah Sistem Informasi Geografis (SIG)**.  
Data yang dibuat berisi representasi **jalan dan titik-titik penting di Kelurahan Sarijadi, Kecamatan Sukasari, Kota Bandung, Jawa Barat**, menggunakan format **GeoJSON**.

Data ini berfokus pada **Jalan Sariasih** dan beberapa ruas jalan kecil di sekitarnya seperti jalan di **kawasan Polban (Politeknik Negeri Bandung)** dan **ULBI (Universitas Logistik dan Bisnis Internasional)**.

---

## 🧭 Tujuan Pembuatan
Tujuan dari pembuatan data ini adalah untuk:
1. Mempelajari cara membuat data **spasial** menggunakan format **GeoJSON**.  
2. Menggambarkan **jalur jalan dan titik penting** di sekitar lokasi tempat tinggal (Sarijadi).  
3. Menyimpan dan menampilkan data geografis ke dalam sistem **SIG digital** seperti **geojson.io**, **QGIS**, dan **MongoDB**.  
4. Membuktikan bahwa format data sudah **valid secara sintaks dan semantik**.

---

## 📍 Lokasi Penelitian
- **Nama Jalan Utama:** Jalan Sariasih  
- **Kelurahan:** Sarijadi  
- **Kecamatan:** Sukasari  
- **Kota:** Bandung  
- **Provinsi:** Jawa Barat  
- **Koordinat Pusat:** 107.576° BT, -6.874° LS  
- **Wilayah Sekitar:** Politeknik Negeri Bandung (Polban), Pusdilat Pos, Pasar Sarijadi, dan ULBI.  
<img width="1411" height="901" alt="image" src="https://github.com/user-attachments/assets/ea67ec29-3c12-48d1-ac34-4916967c7d43" />

---

## 📂 Struktur Dasar GEOJSON
Berikut adalah contoh struktur dasar GEOJSON yang digunakan dalam proyek ini:

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "name": "Nama Jalan"
      },
      "geometry": {
        "type": "LineString",
        "coordinates": [
          [longitude1, latitude1],
          [longitude2, latitude2]
        ]
      }
    }
  ]
}
```
Penjelasan elemen:

* **type** → menentukan jenis data (`FeatureCollection` atau `Feature`)
* **properties** → menyimpan informasi tambahan seperti nama jalan
* **geometry** → berisi tipe geometri dan koordinat lokasi
* **coordinates** → berisi pasangan nilai `[longitude, latitude]`

---

## 🗺️ Data GEOJSON Saya

Berikut isi file GEOJSON yang telah saya buat:

```json
{
  "type": "Feature",
  "properties": {
    "name": "Segmen ULBI 2"
  },
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [107.5757583361837, -6.8739466464968615],
      [107.57571092906232, -6.8742618270786835]
    ]
  }
}
```

### 📍 Informasi Detail

| Atribut               | Nilai                                                                             |
| --------------------- | --------------------------------------------------------------------------------- |
| **Nama Jalan**        | Segmen ULBI 2                                                                     |
| **Lokasi**            | Sekitar Kampus Universitas Logistik dan Bisnis Internasional (ULBI), Kota Bandung |
| **Tipe Geometri**     | LineString                                                                        |
| **Koordinat Titik 1** | (107.5757583361837, -6.8739466464968615)                                          |
| **Koordinat Titik 2** | (107.57571092906232, -6.8742618270786835)                                         |
| **Sistem Koordinat**  | EPSG:4326 (WGS84)                                                                 |

---

## ✅ Validasi dan Pengujian

File GEOJSON telah diuji menggunakan situs **[geojson.io](https://geojson.io)** dengan hasil sebagai berikut:

* ✅ **File berhasil dimuat tanpa error.**
* ✅ **Garis (LineString)** muncul jelas di peta pada area Kampus ULBI Bandung.
* ✅ Properti `name` ditampilkan dengan benar pada tampilan peta.

---

## 🧩 Cara Uji Sendiri di geojson.io

1. Buka situs [https://geojson.io](https://geojson.io)
2. Klik menu **Open → File**
3. Pilih file `jalan_ulbi2.geojson` (atau nama file kamu)
4. Pastikan garis muncul di peta dan nama properti terlihat di sisi kanan

Jika garis muncul tanpa error, berarti file GEOJSON kamu **benar secara sintaks dan semantik** ✅

---

## 📸 Hasil Visualisasi

Tampilan di geojson.io menampilkan:

* Garis pendek (segmen jalan) di sekitar **Universitas Logistik dan Bisnis Internasional (ULBI)**
* Peta dasar (base map) menampilkan area Kota Bandung
* Informasi properti `name: "Segmen ULBI 2"` muncul saat fitur diklik

> *(Tambahkan screenshot peta di sini jika tersedia, misalnya `assets/hasil-geojson.png`)*

---

## 📁 Struktur Repository GitHub

```
📦 geojson-praktek-ulbi
├── README.md
├── jalan_ulbi2.geojson
└── assets/
    └── hasil-geojson.png  (opsional)
```

---

## 🧠 Kesimpulan

* GEOJSON memudahkan penyimpanan dan pertukaran data spasial berbasis web.
* Tipe **LineString** digunakan untuk memetakan objek berbentuk garis seperti jalan, sungai, atau batas wilayah.
* Data yang dibuat berhasil divisualisasikan tanpa kesalahan, menandakan pemahaman yang baik terhadap format GEOJSON.

---

## 🏫 Informasi Pembuat

| Keterangan         | Data                                                 |
| ------------------ | ---------------------------------------------------- |
| **Nama**           | Efendi Sugiantoro                                    |
| **Mata Kuliah**    | Sistem Informasi Geografis (SIG)                     |
| **Institusi**      | Universitas Logistik dan Bisnis Internasional (ULBI) |
| **Dosen Pengampu** | *(Isi sesuai nama dosen pengajar)*                   |
| **Tahun Akademik** | 2025                                                 |

---

## 💬 Catatan Tambahan

Setiap segmen jalan memiliki nilai **5 poin**.
Tugas ini mengerjakan **1 jalan (Segmen ULBI 2)** dengan total **5 poin dari maksimal 30 poin**.

---

## 🔗 Referensi

* [geojson.io](https://geojson.io) – alat untuk membuat dan memverifikasi data GeoJSON
* [GeoJSON Specification (RFC 7946)](https://datatracker.ietf.org/doc/html/rfc7946)
* [QGIS Documentation](https://docs.qgis.org/latest/en/docs/) – perangkat lunak open-source GIS

---

### ✨ Lisensi

Dokumen ini bersifat terbuka untuk keperluan pembelajaran SIG.
© 2025 Efendi Sugiantoro – Universitas Logistik dan Bisnis Internasional (ULBI)

```
