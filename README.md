# Vrijwilligersapp
Mobiele app voor de vrijwilligers van Park de Stadshoeve in Zwolle. In de app kan regulier onderhoud worden gepland en gereed gemeld worden. Ook kunnen vrijwilligers defecten melden.


## Context
Ik bouw een mobiele app voor de vrijwilligers van Park de Stadshoeve in Zwolle-Stadshagen,
een wijkpark met kinderboerderij. Het park wordt gerund door Stichting de Stadshoeve,
met ongeveer 40 vrijwilligers. De stichting heeft geen personeel. Dagbesteding Frion doet
doordeweeks de dierverzorging, het groenonderhoud en klein onderhoud. Er is een
coördinator onderhoud (meestal het bestuurslid met die portefeuille). De documenten in
dit project (meerjarenbeleidsplan, beleidsplan onderhoud) beschrijven de organisatie.
Gebruik ze als achtergrond.

Werkgroepen: Dieren, Tuinen, Avontuurlijk spelen, Klussen, Educatie, Evenementen,
Geschiedenis.

Dit is mijn eerste app. Ik ben geen programmeur. Mijn opvolger is dat ook niet.

## Wat de app moet doen
1. Takenlijst per werkgroep bekijken. Startscherm is "Mijn taken"; de taken van de
   hele werkgroep staan één tik verder.
2. Taken toewijzen aan één persoon per taak. Vrijwilligers pakken een taak zelf op
   ("Ik doe dit") of geven hem terug. Bestuur en coördinator wijzen toe aan iedereen,
   aan zichzelf of aan Frion als groep.
3. Taken gereed melden, eventueel met een foto. Alleen een toegewezen taak kan gereed
   gemeld worden. Een gereed gemelde taak kan weer open gezet worden en de foto kan
   vervangen of verwijderd worden.
4. Gebreken melden: foto (verplicht), plek (keuzeknoppen), toelichting (niet verplicht),
   gevaarlijk ja/nee. De melder ziet de status van zijn melding (Nieuw, Taak gemaakt,
   Toegewezen, Gereed, Geen actie nodig). Bij "gevaarlijk" krijgt de coördinator een e-mail.
5. Taken aanmaken en wijzigen door bestuur en coördinator, op basis van de jaarplanning
   onderhoud, ook direct vanuit een melding ("Maak taak"). Bij een taak uit een melding
   is de werkgroep verplicht en de persoon niet; titel, omschrijving, foto, werkgroep
   (op basis van de plek) en deadline (gevaarlijk: morgen, anders over twee weken) zijn
   alvast ingevuld.    Een melding zonder taak kan op "Geen actie nodig" gezet worden, met een verplichte toelichting die de melder te zien krijgt.

Bouw niets buiten deze vijf functies zonder dat ik dat expliciet vraag. Nieuwe ideeën
zet je op een aparte "later"-lijst.

## Gebruikers en rechten
- Rollen: vrijwilliger, bestuur, coördinator onderhoud, Frion-begeleider.
  Iedereen logt in. Frion-cliënten loggen niet in.
- Rol en werkgroep zijn twee aparte dingen. Iemand kan in meerdere werkgroepen zitten.
- Vrijwilligers zien de taken van hun eigen werkgroepen en hun eigen meldingen.
- Bestuur en coördinator zien alles, wijzen toe en handelen meldingen af.
- Frion-begeleiders zien Dieren, Klussen en Tuinen. Taken voor Frion worden aan
  "Frion" als groep toegewezen; elke Frion-begeleider ziet ze onder "Mijn taken".
- Gereed melden, heropenen en foto's aanpassen mag iedereen uit de werkgroep, de
  persoon aan wie de taak is toegewezen, het bestuur en de coördinator.
- Rechten worden afgedwongen in de database, niet alleen door knoppen te verbergen.

## Leerdoel
Ik bouw deze app zelf om te leren hoe je een app maakt. Claude schrijft code, maar:
- Leg bij elke stap uit wat de code doet en waarom, in gewone taal.
- Laat me zelf kleine aanpassingen doen en geef me opdrachten om te oefenen,
  met tips en een oplossing om achteraf te controleren.
- Geef niet meer code dan nodig voor de stap
