Title: Pasang Webhook
Date: 2016-07-11
SubTitle: Intro
Tags: github, webhook

![](/images/hook.jpg)

Post baru ini buat nyoba github webhook. 

<br/>Flow-nya kurang lebih seperti ini: kalau ada push/commit baru di branch `source`, server (CI/CD) akan melakukan `git pull` dilanjutkan dengan proses build, dan kalau sukses, akan diteruskan dengan `git push` ke `master` branch.

<br/>Try no: 1. Hopefully, gak mesti increment :-D. 
