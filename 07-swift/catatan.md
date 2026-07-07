Hari ini nulis kode swift pertama pake swift playground 

## byte 

# byte loves to collect gems with moveForwards()

- level 1 moveForward()

- moveForward()
- moveForward()
- moveForward()
- collectGem()

# progress part 1 done untuk mainan byte, next level 2

## commit "solved 2 puzzle: turnLeft, toggleSwitch, algoritma!"

- level 2 itu toggleSwitch()

- moveForward()
- moveForward()
- turnLeft()
- moveForward()
- collectGem()
- moveForward()
- turnLeft()
- moveForward()
- moveForward()
- toggleSwitch()

#progess part 2 done byte , next level 3


- level 3 bug and debugging 
07-swift/catatan.md → tambahin:
- level 3: debugging = nemuin & benerin bug
- bug ≠ selalu salah ketik, bisa juga SALAH URUTAN (logic bug)
- cara: run dulu → tonton di mana mulai ngaco → benerin bagian itu doang

- level 4 loops 
 Loop = pengulangan: "lakukan 10x

Masalah yang dia selesaikan simpel banget. Misal Byte harus maju-ambil-permata 4 kali berturut-turut. Cara lamamu:

- moveForward()
- moveForward()
- turnLeft()
- moveForward()
- collectGem()
- moveForward()
- turnLeft()
- moveForward()
- moveForward()
- toggleSwitch()

- cara baru pakai for loop 

- for i in 1 ... 4 {
    moveForward()
    collectGem()
}

## hari 2: if dan else

- else = jalur "kalau nggak": if iya kerjain A, else kerjain B
- dari 2 jalur PASTI TEPAT SATU yang jalan
- if else + loop = kode pendek yang siap ngadepin peta acak
- collectGem() di kotak kosong = error, jangan asal else

## else if — rantai pengecekan

- else biasa itu BUTA: asal bukan A langsung kerjain B (bahaya di kotak kosong!)
- else if = else yang ikut ngecek dulu: "kalau bukan switch, TAPI ada permata, baru ambil"
- if isOnClosedSwitch { toggleSwitch() } else if isOnGem { collectGem() }
- kalau dua duanya nggak cocok → skip, aman di kotak kosong
- rantainya bisa panjang: if → else if → else if → else
- komputer ngecek URUT dari atas, berhenti di yang PERTAMA cocok

## pelajaran dari "very creative!"

- lolos puzzle ≠ pake cara yang bener, playgrounds bisa nyindir 😂
- jangan ada toggleSwitch() / collectGem() telanjang — semua harus dijaga if
