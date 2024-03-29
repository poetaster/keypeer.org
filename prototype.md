# Beschreibe dein Projekt kurz. (100w)

Das keypeer Projekt ist ein Schlüssel-Dienst, im Sinne von API (Application Programming Interface) Schlüssel, keys.

keypeer ermöglicht Entwicklern von Free Open Source Software (FOSS), einen abgabenpflichtigen Dienst in der eigenen App einzubinden und bei einem Nutzer frei zu schalten, der Bezahlt hat, ohne Geschäftsbeziehung und ohne Personen-Daten zu speichern. Nutzern ermöglicht keypeer, Dritt-Anbieter-Dienste in Apps zu unterstützen und somit FOSS.

keypeer selbst nimmt keine Bezahlung entgegen, sondern registriert anonyme Nutzer-Schlüssel und verbindet diese mit einem Dritt-Service API key. Zahlungen werden von einem Verein mit Hilfe von, zum Beispiel, Open Collective Europe (https://opencollective.com/europe) angenommen und ausgegeben.

#  Welche gesellschaftliche Herausforderung willst du mit dem Projekt angehen? * (175w)

Als Beispiel, viele FOSS/OSS Kartendienste bieten neben einer Basis wie Openstreetmaps, Kacheln (eg. Satelliten Bilder) von dritten an die kostenpflichtig sind. Mapbox, zum Beispiel. keypeer wäre die Schnittstelle, der Service, der es dem Nutzer ermöglicht ein Beitrag zu leisten und dafür Schlüssel für einen oder mehrere dritt Anbieter Dienste in einer Anwendung zu bekommen. Mittels keypeer kann ein Nutzer auch mehrere Projekte gleichzeitig unterstützen.

Mittels keypeer wird für jede Anwendung und API eine Marke erzeugt. Der Nutzer gibt diese Marke bei Bezahlung an, zum Beispiel https://opencollective.com/europe. Diese wird beim keypeer registriert und die Anwendung kann das Nutzen vom dritt Dienst freischalten. Bezahlungen werden verwaltet von einem Verein, in einer kollektiven Kasse.  Dieser Verein veranlaßt nur Zahlungen aus dem kollektivem Konto an  dritt Anbieter, bzw. Mapbox. Der Verein https://sailmates.net begleitet die Prototype-phase.

Ziel ist das bündeln von Nutzer Zahlungen um dritt Dienste zu Zahlen, was Einzelentwickler oder Projekte sonst nicht leisten könnte. Des weiteren gilt der Ausbau der Zahlungsdienste im Umfeld von FOSS als ziel. Als transparente finanzielle Vermittlungsstelle soll, zum Beispiel  https://opencollective.com/europe dienen.

# Wie willst du dein Projekt technisch umsetzen? * (175w)

Der Server besteht aus einem Web Service ( REST API ), eine frei erreichbare Schnittstelle, die Entwickler einbinden können, um Nutzer-Marken anonym im keypeer zu prüfen. Wurde bei keypeer die Marke als turnusgemäß bezahlt registriert, kann ein zusätzlicher Dienst freigeschaltet werden.

Die API wird im OpenAPI (https://www.openapis.org Swagger YAML ) format spezifiziert , was somit unabhängig von der endgültigen Umsetzung bleibt.

Dieser REST Prototype wird mittels Flask mit der Connexion Library und Swagger in Python entwickelt. Die Nutzung von Connexion und Swagger gewährleistet, daß die OpenAPI Endpunkte sowohl Standard Konform sind als auch direkt Dokumentation zur Verfügung stellen.

Anvisiert ist eine Zero Proof Datenbank, basierend auf Circuitree, Circuitree: A Datalog Reasoner in Zero-Knowledge | IEEE Journals & Magazine | IEEE Xplore ( https://ieeexplore.ieee.org/document/9718332 ) zu nutzen um Nutzer-Marken zu speichern und zu verifizieren, ohne direkt personenbezogene Daten zu benutzen.

Während der Prototype-phase werden Javascript und C++ Clients die Schnittstelle testen. Als erstes, die Mapping Anwendung Puremaps GitHub - rinigus/pure-maps: Maps and navigation ( https://github.com/rinigus/pure-maps). 


#  Hast du schon an der Idee gearbeitet? Wenn ja, beschreibe kurz den aktuellen Stand und erkläre die geplanten Neuerungen. * (100w)

Bis jetzt wurde diskutiert und die ersten API Entwürfe skizziert. https://github.com/poetaster/keypeer.org/blob/main/doc/api/api.yaml

Impulsgeber is der rinigus,https://github.com/rinigus/pure-maps. Die Puremaps Anwendung wird als 'Konsument' in der Prototyp Phase dienen.

Unter anderem wird mit Ruben De Smet, Vrije Universiteit Brussel (https://ieeexplore.ieee.org/document/9718332) , ein Zero Knowledge Ansatz der Nutzer Verifikation diskutiert. 

#  Welche ähnlichen Ansätze gibt es schon und was wird dein Projekt anders bzw. besser machen? * (60w)

Uns sind keine ähnlichen Projekte bekannt.

# Wer ist die Zielgruppe und wie soll dein Projekt sie erreichen? * 

Sowohl App Endnutzer als Entwickler. Die Anzahl an Anwendung die API keys brauchen wächst stetig und betrifft alle möglichen Bereiche. In erster Linie geht es um Entwicklung von FOSS Anwendungen dem sonst die Mittel fehlen zu unterstützen und dem Nutzer die Wahl alternativer Apps zu gewährleisten.

Die Prototyp Phase wird mit Puremaps, die Karten Anwendung, realisiert, da hier schon eine Zusammenarbeit stattfindet und der Entwickler von Puremaps auch mit anderen Karten-Anwendungs-Entwicklern in Kontakt steht. Wir streben auch Finanzierung zwischen Projekten an.

Andere Bereiche, die wir anvisiert haben, sind Anwendung aus dem Bereichen Gesundheit und Bildung.

# An welchen Software-Projekten hast du / habt ihr bisher gearbeitet? Bei Open-Source-Projekten bitte einen Link zum Repository angeben

https://github.com/poetaster/fahrplan - Fahrplanauskunft und Fahrplananwendung, (Entwickler Team, Maintainer)
https://github.com/poetaster/tomservice - Wordpress Plugin VG Wort dienst, (Entwickler, Maintainer)
https://github.com/poetaster/tidings - RSS/OPML Reader, (Entwickler Team, Maintainer)

# Erfahrung, Hintergrund, Motivation, Perspektive: Was sollen wir über dich (bzw. euch) wissen und bei der Auswahl berücksichtigen? * 

Ich bin seit Anfang der 1990er Jahre involviert in FOSS/OSS Projekten. In den 1990er, netBSD und einige Apache Foundation Projekte (eg. Cocoon). Sowohl als Entwickler als auch im Bereich Gesellschaftlicher Entwicklung. Als Mitinhaber der Newthinking Communications GmbH habe ich die Gründung der https://re-publica.com und https://netzpolitik.org mit getragen. Weitere bestehende Projekte, die wir aufgebaut haben, sind https://berlinbuzzwords.de und die https://foss-backstage.de . Bis Ende 2022 war ich bei Netzpolitik.org angestellt.

Als Technischer Leiter und Programmierer bin ich an verschiedenen FOSS orientierten Initiativen beteiligt. Seit etwa 2018 bin ich zunehmend an der Entwicklung von alternativen mobilen Plattformen, insbesondere SailfishOS, beteiligt. Bis jetzt habe ich mich hauptsächlich um den Erhalt von Anwendungen und neu Entwicklung von Apps bemüht, mit Schwerpunkt Media, Bild-, Video- und Ton-Bearbeitungs-Apps sind Schwerpunkte aus Leidenschaft.

Durch Eigenentwicklung und im Gespräch mit weiteren Entwicklern wurde mir klar, daß wir etwas unternehmen können, um die Kaufkraft von FOSS Unterstützern für viele interagierende Projekte zu bündeln. Ich sehe dies als eine Art ‘Crowd Funding Model’.

Die Motivation mich bei der Prototypefund zu bewerben stammt aus der Entwicklung einer Anwendung vor 2 Jahren die den Brightsky API nutzt (https://github.com/poetaster/harbour-dwd).  Durch Brightsky wurde mir die Prototypefund erst bekannt. In gewisser Hinsicht hat auch Brightsky ein ähnliches Ziel wie ich. Das vereinfachen des Nutzens von APIs.

#  Skizziere kurz die wichtigsten Meilensteine, die im Förderzeitraum umgesetzt werden sollen. * 

Prototype phase:
    REST-API spezifizieren
    Prototyp REST/WS-Dienst, Server
    Sicherheitsaudit, informell
    Prototyp eines REST-Verbrauchers, Client (Puremaps)
    Prototyp der administrativen Schnittstellen des Servers

Vorproduktion:

    Vernetzung von Interessenvertretern/Entwicklern / Treffen
    Gespräche Zahlungsanbietern, Vertrag
    Server Kommunikation mit Zahlungsanbieter Dienst
    Sicherheitsaudit, formal



