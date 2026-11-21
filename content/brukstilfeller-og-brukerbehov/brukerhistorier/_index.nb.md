---
id: 34bd5d8b-c124-43c0-bb51-08ffd6505cf4
title: "Brukerhistorier"
linkTitle: "Brukerhistorier"
weight: 10
lastmod: 2026-11-21T00:22:24+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

Rollene og aktørene i pilot 6, noen personas, og behovene brutt ned i brukerhistorier på formen «Som … ønsker jeg … slik at …». Brukerhistoriene er grunnlaget for å prioritere hva piloten skal vise, og for å teste løsningen.

Alt på siden er et førsteutkast. Rollene står her inntil det finnes et felles rolleregister på tvers av casene. Da bør de flyttes dit, og denne siden lenke til registeret.

## Roller og aktører

Rollene er hentet fra [case 6](/behov/use-cases/06-sentralisert-datatilgang/), [Om pilot 6](/pilotering/pilot-6/om-pilot-6/) og [løsningskonseptet](/pilotering/pilot-6/loesningsvalg/valgt-loesning-naa/). En aktør kan ha flere roller, og en rolle kan fylles av flere aktører.

### Sluttbrukere

| Rolle | Hvem | Hva rollen gjør i pilot 6 |
|---|---|---|
| **Foresatt** | Person med foreldreansvar for eleven | Følger elevens faglige utvikling. Den viktigste brukeren og den som har gevinsten. |
| **Elev** | Barn i grunnskolen, under 18 år | Ser sin egen informasjon i elev-modus, og har rett til å medvirke. |
| **Annen omsorgsperson** | For eksempel fosterforeldre, verge eller forelder uten foreldreansvar | Kan ha behov for innsyn, men har ikke nødvendigvis rett til det. Må avklares juridisk. |

### Offentlige aktører og dataholdere

| Rolle | Hvem | Hva rollen gjør i pilot 6 |
|---|---|---|
| **Skole** | Kontaktlærer, faglærer, rektor | Registrerer vurderinger og fravær, og følger opp eleven sammen med foresatte. |
| **Skoleeier** | Kommunen | Ansvarlig for grunnskolen, fagsystemene og arkivet. Behandlingsansvarlig for mye av dataene. |
| **Utdanningsdirektoratet (Udir)** | Statlig dataholder | Har resultater fra nasjonale prøver og kartlegginger. |
| **Folkeregisteret** | Skatteetaten | Kilde til hvem som har foreldreansvar. |
| **Andre dataholdere** | For eksempel idretten | Mulige kilder senere. Utenfor avgrensningen i første omgang. |

### Leverandører og fellesløsninger

| Rolle | Hvem | Hva rollen gjør i pilot 6 |
|---|---|---|
| **Fagsystemleverandør** | Leverandører av oppvekstadministrative systemer (OAS) | Har mye av dataene og må kunne levere dem videre. |
| **Kanaltilbyder** | KS (Min Kommune), apputviklere, Altinn | Lager sluttbrukertjenesten. Er virksomheten som spør etter data. |
| **Formidler** | Digdir (data.altinn.no, Altinn Events, Dialogporten) | Formidler data, hendelser og dialoger mellom kildene og kanalene. |
| **Regeleier** | SAMT-BU, senere en varig forvalter | Forvalter informasjonsmodellen og regelboka. |

## Personas

Personasene er oppdiktet. De bygger ikke på innsiktsarbeid, og må kvalitetssikres, for eksempel gjennom intervjuer med foresatte, slik case 6 foreslår. Amir er hentet fra presentasjonen av løsningskonseptet.

| Persona | Rolle | Situasjon | Hva som betyr mest |
|---|---|---|---|
| **Amir**, 12 år | Elev | Går i 7. klasse. Liker matte, sliter med lesing. | Å se sine egne resultater, og vite hva foreldrene ser. |
| **Mona**, Amirs mor | Foresatt | Jobber fullt, vant med digitale tjenester, bruker Min Kommune. | Én oversikt, og varsel når noe nytt kommer. |
| **Piotr**, far til to | Foresatt | Skiftarbeid, norsk som andrespråk, kjenner ikke skolesystemet godt. | Å forstå hva resultatene betyr, og hva han kan gjøre. |
| **Lise og Erlend** | Foresatte | Skilt, barna bor fast hos begge. Begge har foreldreansvar. | At begge ser det samme, uten å gå via hverandre. |
| **Nora**, 15 år | Elev | Går i 10. klasse. | Å ha mer å si om hva som deles med foreldrene. |

## Brukerhistorier

Kolonnen **Kilde** viser hvor historien kommer fra: *Case 6*, *Om pilot 6*, *Konsept* (presentasjonen av løsningskonseptet) eller *Forslag* (vårt eget, ikke i kildene). Prioritet settes senere.

### Foresatt

| Id | Som … | ønsker jeg … | slik at … | Kilde |
|---|---|---|---|---|
| F1 | foresatt | å se resultater fra nasjonale prøver og kartlegginger, vurderinger og karakterer for barnet mitt på ett sted | jeg slipper å lete i flere systemer og sette sammen bildet selv | Case 6 |
| F2 | foresatt | å se utviklingen over tid, også på tvers av skoleår og skolebytte | jeg forstår om barnet utvikler seg som forventet | Case 6 |
| F3 | foresatt | å se fraværet til barnet mitt i samme oversikt | jeg ser fravær og resultater i sammenheng | Konsept |
| F4 | foresatt | å få varsel når nye resultater er klare | jeg kan følge opp mens det er aktuelt | Konsept |
| F5 | foresatt | å logge inn med ID-porten og bare se barn jeg har foreldreansvar for | jeg er trygg på at ingen andre ser barnets data | Konsept |
| F6 | foresatt | å få oversikten i en tjeneste jeg allerede bruker, for eksempel Min Kommune | jeg ikke må ta i bruk enda en tjeneste | Case 6 |
| F7 | foresatt med lite kjennskap til skolesystemet | å få forklart hva resultatene betyr, i et enkelt språk | jeg kan følge opp barnet like godt som andre foreldre | Case 6, Forslag |
| F8 | foresatt med delt omsorg | at begge foresatte med foreldreansvar ser den samme informasjonen | vi har samme grunnlag når vi følger opp barnet | Forslag |
| F9 | foresatt | å se hvem som har hentet barnets data, og når | jeg kan stole på at dataene ikke misbrukes | Om pilot 6 |
| F10 | foresatt | å se hvor hver opplysning kommer fra, og hvor jeg melder fra om feil | feil blir rettet i kilden | Forslag |

### Elev

| Id | Som … | ønsker jeg … | slik at … | Kilde |
|---|---|---|---|---|
| E1 | elev | å se mine egne resultater og min utvikling | jeg kan følge med på hvordan det går | Case 6 |
| E2 | elev | å vite hva foreldrene mine kan se om meg | jeg vet hva som deles | Case 6 |
| E3 | eldre elev | å ha mer å si om hva som deles med foreldrene etter hvert som jeg blir eldre | retten min til å medvirke blir tatt på alvor | Konsept, må avklares juridisk |

### Skole og skoleeier

| Id | Som … | ønsker jeg … | slik at … | Kilde |
|---|---|---|---|---|
| S1 | kontaktlærer | at foresatte har oversikten før utviklingssamtalen | samtalen kan handle om oppfølging, ikke om å gå gjennom resultater | Forslag |
| S2 | skoleeier | at dataene deles fra fagsystemene vi allerede har | skolene slipper å registrere det samme flere steder | Forslag |
| S3 | skoleeier | at tilgangen til dataene følger samme regler i alle kanaler | vi oppfyller ansvaret vårt som behandlingsansvarlig | Om pilot 6 |

### Dataholdere og leverandører

| Id | Som … | ønsker jeg … | slik at … | Kilde |
|---|---|---|---|---|
| D1 | dataholder (Udir) | å dele dataene én gang gjennom data.altinn.no | jeg slipper egne integrasjoner mot hver kanal | Konsept |
| D2 | dataholder | at bare virksomheter med hjemmel eller samtykke får hente data, og at uthentingen logges | jeg vet hvem som har fått dataene, og på hvilket grunnlag | Konsept |
| D3 | fagsystemleverandør | en felles informasjonsmodell og API-beskrivelse | jeg kan levere data i samme format til alle | Om pilot 6 |
| D4 | kanaltilbyder | ett API for alle kildene | jeg kan lage tjenesten uten å integrere mot hver kilde | Konsept |
| D5 | kanaltilbyder | å abonnere på hendelser om nye resultater | jeg kan varsle foresatte uten å spørre etter nye data hele tiden | Konsept |
| D6 | regeleier | at kravene til hjemmel, samtykke, representasjon, dataminimering og logging står i én regelbok | alle kanaler følger de samme reglene | Om pilot 6 |

## Neste steg

- Kvalitetssikre roller, personas og historier med foresatte, elever og skoler.
- Prioritere historiene og knytte dem til [brukerreisene i målbildet](/pilotering/pilot-6/maalbilde/brukerreiser/).
- Avklare de juridiske spørsmålene: annen omsorgsperson (rolle), F8 og E3.
- Vurdere et felles rolleregister på tvers av casene.
