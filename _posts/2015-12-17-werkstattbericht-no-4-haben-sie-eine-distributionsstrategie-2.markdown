---
author: 
comments: false
date: 2015-12-17 17:46:12+00:00
layout: post
wplink: http://newsstreamproject.org/werkstattbericht-no-4-haben-sie-eine-distributionsstrategie-2/
slug: werkstattbericht-no-4-haben-sie-eine-distributionsstrategie-2
title: Werkstattbericht No. 4 – Haben Sie eine Distributionsstrategie?
wordpress_id: 3710
categories:
- Blog
tags:
- Peter Adolphs
- Topic Monitoring
---

Die Konkurrenzanalyse gehört in Medienunternehmen zum täglichen Business - insbesondere im Onlinebereich. Dabei steht i.d.R. die Themenagenda im Fokus der Aufmerksamkeit. Kein Nachrichtenunternehmen will schließlich ein wichtiges Thema in der eigenen Berichterstattung auslassen und Nutzer an die Konkurrenz verlieren.

Es gibt einen Aspekt, der für die eigene Strategie mindestens genauso wichtig ist, wie das Themenmonitoring - die Distributionsanalyse.

**Warum ist die Distributionsanalyse wichtig für mich?**

Die Daten, die bei der Distributionsanalyse herangezogen werden, können bei der Optimierung der eigenen Distributionsstrategie helfen die Nutzer besser zu erreichen. Bei der Analyse wird der Zeitpunkt der Publikation herangezogen. Eine Heatmap-Visualisierung eignet sich für die Darstellung der Ergebnisse besonders gut dafür. Durch die gewonnen Erkenntnisse lässt sich die Distributionsstrategie nicht nur klarer nachvollziehen, sondern ermöglicht es auch sich von der Konkurrenz durch ein eigenes Profil abgrenzen. Die Datenanalyse kann dabei helfen u.a. folgende Fragen zu klären:

- Habe ich eine Distributionsstrategie?
- Hat die Konkurrenz eine Distributionsstrategie?
- Welche Themen werden zu welchem Zeitpunkt publiziert?
- Welche Themen stehen momentan bei der Konkurrenz im Fokus der Berichterstattung?
- Hat sich meine Distributionsstrategie über die letzten Wochen verändert?

**Ein Beispiel: Toranalyse BuzzFeed**
BuzzFeed publiziert die meisten Artikel außerhalb der üblichen Kernarbeitszeiten. Sobald wir aber in der Freizeitzone sind, werden wir mit Content versorgt. Besonders intensiv ab 17:00 EST bis spät in die Nacht hinein. Auffällig ist insbesondere die Berücksichtigung der Mittagspause (12:00 EST), die ebenso gezielt für die Contentdistribution genutzt wird.

[caption id="attachment_3695" align="alignnone" width="629" class="align center"][![„Analyse:](http://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.14.50.png)](https://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.14.50.png) Analyse: http://pushthings4ward.com/buzzfeed/index_en.html[/caption]

Sieht man sich hingegen deutschsprachige Nachrichtenanbieter an lässt sich in den meisten Fällen keine eindeutige Distributionsstrategie erkennen - eher ein 7to7-Muster.
[![News-Stream](http://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.18.33.png)](https://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.18.33.png)

Das Themenmonitoring ergänzt die Beurteilung der aktuellen Situation. Nach dem Terroranschlag in Paris hat die Berichterstattung deutlich angezogen.

[![News-Stream](http://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.20.27.png)](https://newsstreamproject.org/wp-content/uploads/2015/12/Bildschirmfoto-2015-12-16-um-13.20.27.png)

**Wie gehen wir bei der Analyse vor**

Wir crawlen Nachrichtenseiten, extrahieren anhand von händisch erstellten Pattern auf der HTML-Struktur der Seiten die Artikelinhalte und Metadaten, wie z.B. das Datum der Veröffentlichung und speichern diese Informationen anschließend in einem Suchindex. Zusätzlich binden wir den dpa Basisdienst ein, der ebenfalls in den gleichen Index geschrieben wird. Dadurch dass Quelle und Veröffentlichungsdatum als Feld im Index gespeichert werden, kann man in Anfragen nach Quelle und Zeitraum filtern. Die Datenbasis für die Heatmap ist dann ganz einfach über eine facettierte Suchanfrage zu erstellen, die pro Quelle und Tag, bzw. Stunde, die Anzahl der veröffentlichten Artikel liefert. Die Visualisierung der Heatmap wurde mit der Javascript-Bibliothek D3.js realisiert.

**Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester [http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
