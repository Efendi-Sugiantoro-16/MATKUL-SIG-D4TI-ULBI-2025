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
##Penjelasan elemen:

type → menentukan jenis data (FeatureCollection atau Feature)

properties → menyimpan informasi tambahan seperti nama jalan

geometry → berisi tipe geometri dan koordinat lokasi

coordinates → berisi pasangan nilai [longitude, latitude]
