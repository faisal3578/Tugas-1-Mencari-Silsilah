![Gambar soal](https://github.com/faisal3578/Tugas-1-Mencari-Silsilah/blob/master/Soal.jpeg)
# Proses
### orang tua, saya sudah meletakkan seluruh nama orang tua berada di sebelah kanan dari data base sehingga memunculkan seluruh nama di sebelah kanan adalah orang tua dan di sebelah kiri adalah anaknya

#### 1. orangTua
```
orangTua(Y,X):-ank(Y,X).
(Y disini adalah subjek yang ingin di cari)
orangTua(Y,X):-ank(Y,X).
proses
Y adalah orangTua dari si X jika Y anak dari X
(Keluar lah hasil orangTua Y adalah X)
```
#### 2. anak
```
anak(Y,X):-ank(X,Y).
(Y disini adalah subjek yang ingin di cari)
proses
Y adlah Anak dari Si X Jika X ank dari Y
(Keluar Hasil anak Y adalah X)
```
#### 3. saudara
```
saudara(Saus1,Saus2):-
    ank(Saus1,Ortu),
    ank(Saus2,Ortu),
    (   Saus1)\=(Saus2).
(Saus1 adalah Subjek yang ingin di cari begitu pula sebaliknya)
saus1 adalah dari saudara saus2 jika
saus1 anak dari ortu dan saus2 ank dari ortu dan
saus1 tidak sama dengan saus2

karena data base langsung mengambil nama dari ortu sehingga
memunculkan nama yang memiliki ortu yang sama
```
#### 4. sepupu
```
sepupu(Spp1,Spp2):-
    ank(Spp1,Ortu1),
    ank(Spp2,Ortu2),
    ank(Ortu1,Kakek),
    ank(Ortu2,Kakek),
    (   Ortu1)\=(Ortu2).
spp1 adalah sepupu dari spp2 jika
spp1 adalah anak dari ortu1 dan
spp2 anak dari ortu2 dan
ortu1 anak dari kakek dan
ortu2 anak dari kakek 
ortu1 tidak sama dengan ortu2

di sini subjek langsung menggambil nama ortu dari spp1,spp2 
dari data base mengelolah nama sang ortu1 dan ortu2 mendapatkan anam kakek
kemudian anak dari kakek yang ingin di cari 
mengambil nama dari anak kakek yang tidak berasal dari subjek
Keluarlah nama dari sepupu

```
#### 5. Kakek/Nenek
```
bolang(Subjek,Kakek):-
    ank(Subjek,Ortu),
    ank(Ortu,Kakek).
Subjek adalah bolang dari Kakek Jika
Subjek ank dari Ortu dan
Ortu Ank dari Kakek

di sini Subjek mencari nama di database nama ortu
dan ortu di cari juga nama sang kakeknya
dapatlah hasil nama Kakek/Nenek nya
```
