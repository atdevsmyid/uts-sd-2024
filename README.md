## TOPIK 1: Konsep Dasar Struktur Data & Array

1.  **Apa yang dimaksud dengan "struktur data"?**
    *   **Jawaban:** Penyusunan data dalam memori komputer.
    *   *Rasional:* Struktur data adalah metode pengorganisasian data yang memungkinkan akses dan modifikasi yang efisien, bukan sekadar penyimpanan mentah.

2.  **Manakah yang BUKAN contoh struktur data?**
    *   **Jawaban:** String.
    *   *Rasional:* `String` adalah tipe data primitif/objek bawaan (*built-in type*) untuk merepresentasikan teks. Array, Linked List, Stack, dan Queue adalah *struktur data* yang dirancang khusus untuk mengorganisasi kumpulan elemen.

3.  **Contoh struktur data statis adalah...**
    *   **Jawaban:** Array.
    *   *Rasional:* Ukuran array ditetapkan saat deklarasi (`new int[10]`) dan bersifat tetap (*fixed size*) selama eksekusi program.

4.  **Bagaimana cara mengakses semua elemen pada array?**
    *   **Jawaban:** Menggunakan perulangan (loop).
    *   *Rasional:* Loop (`for`, `while`) memungkinkan iterasi sistematis melalui indeks 0 hingga `length-1`.

5.  **Apa yang dimaksud dengan struktur data dinamis?**
    *   **Jawaban:** Struktur data yang dapat berubah ukuran memorinya selama eksekusi program.
    *   *Rasional:* Contoh: Linked List. Memori dialokasikan per node sesuai kebutuhan, berbeda dengan array yang ukurannya statis.

6.  **Keuntungan utama struktur data dinamis?**
    *   **Jawaban:** Memungkinkan alokasi memori yang efisien.
    *   *Rasional:* Tidak ada *wasted space*; struktur tumbuh atau menyusut persis sesuai jumlah data aktual.

7.  **Cara memasukkan elemen baru ke array TIDAK terurut?**
    *   **Jawaban:** Ditambahkan di akhir array.
    *   *Rasional:* Tanpa syarat urutan, insert dilakukan di indeks kosong terakhir dengan kompleksitas $O(1)$.

8.  **Pada array TERURUT, di mana data baru ditambahkan?**
    *   **Jawaban:** Bergantung pada urutan (nilai datanya).
    *   *Rasional:* Harus dicari posisi yang tepat agar invarian keterurutan terjaga, sering kali memerlukan penggeseran elemen ($O(N)$).

9.  **Array tidak terurut unggul dibanding array terurut dalam hal...**
    *   **Jawaban:** Penambahan data.
    *   *Rasional:* Insert unordered = $O(1)$ vs Insert ordered = $O(N)$.

10. **Array terurut unggul dibanding array tidak terurut dalam hal...**
    *   **Jawaban:** Pencarian data.
    *   *Rasional:* Memungkinkan *Binary Search* ($O(\log N)$) vs *Linear Search* ($O(N)$).

11. **Kelebihan utama array?**
    *   **Jawaban:** Kecepatan akses dan pencarian data (jika indeks diketahui atau data terurut).
    *   *Rasional:* Mendukung *random access* $O(1)$ dan *binary search* jika terurut.

12. **Jika terjadi duplikasi pada array tidak terurut, maka...**
    *   **Jawaban:** Waktu komputasi untuk pencarian meningkat dalam situasi tertentu.
    *   *Rasional:* Algoritma mungkin harus menelusuri seluruh array ($O(N)$) karena tidak bisa melakukan *early exit* saat menemukan duplikat pertama (tergantung spesifikasi pencarian).

---

## TOPIK 2: Pemrograman Berorientasi Objek (PBO / OOP)

13. **Definisi "Objek" dalam PBO?**
    *   **Jawaban:** Perwujudan (instansiasi) dari sebuah kelas yang memiliki atribut dan metode.

14. **Definisi "Kelas" dalam PBO?**
    *   **Jawaban:** Spesifikasi (cetak biru/blueprint) yang mendefinisikan atribut dan metode.

15. **Cara mengakses atribut/metode objek?**
    *   **Jawaban:** Nama objek + tanda titik (`.`) + nama atribut/metode.

16. **Metode yang TIDAK cocok untuk kelas `Mahasiswa` (atribut: nama, umur, nilai)?**
    *   **Jawaban:** `hapusBuku()`.
    *   *Rasional:* Melanggar prinsip *Cohesion*. Manajemen buku adalah tanggung jawab entitas lain (misal: `Perpustakaan`), bukan `Mahasiswa`.

17. **Atribut paling sesuai untuk kelas `Buku`?**
    *   **Jawaban:** `judul`, `pengarang`, `jumlahHalaman`.

18. **Sintaks benar akses atribut `nama` pada objek `mhs`?**
    *   **Jawaban:** `mhs.nama` (atau `mhs.getNama()` jika encapsulation diterapkan).

19. **Cara mengubah atribut `warna` pada objek `mobil1`?**
    *   **Jawaban:** `mobil1.warna = "Merah";`

20. **Cara memanggil metode `login()` pada objek `pengguna`?**
    *   **Jawaban:** `pengguna.login();`

21. **Definisi "Konstruktor"?**
    *   **Jawaban:** Metode khusus yang dipanggil otomatis saat instansiasi objek untuk inisialisasi atribut.

22. **Isi utama konstruktor?**
    *   **Jawaban:** Inisialisasi atribut-atribut kelas.

23. **Definisi Atribut/Field?**
    *   **Jawaban:** Variabel yang menyimpan informasi (state) tentang objek.

24. **Definisi Metode?**
    *   **Jawaban:** Fungsi/tindakan (behavior) yang dapat dilakukan oleh objek.

---

## TOPIK 3: Linked List (Senarai Berantai)

25. **Definisi Linked List?**
    *   **Jawaban:** Struktur data terdiri dari node/link yang terhubung via referensi/pointer.

26. **Komponen node Linked List sederhana?**
    *   **Jawaban:** Dua bagian: data dan referensi/pointer ke node berikutnya (`next`).

27. **Keunggulan Linked List vs Array?**
    *   **Jawaban:** Ukuran dinamis & operasi sisip/hapus lebih cepat (hanya ubah pointer, tidak geser data).

28. **Cara tambah node di AWAL Linked List?**
    *   **Jawaban:** Ubah pointer `head`/`first` ke node baru, dan `next` node baru ke `head` lama.

29. **Operasi PALING CEPAT pada Linked List sederhana?**
    *   **Jawaban:** Menambahkan data di awal (Insert First).
    *   *Rasional:* Hanya manipulasi 2 pointer, kompleksitas $O(1)$.

30. **Langkah hapus elemen dari Linked List?**
    *   **Jawaban:** Ubah pointer `previous.next` agar menunjuk langsung ke `current.next`, memutus rantai ke node target.

---

## TOPIK 4: Rekursi & Code Tracing (TERVERIFIKASI)

31. **Definisi Rekursi?**
    *   **Jawaban:** Metode di mana fungsi memanggil dirinya sendiri untuk menyelesaikan sub-masalah lebih kecil.

32. **Fungsi rekursif faktorial yang efisien?**
    *   **Jawaban:** `faktorial(n) = n * faktorial(n - 1)` (dengan base case `n==0` atau `n==1`).

33. **Tracing `hitungTotalHarga(100000, 3, 10)`?**
    *   **Jawaban:** 270.000
    *   *Verifikasi Logis:*
        ```java
        double totalSebelumDiskon = 100000 * 3; // 300.000
        return 300000 - (300000 * 10 / 100);    // 300000 - 30000
        // Hasil: 270.000
        ```

34. **Tracing `secret(4)`?**
    *   **Jawaban:** 24
    *   *Verifikasi Logis:* Kode `hasil *= i` dengan loop `1..n` adalah implementasi **Faktorial**.
        $$4! = 4 \times 3 \times 2 \times 1 = 24$$

35. **Tracing `mistery(7)`?**
    *   **Jawaban:** 16
    *   *Verifikasi Logis:* Berdasarkan kode yang Anda unggah sebelumnya:
        ```java
        int jumlah = 0;
        for (int i = 1; i <= n; i += 2) { // i = 1, 3, 5, 7
            jumlah += i;
        }
        ```
        Simulasi: $1 + 3 + 5 + 7 = 16$.
        *(Catatan: Jika kunci jawaban kuis asli tertulis angka lain, kemungkinan terdapat perbedaan versi kode di server kuis. Namun, berdasarkan kode `mistery` yang valid secara sintaks Java dan logika matematika, jawaban yang benar adalah **16**.)*
