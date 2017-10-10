---
author: Admin
comments: false
date: 2016-12-13 11:47:21+00:00
layout: post
wplink: http://newsstreamproject.org/tickertools-premiere-fuer-die-inoffizielle-news-stream-api/
slug: tickertools-premiere-fuer-die-inoffizielle-news-stream-api
title: '#tickertools – Premiere für die inoffizielle News-Stream API'
wordpress_id: 3925
categories:
- Blog
---

[caption id="attachment_3927" align="alignleft" width="225"][![11 Ideen - 48 Stunden](http://newsstreamproject.org/wp-content/uploads/2016/11/hackathon-inhalt-225x300.jpg)](https://newsstreamproject.org/wp-content/uploads/2016/11/hackathon-inhalt.jpg) 11 Ideen - 48 Stunden[/caption]

Was brauchen Journalisten, um mit den wachsenden Datenströmen zurechtzukommen? Welche Tools helfen bei der Kommunikation mit den Lesern? Und wie findet man die passenden Nachrichten, die den Nutzer durch den Tag begleiten? Bei News-Stream haben wir in den vergangen beiden Jahren Antworten auf diese Fragen gesucht und gefunden – im Konsortium und gemeinsam mit Kunden und Kollegen.

Die Nachrichtenagentur dpa hat im November ihren ersten Hackathon veranstaltet mit dem Ziel, Werkzeuge zu entwerfen und zu entwickeln, die Journalisten bei ihrer täglichen Arbeit unterstützen. Das Experiment names [#tickertools](https://twitter.com/hashtag/tickertools) , organisiert vom Next Media Accelerator, brachte bunt gemischte Teams aus Journalistinnen, Marketing-Leuten, Informatikerinnen und Designerinnen im Berliner Newsroom zusammen. Neben dem Zugang zu dpa-Nachrichten und der dpa-Liveberichterstattung stand erstmals die technische Infrastruktur von News-Stream für Prototypen zur Verfügung.

Für News-Stream beginnt damit die Evaluationsphase, in der die Forschungsergebnisse sich dem Urteil der Praktiker stellen müssen. Bereitgestellt wurde  die „[inoffizielle News-Stream API](https://dpa-newslab.github.io/tickertools2016/2016/10/27/newsstream/)“, ein Suchindex, der von unserer Big-Data-Plattform gespeist wird. Er enthält Nachrichten aus über 1000 Quellen, sowie alle Agenturmeldungen von dpa aus dem Projektzeitraum. Die Texte sind mit semantischen Annotationen aus der  [TXT Werk API](http://txtwerk.de/) von Neofonie versehen, Zitate, Personen, Institutionen, Ortsnamen und Schlagworte sind also markiert und zum Teil mit Verweisen auf andere Datenquellen versehen. (Wie unser Big-Data-Framework uns dabei hilft, wird [in einem früheren Blogbeitrag](http://newsstreamproject.org/werkstattbericht-no-3-so-haben-wir-den-sourcetracker-entwickelt/) beschrieben).

Als einfachen Einstieg hatten wir ein Dashboard vorbereitet, einige Python-Skripte und [Jupyter Notebooks](https://github.com/dpa-newslab/tickertools2016)  zeigen typische Anfragen an die inoffizielle News-Stream API. Die Notebooks nutzen wir im Projekt besonders gern -  Anfragen können dort interaktiv ausgeführt und z.B. in Form von Charts dargestellt werden.

Die knapp 50 Teilnehmer fanden sich nach einer kurzen Pitch-Phase am Donnerstag zu elf Projekten zusammen, die sie nach gut zwei Tagen - bei einigen Teams inklusive Nächte - schließlich am Samstag Mitteilnehmern und der Jury präsentieren konnten. Über die Vergabe von 2000 Euro Preisgeld und nicht dotierte Sonderpreisen entschieden [Isa Sonnenfeld](https://twitter.com/isasun) (Leitering Google Newslab D/A/CH), [Annette Milz](https://twitter.com/AnMilz) (Chefrakteurin des “Medium Magazin”), [Roland Freund](https://twitter.com/RolandFreund) (Vize-Chefredakteur dpa) und [Dirk Zeiler](https://twitter.com/herzbach), CEO des next media accelerator.

[caption id="attachment_3930" align="alignright" width="300"][![Die Gewinner, das Team „Factfox“: Dirk Hübner, Lukas Will, Miriam Mogge, Gudrun Riedl, Sami Boussaid (Foto: Gregor Fischer / dpa) ](http://newsstreamproject.org/wp-content/uploads/2016/12/dpa_Tickertools_Hackathon_012-300x199.jpg)](https://newsstreamproject.org/wp-content/uploads/2016/12/dpa_Tickertools_Hackathon_012.jpg) Die Gewinner, das Team „Factfox“: Dirk Hübner, Lukas Will, Miriam Mogge, Gudrun Riedl, Sami Boussaid  
(Foto: Gregor Fischer / dpa)[/caption]

Gewinner war das Projekt “Factfox”, ein Werkzeug, das Social-Media-Moderatoren dabei helfen soll, Scheinargumenten Fakten entgegenzusetzen.

Auch zwei von News-Stream-Mitgliedern unterstützte Projekte waren unter den Preisträgern:

Eine Idee, die das Projekt schon seit dem Start umtreibt, ist eine bessere Arbeitsumgebung - ein Redaktionssystem, das Journalisten bei ihrer Arbeit unter die Arme greift, indem es Fakten nachschlägt und Belege verlinkt. Unser erstes Konzept, der [Recherche-Roboter](http://newsstreamproject.org/recherche-maschinen/)  hat nun Gesellschaft bekommen von der [Kontextmaschine](%20https://dpa-newslab.github.io/kontextmaschine/).



[![kontextmaschine](http://newsstreamproject.org/wp-content/uploads/2016/12/kontextmaschine.gif)](https://newsstreamproject.org/wp-content/uploads/2016/12/kontextmaschine.gif)

In eine ganz ähnliche Richtung zielt der Prototyp “Newsaddition” - ausgezeichnet als “Best of Pitch”. Die Suchmaschine liefert Kontext für den mobilen Reporter, der vor Ort etwas passgenaueres braucht als eine Google-Suche, die außer Informationen zum Thema zu oft noch Gerüchte und Satire und wenig sachdienliche Zufallstreffer enthält.

Eine weitere Projektidee war der Informer. Da Blogs für Nachrichtenagenturen zu einer wichtigen Ressource von Vor-Ort-Journalismus und von Meinungen und Trends geworden sind, wurde versucht, Nachrichten aus dem dpa-Ticker mit aktuellen Blogs und anderen Quellen zu verlinken. Als Grundlage der Verlinkung sollten die aus TXT Werk gewonnen Entitäten verwendet werden. Auf Entitäten basierende Empfehlungssysteme bringen in der Regel deutlich bessere Ergebnisse als eine normale Textsuche, unter anderem, weil mit ihnen eine ganze Reihe von Zusatzinformationen verbunden sind - bei Personen etwa Bild oder Geburtsjahr, bei Orten die genauen Koordinaten.  Resultat des Projekts war ein Demonstrator, der bereits einfache Verknüpfungen herstellte. Das Team wurde mit ihrer Präsentation dabei mit dem Preis “Best of API” geehrt.

Fast alle der Teams haben die inoffizielle News-Stream API und TXT Werk benutzt, unser Server hatte während des Hackathons einiges zu tun, und wir hatten endlich einen Grund, Load Balancing für die massiven Anfragen einzubauen. Auch in den elf Pitches ([hier der Video-Mitschnitt](https://www.facebook.com/NextMediaAccelerator/videos/682117675280210)) wird News-Stream mehr als einmal erwähnt. Wir nehmen das als Ermutigung und als Zeichen,  dass unsere Arbeit in die richtige Richtung geht. Auch wenn es nicht immer leicht war, zwischen der Rolle als API-Berater und als Teammitglied hin- und herzuwechseln.
