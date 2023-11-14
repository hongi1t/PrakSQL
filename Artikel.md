# Praktikum 8: Fungsi Skalar dan Agregasi
##
Nama        : Fathiya Aulia Khoirunnisa
<br>NIM     : 225150600111027
<br>Kelas   :   PTI-DBDSQL-A
## 
Berikut adalah langkah-langkah pengerjaan praktikum disertai dengan hasil screenshot:
##
## Langkah-langkah:
1. Pertama, Menjalankan fungsi Concat dengan syntax seperti berikut:
    ```
    SELECT CONCAT_WS(' ', ID, name) AS PROFIL
    FROM sampel_university.student;
    ```
<br>Kode dan hasil sebagai berikut:
![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(197).png)

2.  Selanjutnya, menjalankan fungsi SUBSTRING_INDEX dengan syntax seperti berikut:
    ```
    SELECT SUBSTRING_INDEX(dept_name, ' ', 1) AS JURUSAN_INDEX
    FROM sampel_university.department;
    ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(199).png)

3. Menjalankan fungsi SUBSTR dengan syntax seperti berikut:
   ```
   SELECT SUBSTR(dept_name, 1, 3) AS KARAKTER
   FROM department;
   ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(201).png) 

4. Menjalankan fungsi LENGTH dengan syntax seperti berikut:
    ```
    SELECT LENGTH(dept_name) AS KARAKTER
    FROM department;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(203).png)

5. Menjalankan fungsi REPLACE dengan syntax seperti berikut:
    ```
    SELECT REPLACE(dept_name, 'old_string', 'new_string') AS UpdatedColumnName
    FROM department;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(205).png)

6. Menjalankan fungsi ABS dengan syntax seperti berikut:
    ```
    SELECT ABS(salary) AS AbsoluteSalary
    FROM instructor;
    ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(207).png)

7.  Menjalankan fungsi CEILING dengan syntax seperti berikut:
    ```
    SELECT CEILING(credits) AS RoundedCredits
    FROM course;
    ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(209).png)

8. Menjalankan fungsi FLOOR dengan syntax seperti berikut:
   ```
   SELECT FLOOR(salary) AS FlooredSalary
    FROM instructor;
   ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(211).png) 

9. Menjalankan fungsi ROUND dengan syntax seperti berikut:
    ```
    SELECT ROUND(budget) AS RoundedBudget
    FROM department;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(214).png)

10. Menjalankan fungsi SQRT dengan syntax seperti berikut:
    ```
    SELECT SQRT(capacity) AS SquareRootCapacity
    FROM classroom;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](../PraktikumSQL/ASSET/Screenshot%20(172).png)

11. Menjalankan fungsi CURDATE dengan syntax seperti berikut:
    ```
    SELECT CURDATE() AS CurrentDate;
    ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(216).png)

12. Menjalankan fungsi CURTIME dengan syntax seperti berikut:
    ```
    SELECT CURTIME() AS CurrentTime;
    ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(218).png)

13. Menjalankan fungsi TIMESTAMP yang ingin dicari dengan syntax seperti berikut:
   ```
   SELECT TIMESTAMP("2023-11-14");
   ```
<br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(220).png) 

14. Menjalankan fungsi AVG dan SUM untuk mengetahui rata-rata dan jumalah untuk atribut pada table tertentu dengan syntax seperti berikut:
    ```
    SELECT AVG(salary) AS rata_rata, SUM(salary) AS jumlah
    FROM instructor;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(221).png)

15. Menjalankan fungsi COUNT dengan syntax seperti berikut:
    ```
    SELECT COUNT(*) AS TotalRecords
    FROM student;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(222).png)

16.  Menjalankan fungsi agregasi (AVG) menggunakan klausa GROUP BY dengan syntax seperti berikut:
        ```
        SELECT building, AVG(salary) as avg_salary
        FROM instructor
        JOIN department ON instructor.dept_name = department.dept_name
        GROUP BY building;
        ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(223).png)

17. Menjalankan fungsi agrgasi (AVG) menggunakan clausa HAVING dengan syntax seperti berikut:
    ```
    SELECT AVG(salary) as avg_salary, department.building
    FROM instructor
    JOIN department ON instructor.dept_name = department.dept_name
    GROUP BY department.building
    HAVING AVG(salary) > 29000;
    ``` 
 <br>Kode dan hasil sebagai berikut:

![Gambar](https://github.com/hongi1t/PrakSQL/blob/main/Screenshot%20(224).png)
