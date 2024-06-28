# Laporan Resmi Praktikum Sistem Operasi 2024 Final Project

## Anggota Kelompok IT 12
| Nama Lengkap          | NRP        |
| --------------------- | ---------- |
| Muhammad Dzaky Ahnaf  | 5027231039 |
| Adlya Isriena Aftarisya  | 5027231066 |
| Nisrina Atiqah Dwiputri Ridzki  | 5027231075 |

# Daftar Isi
- [Deskripsi Soal](#deskripsi-soal)
- [Penjelasan Kode](#penjelasan-kode)
- [Dokumentasi Program](#dokumentasi-program) 

## Deskripsi Soal
Intinya pada tugas Final Project ini, kita diharapkan membuat sebuah program apikasi chatting DiscorIT. DiscorIT terdiri dari 3 program yaitu discorit, server, dan monitor. Program discorit dan monitor berperan sebagai client, sedangkan program server berperan sebagai server yang dimana client dan server berinteraksi melalui socket.
- Program discorit bekerja sebagai client yang mengirimkan request user kepada server.
- Program server berjalan sebagai server yang menerima semua request dari client dan mengembalikan response kepada client sesuai ketentuan pada soal. Program server berjalan sebagai daemon.
- Untuk hanya menampilkan chat, user perlu membuka program client (monitor)

## Penjelasan Kode
## Dokumentasi Program
### 1. Autentikasi User
- Melakukan register dan login user

![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/055b8439-17ea-48da-9beb-f5e19ed5b668)

- Akan tercatat informasi nama user, password yang terenkripsi dengan bcrypt, dan role nya di ```users.csv```

![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/a08a33d3-bf81-449f-8c41-232458da8f63)


### 2. Fitur Channel
- Membuat channel

![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/81032d2e-9dc9-418f-8a0d-fd1bcdcb0aaa)

- Akan tercatat informasi nama channel dan key yang terenkripsi dengan bcrypt di ```channels.csv```

![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/93da0491-52e2-4df7-9456-599dc45720f9)

- Akan terbuat sebuah file baru bernama channel yang dibuat sebelumnya dan ```admin``` didalamnya yang berisi ```auth.csv``` dan ```users.log```. Semua perubahan dan aktivitas user pada channel dicatat dalam file ```users.log``` dan informasi mengenai user dan rolenya pada channel tersebut dicatat dalam file ```auth.csv```

![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/33ffdc4f-c4d4-4841-8fce-6ecd6e9119c6)

  - Isi ```auth.csv```
    
    ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/9b3d3f29-398e-49f6-8b98-ea731429b75e)

  - Isi ```users.log```
    
    ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/dda82a49-5c53-4135-bbe2-5ebca2e73a56)

- User Join channel
  - Ketika user memiliki role ```ROOT``` akan langsung join tanpa memasukkan key
    
    ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/ef314744-3b30-4c7e-b339-54867b50579d)
    
  - Ketika user tidak memiliki role ```ROOT``` akan join dengan memasukkan key
    
    ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/cda4c5c0-5297-40a1-bee7-99d6fdf39ddd)

- User ROOT mengedit dan menghapus channel.
 
    ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/c8950163-b8f2-4502-bac0-a3b58b93199e)

    
### 3. Fitur Room
- Membuat dan join room

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/4f92f53c-1f4d-4e9e-bd6a-fc0f51ed6120)

- Chat didalam room, melihat, mengedit, dan menghapus chat di room.
  
  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/a7d0c4d4-8416-4f60-8950-d06d8f128e71)

- Admin channel mengedit room, menghapus room, dan menghapus semua room.

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/7d3fda4c-f393-4e41-ad5b-0e8e7798146c)


### 4. Fitur pada user ROOT
- User ROOT dapat melakukan edit dan remove user lain.

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/c980d375-ff21-48b7-960b-937839bcf261)

- Admin dapat melakukan ban, unban, dan remove user lain

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/e2791bf3-5641-4edf-adf3-0565316795df)
### 5. Fitur pada user masing-masing
- User bisa mengedit profile masing-masing seperti username dan password.

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/127a384a-ff5b-40f3-a041-79d6aa242f4e)

- User ketika dirinya dibanned karena nakal.

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/8f7bf972-a3c8-499f-9dc5-70d5b1494c3f)

### 6. Hasil ```auth.csv``` dan ```users.log``` setelah eksperimen

- ```auth.csv```

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/7d996320-123e-400b-96cd-ef552ce7f910)

- ```users.log```

  ![image](https://github.com/DzakyAhnaf/Sisop-FP-2024-MH-IT12/assets/110287409/6a06ac96-d6e8-4dd6-a3dd-e2a896bed317)

### 7. Fitur Monitor
