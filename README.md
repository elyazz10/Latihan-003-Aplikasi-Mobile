# LAUNDRY

Ahmad Ilyas - 1125170130

## Business Rules

- **BR-01:** Tarif laundry sebesar Rp7.000 untuk setiap kg.
- **BR-02:** Berat laundry di bawah 2 kg tetap dihitung 2 kg.
- **BR-03:** Layanan Express mendapat tambahan biaya 50%.



```dart
void main() {
  //latihan 3 laundry ilyas
  int berat = 3;
  String layanan = "Express";

  int harga = hitungHarga(berat);
  int tambahan = hitungTambahan(harga, layanan);
  int total = hitungTotal(harga, tambahan);

  print("Berat laundry : $berat kg");
  print("Layanan       : $layanan");
  print("Harga laundry : Rp$harga");
  print("Tambahan      : Rp$tambahan");
  print("Total bayar   : Rp$total");
}


// ngitung harga laundry
int hitungHarga(int berat) {
  if (berat < 2) {
    berat = 2;
  }

  return berat * 7000;
}


// ngitung tambahan biaya ekpress
int hitungTambahan(int harga, String layanan) {
  if (layanan == "Express") {
    return harga * 50 ~/ 100;
  }

  return 0;
}


// ngitung total pembayarannye
int hitungTotal(int harga, int tambahan) {
  return harga + tambahan;
}
```
