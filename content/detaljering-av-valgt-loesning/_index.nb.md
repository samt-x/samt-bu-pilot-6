---
id: 8fafa26e-bc88-4098-954e-afc89edd9151
title: "Detaljering av valgt løsning"
linkTitle: "Detaljering av valgt løsning"
weight: 50
lastmod: 2026-11-20T22:36:53+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

Den valgte løsningen beskrevet nærmere: arkitektur, komponenter, datakilder og informasjonsmodeller, og hvordan dataene hentes fra flere kilder.

## Løsningskonseptet

![Løsningskonseptet for pilot 6 i lag, lest nedenfra og opp. Datakilder: Udir (nasjonale prøver og kartlegginger), fagsystemer (OAS), kommunale fagsystem og andre kilder. SAMT-BU-mellomlaget har tillit (ID-porten, Maskinporten, Folkeregisteret, Altinn Autorisasjon), formidling, hendelser og dialog (data.altinn.no henter fra kildene og gir ett API til kanalene, Altinn Events for tynne hendelser, Dialogporten for dialoger og varsler i arbeidsflaten) og semantikk (felles informasjonsmodell, der det er åpent hvor transformasjonen skjer). Kanaler: Min Kommune, leverandørapper og Altinn arbeidsflate (Altinn-app). Brukere: foresatte og elev (elev-modus). SAMT-BU leverer informasjonsmodell, regelbok, tjenestedefinisjon i data.altinn.no og hendelsestyper i Altinn Events. Data flyter oppover fra kildene, og regelbok og tillitsrammeverk gjelder hele kjeden.](loesningskonsept-nb.svg)

Løsningskonseptet viser pilot 6 i de samme lagene som SAMT-BU-konseptet, lest nedenfra og opp:

- **Datakilder:** Udir, fagsystemene, kommunale arkiv og eventuelt andre kilder, som idrett.
- **SAMT-BU-mellomlaget** har tre deler:
  - tillit: ID-porten, Maskinporten, Folkeregisteret og Altinn Autorisasjon
  - formidling, hendelser og dialog: data.altinn.no med en egen tjeneste for foresattinnsyn, Altinn Events for hendelser og Dialogporten for dialoger og varsler i Altinn arbeidsflate
  - semantikk: felles informasjonsmodell, der det er åpent hvor transformasjonen skjer (se [Løsningsvalg](/pilotering/pilot-6/loesningsvalg/))
- **Kanaler:** konsumentene som bygger sluttbrukertjenesten – Min Kommune, leverandørenes apper og Altinn, der en Altinn-app bygget i Altinn Studio brukes i Altinn arbeidsflate.

data.altinn.no henter fra kildene og tilbyr ett API til alle kanalene, slik at ingen kanal integrerer direkte mot kildene. Regelboka gjelder hele kjeden.

## data.altinn.no

data.altinn.no er en generisk megler for datadeling, forvaltet av Digdir. All uthenting skjer i kontekst av en tjeneste, som styrer hvem som får hente hvilke datasett og på hvilket grunnlag: hjemmel, samtykke eller begge. Fire egenskaper betyr mest for pilot 6:

- **Bare virksomheter kan spørre**, fordi API-et krever Maskinporten-token utstedt til virksomheten som spør. Forelderen er aldri direkte bruker av API-et.
- **Personer kan være subjekt.** Datasettoversikten har allerede datasett med kravet at subjektet må være en privatperson.
- **Ingen lagring av fagdata.** Data hentes fra kilden hver gang. Bare metadata om uthentingen lagres.
- **Pull-basert.** Konsumenten spør etter data, så varsling om nye data må komme fra Altinn Events.

Kilde: [docs.data.altinn.no](https://docs.data.altinn.no/).

## Dialogporten

![Min Kommune, leverandørapp og Altinn-app oppretter dialoger gjennom Dialogporten, et felles API for dialoger og varsler. Dialogene vises i Altinn arbeidsflate, slik at foresatte får én innboks. Dialogen lenker til kanalens egen løsning. Dialogporten gir pilot 6 én innboks for foresatte på tvers av kanaler, kanalene beholder egen løsning, og varsel når nye resultater er klare (flyt B). Må avklares: hvordan foresatte ser dialoger som gjelder barnet, hvem som eier dialogen når flere kanaler finnes, og hvordan doble varsler unngås. Tre fellesløsninger, tre roller: data.altinn.no for data, Altinn Events for hendelser og Dialogporten for dialog og varsel.](dialogporten-nb.svg)

Dialogporten er en fellesløsning i Altinn som lar tjenester vise dialoger i Altinn arbeidsflate, også tjenester som ikke er Altinn-apper. Min Kommune, leverandørenes apper og en eventuell Altinn-app kan alle opprette dialoger, og foresatte får én samlet innboks på tvers av kanalene. Kanalene beholder sin egen løsning for den fulle oversikten over tid, og dialogen lenker dit.

Dialogporten passer sammen med flyt B (se [Aktører og informasjonsflyt](/pilotering/pilot-6/aktoerer-og-informasjonsflyt/)): når en kanal har hentet nye data via data.altinn.no, kan den opprette eller oppdatere en dialog. Tre fellesløsninger får dermed tre tydelige roller: data.altinn.no for data, Altinn Events for hendelser og Dialogporten for dialog og varsel.

Det må avklares hvordan foresatte kan se dialoger som gjelder barnet, hvem som eier dialogen når flere kanaler finnes, og hvordan doble varsler unngås.

## Grunnlag

Figurene og teksten bygger på presentasjonen [Samt-BU og pilot 6 – konsept og løsning](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=nb-NO&rs=nb-NO) ([last ned](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)). Om data.altinn.no generelt: presentasjonen [Data.altinn.no](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Flibrary%2Freusable-solutions%2Fnorway%2Fdigdir-dan%2FDAN%2520-%2520DD.pptx&ui=nb-NO&rs=nb-NO) fra Digdir ([last ned](https://github.com/samt-x/samt-bu-files/raw/main/library/reusable-solutions/norway/digdir-dan/DAN%20-%20DD.pptx)).
