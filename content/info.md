---
title: "Info"
date: 2020-02-07T21:51:21+01:00
draft: true
---
Questa è una pagina soltanto che contiene info che non viene pubblicata.

All the web pages of my web site.
We have a special file for every page on my web site.

Per creare un nuovo contenuto:
1 - hugo new posts/my-first-post.md

Quando creo un nuovo content il metadato draft è impostato su false.
Devo impostarlo a false prima di far partire il server altrimenti
non viene considerato. Oppure far partire il server con il comando
-D:
hugo server -D

Hugo considera due tipi di pagine:
- list page che sono la homepage, /posts
- single page i contenuti specifici di ciascun post ovvero /posts/my-first-post, /posts/my-second-page

le list page arrivano soltanto al primo livello delle cartelle in automatico ovvero fino a /posts. Se io metto un altra sottodirectory devo inserire un file _index.md