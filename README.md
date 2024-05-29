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
  rm -f /usr/bin/bled && wget -O /usr/bin/bled https://raw.githubusercontent.com/syahroni92/hilink/main/bled-hgled/bled && chmod +x /usr/bin/bled && /usr/bin/bled -r 
  ```
- HG680P<br>
  copy paste di terminal script berikut<br>
  ```
  rm -f /usr/bin/hgled && wget -O /usr/bin/hgled https://raw.githubusercontent.com/syahroni92/hilink/main/bled-hgled/hgled && chmod +x /usr/bin/hgled && /usr/bin/hgled -r
  ```


rumus lock band,

#"only LTE": with specific frequency
#LTE band: all
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,7FFFFFFFFFFFFFFF,,"

LTE band: 1(CM_BAND_PREF_LTE_EUTRAN_BAND1) => LTE BC1 - 2100 MHz - AT/- // CR/-
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,1,,"

LTE band: 2(CM_BAND_PREF_LTE_EUTRAN_BAND2) => LTE BC2 - 1900 MHz - AT/- // CR/-
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,2,,"

LTE band: 4(CM_BAND_PREF_LTE_EUTRAN_BAND3) => LTE BC3 - 1800 MHz - AT/3 // CR/Claro + Movistar
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,4,,"

LTE band: 10(CM_BAND_PREF_LTE_EUTRAN_BAND5) => LTE BC5 - 850 MHz - AT/- // CR/-
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,10,,"

LTE band: 40(CM_BAND_PREF_LTE_EUTRAN_BAND7) => LTE BC7 - 2600 MHz - AT/A1 // CR/Kölbi
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,40,,"

LTE band: 80(CM_BAND_PREF_LTE_EUTRAN_BAND8) => LTE BC8 - 900 MHz - AT/- // CR/-
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,80,,"

LTE band: 80000(CM_BAND_PREF_LTE_EUTRAN_BAND20) => LTE BC20 - 800 MHz - AT/A1 // CR/-
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,80000,,"

LTE band: 40000000(CM_BAND_PREF_NO_CHANGE) No band change
#gsmctl -A "AT^SYSCFGEX="03",3FFFFFFF,1,2,40000000,,"

<br><br>
