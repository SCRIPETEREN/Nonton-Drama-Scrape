# Nonton Drama Scrape - Node.js Drama Series Scraper

> **GitHub Repository Title**
>
> ```text
> Nonton Drama Scrape - Node.js Drama Series Scraper
> ```
>
> **Repository Name**
>
> ```text
> nonton-drama-scrape
> ```
>
> **GitHub Repository Description**
>
> ```text
> Node.js CLI scraper for NontonDrama. Get drama lists, latest series, popular titles, ratings, movies, ongoing and completed series, Asian and Western shows, filters, search results, drama details, seasons, episodes, and related series in JSON format.
> ```

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-16%2B-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Axios-HTTP%20Client-5A29E4?style=for-the-badge&logo=axios&logoColor=white" alt="Axios">
  <img src="https://img.shields.io/badge/Cheerio-HTML%20Parser-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Cheerio">
  <img src="https://img.shields.io/badge/Creator-SCRIPETEREN-181717?style=for-the-badge&logo=github&logoColor=white" alt="Creator">
</p>

<p align="center">
  <b>Node.js CLI scraper untuk NontonDrama.</b><br>
  Mengambil data drama, series, movie, pencarian, filter genre dan negara, detail drama, rating, cast, sutradara, season, episode, serta related series dalam format JSON.
</p>

---

## Fitur

- Mengambil data homepage NontonDrama
- Mengambil section atau widget dari homepage
- Mengambil daftar drama terbaru
- Mengambil daftar latest series
- Mengambil drama populer
- Mengambil drama berdasarkan rating
- Mengambil daftar movie
- Mengambil daftar series
- Mengambil daftar series ongoing
- Mengambil daftar series complete
- Mengambil daftar Asian series
- Mengambil daftar Western series
- Mendukung pagination menggunakan custom path
- Filter series berdasarkan genre
- Filter series berdasarkan country
- Filter series berdasarkan tahun
- Mencari drama berdasarkan keyword
- Mengambil detail drama atau series
- Mengambil poster drama
- Mengambil sinopsis
- Mengambil rating dan jumlah voters
- Mengambil tahun rilis
- Mengambil release date
- Mengambil region
- Mengambil status series
- Mengambil country
- Mengambil genre
- Mengambil sutradara
- Mengambil cast atau bintang
- Mengambil total season
- Mengambil total episode
- Mengambil daftar episode dari data season
- Mengambil URL episode pertama
- Mengambil URL episode terbaru
- Mengambil related series
- Mendukung input slug, path URL, dan URL lengkap pada detail
- Output JSON untuk API, bot, website, atau aplikasi Node.js

---

## Teknologi

Project ini menggunakan:

- [Node.js](https://nodejs.org/)
- [Axios](https://axios-http.com/)
- [Cheerio](https://cheerio.js.org/)
- Built-in module `https`

---

## Struktur Project

```text
nonton-drama-scrape/
├── nontondrama.js
├── package.json
├── package-lock.json
├── .gitignore
├── README.md
└── LICENSE
```

---

## Instalasi

Clone repository:

```bash
git clone [https://github.com/SCRIPETEREN/nonton-drama-scrape.git](https://github.com/SCRIPETEREN/nonton-drama-scrape.git)
```

Masuk ke folder repository:

```bash
cd nonton-drama-scrape
```

Install dependency:

```bash
npm install
```

Jika belum memiliki `package.json`, install dependency secara manual:

```bash
npm install axios cheerio
```

Jalankan scraper homepage:

```bash
node nontondrama.js home
```

Command tanpa argument akan otomatis menjalankan `home`:

```bash
node nontondrama.js
```

---

## package.json

Buat file `package.json` dengan isi berikut:

```json
{
  "name": "nonton-drama-scrape",
  "version": "1.0.0",
  "description": "Node.js CLI scraper untuk mengambil data drama, series, movie, episode, dan detail dari NontonDrama.",
  "main": "nontondrama.js",
  "scripts": {
    "start": "node nontondrama.js home",
    "home": "node nontondrama.js home",
    "latest": "node nontondrama.js latest",
    "popular": "node nontondrama.js popular",
    "rating": "node nontondrama.js rating",
    "movie": "node nontondrama.js movie",
    "series": "node nontondrama.js series",
    "ongoing": "node nontondrama.js ongoing",
    "complete": "node nontondrama.js complete",
    "asian": "node nontondrama.js asian",
    "west": "node nontondrama.js west"
  },
  "keywords": [
    "nontondrama",
    "drama",
    "drama-scraper",
    "series-scraper",
    "movie-scraper",
    "asian-drama",
    "western-series",
    "nodejs",
    "axios",
    "cheerio"
  ],
  "author": "SCRIPETEREN",
  "license": "MIT",
  "dependencies": {
    "axios": "^1.7.9",
    "cheerio": "^1.0.0"
  }
}
```

Install package:

```bash
npm install
```

Menjalankan homepage dengan NPM:

```bash
npm start
```

Menjalankan command lain:

```bash
npm run latest
```

```bash
npm run popular
```

```bash
npm run ongoing
```

```bash
npm run complete
```

```bash
npm run asian
```

```bash
npm run west
```

---

## Cara Penggunaan

Format dasar:

```bash
node nontondrama.js <command> <input>
```

Command yang tersedia:

```text
home
latest
popular
rating
movie
series
ongoing
complete
asian
west
page <path>
genre <slug>
country <slug>
year <year>
search <query>
detail <slug|path|url>
```

---

## Daftar Command

| Command | Keterangan | Contoh |
|---|---|---|
| `home` | Mengambil data halaman utama | `node nontondrama.js home` |
| `latest` | Mengambil latest series | `node nontondrama.js latest` |
| `popular` | Mengambil series populer | `node nontondrama.js popular` |
| `rating` | Mengambil series berdasarkan rating | `node nontondrama.js rating` |
| `movie` | Mengambil daftar movie terbaru | `node nontondrama.js movie` |
| `series` | Mengambil daftar latest series | `node nontondrama.js series` |
| `ongoing` | Mengambil series yang masih ongoing | `node nontondrama.js ongoing` |
| `complete` | Mengambil series yang sudah complete | `node nontondrama.js complete` |
| `asian` | Mengambil Asian series | `node nontondrama.js asian` |
| `west` | Mengambil Western series | `node nontondrama.js west` |
| `page <path>` | Mengambil list dari custom pagination path | `node nontondrama.js page /release/page/2` |
| `genre <slug>` | Mengambil series berdasarkan genre | `node nontondrama.js genre action` |
| `country <slug>` | Mengambil series berdasarkan negara | `node nontondrama.js country south-korea` |
| `year <year>` | Mengambil series berdasarkan tahun | `node nontondrama.js year 2026` |
| `search <query>` | Mencari drama atau series | `node nontondrama.js search prophet` |
| `detail <slug>` | Mengambil detail drama | `node nontondrama.js detail /prophet-2026` |

---

## Homepage

Untuk mengambil data dari halaman utama:

```bash
node nontondrama.js home
```

Atau:

```bash
node nontondrama.js
```

Data homepage terdiri dari:

- `sections` — Data dari semua widget yang berhasil dibaca
- `latest` — Daftar drama terbaru dari container utama

Setiap widget disimpan berdasarkan judul widget.

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "sections": {
      "Drama Terbaru": [
        {
          "title": "Contoh Drama",
          "slug": "/contoh-drama-2026",
          "url": "[https://tv9.nontondrama.my/contoh-drama-2026](https://tv9.nontondrama.my/contoh-drama-2026)",
          "poster": "[https://example.com/poster.jpg](https://example.com/poster.jpg)",
          "rating": 8.5,
          "rating_count": 1250,
          "year": 2026,
          "episode": 12,
          "season": "Season 1",
          "genre": "Drama, Romance"
        }
      ]
    },
    "latest": []
  }
}
```

---

## Latest Series

Untuk mengambil latest series:

```bash
node nontondrama.js latest
```

Endpoint:

```text
/latest-series
```

Alias yang menghasilkan data serupa:

```bash
node nontondrama.js series
```

Data list dapat meliputi:

- Judul
- Slug
- URL
- Poster
- Rating
- Jumlah rating
- Tahun
- Jumlah episode
- Season
- Genre
- URL halaman berikutnya

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [
      {
        "title": "Contoh Drama",
        "slug": "/contoh-drama-2026",
        "url": "[https://tv9.nontondrama.my/contoh-drama-2026](https://tv9.nontondrama.my/contoh-drama-2026)",
        "poster": "[https://example.com/poster.jpg](https://example.com/poster.jpg)",
        "rating": 8.5,
        "rating_count": 1250,
        "year": 2026,
        "episode": 12,
        "season": "Season 1",
        "genre": "Drama, Romance"
      }
    ],
    "next": "[https://tv9.nontondrama.my/latest-series/page/2](https://tv9.nontondrama.my/latest-series/page/2)"
  }
}
```

---

## Drama Populer

Untuk mengambil series populer:

```bash
node nontondrama.js popular
```

Endpoint:

```text
/populer/
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [],
    "next": null
  }
}
```

---

## Series Berdasarkan Rating

Untuk mengambil series berdasarkan rating:

```bash
node nontondrama.js rating
```

Endpoint:

```text
/rating/
```

---

## Movie

Untuk mengambil daftar movie terbaru:

```bash
node nontondrama.js movie
```

Endpoint:

```text
/latest
```

---

## Ongoing Series

Untuk mengambil series yang masih berjalan:

```bash
node nontondrama.js ongoing
```

Endpoint:

```text
/series/ongoing
```

---

## Completed Series

Untuk mengambil series yang telah selesai:

```bash
node nontondrama.js complete
```

Endpoint:

```text
/series/complete
```

---

## Asian Series

Untuk mengambil daftar Asian series:

```bash
node nontondrama.js asian
```

Endpoint:

```text
/series/asian
```

---

## Western Series

Untuk mengambil daftar Western series:

```bash
node nontondrama.js west
```

Endpoint:

```text
/series/west
```

---

## Pagination Custom

Gunakan command `page` untuk mengambil data dari halaman lain atau pagination tertentu.

Format:

```bash
node nontondrama.js page <path>
```

Contoh:

```bash
node nontondrama.js page /release/page/2
```

Contoh menggunakan URL penuh:

```bash
node nontondrama.js page [https://tv9.nontondrama.my/release/page/2](https://tv9.nontondrama.my/release/page/2)
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "items": [],
    "next": "[https://tv9.nontondrama.my/release/page/3](https://tv9.nontondrama.my/release/page/3)"
  }
}
```

---

## Filter Genre

Gunakan command `genre` untuk mengambil series berdasarkan genre.

Format:

```bash
node nontondrama.js genre <slug_genre>
```

Contoh:

```bash
node nontondrama.js genre action
```

```bash
node nontondrama.js genre romance
```

```bash
node nontondrama.js genre comedy
```

```bash
node nontondrama.js genre thriller
```

Script membuat path berikut:

```text
/genre/<slug_genre>
```

---

## Filter Country

Gunakan command `country` untuk mengambil series berdasarkan negara.

Format:

```bash
node nontondrama.js country <slug_negara>
```

Contoh:

```bash
node nontondrama.js country south-korea
```

```bash
node nontondrama.js country china
```

```bash
node nontondrama.js country japan
```

```bash
node nontondrama.js country united-states
```

Script membuat path berikut:

```text
/country/<slug_negara>
```

---

## Filter Tahun

Gunakan command `year` untuk mengambil series berdasarkan tahun rilis.

Format:

```bash
node nontondrama.js year <tahun>
```

Contoh:

```bash
node nontondrama.js year 2026
```

```bash
node nontondrama.js year 2025
```

```bash
node nontondrama.js year 2024
```

Script membuat path berikut:

```text
/year/<tahun>
```

---

## Search Drama

Gunakan command `search` untuk mencari drama berdasarkan keyword.

Format:

```bash
node nontondrama.js search "<query>"
```

Contoh:

```bash
node nontondrama.js search prophet
```

```bash
node nontondrama.js search "when life gives you tangerines"
```

```bash
node nontondrama.js search "squid game"
```

```bash
node nontondrama.js search "the witcher"
```

Script menggunakan endpoint:

```text
/search?s=<query>
```

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "query": "prophet",
    "items": [
      {
        "title": "Prophet",
        "slug": "/prophet-2026",
        "url": "[https://tv9.nontondrama.my/prophet-2026](https://tv9.nontondrama.my/prophet-2026)",
        "poster": "[https://example.com/prophet.jpg](https://example.com/prophet.jpg)",
        "rating": 8.1,
        "rating_count": 500,
        "year": 2026,
        "episode": 8,
        "season": "Season 1",
        "genre": "Drama, Mystery"
      }
    ]
  }
}
```

---

## Detail Drama

Gunakan command `detail` untuk mengambil informasi lengkap drama atau series.

Format:

```bash
node nontondrama.js detail <slug|path|url>
```

Contoh menggunakan slug:

```bash
node nontondrama.js detail prophet-2026
```

Contoh menggunakan path:

```bash
node nontondrama.js detail /prophet-2026
```

Contoh menggunakan URL penuh:

```bash
node nontondrama.js detail [https://tv9.nontondrama.my/prophet-2026](https://tv9.nontondrama.my/prophet-2026)
```

Data detail yang dapat diperoleh:

- Judul series
- Slug
- URL detail
- Poster
- Sinopsis
- Rating
- Jumlah voters
- Tahun rilis
- Release date
- Region
- Status series
- Negara
- Genre
- Sutradara
- Cast atau bintang
- Total episode
- Total season
- URL episode pertama
- URL episode terbaru
- Daftar episode
- Related series

Contoh output:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {
    "title": "Prophet",
    "slug": "/prophet-2026",
    "url": "[https://tv9.nontondrama.my/prophet-2026](https://tv9.nontondrama.my/prophet-2026)",
    "poster": "[https://example.com/prophet-poster.jpg](https://example.com/prophet-poster.jpg)",
    "synopsis": "Contoh sinopsis drama.",
    "rating": 8.1,
    "rating_count": 500,
    "year": 2026,
    "release_date": "January 1, 2026",
    "region": "South Korea",
    "status": "Ongoing",
    "country": [
      "South Korea"
    ],
    "genre": [
      "Drama",
      "Mystery",
      "Thriller"
    ],
    "director": [
      "Contoh Sutradara"
    ],
    "cast": [
      "Contoh Aktor",
      "Contoh Aktris"
    ],
    "total_episodes": 12,
    "total_seasons": 1,
    "play_first": "[https://tv9.nontondrama.my/prophet-2026-episode-1](https://tv9.nontondrama.my/prophet-2026-episode-1)",
    "play_latest": "[https://tv9.nontondrama.my/prophet-2026-episode-8](https://tv9.nontondrama.my/prophet-2026-episode-8)",
    "episodes": [
      {
        "season": 1,
        "episode": 1,
        "title": "Episode 1",
        "slug": "prophet-2026-episode-1",
        "url": "[https://tv9.nontondrama.my/prophet-2026-episode-1](https://tv9.nontondrama.my/prophet-2026-episode-1)"
      }
    ],
    "related": [
      {
        "title": "Drama Terkait",
        "slug": "/drama-terkait-2025",
        "url": "[https://tv9.nontondrama.my/drama-terkait-2025](https://tv9.nontondrama.my/drama-terkait-2025)",
        "poster": "[https://example.com/related.jpg](https://example.com/related.jpg)",
        "rating": 7.8,
        "rating_count": 200,
        "year": 2025,
        "episode": 16,
        "season": "Season 1",
        "genre": "Drama"
      }
    ]
  }
}
```

---

## Struktur Episode

Episode diambil dari JSON dengan ID berikut:

```html
<script id="season-data" type="application/json">
```

Setiap episode memiliki struktur:

```json
{
  "season": 1,
  "episode": 1,
  "title": "Episode 1",
  "slug": "nama-series-episode-1",
  "url": "[https://tv9.nontondrama.my/nama-series-episode-1](https://tv9.nontondrama.my/nama-series-episode-1)"
}
```

Field episode:

| Field | Keterangan |
|---|---|
| `season` | Nomor season |
| `episode` | Nomor episode |
| `title` | Judul episode |
| `slug` | Slug episode |
| `url` | URL halaman episode |

---

## Struktur Response

Semua command sukses menggunakan struktur:

```json
{
  "author": "SCRIPETEREN",
  "status": true,
  "data": {}
}
```

Jika terjadi error:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Pesan error"
}
```

---

## Mengubah Author Response

Pada source code awal, response menggunakan `xvlovers`.

Ubah response sukses dari:

```js
console.log(JSON.stringify({
  author: "xvlovers",
  status: true,
  data
}, null, 2))
```

Menjadi:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: true,
  data
}, null, 2))
```

Ubah response error dari:

```js
console.log(JSON.stringify({
  author: "xvlovers",
  status: false,
  message: error.message
}, null, 2))
```

Menjadi:

```js
console.log(JSON.stringify({
  author: "SCRIPETEREN",
  status: false,
  message: error.message
}, null, 2))
```

---

## Error Handling

Script menangani beberapa kondisi berikut:

- Command tidak dikenal
- Path pagination kosong
- Genre kosong
- Country kosong
- Tahun kosong
- Query pencarian kosong
- Slug detail kosong
- Request HTTP gagal
- Website mengembalikan status selain `200`
- Timeout request
- Data JSON dalam halaman tidak valid
- HTML atau selector website berubah

Contoh menjalankan search tanpa keyword:

```bash
node nontondrama.js search
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Contoh: node nontondrama.js search prophet"
}
```

Contoh menjalankan detail tanpa slug:

```bash
node nontondrama.js detail
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Contoh: node nontondrama.js detail /prophet-2026"
}
```

Contoh command tidak dikenal:

```bash
node nontondrama.js test
```

Output:

```json
{
  "author": "SCRIPETEREN",
  "status": false,
  "message": "Command tidak dikenal: test
Gunakan: home | latest | popular | rating | movie | series | ongoing | complete | asian | west | page <path> | genre <slug> | country <slug> | year <year> | search <q> | detail <slug>"
}
```

---

## Penggunaan Sebagai Module

Agar file `nontondrama.js` dapat digunakan pada project Node.js lain, ubah bagian paling bawah file.

Ganti:

```js
main()
```

Menjadi:

```js
if (require.main === module) {
  main()
}

module.exports = {
  getHome,
  getList,
  search,
  getDetail
}
```

Buat file bernama `app.js`:

```js
const {
  getHome,
  getList,
  search,
  getDetail
} = require("./nontondrama")

async function main() {
  try {
    const home = await getHome()

    console.log(JSON.stringify(home, null, 2))

    const searchResult = await search("prophet")

    console.log(JSON.stringify(searchResult, null, 2))

    const dramaDetail = await getDetail("/prophet-2026")

    console.log(JSON.stringify(dramaDetail, null, 2))

    const ongoing = await getList("/series/ongoing")

    console.log(JSON.stringify(ongoing, null, 2))
  } catch (error) {
    console.error(error.message)
  }
}

main()
```

Jalankan:

```bash
node app.js
```

---

## .gitignore

Buat file `.gitignore`:

```gitignore
node_modules/
.env
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.DS_Store
```

---

## Catatan Penting

- Struktur HTML dan JSON pada NontonDrama dapat berubah kapan saja.
- Jika selector HTML, ID script, atau struktur data berubah, scraper mungkin perlu diperbarui.
- Tidak semua series memiliki data lengkap untuk rating, cast, sutradara, season, episode, atau related series.
- Jangan melakukan request dalam jumlah besar dalam waktu singkat.
- Gunakan cache, delay, queue, dan rate limit jika scraper digunakan untuk bot atau aplikasi publik.
- Konfigurasi `rejectUnauthorized: false` dapat melewati validasi sertifikat HTTPS. Hindari penggunaan konfigurasi ini di environment production kecuali memang diperlukan.
- Gunakan project ini untuk pembelajaran Node.js, HTTP request, HTML parsing, JSON parsing, riset, dan pengolahan metadata.
- Patuhi ketentuan website sumber, hukum, serta hak cipta yang berlaku.

---

## License

Project ini menggunakan lisensi MIT.

Buat file `LICENSE`:

```text
MIT License

Copyright (c) 2026 SCRIPETEREN

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Creator

```text
SCRIPETEREN
```

```text
[https://github.com/SCRIPETEREN](https://github.com/SCRIPETEREN)
```

---

## Disclaimer

Repository ini dibuat untuk pembelajaran Node.js, HTTP request, HTML parsing, JSON parsing, dan pengolahan metadata drama atau series yang tersedia secara publik.

Gunakan script secara bertanggung jawab. Jangan gunakan untuk melakukan request berlebihan, menyebarkan konten tanpa izin, melanggar privasi, atau melakukan aktivitas yang melanggar ketentuan layanan dan hukum yang berlaku.

<p align="center">
  Made by <a href="https://github.com/SCRIPETEREN">SCRIPETEREN</a>
</p>