# catatan undo 


## 3 jurus membatalkan kesalahan

- git restore namafile            → buang editan yang BELUM di-add (file balik ke commit terakhir)
- git restore --staged namafile   → keluarin file dari kardus (un-add), tulisan TETAP ADA
- git revert HEAD --no-edit       → batalkan commit terakhir secara resmi

## setup git restore 1 
- cd ~/Documents/learnpartone
- git pull
- mkdir 03-undo
- touch 03-undo/catatan.md
- open -e 03-undo/catatan.md
- git status → merah, modified — Git lihat editanmu
- git restore 03-undo/catatan.md

# jurus 1: git restore

- buat editan jelek yang belum sempet di add
- PERINGATAN: permanen! editan yang dibuang ga bisa balik karena belum pernah di commit
- pastiin emang mau dibuang sebelum ngetik ini

## setup git restore --staged 
- buat editan jelek yang belum sempet di add
- git add . 
- git status kalau yang muncul hijau, staged siap di commit 
- git restore --staged 03-undo/catatan.md
- git status kalau balik merah lagi dia keluar dari kardus tapi editan nya masih ada di file

# jurus 2: git restore --staged

- cuma ngeluarin dari kardus, tulisan di file aman
- status dari hijau (staged) balik ke merah (modified)
- kepake kalo udah git add . tapi ada file yang belum siap ikut commit

## setup git revert

- git add. 
- commit -m "percobaan buat di revert"
- git revert HEAD --no-edit
- git push 

# jurus 3: git revert

- HEAD artinya commit terakhir
- revert GA menghapus commit yang salah, dia bikin commit BARU yang isinya kebalikannya
- riwayat tetap jujur: pernah salah, terus dibatalkan
- makanya aman dipakai walaupun udah ke push
- kalo mau revert commit yang lebih lama: git log --oneline dulu, terus git revert kodecommit

## pelajaran tambahan

- tutup dulu file di TextEdit sebelum git restore / git switch, biar ga ketipu tampilan basi
- percaya sama git status, bukan sama jendela yang kebuka
- ketik nama file yang bener: 03-undo/catatan.md (pake - dan /), bukan pake spasi

