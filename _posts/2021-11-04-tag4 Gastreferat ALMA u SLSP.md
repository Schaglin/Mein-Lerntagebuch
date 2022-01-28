---
title: "Tag 4 Gastreferat zu Alma und SLSP"
date: 2021-11-04

---


**_Liebes Tagebuch_**


Durch die SLSP (Swiss Library Service Plattform) wurde die Einführung von Alma im Dezember 2020 gemacht. Es bildet die Grundlage für das Swisscovery, ist nicht gewinnorientiert. Darunter sind 475 Bibliotheken vertreten mit 50 Mio. Medien. 


**ALMA - das Cloudgestützte Bibliothekssystem von Ex-Libris**
Alma wird betreut durch Ex-Libris mit monatlichen Releases. Cool ist, dass die einzelnen Institutionen ebenfalls eine Mitsprache-Recht haben durch die Idea Exchange Plattform, können sie ihre Ideen anbringen zur Verbesserung von Alma. Es ist ein URM (Infified Resource Management System). Alma hat ein ERM (Elektronische Ressourcenverwaltung), einen Link-Resolver, eine Verwaltung der digitalen Bestände, ein ILS (integriertes  Bibliothekssystem) und für das Discovery (für die Benutzer) gibt es das Primo, wird von Alma verwaltet.


**_ALMA Topologie_**

**Gemeinschaftszone**
Hier werden die E-Ressourcen, Normdaten verwaltet und hier findet sich auch die ALMA-Community.
In der Gemeinschaftszone können alle Metadaten für die Katalogisierung übernommen werden.

**Netzwerkzone**
In der Netzwerkzone werden die einzelnen Titel der Werke/E-Medien aufgenommen und es finden sich die Lizenzen (Konsortiallizenzen). Hier sind alle SLSP- Bibliotheken unter einem Dach.

**Institutionszone (IZ)**
Hier kann man für die einzelnen Bibliotheken indiviuell anpassen z. B. Aktivierungen, Konfigurationen.
Bei den Bibliotheken selbst kann auf Drucker, Öffnungszeiten, Budget Anpassungen gemacht werden. Bei den Beständen können Exemplare, Signaturen hinzugefügt werden. FHNW hat kein Campus, sie nehmen alle die gleiche IP- Range.
Für E-Ressourcen muss ich mich einloggen in der IZ oder suchen,über CDI kann ich ein Journal über die Gemeinschaftszone aktivieren, dass in CDI vorhanden ist, das wird das eingespielt für die Kataloge. Jede IZ kann lokal seine eigene Ansicht haben. Damit nicht jede IZ ein eigenes View aufbauen muss, wir mit einem Master Template gearbeitet. Man kann z.B. die Farbe, Logo, eigene Texte, lokale Ressourcen oder Texte ändern. Jede IZ kann das machen individuell, aber das Grundgerüst ist von der ExLibris.
![slsp](https://user-images.githubusercontent.com/90834735/151616725-500df4e7-1021-461d-9d44-8537a737dc23.png)




**Primo= Discovery-Lösung von Exlibris, wird über Alma verwaltet**
Der Vorteil ist, es wird nicht noch ein System für Verwaltung benötigt. Auch ein Vorteil für Benutzer, wenn beim E-book etwas ändere, dann dauert es 2-3 Minuten und es ist sichtbar. 


**1. LIVE-Demo**:
- **Aufbau und die Grundlagen**. Für die Recherche in Alma: Jede IZ ( IZ= Institutionszone) hat eigene URL um ALMA über Browser aufzurufen. Suche alle physischen Exemplare mit dem Status "vermisst", einschränken nur Bibliothek FHNW. Als Discovery anzeigen lassen.
Zum Aufbau und den Grundlagen gehören auch die Ausleihe und Rückgabe. Pro Benutzer kann eingesehen werden: Bestellung, Mahnen, Rechnung, Kaufbestellung, Lieferanten, Konto bearbeiten. Es gibt auch Vormerkungen, Exemplare Scannen, abgelaufene Bestellungen, Exemplar Prozesse, Strichcode lesen.
Beim Buch ausleihen, muss aber in Theke von FHNW Windisch einloggen, erst dann kann man es machen.

- **E-Ressourcen**: Bei E-Ressourcen sind Lizenzen drin, sogenannte Konsortiumlizenzen.Diese können auch im Detail überwacht werden mit Nutzungsbedingungen z. B. Fernleihe, Download erlaubt oder nicht.

- **Erschliessung**: läuft über Ex-Libris-Masterpaket, kann aber auch wieder konfiguriert werden auf IZ-Ebene für die einzelne Bibliothek.
 
- **AHA**!: Die meisten Konfigurationen (z.B Erwerbung, Erschliessung, Lizenzen, Regeln für Rechnungsprüfung, Leihfristen mit Öffnungszeiten verknüpft) werden auf der IZ -Ebene gemacht. Auch die Primo- Ansicht (Discovery) für die Kunden wird auf der Konfiguration lokal verändert z.B. Farbe, Links.


**Theke 1** kann Rückgabe, Neuberechtigungen, kann für studentische Hilfskräfte Berechtigungen reduzieren. Zahlungsinfo hat es keine, weil keine Kasse an dieser Theke 1 haben. Auch welcher Drucker soll Zugriff haben, kann hier definiert werden. RFID ist auch hinterlegt.


**Hilfeseite, Homepage , Link kann noch individuell angepasst werden**
Einzelne Links kann man anpassen für Homepage der eigenen IZ. und dann diese hochladen. Aber z. B.keine Javascript, da wird alles genommen von SLSP.
Anpassungen anschauen, Test-Views zuerst machen.

- **Katalogisierung**: (geht über Gemeinschaftszone=GZ)
**AHA-Moment** Es werden alle Katalogisate über diese GZ übernommen, ohne dass jede einzelne IZ (Bibliothek) E-Medien selbst katalogisieren muss. Nur Printmedien werden noch selber katalogisiert, vom ersten Anwender, der diese eingekauft hat. Dann werden die Daten auch übernommen von anderen Bibliotheken(Fremddatenübernahme). Die E-Ressourcen seien über WorldCat oder Library of Congress nur für spezifische Institution zugänglich.

Aus der Fragerunde erfuhr ich, dass alles in Marc-21 Format ist, und sich BibFrame noch nicht durchgesetzt. Es wird aber vermutet, dass BibFrame im Hintergrund schon läuft, aber da Alma noch drin ist, ist es noch in Marc21.

**Metadateneditor**
Man katalogisiert immer noch über RDA im Vergleich zu Aleph ist das noch gleich. Aber Felder sind anders aber mit Dollar und Buchstaben = Marc21. Man sehe aber Vorlagen, Warnungen. Es kann direkt ein neuer Bestand erstellt werden.

**2. Live- Demo:**
Wie man ein E-Book, eine Zeitschrift anlegen kann. Das geht alles über die Netwerkzone, die man aktivieren muss.


**Datenbanken**
Es gibt Volltext, keinen Volltext, Referenzdatenbanken.
ABI ist ein Aggregator Datenbank, beinhaltet Portfolios, Volltext-Datenbank kann man im Primo absuchen. Journals kann  via Swisscovery gesucht werden.
"**CDI**:ist integriert= Detail-Suche.Wenn es ein E-Journal ist, können ihre einzelne Artikel über CDI gesucht werden.*z.B. Naxos Music Library = Referenzdatenbank, hat keine Portfolio, hat aber auch CDI für detailierte Suche, aber dieser Datenbank ist so auf Discovery auffindbar.



Tschau, liebes Tagebuch!



