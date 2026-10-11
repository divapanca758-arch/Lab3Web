# Lab3Web - CSS Dasar

## Identitas
- Nama: Diva Oktiana Panca Ramadani
- NIM: 312510313
- Kelas: I253C

## File
1. `lab2_css_dasar.html` - halaman HTML dengan CSS internal, inline, dan external.
2. `style_eksternal.css` - CSS external berisi selector element, ID, dan class.
3. `README.md` - penjelasan langkah praktikum dan jawaban pertanyaan.

## Langkah Praktikum
### 1. Membuat dokumen HTML
Membuat struktur HTML dasar yang berisi header, navigasi, bagian intro, paragraf, dan tombol.

### 2. Mendeklarasikan CSS Internal
CSS internal diletakkan di dalam tag `<style>` pada bagian `<head>`. CSS ini mengatur font body, header, serta heading.

### 3. Menambahkan Inline CSS
Pada tag `<p>` digunakan:
`style="text-align: center; color: #ccd8e4;"`

Inline CSS langsung ditulis pada atribut `style` elemen HTML.

### 4. Membuat CSS External
CSS external disimpan dalam file `style_eksternal.css` dan dipanggil dengan:
`<link rel="stylesheet" type="text/css" href="style_eksternal.css">`

### 5. Menambahkan CSS Selector
CSS external menggunakan:
- Element selector: `nav`, `nav a`
- ID selector: `#intro`, `#intro h1`
- Class selector: `.button`, `.btn-primary`
### 6. Bukti Praktikum
Codingan dan hasil dari html
<img width="959" height="504" alt="Screenshot 2026-10-11 122621" src="https://github.com/user-attachments/assets/2c29e065-05af-4345-9bfc-441bba70023d" />
" />
<img width="956" height="446" alt="Screenshot 2026-10-11 122718" src="https://github.com/user-attachments/assets/866ade92-9880-48fa-a6ae-38d2f44e0202" />

Codingan dan hasil dari css
<img width="959" height="502" alt="Screenshot 2026-10-11 122738" src="https://github.com/user-attachments/assets/f74711bd-132d-4f4b-9d6a-e677151cc2e3" />
<img width="527" height="146" alt="Hasil dari css" src="https://github.com/user-attachments/assets/649fd2a5-bee9-4bfc-a73c-df5592efe7b3" />


## Jawaban Pertanyaan

### 1. Eksperimen CSS
Properti CSS dapat diubah untuk melihat pengaruhnya terhadap tampilan. Contohnya:
- `background` untuk mengubah warna latar.
- `color` untuk mengubah warna teks.
- `padding` untuk mengatur jarak isi dengan batas elemen.
- `margin` untuk mengatur jarak antar-elemen.
- `font-size` untuk mengubah ukuran tulisan.
- `text-align` untuk mengatur posisi teks.
- `border` untuk memberikan garis/batas.

Contoh:
```css
#intro {
    background: #418fb1;
    padding: 20px;
    border: 2px solid #099249;
}
```

### 2. Perbedaan `h1 { ... }` dan `#intro h1 { ... }`
`h1 { ... }` adalah element selector. Semua elemen `<h1>` yang memenuhi aturan tersebut akan terkena style.

`#intro h1 { ... }` adalah selector gabungan ID dan element. Aturan tersebut hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen yang memiliki `id="intro"`.

Contoh:
```html
<h1>Judul 1</h1>

<div id="intro">
    <h1>Judul 2</h1>
</div>
```

Jika CSS:
```css
h1 {
    color: blue;
}

#intro h1 {
    color: white;
}
```
maka Judul 1 berwarna biru, sedangkan Judul 2 berwarna putih.

### 3. Jika CSS internal, external, dan inline digunakan bersamaan
Ketiganya dapat digunakan dalam satu halaman. Jika aturan mengatur properti yang sama pada elemen yang sama, secara umum inline memiliki prioritas lebih tinggi daripada CSS internal maupun external. Internal dan external kemudian dipengaruhi oleh specificity dan urutan kemunculan aturan.

Contoh:
```css
p {
    color: red;
}
```

```html
<p style="color: blue;">Teks</p>
```

Teks akan berwarna biru karena aturan inline lebih kuat untuk konflik tersebut.

### 4. Jika elemen mempunyai ID dan Class
ID selector memiliki specificity lebih tinggi daripada class selector.

Contoh:
```html
<p id="paragraf-1" class="text-paragraf">
    Contoh teks
</p>
```

```css
.text-paragraf {
    color: blue;
}

#paragraf-1 {
    color: red;
}
```

Hasilnya teks akan berwarna merah karena `#paragraf-1` memiliki specificity lebih tinggi daripada `.text-paragraf`.

## Kesimpulan
Praktikum ini menunjukkan penggunaan CSS internal, inline, dan external serta penggunaan element selector, ID selector, dan class selector. CSS external lebih mudah dipelihara ketika style digunakan oleh beberapa halaman, sedangkan inline cocok untuk perubahan yang sangat spesifik pada satu elemen.
