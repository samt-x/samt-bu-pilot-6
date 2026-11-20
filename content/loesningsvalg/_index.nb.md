---
id: ec1bb1f4-17e6-45db-8388-5ebbab4595c6
title: "Løsningsvalg"
linkTitle: "Løsningsvalg"
weight: 40
lastmod: 2026-11-20T23:10:23+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

Hvilke løsningsalternativer som er vurdert for å gi foresatte samlet tilgang til dataene, hva som skiller dem, og hvilket alternativ som er valgt – med begrunnelse.

Løsningskonseptet bygger på data.altinn.no som felles formidler (se [Detaljering av valgt løsning](/pilotering/pilot-6/detaljering-av-valgt-loesning/)). Innenfor konseptet står to valg åpne: hvor transformasjonen til felles informasjonsmodell skjer, og hvilke kanaler som tilbyr sluttbrukertjenesten.

## Hvor skjer transformasjonen?

![Tre steder transformasjonen fra kildens format til felles modell kan skje: 1) i kilden, der Udir eller fagsystemene leverer i felles modell – målbildet, men høy terskel for leverandørene; 2) i data.altinn.no, der datasettene defineres i felles modell og kildeintegrasjonen oversetter – én transformasjon, mange konsumenter, en pragmatisk start som må avklares med data.altinn.no-teamet; 3) hos konsumenten, der hver kanal mapper selv – bør unngås fordi det gjenskaper punkt-til-punkt-problemet, og motsier konseptet.](hvor-skjer-transformasjonen-nb.svg)

Transformasjonen fra kildens format til felles modell kan i prinsippet skje tre steder:

1. **I kilden:** Udir eller fagsystemleverandøren leverer data i felles modell. Det er målbildet, men gir høy terskel.
2. **I data.altinn.no:** Datasettene i tjenesten defineres i felles modell, og kildeintegrasjonen oversetter. Det gir én transformasjon og mange konsumenter, og er en pragmatisk start. Om og hvordan data.altinn.no kan bære denne mappingen, må avklares med teamet.
3. **Hos konsumenten:** Hver kanal mapper selv. Det bør unngås, fordi det gjenskaper punkt-til-punkt-problemet konseptet skal løse.

## Kanaler for sluttbrukertjenesten

![Tre kanaler for sluttbrukertjenesten. A) Min Kommune: nærmest drømmereisen og en kanal foreldre allerede bruker; må avklare KS som virksomheten som spør, og behandlingsansvar. B) Leverandørapper: marked og innovasjon, flere fronter på samme dataprodukt; må avklare å åpne tjenesten for private konsumenter og oppslag på vegne av andre. C) Altinn-app i arbeidsflaten: bygget i Altinn Studio, forhåndsutfylling fra data.altinn.no, raskest til prototype; må avklare at den er skjemaorientert og svak som varig oversikt, og foresatte som representant for barnet. Alle kanalene bruker det samme API-et fra data.altinn.no.](kanaler-for-sluttbrukertjenesten-nb.svg)

Alle kanalene bruker det samme API-et fra data.altinn.no, så valget er ikke enten–eller, og ingen kanal integrerer direkte mot kildene.

- **A) Min Kommune** ligger nærmest drømmereisen og er en kanal foreldre allerede bruker. KS blir virksomheten som spør.
- **B) Leverandører** gir marked og innovasjon. Tilgangskravene i data.altinn.no settes per datasett, og mange krever i dag offentlig konsument. Tjenesten må derfor åpnes bevisst, og regelen om oppslag på vegne av andre må avklares.
- **C) Altinn:** en Altinn-app bygges i Altinn Studio og brukes i Altinn arbeidsflate. Det er raskest for en prototype og gir forhåndsutfylling fra data.altinn.no, men appen er skjemaorientert og egner seg dårlig som varig oversikt over tid. Om foresatte kan opptre for barnet i Altinn, må avklares.

Tjenester utenfor Altinn kan også vise dialoger og varsler i arbeidsflaten via Dialogporten.

## Grunnlag

Figurene og teksten bygger på presentasjonen [Samt-BU og pilot 6 – konsept og løsning](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=nb-NO&rs=nb-NO) ([last ned](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)).
