# Soal Ujian Data Science Analytics & Visualization

![Lintang_Purwadhika](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

#

### **Soal 1 - MySQL World Database**

MySQL secara default menyertakan database ```world``` yang dapat digunakan oleh user untuk mempelajari teknik penggunaan database di MySQL. Database ```world``` merupakan sample real database yang bersumber dari [Statistics Finland]() dan dirilis sekitar awal tahun 2000-an. Database ini berisi 3 buah tabel yang saling berhubungan satu sama lain:

- Tabel ```city``` berisi informasi tentang __4079__ kota di dunia.
- Tabel ```country``` berisi informasi tentang __239__ negara/wilayah yang dianggap negara di dunia.
- Tabel ```countrylanguage``` berisi informasi tentang bahasa yang digunakan oleh negara-negara di dunia.

*__Soal :__* Aktifkan server MySQL Anda, lalu gunakan database ```world``` dan tuliskan langkah-langkah/query MySQL untuk menyelesaikan perintah berikut:

1. Tampilkan daftar __10 kota terpadat di Indonesia__. Kolom yang diwajibkan tampil adalah __id kota__, __nama kota__, __kode negara__, __distrik/provinsi__ dan __populasi__ (semua kolom di tabel ```city```). Output yang diharapkan:

    ```bash
    +-----+----------------+-------------+------------------+------------+
    | ID  | Name           | CountryCode | District         | Population |
    +-----+----------------+-------------+------------------+------------+
    | 939 | Jakarta        | IDN         | Jakarta Raya     |    9604900 |
    | 940 | Surabaya       | IDN         | East Java        |    2663820 |
    | 941 | Bandung        | IDN         | West Java        |    2429000 |
    | 942 | Medan          | IDN         | Sumatera Utara   |    1843919 |
    | 943 | Palembang      | IDN         | Sumatera Selatan |    1222764 |
    | 944 | Tangerang      | IDN         | West Java        |    1198300 |
    | 945 | Semarang       | IDN         | Central Java     |    1104405 |
    | 946 | Ujung Pandang  | IDN         | Sulawesi Selatan |    1060257 |
    | 947 | Malang         | IDN         | East Java        |     716862 |
    | 948 | Bandar Lampung | IDN         | Lampung          |     680332 |
    +-----+----------------+-------------+------------------+------------+
    ```

2. Tampilkan daftar __10 kota terpadat di dunia beserta asal negaranya__. Kolom yang diwajibkan ada minimal adalah __id kota__, __nama kota__, __distrik/provinsi__, __nama negara__ dan __populasi__. Output yang diharapkan:

    ```bash
    +------+-------------------+------------------+--------------------+------------+
    | id   | nama_kota         | district         | negara             | population |
    +------+-------------------+------------------+--------------------+------------+
    | 1024 | Mumbai (Bombay)   | Maharashtra      | India              |   10500000 |
    | 2331 | Seoul             | Seoul            | South Korea        |    9981619 |
    |  206 | SÃ£o Paulo        | SÃ£o Paulo       | Brazil             |    9968485 |
    | 1890 | Shanghai          | Shanghai         | China              |    9696300 |
    |  939 | Jakarta           | Jakarta Raya     | Indonesia          |    9604900 |
    | 2822 | Karachi           | Sindh            | Pakistan           |    9269265 |
    | 3357 | Istanbul          | Istanbul         | Turkey             |    8787958 |
    | 2515 | Ciudad de MÃ©xico | Distrito Federal | Mexico             |    8591309 |
    | 3580 | Moscow            | Moscow (City)    | Russian Federation |    8389200 |
    | 3793 | New York          | New York         | United States      |    8008278 |
    +------+-------------------+------------------+--------------------+------------+
    ```

3. Tampilkan daftar __10 negara yang tercatat merdeka paling awal__. Daftar negara yang tidak diketahui tahun kemerdekaannya, tidak perlu diikutsertakan. Kolom yang diwajibkan ada minimal adalah __kode negara__, __nama negara__, __benua__, __regional__ dan __tahun merdeka (IndepYear)__. Output yang diharapkan:

    ```bash
    +------+----------------+-----------+------------------+---------------+
    | code | name           | continent | region           | tahun_merdeka |
    +------+----------------+-----------+------------------+---------------+
    | CHN  | China          | Asia      | Eastern Asia     |         -1523 |
    | ETH  | Ethiopia       | Africa    | Eastern Africa   |         -1000 |
    | JPN  | Japan          | Asia      | Eastern Asia     |          -660 |
    | DNK  | Denmark        | Europe    | Nordic Countries |           800 |
    | SWE  | Sweden         | Europe    | Nordic Countries |           836 |
    | FRA  | France         | Europe    | Western Europe   |           843 |
    | SMR  | San Marino     | Europe    | Southern Europe  |           885 |
    | GBR  | United Kingdom | Europe    | British Islands  |          1066 |
    | PRT  | Portugal       | Europe    | Southern Europe  |          1143 |
    | AND  | Andorra        | Europe    | Southern Europe  |          1278 |
    +------+----------------+-----------+------------------+---------------+
    ```

4. Tampilkan daftar __jumlah negara yang tidak diketahui tahun kemerdekaannya, di setiap continent/benua__. Output yang diharapkan:

    ```bash
    +---------------+--------------------------------------------+
    | continent     | jml_negara_tak_diketahui_th_kemerdekaannya |
    +---------------+--------------------------------------------+
    | North America |                                         14 |
    | Oceania       |                                         14 |
    | Antarctica    |                                          5 |
    | Africa        |                                          5 |
    | South America |                                          2 |
    | Europe        |                                          3 |
    | Asia          |                                          4 |
    +---------------+--------------------------------------------+
    ```

5. Tampilkan daftar __10 negara yang bahasa resminya (_official language_) adalah bahasa Inggris, dan memiliki persentase pengguna bahasa Inggris tertinggi di dunia__. Kolom yang diwajibkan ada yaitu __kode negara__, __nama negara__, __bahasa__, __kolom isOfficial__ dan __percentage__. Output yang diharapkan:

    ```bash
    +-------------+----------------------+----------+------------+------------+
    | countrycode | name                 | language | isOfficial | percentage |
    +-------------+----------------------+----------+------------+------------+
    | BMU         | Bermuda              | English  | T          |      100.0 |
    | IRL         | Ireland              | English  | T          |       98.4 |
    | GBR         | United Kingdom       | English  | T          |       97.3 |
    | GIB         | Gibraltar            | English  | T          |       88.9 |
    | NZL         | New Zealand          | English  | T          |       87.0 |
    | USA         | United States        | English  | T          |       86.2 |
    | VIR         | Virgin Islands, U.S. | English  | T          |       81.7 |
    | AUS         | Australia            | English  | T          |       81.2 |
    | CAN         | Canada               | English  | T          |       60.4 |
    | BLZ         | Belize               | English  | T          |       50.8 |
    +-------------+----------------------+----------+------------+------------+
    ```

- Contoh screenshot:

    ![tes](./tes.png)

_**Catatan:**_ 

✅ a

❌ b

❌ c

❌ d

✅ _Commit & push source code jawaban soal ini ke __Github__ Anda, buatlah repo dengan nama __nama_Soal__, kemudian lampirkan __url link repo Github__ Anda via email ke lintang@purwadhika.com!_

#

### *__#HappyCoding__* :relaxed:

#### Lintang Wisesa :love_letter: _lintangwisesa@ymail.com_

[Facebook](https://www.facebook.com/lintangbagus) | 
[Twitter](https://twitter.com/Lintang_Wisesa) |
[Google+](https://plus.google.com/u/0/+LintangWisesa1) |
[Youtube](https://www.youtube.com/user/lintangbagus) | 
:octocat: [GitHub](https://github.com/LintangWisesa) |
[Hackster](https://www.hackster.io/lintangwisesa)