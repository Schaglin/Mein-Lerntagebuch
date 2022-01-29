Alex Stingson- soll man noch machen
Autoren von Nordafrika – selber Sparql -Abfrage schreiben
https://medium.com/freely-sharing-the-sum-of-all-knowledge/writing-a-wikidata-query-discovering-women-writers-from-north-africa-d020634f0f6c

ich habe da mal reingeschaut und mir die schon voreingestellte Query Anfrage angeschaut.
![Screenshot from 2022-01-13 19-39-44](https://user-images.githubusercontent.com/90834735/149391283-1944cc8a-1544-480c-9c72-e560a73fc76a.png)

Eine tunesische Ärztin ist bei der ersten Zeile erschienen.
![Screenshot from 2022-01-13 19-40-01](https://user-images.githubusercontent.com/90834735/149391235-95270c6a-b891-4b39-882d-01a7ee7932cc.png)




Aber man muss schauen ob in Wikidata drin sind.



Ich habe aus Spass Katzen gesucht, dazu nahm ich eine "Anfrage"-Vorlage "cats", dass war die Vorlage:
![Screenshot from 2022-01-13 11-59-10](https://user-images.githubusercontent.com/90834735/149377798-52427538-48ba-4e2b-86bc-181f22e70d5d.png)
![Screenshot from 2022-01-13 18-20-57](https://user-images.githubusercontent.com/90834735/149378296-8c6936cf-ba29-47f0-b98e-fc58147499fa.png)

Dabei bekam ich dann ein Ergebnis von Anzahl 153 mit allen Katzen von höheren Rängen (Katze vom Premierminister) oder bekannte schwedische Katze aus Vispy oder eine Katze aus Tiktok etc. und ihre hinterlegten Wikidata-Nummern sah man:
ich habe "Peter" mal näher betrachtet und auf die Wikidata Nummer geklickt

![Screenshot from 2022-01-13 11-57-49](https://user-images.githubusercontent.com/90834735/149377406-3ef6bbfa-e44a-457f-a360-dc3a37219705.png)

Und ich habe noch eine Katze "Toffee" gefunden, mit Foto sogar, ihr Eintrag auf Wikidata ist gut angereicht, sie ist gut verlinkt und hat ihre eigenen Facebook-Identifier. Leider ist sie schon im 2013 gestorben.
![Screenshot from 2022-01-13 11-58-20](https://user-images.githubusercontent.com/90834735/149377438-82fe9e36-86ca-40fe-b3e1-7198c6ef2f47.png)

Von Sparql her, sagt mir jetzt dass "instance of Housecat", dass heisst sie ist eine Instanz (Untergruppe) von Hauskatze. Sie übernimmt also alles was schon bei Hauskatze drin ist. ich schaue mir nochmals die Anfrage an und sehe, dass da noch eine zweite Suche war, welche eben diese Instanz p31 berüchsichtigt.
mit p31 wird vorgegeben, dass die katze eben aus der klasse p31 ist, und diese eine unterklasse von Hauskatze q146 ist. Daraus ergibt sich dann auch die Wikidata Nummer.
![Screenshot from 2022-01-13 18-26-22](https://user-images.githubusercontent.com/90834735/149380292-2a68d7a8-ff40-4ded-a05d-a5f13396a075.png)
