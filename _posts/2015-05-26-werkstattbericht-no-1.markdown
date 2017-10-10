---
author: 
comments: false
date: 2015-05-26 09:26:31+00:00
layout: post
wplink: http://newsstreamproject.org/werkstattbericht-no-1/
slug: werkstattbericht-no-1
title: Werkstattbericht No. 1 - Die Big-Data-Infrastruktur
wordpress_id: 3561
categories:
- Blog
tags:
- Apache Spark
- Banana
- Cloudera
- D3js
- Elastic Search
- Hadoop
- Kibana
- Solr
---

Twitter ist für viele Forschungsprojekte und Journalisten eine der primären Informationsquellen, wenn es um die Analyse von Social-Media-Inhalten oder Breaking-News-Ereignisse geht. Hier kann die Twitter-Analyse ein Einstiegspunkt für weitere Untersuchungen und Recherchen sein.

Um den kontinuierlich, ständig wachsenden Datenstrom in Echtzeit zu bändigen bedarf es flexibler Lösungen. Aus journalistischer Sicht wollten wir uns unbedingt von starren Datendashboards lösen und Journalisten mehr Flexibilität bei der Datenaufbereitung, -analyse und -visualisierung geben.

Im Projekt Newsstream 3.0 wurde pünktlich zu den britischen Unterhauswahlen ein erster Demonstrator umgesetzt, mit dem sich die Twitter-Reaktionen auf die Wahldebatten verfolgen lassen. Das Kopf-an-Kopf-Rennen der Parteien lässt sich an einem Zeitstrahl ablesen, auf dem die Anzahl der Tweets von Labour und Tories verglichen wird. 

[![GE2015_UK](http://newsstreamproject.org/wp-content/uploads/2015/05/GE2015_UK.png)](https://newsstreamproject.org/wp-content/uploads/2015/05/GE2015_UK.png)

Der Demonstrator ist zu einem sehr frühen Zeitpunkt im Projektverlauf entstanden, pünktlich zum ersten Meilenstein, bei dem Anforderungsanalyse und Grobkonzept vorgelegt wurden. Interessant sind an dieser Stelle deshalb weniger die Ergebnisse der Analyse, sondern die verwendeten Technologien. Hinter dem Demonstrator steht eine ausgewachsene Big-Data-Infrastruktur: ein Hadoop-Cluster mit 16 Nodes und einer Speicherkapazität von insgesamt 100 Terabyte, auf dem Clouderas Open-Source-Distribution betrieben wird, die sowohl eine verteilte Stapelverarbeitung als auch die Echtzeitanalyse mit [****Apache Spark****](https://spark.apache.org) ermöglicht. Für die performante Auslieferung von Daten bindet Cloudera die verteilte Open-Source-Suchlösung Apache Solr an.

Das verwendete Dashboard stammt aus einem anderen Kontext, nämlich der Logfile-Analyse. Während Big Data für viele Unternehmen bisher noch kein Thema ist, hat sich im IT-Betrieb die kollaborative Auswertung von großen Mengen von Logfiles durchgesetzt – auch dank des interaktiven Dashboards “[**Kibana**](https://www.elastic.co/products/kibana)”, das ursprünglich als Demo-Applikation für die Open-Source-Suche Elasticsearch entwickelt wurde. Ebenso wie Twitter ist auch bei Logfiles die Zeit die wichtigste Dimension: hier geht es z.B. um die Anzahl der Nutzer oder der Fehlermeldungen pro Zeiteinheit. Mit wenigen Klicks lässt sich bei Kibana ein neues Dashboard als Kopie erstellen oder ein Widget hinzufügen. Die Auswahl reicht von Säulen- und Tortendiagrammen über Kartendarstellungen bis zu Tagclouds und Listen. Flexibilität ist für die Nutzer von Loganalyse-Tools zentral: wenn z.B. zusätzliche Informationen geloggt werden, muss es einfach möglich sein, auf diese Informationen zuzugreifen und sie im Dahsboard anzuzeigen. Eine gute Benutzbarkeit ist angesichts der hektischen Arbeitsbedingungen im IT-Betrieb ebenfalls von großer Bedeutung.

Die Ähnlichkeit zu den Anforderungen von Redakteuren sind frappierend. Für uns lag es deshalb nahe, ein Dashboard wie “Kibana” für die Twitter-Analyse zu verwenden. Um eine nahtlose Integration in [**Clouderas CDH**](http://www.cloudera.com/content/cloudera/en/products-and-services/cdh.html) zu ermöglichen, griffen wir dabei auf einen Entwicklungszweig von Kibana mit Namen “[**Banana**](https://github.com/LucidWorks/banana)” zurück. Die Twitter-Analyse ist für uns nur der Anfang. Im nächsten Schritt wird es darum gehen, eine Vielzahl von Quellen anzubinden und die Nutzungsmuster der Redakteure zu untersuchen. Ergebnisse der im Projekt entwickelten Textanalyse-Algorithmen werden an die Stelle der vom Datenanbieter wie Twitter gelieferten Metadaten treten. Der aktuelle Demonstrator dient dabei als Baukasten. Eine Aufgabe wird der Export von Widgets bzw. der ermittelten Datensätze für die Nutzung in anderen Formaten und Applikationen sein. Auch die visuelle Weiterentwicklung spielt eine Rolle – auch hier ist für eine einfache Erweiterbarkeit gesorgt, da die gewählte Lösung auf der im Datenjournalismus beliebten Open-Source-Bibliothek [**D3.js**](http://d3js.org/) basiert.

Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester **[http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
