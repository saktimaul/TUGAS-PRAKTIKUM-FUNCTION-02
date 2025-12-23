PENJELASAN KODE ARRAY PERKALIAN

-----------------------------------------------------------------
Baris 1-5: Persiapan Awal
-----------------------------------------------------------------
#include <iostream>
using namespace std;
int main() {
    int baris, kolom;
    cout << "Masukkan jumlah baris: ";

FUNGSI:
• Mengimpor library input/output standar C++ (<iostream>)
• Mengaktifkan namespace std agar tidak perlu prefix std:: berulang
• Mendeklarasikan fungsi utama program (main)
• Mendeklarasikan variabel penampung dimensi matriks (baris & kolom)
• Memberikan instruksi awal ke pengguna untuk memasukkan jumlah baris

-----------------------------------------------------------------
Baris 6-10: Input Dimensi & Inisialisasi Array
-----------------------------------------------------------------
    cin >> baris;
    cout << "Masukkan jumlah kolom: ";
    cin >> kolom;
    int matriksA[baris][kolom], matriksB[baris][kolom], hasil[baris][kolom];

FUNGSI:
• Membaca input jumlah baris dari pengguna
• Memberikan instruksi untuk memasukkan jumlah kolom
• Membaca input jumlah kolom dari pengguna
• Mendeklarasikan tiga array 2D dengan dimensi sesuai input:
  - matriksA: Menyimpan matriks pertama
  - matriksB: Menyimpan matriks kedua
  - hasil: Menyimpan output perkalian
• *Catatan: Penggunaan VLA (Variable Length Array) tidak standar di C++ murni

-----------------------------------------------------------------
Baris 11-15: Input Elemen Matriks Pertama
-----------------------------------------------------------------
    cout << "Masukkan elemen matriks A:\n";
    for (int i = 0; i < baris; i++) {
        for (int j = 0; j < kolom; j++) {
            cin >> matriksA[i][j];
        }
    }

FUNGSI:
• Memberikan petunjuk pengisian matriks pertama
• Menggunakan nested loop untuk iterasi:
  - Loop luar (i): Mengontrol baris matriks
  - Loop dalam (j): Mengontrol kolom matriks
• Membaca setiap elemen matriksA[i][j] dari input pengguna
• Menyimpan nilai input ke lokasi memori array yang sesuai

-----------------------------------------------------------------
Baris 16-20: Input Elemen Matriks Kedua
-----------------------------------------------------------------
    cout << "Masukkan elemen matriks B:\n";
    for (int i = 0; i < baris; i++) {
        for (int j = 0; j < kolom; j++) {
            cin >> matriksB[i][j];
        }
    }

FUNGSI:
• Memberikan petunjuk pengisian matriks kedua
• Menggunakan struktur nested loop identik dengan matriks pertama
• Loop luar mengiterasi setiap baris (i=0 hingga baris-1)
• Loop dalam mengisi setiap kolom (j=0 hingga kolom-1)
• Menyimpan input pengguna ke matriksB[i][j]

-----------------------------------------------------------------
Baris 21-25: Proses Perkalian & Output Langsung
-----------------------------------------------------------------
    cout << "Hasil perkalian:\n";
    for (int i = 0; i < baris; i++) {
        for (int j = 0; j < kolom; j++) {
            hasil[i][j] = matriksA[i][j] * matriksB[i][j];
            cout << hasil[i][j] << " ";

FUNGSI:
• Menampilkan header hasil perkalian
• Melakukan iterasi ulang menggunakan nested loop
• Menghitung perkalian elemen sejenis:
  hasil[i][j] = matriksA[i][j] × matriksB[i][j]
• *PENTING: Ini adalah perkalian elemen-wise (bukan perkalian matriks matematis)
• Langsung menampilkan hasil perhitungan setiap elemen
• Spasi (" ") dipakai sebagai pemisah antar elemen dalam satu baris

-----------------------------------------------------------------
Baris 26-30: Penyelesaian Output & Penutup Program
-----------------------------------------------------------------
        }
        cout << endl;
    }
    return 0;
}

FUNGSI:
• Menutup loop dalam (akhir baris matriks)
• cout << endl; : Pindah ke baris baru setelah satu baris selesai
• Menutup loop luar dan blok fungsi main()
• return 0; : Mengembalikan status sukses eksekusi program
• Menutup blok fungsi utama dengan kurung kurawal

-----------------------------------------------------------------
