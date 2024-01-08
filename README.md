
![Website Template Project](https://github.com/BimaBizz/Api-Anoboy-Docs/assets/98264074/21e0e364-8065-4e8f-a10e-dac7d3380143)

# Dokumentasi Api-Anoboy Streaming

## Pengaturan Awal

Proyek ini menggunakan ExpressJS, Morgan, dotenv, Axios, dan Cheerio untuk membuat platform streaming anime. Dokumentasi ini memberikan gambaran singkat tentang struktur proyek dan fitur-fitur yang disediakan.

### Routing Anime

-   Gunakan rute komiku
-   Gunakan rute anime

### Anime Terbaru & Search

Endpoint: `https://animev1.bimabizz.my.id//api/anime/` <br/>
Endpoint Search Anime `https://animev1.bimabizz.my.id//api/anime/?s=(nama_anime)`

Fitur:

-   Mengambil anime terbaru ( baru rilis ) dari Anoboy.
-   Pencarian Anime dari anoboy

Response : 

|Parameter|Deskripsi  |
|--|--|
| *max_page* | Menunjukkan jumlah maksimal halaman (page) yang dapat diakses |
| *next_page* | Tautan ke halaman berikutnya dalam rangkaian data anime |
| *prev_page* | Tautan ke halaman sebelumnya dalam rangkaian data anime. Jika tidak ada halaman sebelumnya, nilainya null |
|*data (Array)*| Array yang berisi informasi tentang anime, seperti judul, parameter, thumbnail, waktu unggah, dan tautan detail.|
-   Contoh Nilai data:
    -   **title**: "Isekai de Mofumofu Nadenade suru Tame ni Ganbattemasu. Episode 2"
    -   **param**: "2024~ 01 ~ isekai-de-mofumofu-nadenade-suru-tame-ni-ganbattemasu-episode-2~"
    -   **thumbnail**: "[https://anoboy.show//img/upload/01as-Isekai%20de%20Mofumofu%20Nadenade%20suru%20Tame%20ni%20Ganbattemasu.jpg](https://anoboy.show//img/upload/01as-Isekai%20de%20Mofumofu%20Nadenade%20suru%20Tame%20ni%20Ganbattemasu.jpg)"
    -   **upload_time**: "UP Senin, 01:52 Wib"
    -   **detail_url**: "[http://animev1.bimabizz.my.id/api/anime/2024~01~isekai-de-mofumofu-nadenade-suru-tame-ni-ganbattemasu-episode-2](http://animev1.bimabizz.my.id/api/anime/2024~01~isekai-de-mofumofu-nadenade-suru-tame-ni-ganbattemasu-episode-2~)" 


### Jadwal Anime Terbaru

Endpoint: `https://animev1.bimabizz.my.id//api/anime/jadwal/terbaru/`

Fitur:

-   Mengambil jadwal anime terbaru dari Anoboy.
-   Menyajikan jadwal berdasarkan hari dengan daftar judul anime dan waktu tayang.

Response:

| Parameter | Deskripsi |
|--|--|
| *day* | Hari dari jadwal anime |
|*shows* (Array)| -   Array yang berisi informasi tentang judul-judul anime yang tayang pada hari tertentu.
-   Contoh Nilai shows:
    -   **title**: "Spirits In Chinese Brushes"
        
    -   **urlOriginal**: "[https://anoboy.show/2023/11/spirits-in-chinese-brushes/](https://anoboy.show/2023/11/spirits-in-chinese-brushes/)"
        
    -   **url**: "[https://animeav1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~11~spirits-in-chinese-brushes](https://animeav1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~11~spirits-in-chinese-brushes)~"
        
    -   **time**: "Senin, 09:10"
        
    -   **title**: "The Eternal Strife"
        
    -   **urlOriginal**: "[https://anoboy.show/2023/12/the-eternal-strife/](https://anoboy.show/2023/12/the-eternal-strife/)"
        
    -   **url**: "[https://animeav1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~12~the-eternal-strife](https://animeav1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~12~the-eternal-strife)~"
        
    -   **time**: "Senin, 14:04" |


### Daftar Anime

Endpoint: `https://animev1.bimabizz.my.id//api/anime-list`

Fitur:

-   Mengambil daftar anime dari Anoboy.
-   Menyajikan daftar anime berdasarkan kategori dengan judul dan tautan ke AnimeBizz Streaming.

Response:

| Parameter | Deskripsi |
|--|--|
| *data (Object)* | Objek yang berisi array anime dengan urutan dari nomor ke angka indeks sebagai kunci. |

Contoh Nilai:

-   **0** (Array):
    
    -   **title**: "“Oshi no Ko”"
    -   **url**: "[https://animev1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~04~oshi-no-ko](https://animev1.bimabizz.my.id/api/anime/jadwal/allepisode/2023~04~oshi-no-ko)~"

### Komik Terbaru & Search

Endpoint: `https://animev1.bimabizz.my.id//api/komiku/` <br/>
Endpoint Search Anime `https://animev1.bimabizz.my.id//api/komiku/?s=(nama_komik)`

Fitur:

-   Mengambil komik terbaru ( baru rilis ) dari komiku.
-   Pencarian komik dari komiku

Response:

| Parameter | Deskripsi |
|--|--|
| *next_page* | Tautan ke halaman berikutnya dalam rangkaian data Komiku dengan tag rekomendasi |
|*prev_page*| Tautan ke halaman sebelumnya dalam rangkaian data Komiku. Jika tidak ada halaman sebelumnya, nilainya null |
|*data (Array)*|Array yang berisi informasi tentang manga, seperti judul, deskripsi, bab terbaru, thumbnail, parameter, dan tautan ke halaman detail manga|

Contoh Nilai data:

-   **title**: "Jishou F-Rank no Oniisama ga Game de Hyouka sareru Gakuen no Chouten ni Kunrin suru Sou desu yo?"
-   **description**: "Update 21 jam lalu. Shishio Academy adalah sekolah terbaik dan bergengsi di Jepang, di mana hanya elit bidang studi, olahraga, silsilah yang~"
-   **latest_chapter**: "Chapter 40"
-   **thumbnail**: "[https://thumbnail.komiku.id/wp-content/uploads/2020/07/Komik-Jishou-F-Rank-no-Oniisama-ga-Game-de-Hyouka-sareru-Gakuen-no-Chouten-ni-Kunrin-suru-Sou-desu-yo.jpg](https://thumbnail.komiku.id/wp-content/uploads/2020/07/Komik-Jishou-F-Rank-no-Oniisama-ga-Game-de-Hyouka-sareru-Gakuen-no-Chouten-ni-Kunrin-suru-Sou-desu-yo.jpg)"
-   **param**: "jishou-f-rank-no-oniisama-ga-game-de-hyouka-sareru-gakuen-no-chouten-ni-kunrin-suru-sou-desu-yo"
-   **detail_url**: "[http://animev1.bimabizz.my.id/api/komiku/jishou-f-rank-no-oniisama-ga-game-de-hyouka-sareru-gakuen-no-chouten-ni-kunrin-suru-sou-desu-yo](http://animev1.bimabizz.my.id/api/komiku/jishou-f-rank-no-oniisama-ga-game-de-hyouka-sareru-gakuen-no-chouten-ni-kunrin-suru-sou-desu-yo)"


### Dukungan Support Project

jika kalian terbantu dengan website ini dan ingin melakukan donasi<br/>
(●'◡'●)<br/>
👇👇👇<br/>
**[DISINI](https://saweria.co/BimaBizz)**

**Note:** seberapa kecilpun donasi kalian akan sangan membantu pengembangan API kedepannya
