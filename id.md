# Pahami algoritma `llama-3.3-70b-versatile`

- Tes telah diluncurkan selama beberapa minggu. Kita dapat melihat bahwa dia secara sistematis menjawab 53 dan 43, dan membuat variasi, namun sangat jarang.  
Artinya, ia menggunakan tanggapan terekam sebanyak 90%. Jadi mengapa melakukan ini?  
Ini sangat bagus, tapi juga sangat mudah ditebak. Jika kita melakukan itu, kita tidak perlu menulis ulang semuanya atau mengulangi perulangan, jika Anda mau.  
Hasilnya, kita bisa merespons dengan cepat, dengan biaya lebih rendah, namun masalahnya adalah kita tidak bisa berinovasi.  
Jika kami menginginkan sesuatu yang baru, kami akan mencoba mengambil potongan kode dan menyatukannya.  
Namun masalahnya adalah kita tidak bisa, misalnya, memiliki frontend yang layak dan inovatif, karena menggunakan kode yang sudah dibuat :)

# Bagaimana saya berhasil memahami

- Sederhananya, saya membuat `script` Python kecil yang digunakan untuk mengirim banyak permintaan.  
Ia bekerja dengan API. Semuanya siap membantu Anda kecuali API.  
Ini kira-kira bagian dari kode yang membuat loop pengiriman ini:

```python
while True:
    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input="Donne-moi un nombre entre 1 et 100",
        max_output_tokens=80
    )
```

- Apakah Anda akan memberi tahu saya: "Ya, perulangan while sederhana dengan Python?" Ya, tapi itu bekerja dengan sangat baik. Dalam 2 minggu, kami berhasil mencapai hasil yang memukau.

# Belajar oleh xql.dev

<h1>Suka AI & matematika</h1>