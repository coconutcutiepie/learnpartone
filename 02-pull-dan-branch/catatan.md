# catatan pull dan branch

## git pull — narik dari github ke laptop

- pull itu kebalikan push: github → laptop
- kapan dipake: tiap MAU MULAI kerja, atau abis ngedit lewat web github
- wajib jadi kebiasaan: git pull dulu sebelum ngedit apapun, biar mulai dari versi terbaru

### cara jalaninnya
1. cd ~/Documents/learnpartone
2. git pull
3. baca outputnya:
   - "Already up to date" = laptop udah sama kayak github, aman
   - "Updating xxx..xxx, Fast-forward" = ada perubahan baru ketarik masuk

## branch — dunia paralel dari kode aku

- branch = label/sticky note, BUKAN folder
- main = dunia utama, harus selalu bagus
- branch baru = tempat eksperimen bebas, main ga bakal kesentuh
- merge = gabungin hasil eksperimen ke main
- abis di merge, branchnya dihapus (isinya udah selamat di main)

### cara jalaninnya (siklus lengkap)
1. git pull                      → mulai dari versi terbaru
2. git switch -c nama-branch     → lahirkan dunia baru + pindah
3. edit file, save, tutup
4. git add . lalu git commit -m "pesan"
5. git switch main               → balik ke dunia utama (editan "ilang" = normal! dia nunggu di branch)
6. git merge nama-branch         → tarik hasilnya ke main
7. git push
8. git branch -d nama-branch     → buang labelnya

### perintah bantu
- git branch          → daftar branch, bintang = posisiku
- git branch -r       → daftar branch versi github

## versi kerja tim: lewat pull request
1. sampai langkah 4 sama kayak di atas
2. git push -u origin nama-branch   → kenalin branch ke github
3. buka PR di web github → direview → merge pake tombol
4. balik ke terminal: git switch main, git pull, git branch -d nama-branch

## jebakan yang harus diinget
- merge itu "narik ke sini" — harus BERDIRI di main dulu baru merge
- file di TextEdit ditutup dulu sebelum git switch, biar ga ketipu tampilan basi
- nama branch ga boleh pake spasi