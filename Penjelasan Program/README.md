
# 🧩 **Penjelasan Program Daftar Nilai Mahasiswa**

Program ini adalah aplikasi sederhana berbasis terminal untuk mengelola data nilai mahasiswa menggunakan **dictionary** di Python. Program menyediakan menu untuk:

✔ Menambah data
✔ Mengubah data
✔ Menghapus data
✔ Menampilkan semua data
✔ Mencari data per mahasiswa
✔ Keluar dari program

---

# 🗂 **1. Struktur Penyimpanan Data**

```python
data_mahasiswa = {} 
```

Data disimpan dalam bentuk dictionary dengan format:

```python
{
    'Nama': [nilai_tugas, nilai_uts, nilai_uas]
}
```

### Contoh isi dictionary:

```python
{
    "Budi": [80, 75, 90],
    "Ani": [70, 85, 88]
}
```

---

# 🧮 **2. Fungsi Menghitung Nilai Akhir**

```python
def hitung_nilai_akhir(tugas, uts, uas):
    nilai_akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
    return nilai_akhir
```

➡ Menghitung nilai akhir berdasarkan bobot:

* **Tugas: 30%**
* **UTS: 35%**
* **UAS: 35%**

---

# ➕ **3. Fungsi Tambah Data**

Program akan:

1. Meminta nama mahasiswa
2. Meminta nilai tugas, UTS, UAS
3. Memvalidasi apakah nilainya antara 0–100
4. Menambahkan data ke dictionary

```python
if nama in data_mahasiswa:
    print("Error: sudah ada")
```

Jika mahasiswa sudah ada, maka program menolak input duplikat.

---

# ✏️ **4. Fungsi Ubah Data**

1. Program meminta nama mahasiswa
2. Jika nama tidak ditemukan → tampilkan error
3. Jika ditemukan → tampilkan nilai lama
4. Minta nilai baru dan validasi
5. Update data mahasiswa dalam dictionary

---

# ❌ **5. Fungsi Hapus Data**

```python
if nama in data_mahasiswa:
    del data_mahasiswa[nama]
```

Jika nama ada, data akan dihapus. Jika tidak, muncul pesan error.

---

# 📋 **6. Fungsi Tampilkan Data**

Program menampilkan seluruh mahasiswa dengan format tabel:

```
Nama              Tugas   UTS     UAS     Nilai Akhir
---------------------------------------------------
Daffa             80.0    85.0    90.0    85.75
Indah             70.0    75.0    80.0    75.25
```

Data disortir berdasarkan nama menggunakan:

```python
for nama in sorted(data_mahasiswa.keys()):
```

---

# 🔍 **7. Fungsi Cari Data**

Program akan:

1. Meminta nama mahasiswa
2. Menampilkan nilai tugas, uts, uas, dan nilai akhir jika ditemukan
3. Jika tidak ditemukan → tampilkan error

---

# 🧭 **8. Fungsi Menu Utama**

Bagian terpenting adalah loop utama:

```python
while True:
```

Menu ditampilkan terus-menerus sampai user memilih **6 (Keluar)**.

Menu pilihan:

1. Tambah Data
2. Ubah Data
3. Hapus Data
4. Tampilkan Data
5. Cari Data
6. Keluar

Pemilihan menggunakan kondisi:

```python
if pilihan == '1':
    tambah_data()
```

---

# 🟢 **9. Bagian Eksekusi Program**

```python
if __name__ == "__main__":
    main_menu()
```

Artinya, fungsi `main_menu()` hanya dijalankan jika file ini dijalankan secara langsung — bukan diimport dari file lain.

---

# 📌 **Kesimpulan Program**

Program ini memberikan fitur CRUD (Create, Read, Update, Delete) sederhana untuk mengelola nilai mahasiswa menggunakan dictionary. Program cocok untuk:

✔ Tugas kuliah
✔ Pembelajaran dasar Python
✔ Belajar struktur data dan control flow

