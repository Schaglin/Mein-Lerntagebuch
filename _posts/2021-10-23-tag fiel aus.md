---
title: "Hausaufgabe für Tag 4"
date: 2021-10-23

---


**Liebes Tagebuch**

Die Hausaufgaben war:   **Installation von Archivprogramm "Archives Space"**

Bevor wir **_Archives Space_** installieren konnten, mussten wir zuerst die Shell updaten mit dem Befehl **sudo apt update** und dann die **_Java 8_** herunterladen mit dem Befehl: **_sudo apt install openjdk-8-jre-headless_** mithilfe unserer Shell. 
![done](https://user-images.githubusercontent.com/90834735/151770751-c172047d-1694-400d-9ff8-586d1cd8eed5.png)


Danach konnten wir die Befehle _wget https://github.com/archivesspace/archivesspace/releases/download/v3.1.0/archivesspace-v3.1.0.zip_
 copy/pasten und das Archive Space downloaden und den Ordern unzippen mit dem Befehl: unzip -q archivesspace-v3.1.0.zip.
 
  ![unzippen](https://user-images.githubusercontent.com/90834735/151770725-58635dca-3f79-4f16-a5f0-cf0538aaa0c8.png)

  
**_Die Installation lief problemlos, was mich sehr freute_ :-)**

Das Archive Space konnte mit dem Befehl: _archivesspace/archivesspace.sh_ gestartet werden und wir konnte dann über die URL aufgerufen werden:

Adminoberfläche:
    http://localhost:8080/ – “Staff Interface”      (admin)
    ![welcome](https://user-images.githubusercontent.com/90834735/151770494-a4de8042-ff91-4d4c-a6d5-38593d20aae6.png)


    
Benutzeroberfläche:  
    http://localhost:8081/ – “Public Interface”        (public)
![8081archive space](https://user-images.githubusercontent.com/90834735/151770523-7c35ada7-2506-48e7-bd60-c8a7118ab838.png)



OAHI-PMH Schnittstelle-Oberfläche:   
    http://localhost:8082/ – OAI-PMH 
![schnittstelle8082](https://user-images.githubusercontent.com/90834735/151770546-66105a34-bcc1-4ec4-80bb-13704b2c4cb1.png)




**AHA-Moment**: Dann habe ich erstaunt festgestellt, dass die public-Seite noch gar keine Einträge drin hat! Beim Nachlesen habe ich erfahren, dass die public - Seite erst verfügbar ist, wenn über die admin-Seite ein **_Repository_** angelegt wurde.

