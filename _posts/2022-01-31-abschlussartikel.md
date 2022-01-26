---
title: "Abschlussartikel"
date: 2022-01-31
---
_Liebes Tagebuch_,
   


**Abschlussartikel**

Zuerst hatte ich Angst vor diesem Modul. Weil ich schlechte Erfahrungen mit dem Terminal gemacht habe beim Modul Aris, wo wir das letzte Mal mit dem Terminal gearbeitet haben.
Zum Glück war aber das Modul nicht so schlimm und es gab viel Hilfestellunge und die Befehler waren alle fein säuberlich notiert und funktionierten grösstenteils.

Ich habe sogar ein paar Erfolgserlebnisse gehabt beim Installieren der Programme (Archive Space, VuFind).


**Was habe ich gelernt?**
Ich habe gelernt, Befehle im Terminal einzugeben, meist mit Copy/Paste. Ich verstehe die Befehle auch und was sie tun.
Ich habe diverse Programme kennengelernt  und wie diese angewendet und installiert werden mithilfe dem Terminal.
Das waren die Programme: Koha, VuFind, Archive Space, Open Refine. Bei DSpace haben wir nur eine Demoversion genomme, ohne Installation.
Suchindexe wie SolR von VUFind.
Ich habe Praxiseinblicke bekommen von SLSP/Alma.
Ich habe Query-Anfragen im Wikidata Query kennengelernt und teils angewendet. Query Builder habe ich ausprobiert.
Ich habe auch gelernt, wie man Config-Dateien konvertiert bei der Übung im VuFind und dann im Browser, die veränderten Suchergebnisse gesehen und diese getestet.
Das hat mir sogar viel Spass gemacht das Konvertieren und die Suchmaske damit zu verändern!
Das ganze Vorgehen (siehe Schaubild), über die 9 Tage verteilt wurden auch im Katalog von Marbach angewendet. Es ist also nahe an der Praxis, was wir gemacht haben in diesem Modul.
Die ganzen Formate (Marc 21, Marc XML, EAD, BibFrame, Dublin Core) wurden nochmals aufgefrischt und man sah dann auch die Unterschiede in der praktischen Anwendung.
Wir konnten eigene Datensätze in Koha, Archive Space, DSpace anlegen und diese dann auch wieder über die Schnittstelle Ernten ="Harvesten" im VUFind, dass war die finale Übung.




**Was habe ich nicht gelernt?**
Ich habe keine Programmiersprache gelernt, was ich auch sehr froh darüber bin.




**AHA-Momente meine Zusammenfassung**:

**Tag 1:** Die Grafik machte zuerst gar kein Sinn für mich, mit den Erklärungen der Dozenten, erschien es dann logischer, was wir machen in diesem Modul.
![image](https://user-images.githubusercontent.com/90834735/133661233-4f8b2d76-36a1-4f85-88d5-3cbce8b3bcc0.png)
Im Terminal habe ich die Basis-Befehle aufgefrischt.

**Tag 2**: Mein Aha-Moment war am Tag 2,als ich Koha installiert hatte und dann eine eigenen Bibliothek mit Ausleihsystem, Benutzer, Suchfunktionen, Ablauffristen eröffnen konnte unter: http://bibliothek-intra.meine-schule.org/cgi-bin/koha/mainpage.pl

**Tag 3**: Beim Tag 3 war sicher interessant zu erfahren, dass alles über die Schnittstelle OAHI-PMH lief. Diese mussten wir für das Bibliothekssystem KOHA aktivieren. Damit gelang es dann die Katalogisate zu übernehmen. So gelingt eben eine Aggegration der Datensätze, und man muss diese so quasi nur einmal eintippen, danach kann man diese übernehmen. (Schnittstelle wurde abgerufen über die Baiss url: <http://bibliothek.meine-schule.org/cgi-bin/koha/oai.pl)


**Tag 4**: Da gab es eine Hausaufgabe, Archive Space zu installieren, das funktionierte zum Glück problemlos über die Befehle im Terminal und wurde dann über localhost 8080 (Admin-Oberfläche und 8081  (Benutzer-Oberlfäche), 8082 (OAHI-PHM Schnittstelle-Oberfläche )aufgerufen. Mein AHA-Moment war, dass noch kein Repository drin war, darum die Seite leer angezeigt wurde.
ISAD (G) wurde nochmals aufgefrischt, weil das das zentrale System hinter den Archivprogrammen wie Archive Space ist.
Beim Archive Space war mein AHA-Erlerbnis, beim Export. Ist der Export von Marc 21 in EAD verlustfrei?. Marc 21 ist nicht verlustfrei in Archivsystemen, weil es eben für Bibliotheken gemacht wurde, es ist ein Format für Bibliotheken und nicht für Archive. Darum fallen auch ein paar Marc 21-Formate dann beim Export in EAD raus!
Beim Gastreferat zu ALMA und SLSP waren meine AHA-Momente, dass eben alle Katalogisate über diese Gemeinschaftszone einfach übernommen werden können, ohne dass jede einzelen IZ (Bibliothek) E-Medien selbst katalogisieren muss. Nur Printmedien werden noch selber katalogisiert, vom ersten Anwender, der diese eingekauft hat, dann werden die Daten auch übernommen von anderen Bibliotheken (Fremddatenübernahme).


**Tag 5**: Es gibt einen goldigen Weg und einen grünen Weg eben mit z.B. DSpace wissenschaftliche Publikationen zu veröffentlichen. Open Data und Open Access wurde erklärt. DSpace wurde in der Demoversion ausprobiert. Ich konnte meine eigene Publikation veröffentlichen. Diese wurde dann aber nach eine Tag wieder gelöscht, weil es nur in der Demoversion gemacht wurde.

**Tag 6**:  Wir haben die Formate und ihre Programme zugeordnet. Für Bibliotheksprogramme gilt Marc 21. Für Archivprogramme gilt EAD . Dublin Core war bei DSpace.
Wir haben Crosswalks gemacht, das heisst Format in ein anderes Format konvertiert das geschah mit dem Programm Marc Edit, welches auch zuerst installiert werden musste.

    - EAD (Archive Spaces) –> in MARC21 ändern
    - MARC21 —>in MARC XML ändern
    - DUBLIN CORE (dspace) –>in MARC21 ändern
    - (Koha ist schon in Marc21, darum muss man dort nichts machen)

EAD für Archive MARC21 für Bibliothek. Es ist nicht so einfach EAD in MARC21 verlustfrei zu importieren, wegen den Feldern!
Als Alternative zu Crosswalks gibt es auch noch XSLT.

**Tag 7**: Das Programm Open Refine wurde installiert. Mein AHA-Moment war da, dass open refine mit wikidata- Datensätzen angereichert werden kann= Reconciliation ist der Fachbegriff dazu.  MAn könnte eigene Templates schreiben um eben Marc Felder zu füllen. Bis jetzt hatten wir autor, titel, url, issn genommen dazu musste man auch wieder die beispieldatenbank aufrufen. Das Template wurde dann als doaj-article-sample-csv. in xml-Format gespeichert. Nun galt es das selbstgemachte Template zu validieren. Bei der Validierung mit der Shell gab es wieder einen AHA-Moment, ich hätte separaten Ordner machen sollen, weil bei der späteren Validierung hat es dann einfach alle Dokumente genommen, und diese validiert. Der doaj-article-sample-csv.xml hat die Validierung funktioniert, bei den anderen downloads, die im selben Ordern Downloads waren, hat die Validierug nicht geklappt. Weil ein Dokument war ja von Archive space in Ead- Format, das gibt’s im marc21 nicht dann gibt es eine Fehlermeldung in der SHELL, wegen der Validierung. Weil bei der Validierung hat es den Standard das Schema Marc21 aus dem loc.gov mit der doaj-articel-sample-csv.xml verglichen.AHA-Moment: So kann man prüfen ob es dem Schema marc21 entspricht, hatten wir im gset sonst immer mit einem Validierungs-tool im Browser gemacht, das war neu für mich, dass man mit dem Terminal auch validieren kann.

**Tag 8**: Hausaufgabe war es das Suchprogramm VuFind  zu installieren. Dazu musste man auch noch Maria DB (eine Datenbank) installieren. Leider klappte die Installation von VUFind nicht auf Anhieb. Dank dem Hinweis von Hr. Lohmeier, dass ich meine Shell updaten soll, das heisst die Paktetverzeichnisse in der Shell updaten soll mit dem Befehl *sudo apt get-update* das  half bei mir tatsächlich. 

Meine weiteren AHA-Moment bei der Suchmaschine VUFInd: In den Config-Dateien das (;)Semikolon davor setzen und die nicht benötigten Suchtherme verschwinden! oder das - Minus davor setzen und ein Stern*, dann gibt es einen Kasten zum anhäkeln. Ich habe auch die Suche geändert von 20 auf 40 und auch die Anpassung der Facetten, auch die Sidebar habe ich verändert gemäss Demian Katz Empfehlungen. Auch eine Checkboox habe ich erstellt. Die Konfiguration der Config-Dateien (searches.ini, facetes.ini ) machte mir sehr Spass, weil ich direkt schauen konnte, was sich im VUFInd verändert hatte bei der Suche (Oberfläche im Browser)!

**Tag 9**:AHA-Moment: Alles war wir im Modul kennengelernt haben, haben sie in der Praxis auch angewendet am Beispiel von dem deutschen Literaturarchiv dem Marbacher Katalog https://www.dla-marbach.de/katalog/!
Open Refine wurde installiert. Beim Open Refine gibt es viele Identifier. Open Refine ist eben gut, um Reconciliation (Fachbegriff für Datenanreicherung) zu machen mit Wikidata. Wikidata ist fast besser als die GND (Gemeinsame Normadatei), weil eben viele Identifier und Contributor (Mitwirkende) hat, sogar Wikidata Japan gibt es. Ein weiterer AHA-Moment: Urheberrechtsfreie Bilder gibt’s auch auf Wikidata, weil laufen unter Creative Common Lizenz Das konnte auch im Katalog von Marbach dann eingefügt werden, weil kein Urheberschutz drauf war (Schiller haben sie z.B. ein Bild aus Wikidata genommen).

So das war mein Abschlussartikel, der alles nochmals zusammenfasste.


Vielen Dank für die geduldigen Dozenten.

Tschau liebes Tagebuch!


