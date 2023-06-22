# Deskripsi

ini gabut gak tau mau ngapain, kalau mau dicoba bisa ganti `listHarga` nya

## Tech Stack

**Language:** Javascript

## Full Code Preview

```js
// Muhammad Hilmi ー　ムハマド・ヒルミ

console.log('<===== SMK.DEV - CHALLANGE =====>');
console.log('<======== Toko Sepatu X ========>');
console.log('');

function getHargaTerbesarKedua(harga) {
  let [hargaTerbesar, hargaTerbesarKedua] = [harga[0], null];

  if (harga.length < 2) {
    return null;
  }

  for (let i = 1; i < harga.length; i++) {
    if (harga[i] > hargaTerbesar) {
      [hargaTerbesarKedua, hargaTerbesar] = [hargaTerbesar, harga[i]];
    } else if (hargaTerbesarKedua === null || harga[i] > hargaTerbesarKedua) {
      hargaTerbesarKedua = harga[i];
    }
  }

  var formatRupiah = new Intl.NumberFormat('id-ID', {
    style: 'currency',
    currency: 'IDR',
  });

  return formatRupiah.format(hargaTerbesarKedua);
}

// ======= Contoh =======  //
const listHarga = [70000, 55000, 120000, 100000, 20000, 5000];
const hargaTerbesarKedua = getHargaTerbesarKedua(listHarga);

console.log(
  hargaTerbesarKedua !== null
    ? `Harga yang harus dibayar adalah: ${hargaTerbesarKedua}`
    : `List harga tidak ada`
);
```

## Cara Jalanin

Clone projectnya kalau mau

```bash
  git clone https://github.com/Wakype/SMK.DEV-JSChallenge2.git
```

terus masuk ke foldernya

```bash
  cd SMK.DEV-JSChallenge2
```

Kalau mau di coba di install dulu packagenya

```bash
  npm install
```

Abis itu tinggal jalanin deh :)

```bash
  npm run dev
```

## Contoh

```javascript
const listHarga = [70000, 55000, 120000, 100000, 20000, 5000];
```

## Screenshots

![App Screenshot](https://i.ibb.co/S0sLLRB/Screenshot-2023-06-22-at-13-52-14.png)
