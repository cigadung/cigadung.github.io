Title: Snippet CBOT untuk Post Barusan
Category: coding
Date: 2016-07-25
Tags: snippet

Berikut snippet perintah yg digunakan untuk men-generate post yang barusan (https://cigadung.github.io/blog/trending-hari-ini)

```bash
# prepare new post
.new post
.title set Trending Hari Ini
.content add Repo trending di github hari ini, untuk semua bahasa.

# get/print trending list + select + render
.ght list
.ght select all
.ght render

# check
.print
.gist

# submit + push
.submit
.push
```

Notes: `.ght select all` memindahkan semua item pada list `.ght list` untuk bahasa yg aktif (`.ght switch all|java|javascript|python`). Kalau mau custom, pilih item yg sesuai dengan perintah `.ght select <index>` dan sebelumnya, untuk mengetahui index, via command `.ght print`.