**Hausaufgabe für Tag 7**

Es war Hausaufgabe das Suchprogramm VuFind für Bibliotheken zu installieren. 

Dazu bekamen wir wieder einen Satz von Shell-Befehlen zur Verfügung:

- wget https://github.com/vufind-org/vufind/releases/download/v8.0.2/vufind_8.0.2.deb

- sudo dpkg -i vufind_8.0.2.deb

- **sudo apt-get update   -(🦖)**

- sudo apt-get install -f

Maria DB mussten wir auch wieder installieren mit Befehl:
**sudo /usr/bin/mysql_secure_installation**
mussten wir ein neues Passwort festlegen, Maria DB ist = My Sql. Hierbei mussten wir noch einige Angaben mit y (yes) bestätigen.
Dann für den Root das Passwort bestätigen:**sudo mysql -uroot -p -e "UPDATE mysql.user SET plugin='' WHERE User='root'; FLUSH PRIVILEGES;"**
Ein Neustart war in unserem Fall nicht erforderlich. Es reichte aus, den genannten Befehl einzugeben:**source /etc/profile**
Um das Solr zu starten mussten wir vorher noch Dateirechte festlegen für das Cache- und das Config-Verzeichnis beim Account des Webservers (www-data).

    -**sudo chown -R $USER:$GROUP /usr/local/vufind
    -sudo chown -R www-data:www-data /usr/local/vufind/local/cache
    -sudo chown -R www-data:www-data /usr/local/vufind/local/config**

Dann konnten wird das Solr starten und VuFind Konfigurieren mit Befehl:**/usr/local/vufind/solr.sh start**
Da wir keinen Domainnamen haben. Verwendeten wir localhost. Nun konnte ich den Browser in der virtuellen Maschine (Linux) mit folgender Adresse aufrufen:
(http://localhost/vufind/Install/Home)
Jetzt sollte VuFind bereits aufrufbar sein, und die Auto-Konfigurationen sollten sichtbar sein.
Leider hatte ich nur eine leere Seite mit. Browser nicht findbar.


**Zur Installation**:
bei mir klappte es leider nicht auf Anhieb auch nach Fehlerbehebung Nummer 1., klappte es immer noch nicht.
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
Also musste ich auch in diesen Order reinzukommen über die Commandozeile.
![reinkommen](https://user-images.githubusercontent.com/90834735/151765594-e2b29ebc-7ac4-4729-a7e4-fb2356b6d66b.png)

Gemäss Demiankatz wäre der Befehl zum ändern der Search-Config-Dateien so gewesen, leider hat es nicht funktioniert.

ich versuche es weiter![weitere versuche](https://user-images.githubusercontent.com/90834735/151765697-69234703-34a3-48df-9bcf-625a38d9927d.png)




weiter Versuche hier, application.config.php komme ich nicht rein, weil es keine directory ist. 
![versuche](https://user-images.githubusercontent.com/90834735/151765760-39c282f8-2dcf-4f12-a6bb-48c60969033c.png)



über die Shell habe ich es dann aufgegeben, ich habe einen Tipp bekommen von Barbora, die auch diesen Kurs besucht. Nun versuche ich meine Glück manuell über den Ordnern zu konfigurieren.

![Screenshot from 2021-12-15 18-12-08](https://user-images.githubusercontent.com/90834735/146233490-a77c58aa-b1e9-4652-8fc7-320f9e7170cb.png)


Die vorgeschlagenen Konfigurationen von DemianKatz aus dem Video zu "Searching und  Facet Settings" .

**Beim Searching**:
- 40 Resultate anzeigen lassen, anstatt nur 20 Suchresultate
- Namen der Suchtherme ändern zum Beipsiel anstatt Autor zu "Person who created" ändern. (übersetzt es richtig, hätte man noch prüfen sollen)
![40 suchresultate](https://user-images.githubusercontent.com/90834735/151765872-0661544c-8573-44c6-bbc1-f11c0a6a1d12.png)


**Meine AHA-Moment** Ja es sieht gut aus, vorher erschienen nur 20 Suchresultate und nun erscheinen tatsächlich 40 Suchresultate, die ich vorher konfiguriert habe!


ich habe es noch mit 100 ausprobiert, es funktionierte, dass freute mich sehr !🦖
![100 resultate](https://user-images.githubusercontent.com/90834735/151765934-34acdb10-148f-416b-8885-d524669b9d62.png)




- Reihenfolge ändern der Suchtherme z.b. Titel vor Autor 
![Screenshot from 2021-12-15 18-43-20](https://user-images.githubusercontent.com/90834735/146238202-af949680-c7e3-46f6-92de-3a64cbd35c0c.png)

*Person who created this stuff" anstatt "author"
![person who created this stuff](https://user-images.githubusercontent.com/90834735/151766034-91f0fff8-97b0-4cac-9bc4-8f7ae569cbb7.png)


**default top recommended= top facettes**-das würde der Demian Katz rausnehmen- dafür muss man Semikolon davor schreiben.

- Demian Katz möchte nun auch noch die OCLC Nummer zu den Suchthermen hinzufügen. Das lasse ich jetzt weg.


**Bei den Facetten**
Ich möchte nun den Instructor und die Building für die Narrow Search rausnehmen, so wie es Demiankatz vorschlägt:
;Institution wegnehmen, in Config-Datei einfach das Semikolon (;)davor schreiben
;Building wegnehmen "

Dazu ändere ich die Config-Datei namens **"facetes.ini"**

**Vorher:** hier war die Institution und das Building noch bei Narrow Search drin:
![narrow search](https://user-images.githubusercontent.com/90834735/151767228-284d5a1b-45a0-4ff7-9264-478037349658.png)


**Nachher**: jetzt sind die Institution und das Gebäude enfernt oder deaktiviert in den Resultaten:
![narrow search angepasst](https://user-images.githubusercontent.com/90834735/151767240-0693b8b5-f855-4519-adc6-a5b448b3909d.png)


**Suggested Toppics: in der Sidebar bei Narrow Search ändern**
![suggested](https://user-images.githubusercontent.com/90834735/151767342-fcc98504-6068-4855-890a-5a2c030593e9.png)


![Screenshot from 2021-12-15 19-45-27](https://user-images.githubusercontent.com/90834735/146246510-acfd1fa4-05ed-40c9-a457-1f7f4acd474f.png)

-**Checkbox**: alle anzeigen wo keinen Autor haben, ich möchte alle Suchresultate rausnehmen, die keinen Autor haben, das kann ich hier sogar mit einer Checkbox machen. Dazu muss ich das Script umändern: **-Autor:*= " No author" *
 ![no autor](https://user-images.githubusercontent.com/90834735/151767485-b7808fe5-d3ff-4240-8eb0-2934cf712085.png)
 
 **Checkbox**: ![checkbox](https://user-images.githubusercontent.com/90834735/151767806-8c1b2f5a-4f47-4a72-a4ea-fddc2f360dab.png)
 
- jetzt kommen alle Medien mit keinem Autor vor. Ich kann einfach das **Häklein anklicken. Es hat geklappt ☑️**

![Screenshot from 2021-12-15 20-05-49](https://user-images.githubusercontent.com/90834735/146249464-e0798254-616d-4005-9250-560302f269e8.png)


**YAML für Advanced Searched und Homepage ändern**
So konnte man auch die Homepage anpassen zum Beispiel Sprache ändern oder Browser by Format.
**bei den search aspects**: bei Yaml könne man auch die Wichtigkeit ändern z.b  der erste Autor ist viel wichtiger als der zweite Autor, also kann man den boosten.Katz hat aus den ursprünglichen 300 dann 3000 gemacht, um  die Wichtigkeit zu erhöhen.autor fuller hat er auf auf 1500 geboostet, so dass er wichtiger erscheint.







