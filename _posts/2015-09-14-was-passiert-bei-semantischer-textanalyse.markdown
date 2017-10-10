---
author: 
comments: false
date: 2015-09-14 11:59:55+00:00
layout: post
wplink: http://newsstreamproject.org/was-passiert-bei-semantischer-textanalyse/
slug: was-passiert-bei-semantischer-textanalyse
title: 'Explainer: Was passiert bei semantischer Textanalyse?'
wordpress_id: 3645
categories:
- Blog
tags:
- neofonie
- Textanalyse
- TXT Werk API
---

Es ist nun fast schon ein halbes Jahrzehnt vergangen, seit IBM mit seinem Computersystem namens Watson in der Fernseh-Show Jeopardy angetreten ist. Das Ziel der Sendung ist es, aus einer gegebenen Antwort die semantisch dazu passende Frage zu stellen, und Watson schlug hier zwei menschliche Teilnehmer, die in der Show bereits gewonnen hatten, um Längen. 
Auch im heutigen Journalismus ist die Unterstützung durch Textanalyse-Verfahren nicht mehr wegzudenken. So werden Redakteure durch die automatische Identifikation von Schlüsselwörtern bei der Verschlagwortung ihrer Artikel unterstützt. Ebenso lassen sich mit dieser Technologie Themenseiten vollkommen automatisiert erstellen, so dass sich z.B. alle Nachrichtenbeiträge verschiedener Anbieter gebündelt darstellen lassen. Getrieben wird der Bereich auch mehr und mehr durch die Auswertung von Textbeiträgen in sozialen Medien (soziale Netzwerke, Blogs und Foren), um für den Anwendungsfall Social Media Monitoring Stimmungen und Diskussionen erfassen zu können.
 
Die maschinelle Auswertung von natürlicher Sprache hat dabei in der Forschung eine längere Tradition als viele vermuten. Wichtige Grundlagen des Feldes gehen auf Arbeiten in den 1940er und 1950er Jahren zurück. So bilden die 1956 erstmalig veröffentlichten theoretischen Überlegungen des US-amerikanischen Linguisten Noam Chomsky zur formalen Beschreibung von (natürlichen) Sprachen auch heute noch einen Grundstein der symbolischen Sprachverarbeitung – und der theoretischen Informatik. Demgegenüber versuchen etwa die Arbeiten von Claude Shannon vom Ende der 40er Jahre, Sprache mit Hilfe von statistischer Modellierung zu beschreiben.

Seitdem hat sich die maschinelle Sprachanalyse in der Wissenschaft kontinuierlich weiterentwickelt. Je nachdem, in welcher wissenschaftlichen Community die jeweiligen Forscher ihren Ursprung hatten, ist die Rede von `Computerlinguistik’, `Natural Language Processing (NLP)’ oder `Sprachtechnologie’. Diese Bereiche umfassen eine extreme Bandbreite von Technologien und Anwendungsfeldern, haben dabei aber einen klaren Fokus auf der Verarbeitung der englischen Sprache. Dementsprechend sind auch wesentlich mehr sprachspezifische Ressourcen und Modelle für Englisch als für andere Sprachen verfügbar.

Im Projekt News-Stream 3.0 ist der Partner Neofonie federführend für die Entwicklung von Textanalyse-Diensten verantwortlich. Die bisher von dem Berliner Unternehmen entwickelten Textmining-Komponenten sollen im Rahmen von News-Stream 3.0 weiterentwickelt werden. Hier wird vor allem auf eine verbesserte Verarbeitungsgeschwindigkeit für Big-Data-Anwendungsfälle sowie auf eine verbesserte Fehlertoleranz bei der Verarbeitung multimodaler Daten abgezielt.

Grundlage der Arbeiten ist [**TXT Werk**](http://www.txtwerk.de), eine von Neofonie bereitgestellte API zur Analyse deutschsprachiger Texte. Kern-Features sind die Eigennamen-Erkennung, die automatische Verschlagwortung und die Ressortklassifikation. 

Bei letzterer wird der Eingabetext anhand einer kleinen Menge von vorgegebenen allgemeinen Themenbereichen zu klassifiziert. Die Themenbereiche entsprechen dabei am ehesten Themenressorts einer Zeitung (z.B. “Kultur”). Der Auto-Tagging Service der TXT Werk API ermittelt Schlüsselwörter bzw. -phrasen, die charakteristisch für den jeweiligen Text sind. Die Kandidaten hierfür werden anhand von linguistischen Mustern identifiziert. Ausgewählt werden die Schlüsselwörter anhand verschiedener Features durch ein maschinell erlerntes Modell (Support-Vector-Machine).
Eine wichtige Klasse von referenzierenden Ausdrücken sind Datums- und Zeitangaben sowie Erwähnungen von Entitäten wie Personen, Organisationen oder Orte. Auch hier ist der Einsatz maschineller Lernverfahren (z.B. Conditional Random Fields) unabdingbar, da lexikalische Ansätze schnell an ihre Grenzen stoßen: das Wort “Kohl” in einem Text kann das Gemüse oder den Alt-Bundeskanzler zum Gegenstand haben. Zudem sind selbst große Wissensbasen wie Wikidata oder Freebase naturgemäß unvollständig; sie sind letztlich digitale Modelle der bisher bekannten Welt. Auch bei der Entitätenerkennung stellt sich das Problem der Mehrdeutigkeit. Handelt es sich bei “Peter Müller” um den deutschen Politiker oder den Ski-Fahrer? Oder wird hier ein weiterer Namensvetter erwähnt, einer, der noch nicht die Popularität erreicht hat, um in einer der Wissensbasen aufgeführt zu werden? Beim Entity Linking (auch Named Entity Disambiguation genannt) wird jeder Fundstelle eine eindeutige Ressource in der Wissensbasis zugeordnet. 

[caption id="attachment_3641" align="aligncenter" width="617"][![NLP-Komponenten und mögliche Pipelines. Die im Artikel ausführlicher behandelten Komponenten sind grün hervorgehoben.](http://newsstreamproject.org/wp-content/uploads/2015/09/Bildschirmfoto-2015-09-14-um-13.53.30.png)](https://newsstreamproject.org/wp-content/uploads/2015/09/Bildschirmfoto-2015-09-14-um-13.53.30.png) NLP-Komponenten und mögliche Pipelines. Die im Artikel ausführlicher behandelten Komponenten sind grün hervorgehoben.[/caption]

Unter [**http://labs.neofonie.de/watt**](http://labs.neofonie.de/watt/)  findet sich ein interaktives Analysewerkzeug, mit dem man sich auch einen praktischen Eindruck der semantischen Textanalyse mit TXT Werk verschaffen kann. Hintergrundinformationen zum Thema finden sich im [**Neofonie-Blog**](http://blog.neofonie.de/2015/06/10/semantische-textanalyse-fuer-deutsche-texte/).

Wollen Sie mehr erfahren? Werden Sie jetzt News-Stream 3.0 Beta-Tester **[http://bit.ly/newsstreambetatester](http://bit.ly/newsstreambetatester)**
