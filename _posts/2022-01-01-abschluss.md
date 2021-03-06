---
title: "Abschlussartikel"
date: 2022-01-01
---
_Liebes Tagebuch_,
   
**Abschlussartikel**

Zuerst hatte ich Angst vor diesem Modul aufgrund schlechter Erfahrungen mit dem Terminal. Zum Glück war aber das Modul nicht so schlimm und es gab viel Hilfestellung und die Befehle für das Terminal waren alle fein säuberlich notiert und funktionierten.
Ich habe sogar ein paar Erfolgserlebnisse gehabt beim Installieren und Ausprobieren der Programme (Koha, Archive Space, VuFind). Am meisten Spass hat mir das Konfigurieren von VuFind gemacht.Was habe ich nicht gelernt? Ich habe keine Programmiersprache gelernt, was ich auch sehr froh darüber bin.

**Meine AHA-Momente zusammengefasst**:
**Tag 1**: Im Terminal habe ich die Befehle aufgefrischt. Die Grafik machte zuerst keinen Sinn für mich, mit den Erklärungen der Dozenten, erschien es dann logischer, was wir machen in diesem Modul.

**Tag 2**: Mein Aha-Moment war am Tag 2, als ich Koha installiert hatte und dann eine eigene Bibliothek mit Ausleihsystem, Benutzer, Suchfunktionen, Ablauffristen eröffnen konnte unter [eigene Bibliothek](http://bibliothek-intra.meine-schule.org/cgi-bin/koha/mainpage.pl).

**Tag 3**: Es war interessant zu erfahren, dass alles über die Schnittstelle OAHI-PMH lief.Diese mussten wir für das Bibliothekssystem KOHA aktivieren. Damit gelang es dann die Katalogisate zu übernehmen. So gelingt eben eine Aggregation der Datensätze, und man muss diese so quasi nur einmal eintippen, danach kann man diese übernehmen. (Schnittstelle wurde abgerufen über die [Basis url](http://bibliothek.meine-schule.org/cgi-bin/koha/oai.pl))

**Tag 4**: Da gab es eine Hausaufgabe, Archive Space zu installieren, das funktionierte zum Glück problemlos über die Befehle im Terminal und wurde dann über localhost 8080 (Admin-Oberfläche) und 8081 (Benutzer-Oberfläche), 8082 (OAHI-PHM Schnittstelle-Oberfläche )aufgerufen. Mein AHA-Moment war, dass noch kein Repository drin war, darum die Seite leer angezeigt wurde. ISAD (G) wurde nochmals aufgefrischt, weil das das zentrale System hinter den Archivprogrammen wie Archive Space ist. Beim Archive Space war mein AHA- Erlebnis, beim Export. Ist der Export von Marc 21 in EAD verlustfrei?. Marc 21 ist nicht verlustfrei in Archivsystemen, weil es eben für Bibliotheken gemacht wurde, es ist ein Format für Bibliotheken und nicht für Archive. Darum fallen auch ein paar Marc 21-Formate dann beim Export in EAD raus! Beim Gastreferat zu ALMA und SLSP waren meine AHA-Momente, dass eben alle Katalogisate über diese Gemeinschaftszone einfach übernommen werden können, ohne dass jede einzelen IZ (Bibliothek) E-Medien selbst katalogisieren muss. Nur Printmedien werden noch selber katalogisiert, vom ersten Anwender, der diese eingekauft hat, dann werden die Daten auch übernommen von anderen Bibliotheken (Fremddatenübernahme).

**Tag 5**: Es gibt einen goldigen Weg und einen grünen Weg eben mit z.B. DSpace wissenschaftliche Publikationen zu veröffentlichen. Open Data und Open Access wurde erklärt. DSpace wurde in der Demoversion ausprobiert. Ich konnte meine eigene Publikation veröffentlichen. Diese wurde dann aber nach eine Tag wieder gelöscht, weil es nur in der Demoversion gemacht wurde.

**Tag 6**: Wir haben die Formate und ihre Programme zugeordnet. Für Bibliotheksprogramme gilt Marc 21. Für Archivprogramme gilt EAD . Dublin Core war bei DSpace. Wir haben Crosswalks gemacht, das heisst Format in ein anderes Format konvertiert das geschah mit dem Programm Marc Edit, welches auch zuerst installiert werden musste.
- EAD (Archive Spaces) –> in MARC21 ändern
- MARC21 —>in MARC XML ändern
- DUBLIN CORE (dspace) –>in MARC21 ändern
- (Koha ist schon in Marc21, daher nichts ändern)
EAD für Archive MARC21 für Bibliothek. Es ist nicht so einfach EAD in MARC21 verlustfrei zu importieren, wegen den Feldern! Als Alternative zu Crosswalks gibt es auch noch XSLT.

**Tag 7**: Das Programm Open Refine wurde installiert. Mein AHA-Moment war da, dass Open Refine mit wikidata- Datensätzen angereichert werden kann, Reconciliation ist der Fachbegriff dazu. Man könnte eigene Templates schreiben, um eben Marc Felder zu füllen. Bis jetzt hatten wir autor, titel, url, issn genommen, es wurde ein Beispiel für das Hinzufügen der DOI gmacht, dazu musste man auch wieder die Beispieldatenbank aufrufen. Das Template wurde dann als doaj-article-sample-csv. in xml-Format gespeichert. Nun galt es das selbstgemachte Template zu validieren. Bei der Validierung mit der Shell, hätte ich einen separaten Ordner machen sollen, weil es dann einfach alle Dokumente genommen, und diese validiert. Der doaj-article-sample-csv.xml hat die Validierung funktioniert, bei den anderen Downloads, die im selben Order waren, hat die Validierung nicht geklappt. Weil ein Dokument war ja von Archive Space in Ead- Format, das gibt’s im marc21 nicht dann gibt es eine Fehlermeldung in der SHELL. Weil bei der Validierung hat es den Standard das Schema Marc21 aus dem loc.gov mit der doaj-articel-sample-csv.xml verglichen.So kann man prüfen ob es dem Schema marc21 entspricht, hatten wir im gset sonst immer mit einem Validierungs-tool im Browser gemacht, das war neu für mich, dass man mit dem Terminal auch validieren kann.

**Tag 8**: Hausaufgabe war es das Suchprogramm VuFind zu installieren. Hinter VUFind steckt der Suchindex Solr. Solr steckt auch hinter Primo und vielen weiteren Suchmaschinen. Neben VUFind musste man auch noch Maria DB (Datenbank), wie wir es schon bei Koha gemacht haben,  installieren. Leider klappte die Installation von VUFind nicht auf Anhieb. Dank dem Hinweis von Hr. Lohmeier, dass ich meine Shell updaten soll, das heisst die Paketverzeichnisse. Der Befehl sudo apt get-update half bei mir tatsächlich. Bei der Suchmaschine VUFInd: In den Config-Dateien das (;)Semikolon davor setzen und die nicht benötigten Suchtherme verschwinden! oder das - Minus davor setzen und ein Stern*, dann gibt es einen Kasten zum anhäkeln. Ich habe auch die Suche geändert von 20 auf 40 und auch die Anpassung der Facetten, auch die Sidebar habe ich verändert gemäss Demian Katz’s Empfehlungen. Auch eine Checkbox habe ich erstellt. Die Konfiguration der Config-Dateien (searches.ini, facetes.ini ) machte mir sehr Spass, weil ich direkt schauen konnte, was sich im VUFind verändert wurde bei der Suche (Oberfläche im Browser=Discovery)!

**Datenintegration**: Ziel des Kurses war ja der Import der Marc Edit mit Open Refine konvertierete Daten aus Koha, Archive Space, Dpsace und DOAJ mithilfe von VUFind. Das geschah dann auch. Zuerst mussten wir die Testdaten löschen diese 250 Dateien.Jetzt haben wir wieder einen leeren Index. Ich habe nicht meine eigenen gesammelten Daten von Koha, ArchiveSpace, doja und Dspace genommen, sondern die empfohlenen Beispieldaten, welche dann als Ordner Koha, ArchiveSpace, DOJA, Dspace heruntergeladen werden konnten. Die Daten von DSpace in Marc XML, Kohar war schon in Marc XML. Dann mit dem Befehl gedit /usr/local/vufind/import/marc_local.properties kam man auf die Marc Properties- Config-Datei. Das war im Editor, dort musste man die Raute wegnehmen, dann muss koha, dpace, archivespace, doaj jedes mal da einfügen bei der collection.Danach mit dem Befehl for f in ~/Downloads/koha/.xml; do /usr/local/vufind/import-marc.sh $f; done konnte ich die gesammelten Beispieldaten aus koha, dpace, archivespace, Doaj raufladen ins VuFind.
Wir haben alle 11 Resultate bekommen aus den 4 Bib- und Archivsystemen:
-Archive Space hat nicht funktioniert
-Koha hat funktioniert
-Doaj hat funktioniert
-DSpace hat nicht funktioniert.

**Tag 9**: Alles war wir im Modul kennengelernt haben, haben sie in der Praxis auch angewendet am Beispiel von dem deutschen Literaturarchiv dem Marbacher [Katalog](https://www.dla-marbach.de/katalog/). Open Refine wurde wieder aufgerufen.Beim Open Refine gibt es viele Identifier. Open Refine ist eben gut, um Reconciliation (Fachbegriff für Datenanreicherung) zu machen mit Wikidata. Es ist fast besser als die GND (Gemeinsame Normdatei), weil eben viele Identifier und Contributor (Mitwirkende) hat, sogar Wikidata Japan gibt es. Urheberrechtsfreie Bilder gibt’s auch auf Wikidata, weil laufen unter Creative Common Lizenz Das konnte auch im Katalog von Marbach dann eingefügt werden, weil kein Urheberschutz drauf war (Schiller Porträt).

So das war mein Abschlussartikel. Vielen Dank für die geduldigen Dozenten.

Tschau liebes Tagebuch!


