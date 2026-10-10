---
id: 37cab3af-72bf-4dc1-9dd6-c63aac96a862
# id: auto-generert – kopierte verdier overskrives automatisk ved push
title: Om pilot 6
weight: 10
lastmod: 2026-10-10T14:41:03+02:00
last_editor: Erik Hagen

---
## INNLEDNING

Dette er en beskrivelse av plan for gjennomføring av pilot 6 – Foreldres tilgang til data. Selv om planen beskriver gjennomføringen som en fasedreven prosess, forutsettes det at vi arbeider iterativt, der enkelte faser gjentas ved behov.

## OMFANG OG AVGRENSNING

### Bakgrunn

Arbeidet tar utgangspunkt i casebeskrivelsen [6. Sentralisert tilgang til data foreldrene trenger](https://docs.samt-bu.no/behov/use-cases/06-sentralisert-datatilgang/).

Caset dreier seg om å gi foresatte enkel og oversiktlig tilgang til data som er relevante for å følge elevens utvikling, slik som nasjonale prøver, nasjonale kartlegginger, sluttvurderinger og karakterer når det er aktuelt.

Det finnes i dag ikke noe sentralt «sted» hvor foresatte kan finne all relevant informasjon om barnets faglige utvikling. Foreldre som ønsker slik oversikt, må lete mange steder og sette sammen informasjonen selv. I en slik prosess er det alltid fare for at informasjon går tapt, og det gjør at terskelen for å engasjere seg i barnets faglige utvikling blir høyere. En samlet oversikt vil trolig gjøre det enklere for foresatte å følge med og engasjere seg, også for foresatte som har mindre ressurser.

Relevante data ligger mange ulike steder: noe i fagsystemene (oppvekstadministrative systemer), noe i kommunens arkivsystemer og noe hos Udir, for å nevne noe. Det finnes ingen samlet oversikt som over tid viser utviklingen for den enkelte.

Så vidt SAMT-BU så langt har brakt på det rene, finnes det heller ingen standardiserte informasjonsmodeller og felles arkitekturprinsipper som gjør det enkelt å lage en sammenhengende tjeneste som dekker behovet. Det er også usikkert om det finnes API-er som er enkle å bruke, og som kan danne grunnlag for å hente ut relevante data.

### Pilotens målsetning

Piloten vil i første fase ha hovedfokus på å kartlegge dagens situasjon og mulighetene som finnes, og se nærmere på arkitekturen som må på plass for å kunne lage sluttbrukerløsninger.

Målet etter tre måneder er å:

- forstå behovet foresatte har for informasjon, og hvordan de ønsker tilgang til informasjonen om alt er perfekt (drømmereise)
- ha oversikt over aktørene, hvor de aktuelle dataene befinner seg og i hvilken grad de er tilgjengelige (AS-IS-beskrivelse)
- ha på plass et arkitekturmålbilde med regelbok og informasjonsmodeller som kan støtte opp under en framtidig løsning
- forstå sammenhengen mellom dette caset og de andre casene i SAMT-BU

Dette må avklares:

- Er det juridiske knuter her?
- Kan frivilligheten inviteres inn, for eksempel ved å hente data fra Idrettsforbundets dataplattform?
- Kan leverandørmarkedet lage sluttbrukerløsningen basert på et dataprodukt SAMT-BU tilbyr, enten gjennom et hackaton eller en «startoff-liknende» anskaffelse?

### Pilotens produkter

Piloten har følgende produkter:

1. Drømmereise for foreldrenes tilgang til data om eleven, med oversikt over hvilke data de ønsker
2. AS-IS-beskrivelse med oversikt over aktørene, systemlandskapet, aktuelle data og om det finnes enkle måter å få tilgang til data på (API)
3. Arkitekturmålbilde med regelbok og informasjonsmodeller som også kan danne grunnlag for et dataprodukt
4. Forslag til neste fase

Selve gjennomføringen av piloten skal også danne grunnlag for oppdatering av prosjektets «dreiebok» for gjennomføring av denne typen prosjekter.

### Hypoteser

Det antas at løsningen må realiseres basert på hendelsesdreven arkitektur og en virtuell kunnskapsgraf mot kildesystemene. Krav til løsningen for blant annet samtykke, hjemmel, fullmakt, representasjon, dataminimering, rettighetsstyring og logging/sporbarhet bør innarbeides i en egen regelbok i samsvar med EUs dataspaces.

En del av de sentrale dataene som skal vises, finnes i fagsystemer. Det vil derfor også være nødvendig å etablere kontakt med de eksisterende systemleverandørene.

### Avgrensning

Piloten skal i første omgang se på data innenfor skoleområdet og bare for elever under 18 år. Det kan bli aktuelt å se på idrettsdata også. I første iterasjon skal det ikke lages løsninger.

### Gevinsteiere

Det er først og fremst foreldre som vil få gevinst dersom piloten fører fram til en kjørende løsning. Men ingen offentlige organer «eier» foreldrenes behov. Den nærmeste gevinsteieren er derfor Digitaliseringsdirektoratet, som har et overordnet ansvar for digitale løsninger i offentlig sektor.

## BEMANNING

Piloten har behov for følgende kompetanse:

- Prosjektleder
- Domenekunnskap for AS-IS-kartlegging (Udir, Sikt og andre, og oversikt over leverandørmarkedet)
- Tjenestedesigner (til drømmereisen)
- Arkitekturgruppa og nasjonal arkitektur (målarkitektur)
- Modellgruppa (ontologi og kunnskapsgraf)
- Kunnskap om Altinn og KS Digitals dataplattform, avhengig av hvor dataproduktene skal tilbys

Bemanningen er ikke avklart ennå.

## GJENNOMFØRING

### Pilotens varighet

Oppstartstidspunktet er ikke avklart ennå.

### Pilotens arbeidspakker

Det er definert følgende arbeidspakker:

1. Drømmereise for foreldrenes tilgang til data om eleven, med oversikt over hvilke data de ønsker
2. AS-IS-beskrivelse med oversikt over aktørene, systemlandskapet, aktuelle data og om det finnes enkle måter å få tilgang til data på (API)
3. Arkitekturmålbilde med regelbok og informasjonsmodeller som også kan danne grunnlag for et dataprodukt
4. Forslag til neste fase

### Avhengigheter

Det er helt avgjørende at piloten får god innsikt i dagens løsninger. God kommunikasjon med Udir er derfor avgjørende, og det samme gjelder dagens systemleverandører.

### Viktige milepæler

Piloten har følgende viktige milepæler:

- Når drømmereisen foreligger
- Når AS-IS-beskrivelsen foreligger
- Når arkitekturmålbildet foreligger
- Når informasjonsmodellen er klar
- Når regelboka er klar
- Når det foreligger forslag til eventuell videreføring av piloten

### Praktisk gjennomføring

Piloten gjennomføres iterativt etter smidige prinsipper, i sprinter på to eller tre uker. Hver sprint starter med et planleggingsmøte og avsluttes med en demo. Det vurderes å kjøre felles demo i SAMT-BU-regi for alle piloter. I utgangspunktet er det ønskelig med standup for hele piloten annenhver dag, men etter hvert kan det være tilstrekkelig at arbeidet koordineres i hver arbeidspakke. Det bør gjennomføres minst én retrospektiv i løpet av pilotperioden.

Pilotens oppgaver følges opp som issues i [samt-bu-pilot-6](https://github.com/samt-x/samt-bu-pilot-6/issues).

### Kommunikasjon

Kommunikasjonsaktiviteter samordnes med kommunikasjonsrådgiveren i SAMT-BUs kjerneteam.
