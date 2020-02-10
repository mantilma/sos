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

*** LIST PAGES, SINGLE PAGES ***
Hugo considera due tipi di pagine:
- list page che sono la homepage, /posts
- single page i contenuti specifici di ciascun post ovvero /posts/my-first-post, /posts/my-second-page

le list page arrivano soltanto al primo livello delle cartelle in automatico ovvero fino a /posts. Se io metto un altra sottodirectory devo inserire un file _index.md.
Infatti tutte le pagine che hanno un _index.md sono list page e per quelle al primo livello hugo le crea automaticamente poi noi semmai le possiamo sovrascrivverle.

*** FRONT MATTER ***
Le front matter sono i metadati che vedo in alto anche in questa pagina, come ad esempio:
title: "Info"
date: 2020-02-07T21:51:21+01:00
draft: true

questi poi possono essere acceduti nei miei template.

*** SHORTCODES: ***
questi sono pezzettini di html code da iniettare nei miei content .md files.
Ad esempio posso inserire un form, un video ecc...
{{< shortcode-name param1>}}

*** TAXONOMIES ***
Raggruppamento dei contenuti in base a tag e categorie in una pagina creata automaticamente da hugo (taxonomy page)
tags: ["tag1", "tag2"]
categories: ["cat1"]

*** TEMPLATE ***
se io ho importato un tema per modificarlo devo utilizzare la cartella layout che andrà a sovrascrivere la medesima presente sotto themes.
Ad esempio se io voglio creare un nuovo template per le list page devo:
1 creo una cartella layouts/_defaults
2 creo un file list.html se voglio creare un template comune per le pagine list, oppure single.html per tutte le pagine single
Per la pagina di home ci sarà la pagina index.html
Poi abbiamo baseof.html the higher level template