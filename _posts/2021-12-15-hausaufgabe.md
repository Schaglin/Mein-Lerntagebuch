**Hausaufgabe für Tag 7**

Es war Hausaufgabe das Suchprogramm VuFind für Bibliotheken zu installieren. 

Dazu bekamen wir wieder einen Satz von Shell-Befehlen zur Verfügung:

- **wget https://github.com/vufind-org/vufind/releases/download/v8.0.2/vufind_8.0.2.deb
- sudo dpkg -i vufind_8.0.2.deb**

- **sudo apt-get update   -(🦖)**

- **sudo apt-get install -f**

Maria DB mussten wir auch wieder installieren mit Befehl:
**sudo /usr/bin/mysql_secure_installation**
mussten wir ein neues Passwort festlegen, Maria DB ist = My Sql. Hierbei mussten wir noch einige Angaben mit y (yes) bestätigen.
Dann für den Root das Passwort bestätigen:**sudo mysql -uroot -p -e "UPDATE mysql.user SET plugin='' WHERE User='root'; FLUSH PRIVILEGES;"**
Ein Neustart war in unserem Fall nicht erforderlich. Es reichte aus, den genannten Befehl einzugeben:**source /etc/profile**
Um das Solr zu starten mussten wir vorher noch Dateirechte festlegen für das Cache- und das Config-Verzeichnis beim Account des Webservers (www-data).

    -**sudo chown -R $USER:$GROUP /usr/local/vufind
    -sudo chown -R www-data:www-data /usr/local/vufind/local/cache
    -sudo chown -R www-data:www-data /usr/local/vufind/local/config**
dann konnten wird das Solr starten und VuFind Konfigurieren mit Befehl:**/usr/local/vufind/solr.sh start**
Da wir keinen Domainnamen haben. Verwendeten wir localhost. Nun konnte ich den Browser in der virtuellen Maschine (Linux) mit folgender Adresse aufrufen:
(http://localhost/vufind/Install/Home)
Jetzt sollte VuFind bereits aufrufbar sein, und die Auto-Konfigurationen sollten sichtbar sein.
Leider hatte ich nur eine leere Seite mit. Browser nicht findbar.


**Zur Installation**:
bei mir klappte es leider nicht auf Anhieb auch nach Fehlerbehebung Nr. 1. klappte es noch nicht.
Jedoch gab es dann Hilfevideos von Hr. Lohmeier, die man anschauen konnte. Erst nach dem Hinweis von Hr. Lohmeier auf Befehl: **sudo apt get-update** gelang es mir.
Aus dem Unterricht zu Aris im Frühling 2020, kannte ich eigentlich den Befehl schon, dort mussten wir oft die Verzeichnisse updaten. Jedoch ist es mir leider nicht mehr in den Sinn gekommen.

Ich hatte Freude, weil ich vorher mehrere Versuche und auch die vorgeschlagenen Fehlerbehebungen ausprobiert habe, und schon fast am verzweifeln war.

Nun war VuFind aufrufbar, zuerst erschien die Auto-Konfiguration. Welche wir auch noch anpassen (fixen)sollten.
Die Security konnte man einfach mit fix darauf klicken und es wurde repariert.
Bei der Datenbank muss ein neues Passwort vergeben sowie das zuvor oben im Abschnitt “MariaDB Passwort für root” eingegeben werden.
Wir haben kein Bibliothekssystem, daher wählen wir NoILS. Dann wird aber trotzdem noch “Failed” angezeigt und wenn wir nochmal auf “Fix” klicken erscheint die folgende Meldung:


    sudo gedit /usr/local/vufind/local/config/vufind/NoILS.ini

    In Zeile 3 ils-offline in ils-none ändern und speichern.

Die schwierigste Auto-Konfiguration war wohl die, wo man in die Config-Datei selbst etwas umschreiben musste nämlich diese
vorher musste man NoiLs auswählen. Aber eigentlich wollen wir gar keine Noils (weil ist ein ILS Driver).
![ils none](https://user-images.githubusercontent.com/90834735/150584450-ed31ccc5-76a5-4b3f-8cf3-c4d88be51116.png)
daher musste man in die config-Dateie reingehen und manuell abändern und zwar von **ils offline zu ils none* abändern, damit es gar keine ILS Driver nimmt!


Demian Katz hat dazu auch ein Video gemacht zu diesen ILS Driver, das habe ich angeschaut: https://www.youtube.com/watch?v=qFbW8u9UQyM

als alles gefixt war, sah es dann so aus. Ich freute mich darüber :-).
![Screenshot from 2021-12-15 10-51-06](https://user-images.githubusercontent.com/90834735/146193562-01443fb2-7c94-4127-a593-c844d8905d92.png)



**Übung: Konfigurationen anpassen / Searching and Facet Settings**
Ein Youtube Video erklärt von Demian Katz, der Meister in VuFind, der auch im Editor erscheint: https://www.youtube.com/watch?v=qFbW8u9UQyM

Der Demiankatz war jetzt im Ordner /usr/local/vufind drin, um überhaupt dann nacher mit den Befehlen die config-Dateien abzufrufen.
Also musste ich auch in diesen Ordner kommen. Ich versuchte nun mit der Commandozeile Cd in diesen /usr/local/vufind reinzukommen.
Gemäss Demiankatz wäre der Befehl zum ändern der Search-Config-Dateien so gewesen, leider hat es nicht funktioniert.
![Screenshot from 2021-12-15 16-07-58](https://user-images.githubusercontent.com/90834735/146213450-505b7373-8c8a-4ef9-872a-49ade46d2f1e.png)

ich versuche es weiter...
![Screenshot from 2021-12-15 16-56-44](https://user-images.githubusercontent.com/90834735/146220478-c198ee89-eb11-471d-b84a-2614b4719fcb.png)


weiter Versuche hier, ich komme einfach nicht in das richtige Verzeichnis rein!!
application.config.php komme ich nicht rein, weil es keine directory ist. 

![Screenshot from 2021-12-15 17-24-10](https://user-images.githubusercontent.com/90834735/146225086-3cb109ee-8c24-42d0-8f0b-d2fe2bc585ab.png)

über die Shell habe ich es dann aufgegeben, ich habe einen Tipp bekommen von Barbora, die auch diesen Kurs besucht. Nun versuche ich meine Glück manuell über den Ordnern zu konfigurieren.

![Screenshot from 2021-12-15 18-12-08](https://user-images.githubusercontent.com/90834735/146233490-a77c58aa-b1e9-4652-8fc7-320f9e7170cb.png)


Die vorgeschlagenen Konfigurationen von DemianKatz aus dem Video zu "Searching und  Facet Settings" .

**Beim Searching**:
- 40 Resultate anzeigen lassen, anstatt nur 20 Suchresultate
- Namen der Suchtherme ändern zum Beipsiel anstatt Autor zu "Person who created" ändern. (übersetzt es richtig, hätte man noch prüfen sollen)

![Screenshot from 2021-12-15 18-24-29](https://user-images.githubusercontent.com/90834735/146235080-9ec96984-149b-44c8-90f7-610e5681d436.png)

**Meine AHA-Moment** Ja es sieht gut aus, vorher erschienen nur 20 Suchresultate und nun erscheinen tatsächlich 40 Suchresultate, die ich vorher konfiguriert habe!
![Screenshot from 2021-12-15 18-29-44](https://user-images.githubusercontent.com/90834735/146236011-f4fb85b4-7775-45d1-a0ac-ac38f10a7f99.png)

ich habe es noch mit 100 ausprobiert, es funktionierte, dass freute mich sehr !🦖
![Screenshot from 2021-12-15 18-38-12](https://user-images.githubusercontent.com/90834735/146237080-a759a9e3-9fff-4a62-9445-acfc1254bc7e.png)


- Reihenfolge ändern der Suchtherme z.b. Titel vor Autor 
![Screenshot from 2021-12-15 18-43-20](https://user-images.githubusercontent.com/90834735/146238202-af949680-c7e3-46f6-92de-3a64cbd35c0c.png)


![Screenshot from 2021-12-15 18-48-09](https://user-images.githubusercontent.com/90834735/146239810-38f3ce84-659d-47ee-8679-4f4c228550ea.png)

![Screenshot from 2021-12-15 18-50-15](https://user-images.githubusercontent.com/90834735/146239027-738fce42-df6f-4ca2-9b54-6519b06d646e.png)


-**default top recommended = top facettes** würde der demiankatz auch rausnehmen-dafür muss man Semikolon davor schreiben.
![Screenshot from 2021-12-15 19-14-22](https://user-images.githubusercontent.com/90834735/146244502-082fd588-3380-47ba-9adf-6b0e498ae634.png)

**Vorher**
![Screenshot from 2021-12-15 19-28-39](https://user-images.githubusercontent.com/90834735/146244647-946d8457-308e-479e-90ac-025804d20f23.png)

**Nachher**
![Screenshot from 2021-12-15 19-29-08](https://user-images.githubusercontent.com/90834735/146244617-24a2d9c2-0dd0-457c-aa32-733fe77bc8a5.png)

- Demian Katz möchte nun auch noch die OCLC Nummer zu den Suchthermen hinzufügen. Das lasse ich jetzt weg.


**Bei den Facetten**
Ich möchte nun den Instructor und die Building für die Narrow Search rausnehmen, so wie es Demiankatz vorschlägt:
;Institution wegnehmen, in Config-Datei einfach das Semikolon (;)davor schreiben
;Building wegnehmen "

Dazu ändere ich die Config-Datei namens **"facetes.ini"**
![Screenshot from 2021-12-15 19-14-22](https://user-images.githubusercontent.com/90834735/146242479-ec4194f8-0bce-4bac-bc49-e934d57c2052.png)


**Vorher:** hier war die Institution und das Building noch bei Narrow Search drin:
![Screenshot from 2021-12-15 19-02-54](https://user-images.githubusercontent.com/90834735/146241189-7c08d2e7-cb46-477c-9d6e-f4d3ed5155fe.png)
**Nachher**: jetzt sind die Institution und das Gebäude enfernt oder deaktiviert in den Resultaten:
![Screenshot from 2021-12-15 19-03-30](https://user-images.githubusercontent.com/90834735/146241350-87d0e6cc-7b3e-4fcc-9970-c92750e432ec.png)

**Suggested Topics**in der Sidebar bei Narrow Search:
![Screenshot from 2021-12-15 19-43-59](https://user-images.githubusercontent.com/90834735/146247047-988e61af-e129-4445-bc35-b9415dbc40ef.png)

![Screenshot from 2021-12-15 19-45-27](https://user-images.githubusercontent.com/90834735/146246510-acfd1fa4-05ed-40c9-a457-1f7f4acd474f.png)

-**Checkbox**: alle anzeigen wo keinen Autor haben, ich möchte alle Suchresultate rausnehmen, die keinen Autor haben, das kann ich hier sogar mit einer Checkbox machen. Dazu muss ich

 das Script umändern: **-Autor:*= " No author" *
 ![Screenshot from 2021-12-15 20-08-11](https://user-images.githubusercontent.com/90834735/146249560-9ed85e3f-07ca-4109-9763-ab0e11156d33.png)
 
- jetzt kommen alle Medien mit keinem Autor vor. Ich kann einfach das **Häklein anklicken. Es hat geklappt ☑️**
![Screenshot from 2021-12-15 20-05-49](https://user-images.githubusercontent.com/90834735/146249464-e0798254-616d-4005-9250-560302f269e8.png)


**YAML für Advanced Searched und Homepage ändern**
So konnte man auch die Homepage anpassen zum Beispiel Sprache ändern oder Browser by Format
**bei den searchaspects**: bei Yaml könne man auch die Wichtigkeit ändern z.b  der erste Autor ist viel wichtiger als der zweite Autor, also kann man den boosten.
er hat aus den ursprünglichen 300 dann 3000 gemacht, um  die Wichtigkeit zu erhöhen.autor fuller hat er auf auf 1500 geboostet, so dass er wichtiger erscheint.







