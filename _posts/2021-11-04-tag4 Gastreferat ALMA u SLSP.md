---
title: "Tag 4 Gastreferat zu Alma und SLSP"
date: 2021-11-04

---


**Liebes Tagebuch**


Wir hatten heute ein Gastreferat von der FHNW in Windisch. Die Systembibliothekarin (Selina Hodel) hat uns die Grundlagen von Alma erklärt und präsentiert mit einer Live-Demo und Beispielen. Die Leiterin der E-Ressourcen (Charlotte Frauchlinger) hat den gesamten Aufbau der SLSP (Swiss Library Service Plattform) und deren Entwicklung erklärt. Dann gabe es noch "strategische Spielereien" und Fragen wurden geklärt.

**SLSP- Swiss Library Service Plattform**
Die Idee kam 2014, danach im 2017 erfolgte die Umsetzung,im Jahr 2020 konnte SLSP eingesetzt werden. Durch die SLSP wurde die Einführung von Alma im Dezember 2020 gemacht. Es ist ein nicht-gewinnorientieres Unternehmen. Es bildet die Grundlage für das Swisscovery. Darunter sind 475 Mitgliederbibliotheken vertreten mit 50 Mio Medien. 


**ALMA - das Cloudgestützte Bibliothekssystem von Ex-Libris**
Das Rechenzentrum liegt in Amsterdam. Alma wird betreut durch Ex-Libris. Das heisst, es gibt monatliche Releases von Ex-Libris. Cool ist, dass die einzelnen Institutionen ebenfalls eine Mitsprache- Recht haben durch die Idea Exchange Plattform, können sie ihre Ideen und Vorschläge anbringen zur Verbesserung von Alma. Es ist ein URM (Infified Resource Management System). Alma hat ein ERM (Elektronische Ressourcenverwaltung), einen Link-Resolver, eine Verwaltung der digitalen Bestände, ein ILS (integriertes  Bibliothekssystem) und für das Discovery (also für die Benutzer) gibt es das Primo. Das Primo wird über Alma verwaltet.

Im Alma wurde uns gezeigt: Grundaufbau, Suche, E-Ressourcen über Gemeinschaftszone, Verwaltung der Bibliotheken, Beispiel von übergreifender Bibliothek.


![grafik](https://user-images.githubusercontent.com/90834735/140959464-6b462add-cd3a-4309-879c-ce573bc0c1d1.png)

**_ALMA Topologie_**

**Gemeinschaftszone**
Hier werden die E-Ressourcen, Normdaten verwaltet und hier findet sich auch die ALMA-Community.
In der Gemeinschaftszone können alle Metadaten für die Katalogisierung übernommen werden.

**Netzwerkzone**
In der Netzwerkzone werden die einzelnen TItel der Werke/E-Medien aufgenommen und es finden sich die Lizenzen (Konsortiallizenzen). Hier sind alle SLSP- Bibliotheken unter einem Dach.

**Institutionszone (IZ)**
Hier kann man für die einzelnen Bibliotheken indiviuell anpassen z. B. Aktivierungen, Konfigurationen.
Bei den Bibliotheken selbst kann auf Drucker, Öffnungszeiten, Budget Anpassungen gemacht werden. Bei den Beständen können Exemplare, Signaturen hinzugefügt werden. Man könnte hier auch einen Campus machen, FHNW hat das aber nicht, sie nehmen alle die gleiche IP- Range.
Für E-Ressourcen muss ich mich einloggen in der IZ oder suchen,über CDI kann ich ein Journal über die Gemeinschaftszone aktivieren, dass in CDI vorhanden ist, das wird das eingespielt für die Kataloge. Jede IZ kann lokal seine eigene Ansicht haben. Damit nicht jede IZ ein eigenes View aufbauen muss, wir mit einem Master Template gearbeitet. Man kann z.B. die Farbe, Logo, eigene Texte, lokale Ressourcen oder Texte ändern. Jede IZ kann das machen individuell, aber das Grundgerüst ist von der ExLibris vorgegeben.


![grafik](https://user-images.githubusercontent.com/90834735/140961441-0b06b854-a620-4608-b94f-894bd1df0fb9.png)

**Primo= Discovery-Lösung von Exlibris, wird über Alma verwaltet**
Der Vorteil ist, es wird nicht noch ein System für Verwaltung benötigt. Auch ein Vorteil für Benutzer, wenn beim E-book etwas ändere, dann dauert es 2-3 Minuten und es ist dann wieder sichtbar. 


Es gab eine **LIVE-Demo** über:
- **Aufbau und die Grundlagen**. Für die Recherche in Alma: Jede IZ ( IZ= Institutionszone) hat eigene URL um ALMA über Browser aufzurufen. Suche alle physischen Exemplare mit dem Status "vermisst". Dann diese noch einschränken nur Bibliothek FHNW. Als Discovery anzeigen lassen.

Zum Aufbau und den Grundlagen gehören:
- Ausleihe und Rückgabe: Buch ausleihen, muss aber in Theke von FHNW Windisch einloggen, erst dann kann man es machen.
- Kategorien: Ausleihen und Rückgabe, Vormerkungen, Listeraturlisten sind da drin.
- Bei den Ausleihen sind Benutzerkonfiguration, Mahnungen, Offline Ausleihe hinterlegt. 
- Vormerkungen: Aus dem Regal nehmen, Exemplare Scannen, Abgelaufene Bestellungen, Exemplar-Prozesse überwachen. Strichcode einlesen, Vormerkung, Rückgabe machen.
- Pro Benutzer: Bestellung, Mahnen, Rechnung, Kaufbestellung, Lieferanten bearbeiten, Kontos bearbeiten.

- **E-Ressourcen**: Bei E-Ressourcen sind Lizenzen drin, sogenannte Konsortiumlizenzen.Diese können auch im Detail berwacht werden mit Nutzungsbedingungen z. B. Fernleihe, Download erlaubt oder nicht.
- Benutzerverwaltung: Hier gibt es Rollenvorlagen für Mitarbeiter z.b Admin Berechtigung ohne Rollen separat zu verteilen.

- **Erschliessung**
Das Zentrale Paket ist das Masterpaket als Grundlage für alle Bibliotheken, durch kundenspezifisches Paket können noch Anpassungen gemacht werden. Aber man kann Konfigurationen machen für einzelne IZ oder Bibliothek.

- **Konfiguration**: Pro Bibliothek kann man auf der Bibliotheksebene (IZ) einstellen, Drucker, Öffnungszeiten etc. Die Öffnungszeiten sind mit den Leihfristen verknüpft. Die FHN will zum Beispiel keine Leihfristen auf den Samstag festlegen, obwohl die Bibliothek am Samstag offen ist. Oder Weihnachtsferien, da sollen die Fristen nicht weiterlaufen, sondern erst wieder ab dem 1.1.
- **AHA-Moment: Die meisten Konfiguration (z.B Erwerbung, Lizenzen, Regeln für Rechnungsprüfung) werden auf der IZ -Ebene gemacht:**
- **auch die Primo- Ansicht (Discovery) für die Kunden wird auf der Konfiguration lokal verändert:
- Discovery ist gelb, das ist typisch für die FHWN und auch die Texte sind lokal angepasst worden.
- Verlinken auf  E-Ressourcen der FHWN 
- Weitere Konfigurationen: Registerkarten, Timeout, Standardsprache, Statisitk, Suche, Medadaten, Konfiguration der Briefe. z.B. ein Ausleihbeleg** -   Sprache kann man auch anpassen. Der Brief wird als xml-File so definiert. Es gibt auch eine Vorschau.

Auch eine Liste der **physischen Standorte** für die gedruckten Medien pro Bibliothek kann hier gefunden werden: Jeder Standort hat einen Code, einen Namen, Typ etc. Welche Leihstelle dieser Standort verwaltet.
Zum Beispiel der Book-Return (automatische Rückgabemaschine) kann keine Wiedereinstellung vornehmen.
**Beispiel Theke 1** kann Rückgabe, Neuberechtigungen, kann für studentische Hilfskräfte Berechtigungen reduzieren. Zahlungsinfo hat es keine, weil keine Kasse an dieser Theke 1 haben. Auch welcher Drucker soll Zugriff haben, kann hier definiert werden. RFID ist auch hinterlegt.


**Hilfeseite, Homepage , Link kann noch individuell angepasst werden**
Einzelne Links kann man so anpassen für Homepage auf eigene IZ. und dann diese hochladen. Aber z. B.keine Javascript, da wird alles genommen von SLSP.
Anpassungen anschauen, Test-Views zuerst machen.



**Fragerunde**
**AHA-Moment**: Es werden also alle Katalogisate über diese Gemeinschaftszone einfach übernommen, ohne dass jede einzelen IZ (Bibliothek) E-Medien selbst katalogisieren muss. Nur Printmedien werden noch selber katalogisiert, vom ersten Anwender, der diese eingekauft hat, dann werden die Daten auch übernommen von anderen Bibliotheken(Fremddatenübernahme).Aus der Fragerunde war  zu vernehmen, dass alles noch in Marc-21 Format ist, und BibFrame noch nicht durchgesetzt. Es wird aber vermutet, dass BibFrame im Hintergrund schon läuft, aber da Alma noch drin ist, ist es noch in Marc21-Format.


- **Katalogisierung**: (geht über Gemeinschaftszone)
- Katalogisierung auf der Netzwerkzone (printbestände)
- e-Ressourcen nur für spezifische Institution zugänglich
- von WorldCat oder Library of Congress das übernehmen
**Aber printmedien werden immer noch von Bibliotheken selber katalogisiert, und andere Bibliotheken könne über Gemeinschaftszone übernehmen.**

**Metadateneditor**
Man katalogisiert immer noch über RDA im Vergleich zu Aleph ist das noch gleich. Aber Felder sind anders aber mit Dollar und Buchstaben. Feldinformationen von Marc 21 sieht man gleich, Warnungen, Beispiele,Vorlagen.Es kann direkt ein neuer Bestand erstellt werden.



**Live- Demo:**
Wie man ein E-Book, eine Zeitschrift anlegen kann. Das geht alles über die Netwerkzone, die man aktivieren muss.


**Beispiel Datenbanken**
Es gibt Volltext, keinen Volltext, Referenzdatenbanken.
ABI ist ein Aggregator Datenbank, beinhaltet einzelene Portfolios, Volltext-Datenbank kann man im Primo absuchen. Journals kann man via Swisscovery so suchbar machen.
"**CDI*:ist integriert. Das heisst gibt eine detailliertere Suche: _Wenn es ein E-Journal ist, können ihre einzelne Artikel über CDI gesucht werden_.*
Naxos Music Library = Referenzdatenbank, hat keine Portfolio, hat aber auch CDI für detailierte Suche, aber dieser Datenbank ist so auf Discovery auffindbar.



**Strategische Spielereien:**
Es wurden Fragen gestellt betreffend dem Mitteleinsatz (einfachere Fernleihe, monatliche Updates, Mehrwehrt für Nutzer), Performance im Arbeitsbetrieb (gute Internetverbindung), Motivation und Kommunikation der beteiligten Bibliotheken (alle Bibliotheken ins Boot holen, informieren), wie man den Change begleiten könnte (z.B. Schulungen).  Welche  Vor- und Nachteile es gibt bei einem cloudbasierten System wie bei ALMA. Was für Alternativen es gibt, z.b. Koha (Open-Source-Lösung).
Und die Konfigurationsmöglichkeiten wurden beurteilt, dass eben Individualisierung möglich ist, aber bei SLSP viel über diese Gesamt-IZ läuft.

Tschau, liebes Tagebuch!



