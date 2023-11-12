# Praktikum 7: JOIN, ROF dan CF

Berikut adalah langkah-langkah pengerjaan praktikum disertai dengan hasil screenshot:
##
 
## Langkah-langkah:
1. Pertama, buat beberapa table pada script dan masukkan data sesuai dengan yang diminta
<br>Kode dan hasil sebagai berikut:

![Gambar](../Fol%201/Gambar/Screenshot%20(169).png)

2. Untuk menampilkan semua nama nama mahasiswa beserta nama departemen mahasiswa tersebut, dapat menggunakan 
 ```
    SELECT s.name as Nama_Mahasiswa, d.dept_name as Departemen
    from student s
    left join department d on s.dept_name = d.dept_name;
 ``` 
<br>Kode dan hasil sebagai berikut:

![Gambar](../Fol%201/Gambar/Screenshot%20(170).png)

3. Untuk menampilkan semua nama student beserta nama department yang memiliki total SKS
(total credit) lebih dari 100 dapat menggunakan
 ```
    SELECT s.name as Nama_Mahasiswa, d.dept_name as Departemen
    from student s
    inner join department d on s.dept_name = d.dept_name
    where s.tot_cred > 100;
 ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](../Fol%201/Gambar/Screenshot%20(171).png)

3. Untuk menampilkan nama student dan nama instructor yang bekerja pada department yang
sama
 ```
    SELECT s.name as Nama_Mahasiswa, d.dept_name as Departemen
    from student s
    join instructor i on s.dept_name = i.dept_name ;
 ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](../Fol%201/Gambar/Screenshot%20(172).png)