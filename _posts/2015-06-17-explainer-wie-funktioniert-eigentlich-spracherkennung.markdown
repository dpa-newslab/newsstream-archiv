---
author: 
comments: false
date: 2015-06-17 07:25:53+00:00
layout: post
wplink: http://newsstreamproject.org/explainer-wie-funktioniert-eigentlich-spracherkennung/
slug: explainer-wie-funktioniert-eigentlich-spracherkennung
title: 'Explainer: Wie funktioniert eigentlich Spracherkennung'
wordpress_id: 3579
categories:
- Blog
tags:
- Dr. Daniel Stein
- Explainer
- IAIS
- Spracherkennung
---

Hat Angela Merkel gestern in ihrer Ansprache eigentlich noch etwas zum Thema Griechenland gesagt? Wo in meinem Videoarchiv war denn nochmal das Original-Zitat zum Thema "Neuland"? Kann ich von der Talk-Runde gestern schnell eine kurze Übersicht der wichtigsten Schlüsselwörter angezeigt bekommen?

Sprachinhalte in multimedialen Beiträgen - Radiointerviews, Fernsehbeiträge, User Generated Content... - sind auch bei schlechter Aufnahmequalität für einen menschlichen Zuhörer ohne weiteres erfassbar. Allerdings können sie in dieser Form nicht von Text Mining Verfahren (etwa für Suchanfragen oder Schlüsselwortextraktion) weiterverwendet werden, da keine maschinenlesbaren Inhalte vorliegen. Aufgrund des hohen Aufwands der manuellen Verschriftlichung - je nach Genauigkeit bis zur siebenfachen menschlichen Arbeitszeit im Bezug auf Videolänge, also etwa acht Stunden transkribiertes Material pro Arbeitswoche - erscheint offensichtlich, dass einfließende Datenströme in Echtzeit nur mit automatischer Spracherkennung erfassbar sind.

Spracherkennung hat, nicht zuletzt durch mobile Anwendungen, längst den Weg in unseren Alltag gefunden. Wo finde ich in der Nähe eine Apotheke? Gibt es noch Reservierungsmöglichkeiten für eine Zugfahrt nach Freiburg? Die zugrundeliegenden Technologien haben also durchaus Marktreife, und auch der Forschungsstand hat sich in den letzten Jahren kontinuierlich weiterentwickelt. Als letzter großer Qualitätssprung wird z.B. die Verwendung von sogenannten Deep Neural Networks für die Spracherkennung, seit dem Jahre 2011, angesehen.

Dennoch entstehen bei der Transkription auch eine ganze Reihe von Fehlern, die es im Kontext von News-Stream zu berücksichtigen gilt. Um diese zu reduzieren, muss man zunächst die Arbeitsweise eines modernen Spracherkenners betrachten: grundsätzlich wird das Audiosignal auf die wesentlichen Sprachmerkmale reduziert und dann üblicherweise auf kleinere (und damit besser erlernbare) Spracheinheiten, die sogenannten Phoneme, heruntergebrochen. Aus News-Stream wird also zunächst so etwas wie N-JU-S-T-R-IE-M. Ein hinterlegtes Lexikon ist dann in der Lage, aus dieser Phonemfolge das Wort zu rekonstruieren. Ein weiteres Sprachmodell überprüft und korrigiert das Ergebnis mit Blick auf im Deutschen übliche Wortabfolgen.

[caption id="attachment_3586" align="aligncenter" width="555"][![Allgemeiner Aufbau eines automatischen Spracherkenners](http://newsstreamproject.org/wp-content/uploads/2015/06/Bildschirmfoto-2015-06-17-um-09.52.35.png)](https://newsstreamproject.org/wp-content/uploads/2015/06/Bildschirmfoto-2015-06-17-um-09.52.35.png) Allgemeiner Aufbau eines automatischen Spracherkenners.[/caption]

Optimiert werden diese Verfahren auf speziellem Trainingmaterial. Aus diesem Grund ist auch die Qualität der Spracherkennung dann am besten, wenn sich die Sprache im vorliegenden Audiosignal diesem Trainingsmaterial ähnelt - umgekehrt wird das Transkript umso schlechter, desto stärker sich die Eingabe vom Trainingsmaterial unterscheidet. Anderes Mikrophon, lispelnder Sprecher, Dialekte, Hall-Effekte, Musik im Hintergrund, ungewöhnliche Themen... die Liste läßt sich fast beliebig erweitern. Ein kleiner Vorteil beispielsweise für eingangs erwähnte Mobil-Applikationen: der Anbieter kennt zumindest im Vorfeld die verwendete Hardware und den ungefähren Abstand zum Mikrophon des Sprechers.



In News-Stream verwenden wir etwa 1000 Stunden vortranskribiertes Trainingsmaterial aus dem Broadcast-Bereich - ideal für heterogene Nachrichtenströme. Dazu kommen einige Millionen Sätze aus dem Deutschen für das Sprachmodell sowie etwa 350-tausend Wörter und deren Aussprache zur Befüllung des Phonemlexikons. Die Praxis zeigt, dass ein Transkript nicht perfekt sein muß, um sinnvoll weiterverarbeitet zu werden; vielmehr gilt als Schallmauer eine Wortgenauigkeit von gerade mal 60 Prozent. Tatsächlich erreichen wir mit unserer Technologie auf durchschnittlichen Inhalten aber deutlich über 80 Prozent Genauigkeit.

Zugegeben, wenn z.B. Herr Seehofer in etwas breiterem Dialekt über Offshore-Windparks referiert und im Hintergrund vielleicht sogar Blasmusik spielt, ist das entstehende Transkript bestenfalls belustigend. Für einen Großteil der Inhalte in News-Stream aber ist automatische Spracherkennung ein wichtiger Baustein bei der Echtzeitanalyse der multimedialen Nachrichtenströme.

Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester **[http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
