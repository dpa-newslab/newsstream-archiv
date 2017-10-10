---
author: Martin Virtel
comments: false
date: 2016-08-04 05:04:11+00:00
layout: post
wplink: http://newsstreamproject.org/recherche-maschinen/
slug: recherche-maschinen
title: 'Vom Strom in den Text: Die anderen Roboter'
wordpress_id: 3882
categories:
- Blog
---

Ja, wir geben es zu: Wir wollen automatisieren. Es soll mehr Roboter geben in den Redaktionen. Wir glauben, dass Maschinen den Menschen beim Recherchieren unter die Arme greifen sollten. Dass sie helfen können, Texte präziser und gehaltvoller zu machen. Dass sie das Verlinken von Quellen unterstützen und die Arbeit in den Redaktionen so überprüfbar und damit glaubwürdiger wird.

Das sind die anderen Roboter. Im Journalismus kümmert sich die Mehrheit der Forscher und Entwickler im Moment darum, Automaten zum [Layouten von Zeitschriften](http://www.thedrum.com/news/2016/06/15/ibm-watson-drum-team-first-magazine-edited-ai), zum [Beschneiden von Bildern](https://github.com/jwagner/smartcrop.js/) oder zum  Schreiben von Texten zu bauen. Gerade hier ist im Moment viel in Bewegung:  Deutsche Medienunternehmen haben in den vergangenen Monaten in [mehrere](https://kress.de/news/detail/beitrag/135109-drei-neue-investoren-bei-ax-semantics-traditionshaeuser-investieren-in-roboterjournalismus.html) [Textroboter-Firmen](http://www.nma.vc/2016/03/welcome-batch-2-narrativa-bagmovies-yatrusanalytics/) investiert. Die Deutsche Welle kooperiert im Rahmen eines Förderprojekts mit dem Wahlvorhersage-Tool "PollyVote" und hat einen [Prototypen entwickelt](http://blogs.dw.com/innovation/tag/pollyvote/). Bei PollyVote werden die Daten neuer Umfragen in kürzester Zeit in Texte verwandelt, die Journalisten bei der Recherche und Bewertung unterstützen.

Maschinentexte sind schon unter uns - meist unbemerkt als Produktbeschreibungen auf großen E-Commerce-Websites, aber ab und zu auch gemischt mit ganz normalem Journalismus, als  [Wirtschafts-](http://www.wired.com/2015/10/this-news-writing-bot-is-now-free-for-everyone/) oder [Fußball-Berichte](http://www.retresco.de/Roboter-Journalismus_rtr_textengine_Weser-Kurier) aus dem Computer. Kleine Ironie der Technik:  die Texte entstehen aus Daten,  die zuvor von Menschen erfasst wurden, ohne dieses Futter würden die Textroboter stillstehen.

Im News-Stream-Projekt haben wir uns für eine andere Facette entschieden, die nach unserer Beobachtung bislang weniger Beachtung findet: die maschinelle Hilfe beim Erstellen von Texten. Diese Ausrichtung war von Anfang an Teil des Projektplanes. Sie ist auch die logische Fortsetzung des Ziels, Nachrichtenströme zu bändigen. Diese Aufgabe hält uns seit Projektstart beschäftigt, und sie wird es auch weiter tun. Es ist eine dieser Tätigkeiten, mit denen man auf absehbare Zeit nicht fertig wird. Zumindest, solange die Welt nicht aufhört, das Internet zu aktualisieren, solange die Algorithmen weiter entwickelt werden, mit denen man das Ganze dann wieder einsammeln, verarbeiten und klassifizieren kann.

Aber wie bekommt man den Strom in den Text? Wie kann man die Informationen so verpacken, dass sie Journalisten bei der Arbeit unterstützen? In den Worten von Friedrich Lindenberg, einem der originellsten und produktivsten Köpfe an der Grenze zwischen Technik und Journalismus: "Tools sind nur der Anfang, ich will Journalisten in die Köpfe zu schauen: Was denkt ihr? Was braucht ihr?"

Antworten gab es vom Publikum, auf einem Workshop auf der Jahrestagung des "Netzwerk Recherche", den wir zusammen mit Friedrich Lindenberg und der Journalistin Patricia Ennenbach im Juli in Hamburg veranstaltet haben (Die Präsentation zum Workshop finden Sie am Ende dieses Artikels). Und wie immer, wenn man seine Nutzer fragt - die Reaktionen waren andere, als wir es erwartet haben. Mit einigen der angesprochenen Punkte beschäftigen wir uns innerhalb des News-Stream-Projektes bislang nicht. Etwa, wie Journalisten davor geschützt werden können, bei der Recherche abgehört zu werden. Mit anderen sehr intensiv: Wie schafft man es überhaupt, das Menschen neue Werkzeuge akzeptieren?

Eine Antwort darauf ist: Die Arbeitsweise beobachten - und die Werkzeuge so gestalten, dass sie sich nahtlos einfügen. Ein Vorbild sind die Arbeitswerkzeuge, über die Softwareentwickler verfügen. Eine Idee, die Friedrich Lindenberg in [einem Blogpost](http://pudo.org/blog/2014/12/03/newsclipse.html) vorstellt und in einen Hackathon-Prototypen gegossen hat:

[![newsclip.se Prototyp](http://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-080601-300x232.png)](https://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-080601.png)

Daraus ist unser erster Prototyp entstanden: Der Rechercheroboter, ein Editor, der im Text nach Hinweisen sucht, an welchen Stellen er helfen kann.

[![Neofonie Recherche Roboter](http://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-080738-300x244.png)](https://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-080738.png)



Und, nach Rückfragen in der Redaktion, die Verfeinerung: Der Editor schaut nicht den kompletten Text an, er bekommt von der Autorin ein paar Hinweise. Inspiration für diese Verfeinerung war die Beobachtung, dass viele Journalisten in Hektik genau so arbeiten - sie hinterlassen Hinweise an sich selbst, an welchen Stellen eine Information fehlt. (Programmierer tun das genauso, sie halten auf diese Weise etwa Gedanken fest, die ihren Code bei einer späteren Verbesserungsrunde robuster machen könnten). Diese Hinweise sind mit ein paar Abstrichen maschinenlesbar.

[![Prototyp Recherche-Roboter II](http://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-081234-300x190.png)](https://newsstreamproject.org/wp-content/uploads/2016/07/Screenshot-from-2016-07-27-081234.png)



Und an dieser Stelle arbeiten wir nun weiter.  Die nächste Verfeinerung gibt es auf dem Scoopcamp Ende September in Hamburg zu sehen.



Die Präsentation von Newsstream, [Friedrich Lindenberg](https://twitter.com/pudo) und [Patricia Ennenbach](https://twitter.com/pen1710) auf der [Jahrestagung des Netzwerk Recherche](https://nr16.sched.org/event/6vUA/wissen-vernetzen-wie-algorithmen-die-recherche-unterstutzen).

