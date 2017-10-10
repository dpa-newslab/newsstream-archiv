---
author: 
comments: false
date: 2015-04-29 10:59:16+00:00
layout: post
wplink: http://newsstreamproject.org/wie-funktioniert-eigentlich-sprechererkennung/
slug: wie-funktioniert-eigentlich-sprechererkennung
title: 'Explainer: Wie funktioniert eigentlich Sprechererkennung?'
wordpress_id: 3536
categories:
- Blog
tags:
- Dr. Daniel Stein
- IAIS
- Sprechererkennung
---

Wahlabend, 18:05 Uhr. Die ersten Hochrechnungen flimmern über die Bildschirme - Zitterpartie! - die Nacht in der Redaktion wird lang. Noch halten sich die Spitzenvertreter der Parteien bedeckt. Wer wird wann das erste offizielle Statement vor der Kamera abgeben?  Auf welchen der vielen, parallel laufenden, Fernsehsender soll ich denn nun zuerst achten?

Ein Hauptziel von News-Stream ist die kontinuierliche Erweiterung der bereits bestehenden Recherchewerkzeuge für die automatisierte Datenanalyse heterogener Daten. Die maschinelle Sprechererkennung auf Tonspuren ist im digitalen Zeitalter wichtiger denn je. Sie ermöglicht eine automatische Erkennung aller Sprecher - gleichzeitig und kontinuierlich, auf multiplen, parallelen Nachrichtenströmen. Vordefinierte Benachrichtigung bei besonders zentralen Personen natürlich in Echtzeit. Und nicht nur das: selbst wenn der Sprecher erst plötzlich aktuell geworden ist und vorher praktisch unbekannt war, kann man dessen Redebeiträge im Archivmaterial identifizieren, ohne dabei den Namen kennen zu müssen - praktisch eine Audio-basierte Suche.




Moderne Sprechererkennung nutzt dabei immer häufiger das sogenannte i-vektor ("identity vector") Paradigma. Einem Tonsegment wird in diesem Verfahren eine Art akustische Signatur zugeordnet, und je ähnlicher sich zwei Signaturen sind, desto größer ist die Wahrscheinlichkeit, dass es sich dabei um den gleichen Sprecher handelt. Ordnet man nun einmalig bereits bekannte Sprecher ihren Signaturen zu und speichert diese Paare in einer Datenbank, ist die eigentliche Sprechererkennung für ein neues Tonsegment in wenigen Millisekunden gemacht: man vergleicht jede einzelne Datenbanksignatur mit der neuen und unbekannte Signatur - dort, wo die Ähnlichkeit am größten ist, wird der zugehörige Sprecher ausgelesen und somit "erkannt".

[caption id="attachment_3537" align="aligncenter" width="845"][![Prinzip der Sprechererkennung. Gleiche Sprecher sind im Merkmalsraum eng beieinander, unterschiedliche Sprecher liegen weit auseinander.](http://newsstreamproject.org/wp-content/uploads/2015/04/Sprechererkennung-845x684.png)](https://newsstreamproject.org/wp-content/uploads/2015/04/Sprechererkennung.png) Prinzip der Sprechererkennung. Gleiche Sprecher sind im Merkmalsraum eng beieinander, unterschiedliche Sprecher liegen weit auseinander.[/caption]

Gegenüber älteren Paradigmen haben die i-vektoren den entscheidenden Vorteil, dass sie aufgrund ihrer Speichergröße für große, schnell einströmende und heterogene Audiodaten (Stichwort Big Data) sehr gut geeignet sind. Ein i-vektor kommt üblicherweise mit wenigen hundert Zahlenwerten aus und erfasst dabei das gesamte Segment. Das heißt also, dass die Sprecherdaten in einem Videobeitrag mit einem Bruchteil des ursprünglichen Umfangs abgelegt werden können: bei einem Video in HD Qualität von etwa 30 Minuten Länge, etwa ein Gigabyte Speicherplatz, fallen bei 100 Sprecherwechseln etwa 50 Kilobyte an Daten an, also lediglich 0,005% Speicherplatz des Originalvideos.



[caption id="attachment_3543" align="aligncenter" width="845"][![i-Vektoren](http://newsstreamproject.org/wp-content/uploads/2015/04/i-Vektoren-845x684.png)](https://newsstreamproject.org/wp-content/uploads/2015/04/i-Vektoren.png) Graphische Darstellung der I-Vektoren von Angela Merkel und Wolfgang Schäuble[/caption]

Ein weiterer Vorteil der Informationskompression: der Datenschutz bleibt gewährleistet, denn ohne das zugehörige Videomaterial und ohne den Schlüssel zur Erzeugung der Werte sind die i-vektoren zunächst nutzlos. Das Wissen über die ursprüngliche Tonspur geht bei dem Prozess unwiederbringlich verloren - aus 400 Zahlen lassen sich die Originaltöne nicht mehr extrahieren.
Insbesondere bei zentralen Medienereignissen wie etwa Wahlabenden oder _Breaking News Events_ ist das automatisierte Sprechermonitoring ein zentrales Datenanalyseverfahren. Der Journalist wird bei seiner Recherche entlastet und kann sich auf andere Kernaufgaben fokussieren. Wenn Frau Merkel dann endlich vor die Mikrophone tritt, wird sich die Sprechererkennung schon melden.
