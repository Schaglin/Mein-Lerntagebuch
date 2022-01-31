**üben im Archive Space**


**Import**
Man solle eine "raw xml file" sollte nun als EAD-DAtei importiert werden, und auf die virutelle Festplatte gedownloaded werden um sie als " Background" anzulegen.
Das habe ich dann auch gemacht.

![Screenshot from 2021-11-15 19-06-39](https://user-images.githubusercontent.com/90834735/141852032-1ae02510-ac68-4e00-9cfc-4787f530277a.png)



![Screenshot from 2021-11-15 18-58-36](https://user-images.githubusercontent.com/90834735/141849676-dc819417-d19b-405f-acbc-ed3bc0a9b607.png)

Dieser "Background" habe ich nun auch wieder zu meinem Beispieldossier erfasst.
![Screenshot from 2021-11-15 19-09-27](https://user-images.githubusercontent.com/90834735/141849803-d5824b0f-5865-4947-a503-3f1445d6b8cf.png)




diese  _"a raw XML file"_ sollte nun in EAD importiert werden:

![Screenshot from 2021-11-15 19-06-07](https://user-images.githubusercontent.com/90834735/141850291-e7fb5ab4-4dc1-4b81-8865-bc49791913d9.png)

Dann konnte man überprüfen, ob es geklappt hat und es erschienen " **DONE**" (gruen) unter new Modified Records "**Die American Assocation of Industrial Editors (AAIE) Records**"
![Screenshot from 2021-11-15 19-06-07](https://user-images.githubusercontent.com/90834735/141850291-e7fb5ab4-4dc1-4b81-8865-bc49791913d9.png)

"**Background-Job has completed**":



------------------------------



![Screenshot from 2021-11-15 22-06-56](https://user-images.githubusercontent.com/90834735/141854142-8c1039cd-6a2b-4288-8a4e-88aa845b3943.png)
![Screenshot from 2021-11-15 22-06-02](https://user-images.githubusercontent.com/90834735/141854154-a5d4970d-4d7f-42de-b6c7-5762790b1737.png)


![Screenshot from 2021-11-15 19-09-34](https://user-images.githubusercontent.com/90834735/141851163-07b9cd25-962e-465d-b53b-84fc43aab275.png)

Diese AAIE Records musste nun heruntergeladen werden und als .json abgespeichert werden.
![Screenshot from 2021-11-15 22-05-59](https://user-images.githubusercontent.com/90834735/141854711-e694aeaf-7535-4bba-8d19-286c44105ccc.png)

Meine *Downloads*:   die Datei erschien aber nur in xml, kam nicht in json!!
![Screenshot from 2021-11-15 19-06-07](https://user-images.githubusercontent.com/90834735/141850291-e7fb5ab4-4dc1-4b81-8865-bc49791913d9.png)




Vergleich mit Archive Space und der Ansicht von html:
------------------------------------------------------------



Man sah, dass Archive Space die EAD-Felder selbstständig ausgefüllt hatte und auch ein ID - Identifier, der ja so wichtig ist für die eindeutige Verifzierung erschien bwz. ob das Dokument integer und authentisch ist. Das heisst nicht abgeändert oder irgendwie modifiziert wurde ohne Befugnis.
![Screenshot from 2021-11-15 22-08-36](https://user-images.githubusercontent.com/90834735/141854131-66973f5f-2169-4ad7-ab0b-eaa44140213a.png)

Finding Aid Data:
![Screenshot from 2021-11-15 20-05-04](https://user-images.githubusercontent.com/90834735/141860096-c7324923-e86b-4b25-99da-e8362fc01652.png)


----------------------------------------------------------------

**Vergleich: biografische Geschichte**
Viel übersichtlicher so wie es in Archive Space dargestellt wird. aber das Feld:**"Geschenk von Samuel V. Kennedy, 1980 " <subfield code="a">Gift of Samuel V. Kennedy , 1980.</subfield> findet sich unter einer anderen Stelle wieder.Viel detaillierter und es war unter Acquisitation (Erwerbung) und Subnotes (Notizen) vermerkt. 
Mein AHA-Moment: jetzt ist es mir klar, diese AAIE Records  waren ein Geschenk von Samuel V. Kennedy im Jahr 1980, so wurden diese erworben. Das finde ich doch noch einen wichtigen Hinweis für Archivare!!

in ***HTML**: 
![Screenshot from 2021-11-15 22-29-13](https://user-images.githubusercontent.com/90834735/141856395-c2b22e3d-ba28-4e12-8f7b-f9ac90a9410e.png)

in ****ARCHIVE SPACE**
![Screenshot from 2021-11-15 22-43-07](https://user-images.githubusercontent.com/90834735/141858100-349b7e11-0bf6-4c40-ba86-f87eed2756d4.png)



Export
----

diese _"a raw xml file"_, die importiert wurde, sollte nun in Marc XML auf der virtuellen Festplatte gespeichert werden:
![Screenshot from 2021-11-15 22-37-11](https://user-images.githubusercontent.com/90834735/141857327-b585f9a9-c339-4cc4-ba28-f5427f8ccafd.png)


**AHA-Moment:***Ist der Export verlustfrei?**
Wenn ich nun wieder diese Notiz mit dem Geschenk von Samuel V. Kennedy vergleiche, war der Export der Datei **auf den ersten Blick "verlustfrei"**. Aber Marc 21 ist ja eigentlich nicht verlustfrei nur das EAD. Darum habe ich wohl etwas übersehen. Marc 21 ist nicht verlustfrei in Archivsystemen, weil es eben für Bibliotheken gemacht wurde, es ist ein Format für Bibliotheken und nicht für Archive. Darum fallen auch ein paar Marc 21-Formate dann beim Export in EAD raus!



**XML-Datei als Export von Archive Space:**
![Screenshot from 2021-11-15 22-35-45](https://user-images.githubusercontent.com/90834735/141857341-37b8e6f7-0f03-4c62-9103-f0437e13135f.png)


**Lösung:** In der Lösung kam dann raus, dass die University eben viel detaillierter erschlossen hat mit Inventar und allem. Das Archive Space hat aber nicht so detailliert erschlossen. Archive Space hat z. B. auch das Jahr nicht richtig erschlossen dort steht von 1939- 1958, aber auf der Universitätsseite steht von 1939 - 1969. Auch der Bestand wird viel oberflächlicher im Archive Space erschlossen, als die University erschlossen hat.Die EAD- Datei im Archive Space hat z.b. nur eine Resource und keine Archival Objects erschlossen. Die HTML- Ansicht von der University zeigt aber ein ganzes **Inventar* auf wo auch drin steht welche Box und wie viele Folder es hat, also Laufmeter/Umfang die Box hat:
https://library.syr.edu/digital/guides/a/aaie.htm


![Screenshot from 2021-11-18 08-49-22](https://user-images.githubusercontent.com/90834735/142373901-27fc9b7a-fb72-49f9-bf10-83264cc8c100.png)




