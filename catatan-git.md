
# HOW TO BUILD A SECOND REPOSITORY OR REPO 

- cd ~/Documents/learnpartone git pull
- outputnya udah already up to date , artinya good 
- build a sec repo 
- git switch -c catatan
- touch catatan-git.md open -e catatan-git.md
- touch itu bikin file kosong baru 
- kan kalo langsung open -e file belum ada makanya "touch" dulu 


# isi file nya di TextEdit 

# catatan git aku

## siklus harian
- cd ~/Documents/learnpartone   # 1. masuk folder repo
- git pull                      # 2. tarik yang terbaru DULU sebelum ngedit
- open -e README.md             # 3. edit → save → tutup
- git status                    # 4. lihat apa yang berubah
- git add .                     # 5. masukin ke "kardus"
- git commit -m "pesan jelas"   # 6. segel + label kardusnya
- git push                      # 7. kirim ke github


## branch
- git switch -c nama-branch   # lahirkan dunia baru + pindah ke sana
- git switch main             # balik ke dunia utama
- git merge nama-branch       # (dari main) tarik hasil eksperimen ke sini
- git branch -d nama-branch   # buang label yang udah selesai

## jebakan yang pernah aku alamin
- dquote> = kutip belum ketutup, keluarnya control+C
- git status 

## cara buka file ini 
- cd ~/Documents/learnpartone
- git pull
- open -e catatan-git.md

## kalau udah langsung jalanin kaya biasa command s atau save 

- git status
- git add .
- git commit -m "benerin judul catatan"
- git push
