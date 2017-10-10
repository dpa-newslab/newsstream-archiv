---
author: 
comments: false
date: 2015-10-05 13:45:56+00:00
layout: post
wplink: http://newsstreamproject.org/werkstattbericht-no-3-so-haben-wir-den-sourcetracker-entwickelt/
slug: werkstattbericht-no-3-so-haben-wir-den-sourcetracker-entwickelt
title: Werkstattbericht No. 3 – So haben wir den SourceTracker entwickelt
wordpress_id: 3650
categories:
- Blog
tags:
- Apache Spark
- HBase
- Lambda-Architektur
- SourceTracker
---

Datenjournalisten und Big-Data-Experten haben einen sehr unterschiedlichen Blick auf Daten: Erstere möchte die Daten am liebsten in einem interaktiv Framework untersuchen und eine Geschichte erzählen. Letztere kämpfen mit der Integration heterogener Daten und befassen sich mit verteilten Algorithmen des maschinellen Lernens oder der Graphanalyse. Wie können Datenjournalisten und Big-Data-Experten bei der Entwicklung einer komplexen Big-Data-Plattform wie News-Stream 3.0 produktiv zusammenarbeiten und voneinander lernen? 

Die gemeinsame Entwicklung und Nutzung unserer Big-Data-Plattform soll am Beispiel des “SourceTrackers” gezeigt werden, unseres jüngsten Demonstrators. 

Ziel des SourceTrackers ist es, die Verbreitung von Aussagen auf den Websites von Medien nachzuvollziehen - etwa, um zu verfolgen, welche Aussagen aus PR-Material unverändert übernommen werden oder in welchen Fällen die Meldungen aus dem Dienst der dpa vor der Veröffentlichung stark oder weniger stark umgeschrieben werden. Die Vermutung: für die dpa-Redaktion, aber auch für PR-Agenturen ergeben sich daraus nützliche Hinweise für die Gestaltung von Meldungen. 
Inspiriert hat uns dabei das Projekt [Churnalism](http://www.churnalism.com), eine britische Suchmaschine, die handwerklich fragwürdigen Copy & Paste Journalismus aufdecken sollte, inzwischen aber eingestellt wurde.

**Wie gehen wir bei der Analyse vor?**

Bei unserer Analyse werden die Dokumente zunächst anhand ihrer digitalen Fingerabdrücke verglichen. Im nächsten Schritt werden die Dokumente auf Zeichenebene verglichen. Ein Demonstrator visualisiert die Analyse einzelner Dokumente und ihrer Nutzung.

[![SourceTracker](http://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.26.58.png)](https://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.26.58.png)

Eine weitere Art der Analyse ist die Gesamtschau auf einen Tag - im Beispiel der 29. September 2015. Jeder Kreis steht für eine eine Meldung aus dem dpa-Basisdienst. Je weiter oben der Kreis eingezeichnet ist, desto mehr Websites haben Bestandteile dieser Meldung übernommen (y-Achse). Je weiter rechts der Kreis eingezeichnet ist, desto weniger Sätze der Meldung wurden verändert. Die Farben stehen für die dpa-Ressorts (wi=Wirtschaft, pl=Politik, vm=Vermischtes, sp=Sport, ku=Kultur).

[![SourceTracker Analyse](http://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.28.54.png)](https://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.28.54.png)

Hier noch einmal die Liste der Top 5 Geschichten vom 25. 9. Lesebeispiel: “Bestandteile der Game of Thrones-Meldung wurden auf 166 Websites verwendet. Im Durchschnitt haben die Websites 66,98% übernommen”.

[![SourceTracker Analyse2](http://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.30.23.png)](https://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.30.23.png)

**Unser Big-Data-Framework**

Wir wollten von Projektbeginn an unter Big-Data-Bedingungen arbeiten: nicht mit “Spielzeugdaten”, sondern große Datenmengen und hochperformanten verteilte Algorithmen. Neben dem dpa Basisdienst und Twitter verarbeiten wir einen Newsfeed mit Artikeln aus über 1000 Online-Nachrichtenquellen, die von unserem Spider dafür extrahiert wurden. Das Big-Data-Framework Apache Spark bildet das Herzstück unseres Clusters. Spark ist im Vergleich zu seinem Vorgänger Hadoop MapReduce rasend schnell, weil es auf die verteilte Verarbeitung im Arbeitsspeicher setzt - und es erlaubt sowohl die Echtzeitverarbeitung von Datenströmen als auch die effiziente Abarbeitung von “Datenstapeln” (Batch-Verarbeitung). Der Entwicklungscluser von News Stream 3.0 füllt einen kompletten Serverschrank, aktuell 16 Server mit insgesamt 100 Terabyte Festplattenplatz, Tendenz wachsend.

Unsere Plattform basiert auf einer “Lambda-Architektur”. Dieser Begriff beschreibt ein Modell, bei dem die verwendeten Rohdaten unverändert gespeichert werden. Parallel zur echtzeitnahen Verarbeitung neu eintreffender Daten kann eine Neuprozessierung von Teilen oder des gesamten Datenbestandes stattfinden. Das erleichtert die Erprobung und Verbesserung von Algorithmen. Die Ergebnisse, also in unserem Fall Dokumente mit dokumentbezogenen oder dokumentübergreifenden Metadaten, werden über eine Auslieferungsschicht verfügbar gemacht. Die Rohdaten, das können je nach Clustergröße Terabytes oder Petabytes sein, werden bei uns in der verteilten Datenbank HBase gespeichert. Ausgeliefert werden die prozessierten Daten über eine verteilte Suche - hier ist die maximale Datenmenge durch den verfügbaren Arbeitsspeicher begrenzt - in unserem Fall auf mehre Milliarden Dokumente.

[![BigData Frameform](http://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.34.44.png)](https://newsstreamproject.org/wp-content/uploads/2015/10/Bildschirmfoto-2015-10-05-um-15.34.44.png)

Mehrere Suchindexe biete Zugriff auf einen Teil der prozessierten Daten - entsprechend den aktuellen Anforderungen der Demonstratoren. Über die Such-Schnittstelle lassen sich bereits einige der Fragen beantworten, die uns nach der Präsentation unserer ersten SourceTracker-Demo gestellt wurden: 

Können wir diese Analysen für alle dpa-Meldungen eines Tages, einer Woche oder eines Monats durchführen? 


* Was sind meistzitierten Sätze? 


* Welche Medien übernehmen große Teile der dpa-Meldungen? 


* Welche nur einzelne Passagen? 


* Ist das von Ressort zu Ressort unterschiedlich? 



Per Python-Skript kann der Entwicklungsredakteur direkt auf die Such-API zugreifen und experimentieren. Und sobald klar ist, welche Reports regelmäßig gewünscht werden, können wir diese effizient für Spark implementieren.

Andere Fragen erfordern eine Anpassung unserer bisherigen Datenverarbeitungs-Pipeline. 

	
* Werden die Agenturinhalte im Laufe eines Tages nach und nach durch redaktionelle Inhalte ersetzt? Hierfür müssten wir verschiedene Versionen von Artikeln vorhalten. 


	
* Könnten wir nicht mit den gleichen Methoden herausfinden, welche Medien sich bei Wikipedia bedienen? Hierzu müssten wir nur die regelmäßig bereitgestellten Wikipedia-Dumps einlesen und prozessieren.

 
	
* Kann ich mich benachrichtigen lassen, sobald ein Artikel von anderen Medien aufgegriffen wird? Das wäre ein erster Anwendungsfall für ein Alert-Modul in unserer Spark-Pipeline.

 

Währenddessen laufen auf dem Cluster längst neue Experimente: es geht um die Topic-Erkennung in Nachrichten und eine Verknüpfung maschinell gelernter Themen mit des semantsichen Metadaten der Dokumente (vgl. [**Blogbeitrag**](http://newsstreamproject.org/was-passiert-bei-semantischer-textanalyse/)). Die nächste Demo wird nicht lange auf sich warten lassen.

Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester **[http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
