# Prosedyrer

Roller omtalt her:

* Produkteier
* Fagansvarlig
* Utviklingsteam
* NHN kundesenter
* Superbruker
* Brukere

## Ny database i eFORSK (prod)

Utføres av fagansvarlige.

#### Forberedelser

* Det må først foreligge en avtale om bruk av eFORSK. Informasjon fra denne brukes for å sette opp databasen. http://virksomhetsportal.helsemn.no/omrader/hemit/enhet/Systemutvikling/Oppdrag/Forms/AllItems.aspx?RootFolder=%2fomrader%2fhemit%2fenhet%2fSystemutvikling%2fOppdrag%2feFORSK%5fBruk%20av%20somatropin%5fforskningsstudie%5fHMR&FolderCTID=&View=%7b7BD7272F%2dCD5E%2d4156%2d87CF%2d9F1921AF505A%7d
* Brukere som skal ha tilgang må inn i Falk, send e-post til disse: "Fyll ut skjema på https://falk.eforsk.nhn.no/u/apply?app=eFORSK for å klargjøre din bruker i eFORSK. Lokasjon trengs ikke besvares, denne er ikke klar ennå."
* Hvis ePROM:
  * Bestill bestillersystem i ePROM til systemutvikling@hemit.no: "Bestiller bestillersystem i QA og PROD med navn [sett inn prosjektnavnet], send API-nøkler i retur". Benytt API-nøkkel for QA til testmodus, og API-nøkkel for PROD til ikke-testmodus. Etter API-nøkler er lagt inn i eFORSK, klikk "Test ePROM tilkobling" knappen.
  
#### Når dette er gjort, gå videre med selve opprettelsen i eFORSK
  
* Aktiver database på https://eforsk.nhn.no/ administrasjon
* Gi tilgang til brukere i FALK. Superbruker bør få tilgangstildererollen for databasen. https://falk.eforsk.nhn.no/u/a/orders/4 **Vær nøye på å gi riktige tilganger**
* Hvis gjenstående ledige databaser har nådd 3 eller mindre, bestill opp flere fra NHN kundesenter@nhn.no: "Bestiller herved opp 10 nye databaser for eFORSK PROD med tilhørende oppslag i keys-fila."

## Ny demodatabase i eFORSK (mrsweb)

Utføres av fagansvarlig? Evt utviklingsteam..

Når en person vil ha demodatabase;

* Finn ledig statisk fødselsnummer i test p-reg
* Logg på administrasjonen som administrator på https://mrsweb.hemit.org/eFORSK/
* Finn ledig database. 
  * Legg personens navn i databasenavnet.
  * Legg inn personens navn i "Navn på databaseansvarlig ".
  * Legg til fødselsnummer i fakturafeltet slik at vi har det lagret
  * Aktiver ePROM, gjenbruk API nøkler fra andre databaser
  * Aktiver alle funksjoner til utprøving
* Logg på falk med fødselsnummeret og søk tilgang til databasen
* Logg på falk som eFORSK administrator og finn søknaden, gi databaseansvarlig rollen til databasen, og tilgangstildeler rollen til databasen.

## Planlegging av ny versjon

Utføres av utviklingsteam, fagansvarlige og produkteier

todo

## Produksjonssetting av ny versjon

Utføres av utviklingsteam (?)

* Hold endringslogg i brukermanual oppdatert på endringer og datoer fortløpende
* Logg på eFORSK prod i administrasjon og opprett nye varsler for ny versjon (se tidligere varsler for eksempel her)
* (Send ut e-post til alle aktive brukere siste måned med varsler om ny versjon?)
* Etter produksjonssetting, sjekk status på integrasjoner i eFORSK administrasjon
* Følg opp feil og advarsler i splunk
* Oppdater brukermanual

## Nytt ePROM skjema

todo

## Henvendelser fra brukere

Skjer i følgende rekkefølge:

Brukere (og potensielle brukere) av eFORSK skal via sin forskningsavdeling få en superbruker som dem henvender seg til. Brukere har ikke direkte kontakt med andre i normale tilfeller. https://www.helseforskningsportalen.no/ se kontaktinformasjon. Brukere og superbrukere støtter seg først og fremst på brukermanualen.

Hvis superbruker ikke kan hjelpe eller har svar, tar superbruker videre kontakt med fagansvarlig.

Hvis fagansvarlig ikke kan hjelpe eller har svar, tar fagansvarlig videre kontakt med utviklingsteam (evt enda et ledd med produkteier?).

Utviklingsteam oppdaterer brukermanual der det er hensiktsmessig.

## Feil i løsningen

Brukere tar kontakt med NHN kundeservice som anvist i footer på eFORSK.

NHN kundesenter tar i tur kontakt med utviklingsteam hvis dem ikke kan hjelpe.