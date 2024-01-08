# UAS

| NAMA   | Agung Pratama Sentosa  |
| --- | --- |
| NIM    | 312310611 |
| KELAS  | TI.23.A6 |
| DOSEN  | Agung Nugroho,S.Kom.,M.Kom |
| LINK  |  https://youtu.be/QKFnIQJNBCo?si=DDmdyxZ3c1xHx7Aw |


1. *Menu dan Harga:*
   ```python
   menu = {
       'Nasi bakar': 15000,
       'Mie rebus telor': 12000,
       'Ayam bakar': 18000,
       'baso aci': 8000,
       'Es Teh': 5000,
       'Es Jeruk': 6000,
       'Air Mineral': 3000
   }
   ```
   
   - Mendefinisikan menu makanan/minuman beserta harganya menggunakan dictionary.

2. *Fungsi tampilkan_menu:*

    ```python
   def tampilkan_menu():
       print("Menu Makanan/Minuman:")
       for item, harga in menu.items():
           print(f"{item}: Rp {harga}")
   ```
   
   - Fungsi ini digunakan untuk menampilkan menu makanan/minuman beserta harganya.

4. *Fungsi hitung_total:*
   ```python
   def hitung_total(harga, jumlah):
       return harga * jumlah
   ```
   
   - Fungsi ini digunakan untuk menghitung total harga berdasarkan harga per item dan jumlah pesanan.

5. *Fungsi main:*

   ```python
   def main():
       pesanan = {}

       while True:
           tampilkan_menu()
           pilihan = input("Masukkan nama makanan/minuman yang ingin dipesan (ketik 'sudah' untuk menampilkan struk): ")

           if pilihan.lower() == 'sudah':
               break

           if pilihan in menu:
               jumlah = int(input(f"Masukkan jumlah {pilihan}: "))
               harga_total = hitung_total(menu[pilihan], jumlah)
               pesanan[pilihan] = {'jumlah': jumlah, 'harga_total': harga_total}
           else:
               print("Menu tidak ada. Silakan pilih menu yang tersedia.")
   ```

       # Tampilkan struk pembelian
   
   ```python
       print("\nStruk Pembelian:")
       total_pembelian = 0
       for item, detail in pesanan.items():
           print(f"{item} x{detail['jumlah']}: Rp {detail['harga_total']}")
           total_pembelian += detail['harga_total']

       print(f"\nTotal Pembelian: Rp {total_pembelian}")

   if __name__ == "__main__":
       main()
   ```
   - Fungsi main adalah inti dari program. Pada bagian ini, program meminta input pengguna untuk memilih makanan/minuman dan jumlahnya.
   - Pengguna dapat menghentikan pemesanan dengan memasukkan 'sudah'.
   - Program akan menyimpan pesanan dalam bentuk dictionary pesanan.
   - Setelah selesai memesan, program akan menampilkan struk pembelian beserta total pembelian.

7. *Block Terakhir:*

```python
   if __name__ == "__main__":
       main()
```

   - Ini adalah blok yang akan dieksekusi saat skrip dijalankan secara langsung (bukan diimpor sebagai modul). Itu memanggil fungsi main() untuk memulai eksekusi program. Perlu diperbaiki menjadi __main__ agar berfungsi dengan benar (if __name__ == "__main__":).
