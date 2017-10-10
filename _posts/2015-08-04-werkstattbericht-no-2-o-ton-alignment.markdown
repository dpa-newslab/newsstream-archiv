---
author: 
comments: false
date: 2015-08-04 12:55:30+00:00
layout: post
wplink: http://newsstreamproject.org/werkstattbericht-no-2-o-ton-alignment/
slug: werkstattbericht-no-2-o-ton-alignment
title: Werkstattbericht No. 2 - Wie funktioniert O-Ton Alignment?
wordpress_id: 3607
categories:
- Blog
tags:
- Dr. Daniel Stein
- IAIS
- O-Ton Alignment
---

“… sagte Frau Merkel in einer Pressekonferenz im Juni 2013, dass das Internet für sie Neuland sei…” In welchem Kontext hatte die Bundeskanzlerin dieses Statement abgegeben, und wie ging der Satz dann eigentlich weiter? 

Bei der Einbettung von O-Tönen in seine redaktionellen Texte steht der Journalist gleich vor zwei Herausforderungen: einerseits muss eine prägnante Aussage häufig aus einer längeren Textpassage herausgesucht werden. Andererseits möchte man das gekürzte Zitat aber gerne mit der vollständigen Originalquelle verknüpfen.

Liegt zu dem Originalbeitrag kein Transkript vor, so kann man die Audiospur mittels automatischer Spracherkennung erschließen (vgl. [**Blog-Beitrag**](http://newsstreamproject.org/explainer-wie-funktioniert-eigentlich-spracherkennung)). Häufig genug findet man aber in den eigenen Archiven oder bei frei verfügbaren Podcasts auch eine bereits verschriftlichte Form des Interviews vor, was eine zeitliche Zuordnung von O-Ton und Audioschnipsel erheblich vereinfacht. Im Prinzip kommt hier ebenfalls die Technik der Spracherkennung zum Einsatz, da man aber eine zeitliche Zuordnung (engl.: alignment) zu existierendem Text erzwingen möchte, spricht man in diesem Zusammenhang von einem _forced alignment_.



Der Ablauf ist dabei wie folgt: zunächst wird ein Parser den eigentlichen Text aus dem Dokument extrahieren, denn häufig genug ist das Transkript Teil einer Webseite mit einer ganzen Reihe an anderer Information, Werbung, Impressum etc. Im Tokenisierungsschritt werden nun die gesprochenen Wörter isoliert: 
* Interpunktionszeichen werden entfernt, wenn es Satzmarkierungen sind (da sie nicht gesprochen werden)
* Abkürzungen wie “z.B.” werden ausgeschrieben
* Zahlen sowie Groß- und Kleinschreibung werden vereinheitlicht


Danach wird die orthographische Schreibweise in eine phonetische umgewandelt - aus “was wird da gesprochen” wird somit ein “wie wird das ausgesprochen”. Die Umwandlung erfolgt durch existierende Lexika, kann aber mit Hilfe von statistischen Verfahren auch automatisch auf neue und unbekannte Wörter erweitert werden. Im letzten Schritt startet man nun die eigentliche Spracherkennung auf dem Audiomaterial, lässt aber nur diese Phonemabfolge zu und gibt dem Algorithmus lediglich Spielraum, wie die Start- und Endzeiten zu setzen sind.

Für den Produktiveinsatz im News-Stream Kontext sind nun folgende Schritte anzugehen: 
* durch ein einfach zu wartendes Template-System muss sichergestellt werden, dass auch weniger technikaffine Redakteure in der Lage sind, das forced alignment auf interessante Quellen (intern und extern) anzuwenden
* das System muss auch lange (>10 min.), möglicherweise fehlerbehaftete Transkripte hinreichend genau zuordnen
* insbesondere bei Telefoninterviews muss die Audiotechnologie mit der schlechteren Tonqualität umgehen können
* die Technologie muss im Big-Data Kontext so verankert werden, dass der Journalist auf einer Editier-Oberfläche schnell Zugriff erhält.


[![Verarbeitung: forced alignment](http://newsstreamproject.org/wp-content/uploads/2015/08/Bildschirmfoto-2015-08-04-um-14.45.28-e1438692545943.png)](https://newsstreamproject.org/wp-content/uploads/2015/08/Bildschirmfoto-2015-08-04-um-14.45.28-e1438692545943.png) **Abbildung: Ein möglicher Workflow für die Verarbeitung von forced alignment Material.**

Wie ein solches System aussehen könnte, haben wir mit Material aus einem Deutschlandfunk **[in einer Demo dargestellt](https://dpa-newslab.github.io/newsstream-audio-alignment/dlf-20150621/)** (mit freundlicher Genehmigung des [Deutschlandfunks](http://www.deutschlandfunk.de/)).

Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester **[http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
