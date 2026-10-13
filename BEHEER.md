# Beheerhandleiding Vrijwilligersapp

Deze handleiding is voor de beheerder van de app. Je hoeft geen programmeur te zijn.
De app is nog een ontwerp: alle gegevens zijn verzonnen en er wordt niets bewaard.

## Waar staat de app?
- **Code:** GitHub, organisatie `park-de-stadshoeve`, repository `Vrijwilligersapp`.
- **Online:** https://park-de-stadshoeve.github.io/Vrijwilligersapp/
- **Bestuursversie (demo):** dezelfde link met `?rol=bestuur` erachter.

## Welk bestand doet wat?
| Bestand | Wat staat erin | Wanneer pas je het aan? |
|---|---|---|
| `index.html` | Het geraamte: kopbalk, middenruimte, menu onderaan | Zelden |
| `stijl.css` | Het uiterlijk: kleuren, groottes, knoppen | Kleur of tekstgrootte veranderen |
| `app.js` | De logica en de voorbeeldgegevens | Plekken, werkgroepen, termijnen |
| `CLAUDE.md` | Instructies voor Claude en de stand van zaken | Als er afspraken veranderen |

## Veelvoorkomende aanpassingen (in `app.js`)
- **Plek op het park toevoegen:** in de lijst `PLEKKEN` (vóór "Overig"), en in
  `PLEK_WERKGROEP` bij welke werkgroep hij hoort.
- **Werkgroep toevoegen:** in de lijst `alleWerkgroepen`. Let op exact dezelfde spelling.
- **Standaard deadline bij een melding:** `DAGEN_GEVAARLIJK` en `DAGEN_NORMAAL`.
- **Hoe lang "Ongedaan maken" zichtbaar is:** `MELDING_DUUR` (in milliseconden).

## Kleuren aanpassen (in `stijl.css`)
Alle kleuren staan bovenaan bij `:root`. Houd voldoende contrast, zodat alles buiten in
de zon leesbaar blijft.

## Iets ging mis?
- **Pagina leeg na een wijziging?** Meestal een vergeten komma of haakje. Open het
  bestand in GitHub, klik op **History** en zet een eerdere versie terug.
- **Wijziging niet zichtbaar?** Wacht een à twee minuten en ververs de pagina.
- **Publiceren mislukt?** Kijk in GitHub onder **Actions**: rood kruisje = mislukt,
  groen vinkje = gelukt.

## Iemand anders beheerder maken
In GitHub: open de organisatie, kies **People** > **Invite member**, rol **Owner**.
