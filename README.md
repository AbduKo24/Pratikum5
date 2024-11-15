# Pratikum5

## Hasil Latihan Praktikum 5 
````Python
data_mahasiswa = []

while True:
    print("\nMasukkan data mahasiswa:")
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))

    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

    data_mahasiswa.append({
        'nama': nama,
        'nim': nim,
        'tugas': tugas,
        'uts': uts,
        'uas': uas,
        'nilai_akhir': nilai_akhir
    })

    tambah = input("\nTambah data lagi? (y/t): ").lower()
    if tambah == 't':
        break

print("\nDaftar Nilai Mahasiswa:")
print("="*80)
print(f"{'Nama':<15} {'NIM':<10} {'Tugas':<10} {'UTS':<10} {'UAS':<10} {'Nilai Akhir':<10}")
print("="*80)

for mhs in data_mahasiswa:
    print(f"{mhs['nama']:<15} {mhs['nim']:<10} {mhs['tugas']:<10} {mhs['uts']:<10} {mhs['uas']:<10} {mhs['nilai_akhir']:<10.2f}")

print("="*80)

````

## Hasil Output Pratikum 5
```markdown
Masukkan data mahasiswa:
Nama: Muhamad abdu
NIM: 312410143
Nilai Tugas: 95
Nilai UTS: 97
Nilai UAS: 98

Tambah data lagi? (y/t): t

Daftar Nilai Mahasiswa:
================================================================================
Nama            NIM        Tugas      UTS        UAS        Nilai Akhir
================================================================================
Muhamad abdu    312410143  95.0       97.0       98.0       96.75
================================================================================
```
# Penjelasan Latihan Praktikum 5
## Analisis Kode Python untuk Input dan Perhitungan Nilai Mahasiswa
1. Inisialisasi List untuk Menyimpan Data
   Di sini, data_mahasiswa adalah sebuah list kosong yang akan menyimpan data mahasiswa dalam bentuk dictionary.
 Setiap dictionary berisi data pribadi mahasiswa dan nilai-nilai yang telah dihitung.
2. Loop untuk Input Data Mahasiswa
   Program masuk ke dalam loop while True, yang berarti akan terus meminta input dari pengguna sampai kondisi tertentu tercapai untuk berhenti.
Di dalam loop, program meminta input berupa nama, NIM, nilai tugas, UTS, dan UAS.
Nilai tugas, UTS, dan UAS dikonversi ke tipe data float karena input tersebut berupa angka desimal.
3. Perhitungan Nilai Akhir
   Nilai akhir dihitung menggunakan rumus tertentu, yaitu:

    Nilai Tugas (30% dari total nilai)
    Nilai UTS (35% dari total nilai)
    Nilai UAS (35% dari total nilai)
Hasil dari perhitungan nilai akhir ini disimpan dalam variabel nilai_akhir.
4. Menambahkan Data Mahasiswa ke List
   Setelah menghitung nilai akhir, data mahasiswa disimpan dalam bentuk dictionary dan ditambahkan ke dalam list data_mahasiswa.
Dictionary tersebut berisi informasi nama, NIM, nilai tugas, nilai UTS, nilai UAS, dan nilai akhir mahasiswa.
5. Mengecek Apakah Pengguna Ingin Menambah Data Lagi
   Program meminta input apakah pengguna ingin memasukkan data mahasiswa lagi. Jika pengguna menjawab dengan 't' (untuk "tidak"), maka loop akan
berhenti dan program akan melanjutkan ke tahap berikutnya. Fungsi .lower() digunakan untuk memastikan bahwa input diterima
dalam format huruf kecil (misalnya 'Y' atau 'y' tetap dianggap sebagai jawaban "ya").
6. Menampilkan Data Mahasiswa dalam Format Tabel
   Setelah loop selesai, program menampilkan daftar nilai mahasiswa dalam format tabel.
print("="*80) digunakan untuk membuat garis pembatas yang panjang.
Baris pertama tabel mencetak header dengan nama kolom yang diposisikan dengan lebar tertentu menggunakan format f-string
seperti {'Nama':<15}, yang memastikan bahwa setiap kolom memiliki lebar yang konsisten.
Program kemudian melakukan iterasi melalui list data_mahasiswa dan mencetak informasi setiap mahasiswa dalam format yang sesuai.
Nilai akhir ditampilkan dengan dua digit setelah koma desimal (<10.2f).
7. Menutup Tabel dengan Garis Pembatas
   abel ditutup dengan garis pembatas lagi untuk membuat tampilannya lebih rapi.

# Kesimpulan
Secara keseluruhan, kode ini sudah berfungsi dengan baik untuk menginput data mahasiswa, menghitung nilai akhir, dan menampilkan hasilnya dalam bentuk tabel.
Dengan sedikit perbaikan dalam validasi input dan modularisasi, kode ini bisa lebih robust dan lebih mudah dipelihara.

