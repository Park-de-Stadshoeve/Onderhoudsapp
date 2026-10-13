# Vrijwilligersapp Park de Stadshoeve

## Context
Ik bouw een mobiele app voor de vrijwilligers van Park de Stadshoeve in Zwolle-Stadshagen,
een wijkpark met kinderboerderij. Het park wordt gerund door Stichting de Stadshoeve,
met ongeveer 40 vrijwilligers. De stichting heeft geen personeel. Dagbesteding Frion doet
doordeweeks de dierverzorging, het groenonderhoud en klein onderhoud. Er is een
coördinator onderhoud (meestal het bestuurslid met die portefeuille). Onderhoud wordt
gepland via een meerjarenonderhoudsplan (MJOP), een jaarplanning en een maandplanning.

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
4. Gebreken melden: foto (verplicht), plek (keuzeknoppen, verplicht), toelichting (niet
   verplicht), gevaarlijk ja/nee (standaard nee). De melder ziet de status van zijn
   melding (Nieuw, Taak gemaakt, Toegewezen, Gereed, Geen actie nodig). Bij "gevaarlijk"
   krijgt de coördinator een e-mail.
5. Taken aanmaken en wijzigen door bestuur en coördinator, op basis van de jaarplanning
   onderhoud, ook direct vanuit een melding ("Maak taak"). Elke taak heeft een
   verplichte plek (zelfde keuzes als bij melden) en een verplichte werkgroep; de
   persoon is niet verplicht. Bij een taak uit een melding zijn titel, omschrijving,
   foto, plek, werkgroep (op basis van de plek) en deadline (gevaarlijk: morgen, anders
   over twee weken) alvast ingevuld. Een melding zonder taak kan op "Geen actie nodig"
   gezet worden, met een verplichte toelichting die de melder te zien krijgt.

Bouw niets buiten deze vijf functies zonder dat ik dat expliciet vraag. Nieuwe ideeën
zet je op de later-lijst onderaan dit bestand.

## Gebruikers en rechten
- Rollen: vrijwilliger, bestuur, coördinator onderhoud, Frion-begeleider.
  Iedereen logt in. Frion-cliënten loggen niet in.
- Rol en werkgroep zijn twee aparte dingen. Iemand kan in meerdere werkgroepen zitten.
  Een bestuurslid kan ook gewoon lid zijn van werkgroepen.
- Vrijwilligers zien de taken van hun eigen werkgroepen en hun eigen meldingen.
- Bestuur en coördinator zien alles, maken en wijzigen taken, wijzen toe en handelen
  meldingen af.
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
- Doe niet meer dan nodig voor de stap waar we zijn. Eén stap tegelijk.
- Vertel vóór je bestanden wijzigt wat je gaat doen en welke bestanden het raakt.
  Vat na afloop samen wat er veranderd is.

## Hoe je met mij werkt
- Stel eerst vragen voordat je iets bouwt of adviseert, tot het doel helder is.
  Stel maximaal 3 vragen tegelijk, de belangrijkste eerst, met je advies erbij.
- Geef directe, to-the-point feedback. Zeg het gewoon als een idee niet goed is,
  te groot is of onnodig ingewikkeld. Geef dan een beter alternatief.
- Leg technische begrippen in één zin uit wanneer ze voor het eerst voorkomen.
- Werk in kleine stappen. Elke stap levert iets op dat ik op mijn telefoon kan testen.
- Benoem bij elke keuze: kosten per maand, onderhoudslast voor een niet-programmeur,
  en privacygevolgen.
- Maak per stap een commit met een duidelijke Nederlandse beschrijving.
- Antwoord in het Nederlands.

## Platform
- Frontend: Progressive Web App (PWA) in HTML, CSS en JavaScript. Mobile-first.
  Geen zwaar framework en geen build-stap tenzij er een duidelijke reden is.
- Backend: beheerde dienst (bijv. Supabase) voor database, login en foto-opslag,
  met dataopslag in de EU. Bouw nooit zelf login of wachtwoordbeheer.
- Inloggen via een link in de mail (magic link), zonder wachtwoord.
- Code staat in GitHub: organisatie park-de-stadshoeve, repository Vrijwilligersapp.
  Hosting via GitHub Pages: https://park-de-stadshoeve.github.io/Vrijwilligersapp/
  Budget: hooguit een paar euro per maand.
- De repository is openbaar. Zet er nooit echte namen, persoonsgegevens, wachtwoorden,
  geheime sleutels of interne stukken van de stichting in. Een publieke sleutel die
  bedoeld is voor de browser mag wel; een geheime of beheerderssleutel nooit.
- Gebruikers, werkgroepen en plekken op het park worden beheerd via een beheerscherm,
  niet in de code.
- Meldingen naar de coördinator gaan per e-mail. Geen WhatsApp (kosten, onderhoud, AVG).
- Waarschuw me direct als een keuze een beveiligingsrisico of extra kosten oplevert.

## Uitgangspunten
- Onderhoudbaarheid door een niet-programmeur weegt zwaarder dan slimme oplossingen.
  Houd de code simpel, geef alles duidelijke Nederlandse namen en zet uitleg in de code.
- De app werkt op zowel iPhone als Android, zonder app store.
- De app moet bruikbaar blijven bij slecht bereik buiten op het park.
- AVG: sla zo min mogelijk persoonsgegevens op (voornaam is genoeg). Leg vast wie
  foto's mag zien en hoe lang ze bewaard blijven. Verklein foto's en verwijder
  locatiegegevens voor upload. Let op foto's waarop cliënten, kinderen of bezoekers
  staan.
- Beheer van gebruikers (toevoegen, verwijderen, werkgroep of rol wijzigen) moet door
  een niet-technische beheerder te doen zijn.
- Lever bij elke opgeleverde stap een korte beheerhandleiding in gewone taal, en houd
  BEHEER.md in de repository bij.

## UI- en designregels
- Mobile-first: ontwerp voor één hand en duimbereik. Belangrijke knoppen staan onderaan.
- Tikdoelen zijn minimaal 44×44 pt (Apple) en 48×48 dp (Android), met ruimte ertussen.
- Eén hoofdactie per scherm of kaartje. Maximaal 4–5 items in de navigatie.
- Tekst is minimaal 16 px en in eenvoudige taal (B1). Gebruik geen jargon.
- Hoog contrast (WCAG AA) zodat alles leesbaar is in de zon. Gebruik nooit alleen
  kleur om iets duidelijk te maken.
- Een taak gereed melden of een gebrek melden kost maximaal 3 tikken plus de foto.
  Formulieren zijn kort en hebben slimme standaardwaarden. Kies liever keuzeknoppen
  dan typen.
- Elke actie geeft een melding met "Ongedaan maken", in plaats van "Weet je het zeker?".
- Inloggen gebeurt eenmalig per toestel. Daarna blijft de gebruiker ingelogd.
- Schermen laden snel. Geef direct zichtbare feedback na elke tik (laden, gelukt, fout).
- Foutmeldingen zeggen wat er mis is en wat je moet doen.
- De gebruikers zijn vrijwilligers van 16 tot 80+ met wisselende digitale vaardigheid.
  Test elk ontwerp tegen de vraag: snapt een vrijwilliger dit zonder uitleg?

## Stand van zaken
Werk deze sectie bij aan het eind van elke stap.

Klaar (als werkend ontwerp met voorbeeldgegevens, nog zonder database):
- Alle vijf de functies, verdeeld over drie bestanden: index.html (geraamte),
  stijl.css (uiterlijk) en app.js (logica en voorbeeldgegevens).
- Demo: "?rol=bestuur" achter de link maakt Kirsten bestuurslid.
- Menu onderaan: Mijn taken, Werkgroep, Melden, Meldingen.
- Elke actie heeft "Ongedaan maken" (6 seconden).
- De status van een melding wordt afgeleid van de gekoppelde taak (taakId), niet
  apart opgeslagen.
- Plekken op het park staan in PLEKKEN; de standaardwerkgroep per plek in
  PLEK_WERKGROEP.
- De voorbeeldgegevens gebruiken verzonnen namen (Kirsten, Piet, Fatima, Kees,
  Sanne, Jan).

Volgende stappen:
0. Demo-trucje "?rol=bestuur" verwijderen uit app.js zodra echt inloggen werkt.
1. Feedback van het bestuur verwerken.
2. Database en inloggen koppelen. Daarbij:
   - één tabel gebruikers met per persoon een rol en werkgroepen;
   - rechten afdwingen in de database;
   - foto's verkleinen en locatiegegevens verwijderen voor upload;
   - bewaartermijn voor foto's afspreken;
   - vastleggen wie de foto bij een melding mag zien (voorstel: de melder, de
     werkgroep van de taak, bestuur en coördinator);
   - e-mail aan de coördinator bij een gevaarlijke melding;
   - beheerscherm voor gebruikers, werkgroepen en plekken.

## Later-lijst
1. Geschiedenis per taak: wie wat wanneer deed.
2. Bericht aan de werkgroep als een taak is teruggegeven.
3. WhatsApp-bericht bij een gevaarlijke melding (afgeraden: kosten, onderhoud, AVG).
4. Filters op de schermen. Pas bepalen na een paar weken gebruik.
5. Taken verwijderen (bijvoorbeeld een taak die per ongeluk is aangemaakt).
