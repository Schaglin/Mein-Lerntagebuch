---
title: "Hausaufgabe"
date: 2021-11-19
---
_Liebes Tagebuch_,



**Dspace**

 **Aufgabe zur OAI-PMH-Schnittstelle**       

Ich habe die von mir erstellte Publikation von gestern heute laden können in der DSpace Demo über die OAI-PMH-Schnittstelle (Daten erscheinen dort zeitverzögert ca. 1 Tag)
Da in der Demoversion alle Daten jeden Samstag nachts gelöscht werden, um eine einwandfreie Demo zu garantieren, musste ich es heute Mittag schnell machen.
    
Dann habe ich die Schnittstelle geöffnet und bin unter meiner Community [BAIN übung_18_11_21](http://demo.dspace.org/oai/request?verb=ListSets) und habe den Link 
“Records” aufgerufen.
Ich habe meine Daten im Kasten “Metadata” nun aufrufen können.
Ich habe den Inhalt kopiert in einen Texteditor und diesen gespeichert unter Dokumente.


Hier die Metadata zur erstellten Publikation:

	<oai_dc:dc xsi:schemaLocation="http://www.openarchives.org/OAI/2.0/oai_dc/ http://www.openarchives.org/OAI/2.0/oai_dc.xsd">  **_hier sehe OAI-PH Schnittstelle_**

	<dc:title>Bespiel- Publikation</dc:title>

	<dc:creator>Kueng</dc:creator>

	<dc:subject>pdf</dc:subject>

	<dc:description>hier das beispiel pdf</dc:description>

	<dc:date>2021-11-18T10:00:28Z</dc:date>

	<dc:date>2021-11-18T10:00:28Z</dc:date>

	<dc:date>2021-11-18</dc:date>

	<dc:type>Article</dc:type>

	<dc:identifier>http://hdl.handle.net/10673/167</dc:identifier>

	<dc:rights>Attribution-NoDerivs 3.0 United States</dc:rights>

	<dc:rights>http://creativecommons.org/licenses/by-nd/3.0/us/</dc:rights>

	<dc:format>application/pdf</dc:format>

	<dc:publisher>Kueng</dc:publisher>

	</oai_dc:dc>
Die ganzen Metadata sind in DC= Dublin Core geschrieben.

![metadata zu publikation](https://user-images.githubusercontent.com/90834735/151631100-3382e13c-b64b-45d7-b5e6-eb49544d538d.png)




Heute ist auch ein schönes Bild vom Skript zu Harry Potter auf DSpace Demo erschienen.

![dspace harry potter](https://user-images.githubusercontent.com/90834735/151631093-5ce30c7d-779d-47e9-a7f0-090cf7047e28.png)


-------------------------




mehr zu Import und Export von Metadaten und zu Schnittstellen:

DSpace bietet auch dateibasierten Import, besonders relevant sind im Kontext von Repositorien aber die Schnittstellen:
**SWORD**
Die Schnittstelle "SWORD" ermöglicht die Publikation in DSpace auf anderen Webseiten aufzurufen.
SWORD kann Publikationen in einem Repository abliefern. Damit kann ein Formular mit Dateiupload auf einer Webseite (ausserhalb der Repository-Webseite) angeboten werden. Um Daten aus dem Repository auf Webseiten anzuzeigen, z.B. eine Publikationsliste, werden andere Schnittstellen wie RSS-Feeds verwendet.

**RSS-Feeds** verwenden wir bei der GitHUb Seite.
Gemäss Wikipedia:
Rich Site Summary (RSS) sind Dateiformate für Web-Feeds. Sie zeigen Änderungen auf Websites, z. B. auf News-Seiten, Blogs, Audio-/Video-Logs etc. Das Backronym steht aktuell für Really Simple Syndication (etwa sehr einfache Verbreitung), vormals waren bereits andere Bedeutungen gegeben. Es ist wie ein Newsticker.
Feed, weil füttern, einspeisen von neuen Daten, die der Client über den RSS-Channel abonniert hat. Weil RSS-Dienste werden eimst über spezielle Service-Websites angeboten, songenannte RSS-Channels.

**OAI-PMH**:
OAI-PMH ermöglicht es eben die erfassten Metadaten aus DSpace zu holen.
OAI-PMH-Schnittstelle der DSpace-Demo (ein Tag später sind online): http://demo.dspace.org/oai/request?verb=ListSets
Diese Schnittstelle OAI-PMH BASE Harvesting von Bielefeld ist enorm effizient!!
Unterschied Institutionellen und Fachrepositorien sind also viele Dokumente verstreut.Hingegen diese BASE Suchmaschine, vereint die Fachrepositorien, sie hat  darum auch 250 Mio. Fachbeiträge in einem Repository drin!




