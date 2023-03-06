# Beschreibe dein Projekt kurz. (100w)

Das keypeer Projekt ist ein Schlüssel dienst, im Sinne von API (Application Programming Interface) keys.

Entwickler von Freier Offener Source Software (FOSS) ermöglicht keeypeer einen abgabenpflichtigen Dienst in der eigenen App einzubinden und bei einem Nutzer frei zu schalten der Bezahlt hat ohne Geschäftsbeziehung und ohne Personen Daten zu speichern. Nutzern ermöglicht keypeer dritt Anbieter Diensten in Apps zu unterstützen.

keypeer selbst nimmt keine Bezahlung entgegen sondern registriert nur einen Anonymen Nutzer Schlüssel und verbindet die mit einem dritt Service API key. 

#  Welche gesellschaftliche Herausforderung willst du mit dem Projekt angehen? * (175w)

Als Beispiel, viele FOSS/OSS Kartendienste bieten neben einer Basis wie Openstreetmaps, Kacheln (eg. Satelliten Bilder) von dritten an die ab einer gewissen Anzahl von Nutzern/Abrufe kostenpflichtig sind. Mapbox, zum Beispiel. keypeer wäre die Schnittstelle, der Service, der es dem Nutzer ermöglicht ein Beitrag zu leisten und dafür Schlüssel für einen oder mehrere dritt Anbieter Dienste in Apps zu bekommen. Mittels keypeer kann ein Nutzer auch mehrere Projekte gleichzeitig unterstützen.

Mittels keypeer wird eine Nutzer<->App Marke erzeugt. Der Nutzer gibt diese bei Bezahlung an, zum Beispiel https://opencollective.com/europe. Diese wird beim keypeer registriert und die App kann das Nutzen vom dritt Dienst freischalten. Bezahlungen werden verwaltet von einem Verein, in einer kollektiven Kasse.  Dieser Verein veranlaßt nur Zahlungen aus dem kollektivem Konto an  dritt Anbieter, bzw. Mapbox. Der Verein https://sailmates.net hat sich bereit erklärt die Prototype-phase zu begleiten.

Ziel ist das bündeln von Nutzer Zahlungen um den dritt Dienst zu Zahlen, was der Entwickler oder das Projekt nicht leisten könnte.

Als transparente finanzielle Vermittlungsstelle soll, bzw.,  https://opencollective.com/europe dienen.

# Wie willst du dein Projekt technisch umsetzen? * (175w)

Der Server besteht aus einem Web Service ( REST API ), eine frei erreichbare Schnittstelle die Entwickler einbinden können um Nutzer Tokens/Marken anonyme von keypeer zu bekommen und prüfen. Wurde bei keypeer die Marke als bezahlt (Turnus gemäß) registriert, kann ein zusätzlicher Dienst eingeschaltet werden. 

Dieser Webservice besteht im Hintergrund aus einer Zero Proof Datenbank Anwendung, basierend auf Circuitree, https://ieeexplore.ieee.org/document/9718332

Während der Prototype-phase werden Javascript und C++ Clients die Schnittstelle testen. Als erstes, mit der Mapping Anwendung Puremaps https://github.com/rinigus/pure-maps

#  Hast du schon an der Idee gearbeitet? Wenn ja, beschreibe kurz den aktuellen Stand und erkläre die geplanten Neuerungen. * (100w)

Bis jetzt wurde nur skizziert und diskutiert. Impulsgeber is der der rinigus,https://github.com/rinigus/pure-maps.  Unter anderem wird mit Ruben De Smet, https://ieeexplore.ieee.org/document/9718332 , ein Zero Knowledge Ansatz der Nutzer Verifikation diskutiert.

#  Welche ähnlichen Ansätze gibt es schon und was wird dein Projekt anders bzw. besser machen? * (60w)

Keine.

# Wer ist die Zielgruppe und wie soll dein Projekt sie erreichen? * 

Sowohl App Endnutzer als Entwickler. Die Anzahl an Anwendung die API keys brauchen wächst stetig und betrifft alle möglichen Bereiche von Gesundheit zur Bildung, Navigation bis zur Geology. In erster Linie geht es um Entwicklung von FOSS Anwendungen dem sonst die Mittel fehlen zu unterstützen und dem Nutzer die Wahl.

# An welchen Software-Projekten hast du / habt ihr bisher gearbeitet? Bei Open-Source-Projekten bitte einen Link zum Repository angeben

https://github.com/poetaster/fahrplan (Entwickler Team, Maintainer)
https://github.com/poetaster/tomservice (Entwickler, Maintainer)
https://github.com/poetaster/tidings (Entwickler Team, Maintainer)

# Erfahrung, Hintergrund, Motivation, Perspektive: Was sollen wir über dich (bzw. euch) wissen und bei der Auswahl berücksichtigen? * 

Ich bin seit vielen Jahren (Anfang der 1990er) involviert in FOSS/OSS Projekten jedoch auch im Bereich Gesellschaftlicher Entwicklung. Als mit Inhaber der Newthinking Communications GmbH habe ich die Gründung der re-publica.com und netzpolitik.org mit getragen. Bis ende 2022 war ich noch bei netzpolitik.org angestellt. Als Technische Leitung und Programmierer bin ich an verschiedenen FOSS orientierten Initiativen  beteiligt. Seit etwas 2018 bin ich zunehmend an der Entwicklung von Alternativen mobilen Plattformen, insbesondere SailfishOs, beteiligt. Bis jetzt habe ich mich hauptsächlich um den Erhalt von Anwendungen und neu Entwicklung von Apps bemüht, mit Schwerpunkt Media. Bild, Video und Ton Bearbeitungs- Apps sind Schwerpunkt, aber nur ein Kleines teil der Arbeit.




