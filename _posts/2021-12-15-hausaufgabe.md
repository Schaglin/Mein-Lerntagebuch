Hausaufgabe war es das Suchprogramm VuFind für Bibliotheken von Bibliotheken zu installieren. 

Dazu bekamen wir wieder einen Satz von Shell-Befehlen zur Verfügung, diese konnte man einfach copy/pasten:
**wget https://github.com/vufind-org/vufind/releases/download/v8.0.2/vufind_8.0.2.deb
sudo dpkg -i vufind_8.0.2.deb
sudo apt-get update   -(Nachtrag vom 14.12.21, dank diesem Befehl hat es bei mir dann tatsächlich funktioniert- Vielen Dank dafür 🦖)
sudo apt-get install -f**

Maria DB mussten wir auch installieren mit Befehl:
***sudo /usr/bin/mysql_secure_installation**
mussten wir ein neues Passwort festlegen, Maria DB ist = My Sql 
hierbei mussten wir noch einige Angaben mit y (yes) bestätigen.
dann für den Root das Passwort bestätigen:**sudo mysql -uroot -p -e "UPDATE mysql.user SET plugin='' WHERE User='root'; FLUSH PRIVILEGES;"**
Ein Neustart war in unserem Fall nicht erforderlich. Es reichte aus, den genannten Befehl einzugeben:**source /etc/profile**
Um das SOlr zu starten mussten wir vorher noch Dateirechte festlegen fürdas Cache- und das Config-Verzeichnis beim Account des Webservers (www-data).
**sudo chown -R $USER:$GROUP /usr/local/vufind
sudo chown -R www-data:www-data /usr/local/vufind/local/cache
sudo chown -R www-data:www-data /usr/local/vufind/local/config**
dann konnten wird das Solr starten und VuFind Konfigurieren mit Befehl:**/usr/local/vufind/solr.sh start**
Da wir keinen Domainnamen haben. Verwendeten wir localhost. Nun konnte ich den Browser in der virtuellen Maschine (Linux) mit folgender Adresse aufrufen:
http://localhost/vufind/Install/Home
Jetzt sollte VuFind bereits aufrufbar sein, und die Auto-Konfigurationen sollten sichtbar sein.
Leider hatte ich nur eine leere Seite mit. Browser nicht findbar.

so versuchte ich dann die vorgeschlagene Fehlerbehebung Nr. 1, weil es mir das VUFind im Browser gar nicht angezeigt hatte:
Fehlerbehebung

Falls etwas schief geht, können die folgenden Befehle helfen die Installation teilweise oder ganz zurückzusetzen.
Fall 1: Auto Configuration ist nicht mehr erreichbar

    Problem: Die Seite “Auto Configuration” unter http://localhost/vufind/Install/Home war schon einmal aufrufbar, aber kann nun nicht mehr geladen werden.

    Ursache: Die Konfiguration ist defekt und kann von VuFind nicht mehr gelesen werden.

    Lösung:

        Die lokale Konfiguration (im Verzeichnis /usr/local/vufind/local/) manuell löschen.

        sudo rm /usr/local/vufind/local/config/vufind/config.ini

        Datenbank und Nutzer löschen (bei der folgenden Abfrage das Root-Passwort für MariaDB eingeben, das oben festgelegt wurde)

        sudo mysql -uroot -p -e "DROP DATABASE IF EXISTS vufind; DROP USER IF EXISTS vufi

**Zur Installation**:
bei mir klappte es leider nicht auf Anhieb.
Jedoch gab es dann Hilfevideos von Hr. Lohmeier, die man anschauen konnte.

**Mein AHA-Moment**: Und der Befehl: **sudo apt get-update** half bei mir tatsächlich. Der Befehl war gut um die Pakteverzeichnisse zu aktualisieren. ICh kannte den Befehl eigentlich schon 
aus dem Unterricht zu Aris im Frühling 2020, dort mussten wir oft die Verzeichnisse updaten. Jedoch ist es mir leider nicht mehr in den Sinn gekommen.
Es erscheint eine Fehlermeldung, dass noch nicht alle von VuFind benötigten Pakete installiert sind.
Zunächst aktualisieren wir das Paketverzeichnis (Nachtrag 14.12.):
Endlich hat es mir auf den Browser Port 80 nun die VuFInd Oberfläche angezeigt.

Ich hatte Freude, weil ich vorher mehrere Versuche und auch die vorgeschlagenen Fehlerbehebungen ausprobiert habe, und schon fast am verzweifeln war.

Nun war VuFind aufrufbar, zuerst erschien die Auto-Konfiguration. Welche wir auch noch anpassen (fixen)sollten.
Die Security konnte man einfach mit fix darauf klicken und es wurde repariert.
Bei der Datenbank muss ein neues Passwort vergeben sowie das zuvor oben im Abschnitt “MariaDB Passwort für root” eingegeben werden.
Wir haben kein Bibliothekssystem, daher wählen wir NoILS. Dann wird aber trotzdem noch “Failed” angezeigt und wenn wir nochmal auf “Fix” klicken erscheint die folgende Meldung:

    (…) You may need to edit the file at /usr/vufind/local/config/vufind/NoILS.ini

    Datei im Texteditor (gedit) mit Administratorrechten öffnen

sudo gedit /usr/local/vufind/local/config/vufind/NoILS.ini

    In Zeile 3 ils-offline in ils-none ändern und speichern.

Nun musste ich nur noch die Auto-Konfigurationen fixen. Das ging auch gut,mithilfe des Videos von Hr. Lohmeier.
Die schwierigste Auto-Konfiguration war wohl die, wo man in die Config-Datei selbst etwas umschreiben musste nämlich diese
vorher musst man NoiLs auswählen. Aber eigentlich wollen wir gar keine NoiLS (ist ein ILS Driver).
von **ils offline zu ils none* abändern, damit es gar keine ILS Driver nimmt:

![Screenshot from 2021-12-15 10-50-36](https://user-images.githubusercontent.com/90834735/146192793-ee89b8e2-e9f4-4771-bca4-e8d7b119ae7c.png)

demiankatz hat dazu auch ein Video gemacht zu diesen ILS Driver https://www.youtube.com/watch?v=qFbW8u9UQyM

als alles gefixt war, sah es dann so aus. Ich freute mich darüber :-).
![Screenshot from 2021-12-15 10-51-06](https://user-images.githubusercontent.com/90834735/146193562-01443fb2-7c94-4127-a593-c844d8905d92.png)



**Übung: Konfigurationen anpassen / Searching and Facet Settings**
Ein Youtube Video erklärt von demiankatz, der Meister in VuFind: https://www.youtube.com/watch?v=qFbW8u9UQyM
Wer hat eigentlich VUFind entwickelt? War das dieser demiankatz? als beim Harvester Vufind war auf jeden Fall der Daminakatz involiert, wie ich gerade in den Dateien im Editor herausgefunden habe..


Hier gab es bei mir auch einen **AHA-Moment!** Das ; Semikolon davor setzen und die nicht benötigten Suchtherme verschwinden!
oder das - Minus davor setzen und ein Stern*, dann gibt es einen Kasten zum anhäkeln. Ich versuchte es nachzumachen. ich war mir jedoch unsicher wieder.
Mit ls habe ich mal alle Verzeichnisse angeschaut, und festgestellt, dass ich 3 Versionen von VuFind daraufhabe. Das deckte sich auch mit meinen Ordnern.


Der Demiankatz war jetzt im Ordner /usr/local/vufind drin, um überhaupt dann nacher mit den Befehlen die config-Dateien abzufrufen.
Also musste ich auch in diesen Ordner kommen. Ich versuchte nun mit der Commandozeile Cd in diesen /usr/local/vufind reinzukommen.
![Screenshot from 2021-12-15 15-41-13](https://user-images.githubusercontent.com/90834735/146207073-1436cade-1843-46b4-9ad4-a9f0a178330e.png)


Gemäss Demiankatz wäre der Befehl zum ändern der Search-Config-Dateien so gewesen, leider hat es nicht funktioniert.
![Screenshot from 2021-12-15 16-07-58](https://user-images.githubusercontent.com/90834735/146213450-505b7373-8c8a-4ef9-872a-49ade46d2f1e.png)

ich versuche es weiter... ist ja Hausaufgabe...
![Screenshot from 2021-12-15 16-56-44](https://user-images.githubusercontent.com/90834735/146220478-c198ee89-eb11-471d-b84a-2614b4719fcb.png)


weiter Versuche hier, ich komme einfach nicht in das richtige Verzeichnis rein!!
application.config.php komme ich nicht rein, weil es keine directory ist. weiss nicht mal ob das das richtige verzeichnis ist.
bei demiankatz war es ganz eine andere ordnung und ich finde auch keine config dateien, bei ihm waren diese ja schon ohne befehle ersichtlich als texteditordateien oder so etwas Ähnliches.
![Screenshot from 2021-12-15 17-24-10](https://user-images.githubusercontent.com/90834735/146225086-3cb109ee-8c24-42d0-8f0b-d2fe2bc585ab.png)

über die Shell habe ich es danna ufgegeben, ich habe einen Tipp bekommen von Barbora, die auch diesen Kurs besucht. Nun versuche ich meine Glück manuell über den Ordnern zu konfigurerien.

![Screenshot from 2021-12-15 18-12-08](https://user-images.githubusercontent.com/90834735/146233490-a77c58aa-b1e9-4652-8fc7-320f9e7170cb.png)




Die vorgeschlagenen Konfigurationen von DemianKatz aus dem Video zu "Searching und  Facet Settings" habe ich einmal hier notiert.

**Beim Searching**:
- 40 Resultate anzeigen lassen, anstatt nur 20 Suchresultate
- Namen der Suchtherme ändern zum Beipsiel anstatt Autor zu "Person who created" ändern. (aber man müsse aufpassen, wenn ich Sprache ändere, sollte es automatisch auch wieder richtig übersetzen?)

nun habe ich die Anzahl von *20 auf 40 erhöht für die Suchresultate bezogen*. nun bin ich gespannt, ob es meine Änderungen genommen hat und schaue im vufind im Browser.
![Screenshot from 2021-12-15 18-24-29](https://user-images.githubusercontent.com/90834735/146235080-9ec96984-149b-44c8-90f7-610e5681d436.png)

**Meine AHA-Moment** Ja es sieht gut aus, vorher erschienen nur 20 Suchresultate und nun erscheinen tatsächlich 40 Suchresultate, die ich vorher konfiguriert habe!
![Screenshot from 2021-12-15 18-29-44](https://user-images.githubusercontent.com/90834735/146236011-f4fb85b4-7775-45d1-a0ac-ac38f10a7f99.png)

ich habe es noch mit 100 ausprobiert, ob es jetzt wirklich funktioniert hat und es hat funktioniert. das freute mich sehr !🦖
![Screenshot from 2021-12-15 18-38-12](https://user-images.githubusercontent.com/90834735/146237080-a759a9e3-9fff-4a62-9445-acfc1254bc7e.png)





- Reihenfolge ändern der Suchtherme z.b. Titel vor Autor , konnte man einfach mit copy/paste machen. nun schaue ich im vufind ob es tatsächlich geändert hat oder nicht
![Screenshot from 2021-12-15 18-43-20](https://user-images.githubusercontent.com/90834735/146238202-af949680-c7e3-46f6-92de-3a64cbd35c0c.png)

der Autor habe ich gmäss Demiankatz auch noch geändert zu "Person who created this stuff" das hat mir Spass gemacht die Verzeichnisse umzuändern, wie es mir beliebt.:-)
![Screenshot from 2021-12-15 18-48-09](https://user-images.githubusercontent.com/90834735/146239810-38f3ce84-659d-47ee-8679-4f4c228550ea.png)
ja es hat sogar geklappt!
![Screenshot from 2021-12-15 18-50-15](https://user-images.githubusercontent.com/90834735/146239027-738fce42-df6f-4ca2-9b54-6519b06d646e.png)



- OCLC Nummer hinzufügen


**Bei den Facetten**
Ich möchte nun den Instructor und die Building für die Narrow Search rausnehmen, so wie es Demiankatz vorschlägt, dazu muss ich nur die Semikolon davor setzten und das ganze wird nicht mehr grün angezeigt und somit auch in der Narrwo Search nicht mehr angezeigt.
;Institution wegnehmen, in Confi-Datei einfach das Semikolon (;)davor schreiben
;Building wegnehmen, in Config-Datei einfach das Semikolon (;) davor schreiben

**Vorher:** hier war die Institution und das Building noch bei Narrow Section drin:
![Screenshot from 2021-12-15 19-02-54](https://user-images.githubusercontent.com/90834735/146241189-7c08d2e7-cb46-477c-9d6e-f4d3ed5155fe.png)
**Nachher**: jetzt sind die Institution und das Gebäude enfernt oder deaktiviert in den Resultaten:
![Screenshot from 2021-12-15 19-03-30](https://user-images.githubusercontent.com/90834735/146241350-87d0e6cc-7b3e-4fcc-9970-c92750e432ec.png)





- Autor *no author* , ich möchte alle Suchresultate rausnehmen, die keinen Autor haben


**YAML für Advanced Searched und Homepage ändern**
für advanced searched sei das gemäss demiankatz
hier kann man sogar Checkboxen erstellen zum Beispiel: ich möchte Formate selbst auswählen durch anklicken z. b . Bücher, Zeitschriften, ...
und davon soll es 10 Formate zur Auswahl haben.
So konnte man auch die Homepage anpassen zum Beispiel Sprache ändern oder Browser by Format
**bei den searchaspects**: bei Yaml könne man auch die Wichtigkeit ändern z.b  der erste Autor ist viel wichtiger als der zweite Autor, also kann man den boosten.
er hat aus den ursprünglichen 300 dann 3000 gemacht, um  die Wichtigkeit zu erhöhen.autor fuller hat er auf auf 1500 geboostet, so dass er wichtiger erscheint.

zum Schluss habe ich noch die Suche ein wenig ausprobiert mit advanced Search bekam ich zuerst gar keine Treffer (limit nur German und das Jahr grenzte ich ein 1990- 2020), da musste ich die Suche öffnen und ohne Limitierungen bekam ich 3 Treffer, jedoch ist das ja nur eine Beispieldatenbank:


![Screenshot from 2021-12-15 16-15-00](https://user-images.githubusercontent.com/90834735/146212897-d37eae11-8c4f-4809-9124-845c6fdf66c1.png)






