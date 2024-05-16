# SCRIPT MODEM HILINK DAN PETUNJUK INSTALL
# TESTED
- ***Modem E5577***
- ***Modem E5372***
- ***Modem E5573***
- ***Modem E3372***
- ***Modem STC/MOD HUAWEI***


Copy paste di terminal OPENWRT:
```
bash -c "$(wget -qO - 'https://raw.githubusercontent.com/syahroni92/hilink/master/setup.sh')"
```

# Untuk menjalankan auto ganti ip ketika tidak ada koneksi
1. CARA 1

Hapus terlebih dahulu jika stbmu 
- B860H<br>
  copy paste di terminal script berikut<br>
  ```
  rm -f /usr/bin/bled && wget -O https://raw.githubusercontent.com/syahroni92/hilink/main/bled-hgled/bled && chmod +x /usr/bin/bled && /usr/bin/bled -r 
  ```
- HG680P<br>
  copy paste di terminal script berikut<br>
  ```
  rm -f /usr/bin/hgled && wget -O /usr/bin/hgled https://raw.githubusercontent.com/syahroni92/hilink/main/bled-hgled/hgled && chmod +x /usr/bin/hgled && /usr/bin/hgled -r
  ```
<br><br>
