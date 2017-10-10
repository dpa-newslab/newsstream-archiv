---
author: Admin
comments: false
date: 2016-06-23 19:17:45+00:00
layout: post
wplink: http://newsstreamproject.org/explainer-warum-wir-das-training-unserer-sprechererkennung-von-100-auf-1000-stunden-erhoeht-haben/
slug: explainer-warum-wir-das-training-unserer-sprechererkennung-von-100-auf-1000-stunden-erhoeht-haben
title: 'Explainer: Warum wir das “Training” unserer Sprechererkennung von 100 auf
  1000 Stunden erhöht haben'
wordpress_id: 3868
categories:
- Blog
---

Bei “News-Stream” arbeiten wir daran, eine deutliche höhere Qualität bei der Zuordnung von O-Tönen (Audioaufnahmen aus Radio- oder Fernseh-Interviews) anzubieten. Dieser kurze Beitrag liefert einen Einblick was dazu technisch notwendig ist.

Nehmen wir das Beispiel Flüchtlingskrise... ein großes, drängendes Thema, zu dem es viele unterschiedliche Meinungen gibt. Aber: Wer vertritt hierbei welche Position, und wie stand der- oder diejenige vielleicht noch vor ein paar Monaten zu dem gleichen Thema? Heute werden solche Vergleiche von Hand mit viel Zeitaufwand erstellt, wenn überhaupt. Denn in vielen Redaktionen ist kaum Zeit für solche aufwändigen Vergleiche - die mühevolle Suche im Archiv dauert einfach zu lange.

Im Rahmen des “News-Stream” Projekts entwickeln wir jetzt jedoch Big-Data Analysetools, die für solche Fragestellungen eine deutliche Vereinfachung gepaart mit automatisierter Erkennung relevanter Inhalte bieten. Daran arbeitet das Team des News-Stream Projektpartners Fraunhofer IAIS im Rahmen des Themenbereichs “Audio Minings”.

Die Grundvoraussetzung für eine gute Audioanalyse ist, dass ein bestimmter Sprecher in einem Archiv mit vielen Aufnahmen oder bei neu erstellten Interviews im Radio oder Fernsehen verlässlich identifiziert wird. Wir sind bereits in einem Beitrag unseres Blogs auf die [Sprecheridentifikation in einem Audiobeitrag](http://newsstreamproject.org/explainer-wie-funktioniert-eigentlich-spracherkennung/) eingegangen. Als Grundlage verfügt unser System über sogenannte i-Vektoren. Diese charakterisieren einen akustischen Sprachbeitrag. Die Vektoren ähneln sich, inbesondere wenn dann, wenn sich das akustische Profil der Stimme im Sprachbeitrag ähnelt. Für die Erkennung des Sprechers gilt: Je besser der i-Vektor, desto genauer lässt sich ein bestimmter Sprecher später erkennen.

**Wie sieht ein i-Vektor aus?
**

Die folgenden drei Tabellen zeigen, wie sich mit Hilfe einer Vielzahl verschiedener Parameter Muster und Übereinstimmungen ermitteln lassen: Ein unbekannter, neuer i-Vector einer Aufnahme wird mit einem bereits bekannten Profil verglichen. Je nach Grad der Übereinstimmung ist dann eine Erkennung des mit diesem i-Vektor verbundenen Sprechers möglich.

**Beispiel 1: Unbekannter (neuer) i-Vector**

[![Bildschirmfoto 2016-06-23 um 17.17.41](http://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.17.41.png)](https://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.17.41.png)

**Beispiel 2: i-Vektor Angela Merkel (Sprechermerkmale)**

[![Bildschirmfoto 2016-06-23 um 17.17.54](http://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.17.54.png)](https://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.17.54.png)

**Beispiel 3: Vergleichs Ergebnis (Kosinus Distanz), Positiver Match**

[![Bildschirmfoto 2016-06-23 um 17.18.04](http://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.18.04.png)](https://newsstreamproject.org/wp-content/uploads/2016/06/Bildschirmfoto-2016-06-23-um-17.18.04.png)

**Training für Spracherkennung**

Einmal festgelegt ändern sich die i-Vektoren nicht mehr.  Allerdings muss man ihre Herstellung doch trainieren. Damit wird sicher gestellt, dass gleiche Sprecher ähnlich und ungleiche Sprecher unähnlich werden. Für dieses Training braucht man eine große Datenmenge von vormarkierten Sprachsegmenten, von denen man die Sprecher bereits kennt.

Aus diesem Training der i-Vektoren auf ein bestimmtes Sprecherprofil entsteht eine Art “Fingerabdruck”, der dann bei neuen Audioaufnahmen benutzt wird. Später muss man dann zwar auf diese Daten nicht mehr zurückgreifen, umgekehrt kann man ein suboptimales Training aber auch nicht mehr rückgängig machen.

Warum ist das so? Ein Beispiel: Wenn alle i-Vektoren optimal auf Bundestagssprecher trainiert wurden, dann sind die Modelle stark auf das eine Mikrophon vorne am Rednerpult optimiert. Sprechen dann aber in einem Radio-Interview zwei  Sprecher über Telefon miteinander, dann weicht der Charakter der Aufnahmen so stark von den Trainingsdaten ab, dass alles Mögliche passieren kann. Vermutlich werden sich die i-Vektoren der Telefonaufnahmen untereinander viel zu ähnlich sein. Grund ist die Tonmodulation von Stimmen über ein Telefon. Selbst wenn beispielsweise ein männlicher und ein weiblicher Sprecher vorliegen, werden die Aufnahmen der Sprecher zueinander ähnlicher sein als ihren "trainierten" Sprechermodellen. Mann und Frau aus den Telefonaufnahmen würden möglicherweise als derselbe Sprecher _fehl_-erkannt.

**Von 100 auf 1000 Stunden Training für die Sprechererkennung**

Die Herausforderung aus technischer Sicht lautet, eine Sprecherin wie zum Beispiel Angela Merkel in ganz unterschiedlichen Aufnahmesituationen und Audioqualitäten verlässlich an bestimmten Merkmalen ihrer Stimme zu erkennen. Im Journalismus-Kontext werden vor allem morgens viele wichtige Radio-Interviews mit Politikern geführt, häufig per Telefon. Das Trainingsset sollte also mindestens diese Tatsache berücksichtigen.

Wir haben daher unsere Modelle für die Sprechererkennung nochmal generalüberholt und statt der bisher knapp 100 Stunden Training nun auf über 1000 Stunden Beiträge in 20 Sprachen erweitert. Dabei wurden etwa zu Hälfte Aufnahmen über Mikrophone, zur anderen Hälfte Aufnahmen über Telefone benutzt. Die Ergebnisse und die dadurch deutlich verfeinerten i-Vektoren wurden im Rahmen einer Masterarbeit auf Herz und Nieren überprüft.

Dabei wirkte sich vor allem ein Verfahren positiv aus, dass die i-Vektoren zusätzlich verfeinert, indem es verschiedene Kanäle (etwa: Außenaufnahme, Telefonie) als auch verschiedene Sprechermodalitäten (z.B. heiser, laut) mit modelliert. Der Verlauf des i-Vektors nimmt also viel mehr Facetten einer Sprechstimme auf. Die Trefferrate bei unserer internen Evaluierung lag nach diesem ausgeweiteten Training bei sehr guten 91%.

**Sprechererkennung für Redaktionen nutzbar machen**

Jetzt, wo die Modelle stabil stehen, wird die nächste Herausforderung darin liegen, möglichst effizient öffentlich verfügbare Quellen dazu zu benutzen, die Sprecherdatenbank zu befüllen und im laufenden Betrieb zu aktualisieren. Dann kann der Journalist sowohl bei vielen Beiträgen gleichzeitig als auch bei der Recherche in großen existierenden Archiven schnell das Sprachsegment mit der für ihn interessanten Person identifizieren und den O-Ton in seinen Artikel integrieren.

**Innovative Werkzeuge **

Damit kommen wir unserem Ziel näher im Rahmen von “News-Stream” eine ganze Reihe innovativer Analysetools für großen Mengen an Inhalten und Audio-Archiven bereit zu stellen.  Interessant ist das nicht nur für TV- und Radiosender, sondern auch für Zeitungen, Magazine und Online-Angebote, die immer stärker multimedial berichten und arbeiten.



**Hintergrund:** Das Projekt “News-Stream” erforscht mit den Partnern Fraunhofer IAIS, Neofonie sowie den Anwendungspartnern dpa und Deutsche Welle neue Anwendungsmöglichkeiten für Big Data-Analysen in Redaktionen und anderen Kommunikationsbereichen.  Mit der IAIS-Technologie »Audio Mining« lassen sich gesprochene Wörter in Audiodateien und Videos erfassen und wie eine textbasierte Datei analysieren.

Eine weitere Besonderheit ist die Sprechererkennung: Sie ermöglicht eine automatische Erkennung der Person, die gerade in einem Beitrag spricht. Diese Technologie basiert auf dem »i-Vektor-Paradigma«, bei dem jedem Tonsegment eine akustische Signatur zugeordnet wird. Dank ihrer Speicherkapazität sind i-Vektoren in der Lage, auch große, schnell einströmende und heterogene Audiodaten in kürzester Zeit zu analysieren. In der News-Stream-Plattform soll die Sprechererkennung Redakteure unter anderem dabei unterstützen, keine Wortmeldung wichtiger Akteure zu verpassen: Sobald etwa die Bundeskanzlerin vor die Kameras tritt, um sich zu einem aktuellen Thema zu äußern, erscheint ein entsprechender Hinweis auf die Übertragung im Bildschirm. Redebeiträge lassen sich über diese audiobasierte Suche aus den Nachrichtenströmen eindeutig einzelnen Sprechern zuordnen und herausfiltern.  Wenn Sie Interesse an weiteren Einblicken haben oder erste Demonstratoren selbst testen wollen, nehmen Sie gern Kontakt auf.

_Ansprechpartner:_ David Laqua, Fraunhofer IAIS - E-Mail: david.laqua [AT] iais.fraunhofer.de
