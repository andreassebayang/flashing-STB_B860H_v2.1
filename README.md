# flashing-STB_B860H_v2.1
This is how to flashing and root the STB B860H v2.1

## 1. Persiapan
- Buka aplikasi USB Burning Tool
  Digunakan hanya untuk mendeteksi apakah sudah berhasil kedtect oleh Laptop/PC yang digunakan
- Sediakan kabel USB Male to Male
  Collokkan kabel USB Male to Male di laptop terlebih dahulu lalu dilanjutkan tekan dan tahan tombol power sambil mencolokkan kabel USB Male to Male di sisi STB
- Perhatikan Aplikasi USB Burning Tool
Perhatikan pada aplikasi Burning Tool apaka sudah sukses terbaca

## 2. **Menginstallan**
- BootcardMaker
  Buka aplikasi BootcardMaker dan jangan lupa tancapkan juga MicroSD Cardnya
- Choose Disk
  arahkan ke disk/microsd yang terdeteksi di Laptop/PC
- To Partition and Format
  janga lupa untuk centang pada Yes
- Choose your bin files
  Pada tahap ini klik open lalu cari file dengan nama u.boot.bin
- Proses
  Setelah klik Make maka akan proses dan tunggu hingga selesai

## 3. **Flasing**
- Setelah berhasil membuat bootloader dilanjut dengan tahap flashing
- car 3 file yang bernama:
  - boot.img
  - bootloader.img
  - u-boot.bin
  copy dan paste 3 file ini kedaam microsd card tadi lalu eject dan tancapkan ke dalam slot microsd card pada STB
- buka aplikasi Pulpstone_Amlogic_Update_USB_Tool_v2.1.exe
- lalu input angkat 8 dan enter
- Jika sudah selesai prosesnya maka lanjutkan step berikutnya,
- Copot kabel USB Male to Male, tancapkan kable power dan kabel HDMI yang terhubung ke Monitor/TV
- Tunggu proses booting
- taraaa sudah berhasil menginstall firmware dengan Pulstone

## 4. **Finishing**
- Buka terminal di STB
  - Ketik *Su* agar menjadi root user
  - ketik **ls storage** dan ini akan men-generate kode unik untuk storage anda
  - Selanjutnya ketikkan perintah berikut ini
    **dd if=/storage/xxx-xxxx/bootloader.img of=/dev/block/bootloader** lalu enter
    xxx-xxx = inputkan kode unik yang muncul ketika melakukan ls storage

## 5. **Flashing dan root sudah selesai**
