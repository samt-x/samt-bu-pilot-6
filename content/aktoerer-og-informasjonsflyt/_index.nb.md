---
id: 9df441eb-96d2-49d3-a015-8103b279a237
title: "Aktører og informasjonsflyt"
linkTitle: "Aktører og informasjonsflyt"
weight: 30
lastmod: 2026-11-20T22:36:53+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

Hvem som er involvert, hvor de aktuelle dataene ligger, og hvordan informasjonen flyter mellom aktørene i dag (AS-IS): foresatte, skoler og kommuner, Udir, systemleverandører og andre kilder.

Løsningskonseptet (se [Detaljering av valgt løsning](/pilotering/pilot-6/detaljering-av-valgt-loesning/)) har to flyter: henting ved behov og hendelsesstyrt henting.

## Flyt A: henting ved behov

![Flyt A i fem steg: 1) forelderen logger inn i kanalen med ID-porten; 2) kanalen sjekker foreldreansvar i Folkeregisteret; 3) kanalen kaller tjenesten «Foresattinnsyn» i data.altinn.no med elevens fødselsnummer som subjekt, autentisert med Maskinporten; 4) Udir og fagsystemene leverer data; 5) kanalen sammenstiller og viser utviklingen over tid som en samlet oversikt. Forelderen er aldri direkte bruker av data.altinn.no.](flyt-a-henting-ved-behov-nb.svg)

Typisk når forelderen åpner tjenesten:

1. Forelderen logger inn i kanalen med ID-porten.
2. Kanalen (konsumentløsningen) sjekker at innlogget person har foreldreansvar for eleven. data.altinn.no har allerede et relasjonsdatasett fra Folkeregisteret.
3. Konsumenten kaller tjenesten «Foresattinnsyn» i data.altinn.no med elevens fødselsnummer som subjekt, autentisert med Maskinporten som virksomhet.
4. data.altinn.no henter fra Udir og fagsystemene og minimerer dataene.
5. Konsumenten sammenstiller og viser utviklingen over tid.

data.altinn.no logger hvilken virksomhet som spurte, ikke hvilken forelder. Det må konsumenten logge selv.

## Flyt B: hendelsesstyrt henting

![Flyt B i fem steg: 1) et nytt resultat registreres i datakilden; 2) kilden publiserer en tynn hendelse i Altinn Events, bare en referanse; 3) kanalen mottar hendelsen gjennom et abonnement; 4) kanalen henter dataene via data.altinn.no, med tilgangskontroll og minimering; 5) forelderen får varsel via Dialogporten. Polling er et alternativ der kilden ikke publiserer hendelser, og om dataholderne kan publisere hendelser, må avklares med hver enkelt.](flyt-b-hendelsesstyrt-henting-nb.svg)

1. Et nytt resultat registreres i kilden, for eksempel resultat fra en nasjonal prøve.
2. Kilden publiserer en tynn hendelse i Altinn Events, bare en referanse og ingen fagdata.
3. Kanaler som abonnerer, mottar hendelsen.
4. Kanalen henter selve dataene via data.altinn.no, med samme tilgangskontroll og minimering som i flyt A.
5. Kanalen oppretter eller oppdaterer en dialog i Dialogporten, slik at forelderen ser i Altinn arbeidsflate at noe nytt finnes. Dialogen lenker tilbake til kanalens egen løsning.

Arbeidsdelingen er bevisst: Altinn Events signaliserer, data.altinn.no forvalter tilgang og fagdata. Der kilden ikke kan publisere hendelser, er polling jevnlig eller ved behov et fullverdig alternativ. Om dataholderne kan levere push, må avklares med hver aktør.

## Grunnlag

Figurene og teksten bygger på presentasjonen [Samt-BU og pilot 6 – konsept og løsning](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=nb-NO&rs=nb-NO) ([last ned](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)).
