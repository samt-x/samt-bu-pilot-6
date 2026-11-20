---
id: 9df441eb-96d2-49d3-a015-8103b279a237
title: "Actors and information flow"
linkTitle: "Actors and information flow"
weight: 50
lastmod: 2026-11-21T00:25:33+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

Who is involved, and how information flows between the actors in the chosen solution: parents and guardians, the channels, the common Altinn solutions and the data sources. The flow today is described under [Current situation](/en/pilotering/pilot-6/naasituasjon/aktoerer-og-informasjonsflyt/), and the desired flow under [Target picture](/en/pilotering/pilot-6/maalbilde/aktoerer-og-informasjonsflyt/).

The solution concept (see [Chosen solution now](/en/pilotering/pilot-6/loesningsvalg/valgt-loesning-naa/)) has two flows: retrieval on demand and event-driven retrieval.

## Flow A: retrieval on demand

![Flow A in five steps: 1) the parent logs in to the channel with ID-porten; 2) the channel checks custody in the Population Register; 3) the channel calls the service «Foresattinnsyn» in data.altinn.no with the pupil's national identity number as subject, authenticated with Maskinporten; 4) Udir and the school systems deliver data; 5) the channel combines and shows progress over time as a combined overview. The parent never uses data.altinn.no directly.](flyt-a-henting-ved-behov-en.svg)

Typically when the parent opens the service:

1. The parent logs in to the channel with ID-porten.
2. The channel (the consumer solution) checks that the logged-in person has parental responsibility for the pupil. data.altinn.no already has a relationship dataset from the Population Register.
3. The consumer calls the service «Foresattinnsyn» (parental access) in data.altinn.no with the pupil's national identity number as subject, authenticated with Maskinporten as an organisation.
4. data.altinn.no retrieves from Udir and the school systems and minimises the data.
5. The consumer combines and shows progress over time.

data.altinn.no logs which organisation asked, not which parent. The consumer must log that itself.

## Flow B: event-driven retrieval

![Flow B in five steps: 1) a new result is registered in the data source; 2) the source publishes a thin event in Altinn Events, only a reference; 3) the channel receives the event through a subscription; 4) the channel retrieves the data via data.altinn.no, with access control and minimisation; 5) the parent is notified via Dialogporten. Polling is an alternative where the source does not publish events, and whether data holders can publish events must be clarified with each of them.](flyt-b-hendelsesstyrt-henting-en.svg)

1. A new result is registered in the source, for example a result from a national test.
2. The source publishes a thin event in Altinn Events – only a reference, no case data.
3. Channels that subscribe receive the event.
4. The channel retrieves the actual data via data.altinn.no, with the same access control and minimisation as in flow A.
5. The channel creates or updates a dialogue in Dialogporten, so that the parent sees in the Altinn workspace that something new exists. The dialogue links back to the channel's own solution.

The division of work is deliberate: Altinn Events signals, data.altinn.no manages access and case data. Where the source cannot publish events, regular or on-demand polling is a full alternative. Whether the data holders can deliver push must be clarified with each actor.

## Basis

The figures and text build on the presentation [Samt-BU and pilot 6 – concept and solution](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=en-US&rs=en-US) (in Norwegian, [download](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)).
