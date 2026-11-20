---
id: 8fafa26e-bc88-4098-954e-afc89edd9151
title: "Details of the chosen solution"
linkTitle: "Details of the chosen solution"
weight: 50
lastmod: 2026-11-20T22:36:53+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

The chosen solution described in more detail: architecture, components, data sources and information models, and how the data is retrieved from several sources.

## The solution concept

![The solution concept for pilot 6 in layers, read from the bottom up. Data sources: Udir (national tests and assessments), school administration systems (OAS), municipal systems and other sources. The SAMT-BU middle layer has trust (ID-porten, Maskinporten, the Population Register, Altinn Authorization), brokering, events and dialogue (data.altinn.no retrieves from the sources and gives one API to the channels, Altinn Events for thin events, Dialogporten for dialogues and notifications in the workspace) and semantics (a common information model, where it is open where the transformation happens). Channels: Min Kommune, vendor apps and the Altinn workspace (Altinn app). Users: parents and pupil (pupil mode). SAMT-BU delivers the information model, the rulebook, the service definition in data.altinn.no and event types in Altinn Events. Data flows upwards from the sources, and the rulebook and trust framework apply to the whole chain.](loesningskonsept-en.svg)

The solution concept shows pilot 6 in the same layers as the SAMT-BU concept, read from the bottom up:

- **Data sources:** Udir, the school systems, municipal archives and possibly other sources, such as sports.
- **The SAMT-BU middle layer** has three parts:
  - trust: ID-porten, Maskinporten, the Population Register and Altinn Authorization
  - brokering, events and dialogue: data.altinn.no with a dedicated service for parental access, Altinn Events for events and Dialogporten for dialogues and notifications in the Altinn workspace
  - semantics: a common information model, where it is open where the transformation happens (see [Choice of solution](/en/pilotering/pilot-6/loesningsvalg/))
- **Channels:** the consumers that build the end-user service – Min Kommune, the vendors' apps and Altinn, where an Altinn app built in Altinn Studio is used in the Altinn workspace.

data.altinn.no retrieves from the sources and offers one API to all the channels, so that no channel integrates directly with the sources. The rulebook applies to the whole chain.

## data.altinn.no

data.altinn.no is a generic broker for data sharing, managed by the Norwegian Digitalisation Agency (Digdir). All retrieval takes place in the context of a service, which controls who may retrieve which datasets and on what basis: legal authority, consent or both. Four properties matter most for pilot 6:

- **Only organisations can ask**, because the API requires a Maskinporten token issued to the organisation asking. The parent never uses the API directly.
- **Persons can be the subject.** The dataset overview already has datasets with the requirement that the subject must be a private individual.
- **No storage of case data.** Data is retrieved from the source every time. Only metadata about the retrieval is stored.
- **Pull-based.** The consumer asks for data, so notification of new data must come from Altinn Events.

Source: [docs.data.altinn.no](https://docs.data.altinn.no/).

## Dialogporten

![Min Kommune, vendor app and Altinn app create dialogues through Dialogporten, a common API for dialogues and notifications. The dialogues are shown in the Altinn workspace, so that parents get one inbox. The dialogue links to the channel's own solution. Dialogporten gives pilot 6 one inbox for parents across channels, the channels keep their own solution, and notification when new results are ready (flow B). To be clarified: how parents see dialogues concerning the child, who owns the dialogue when there are several channels, and how duplicate notifications are avoided. Three common solutions, three roles: data.altinn.no for data, Altinn Events for events and Dialogporten for dialogue and notification.](dialogporten-en.svg)

Dialogporten is a common Altinn solution that lets services show dialogues in the Altinn workspace, including services that are not Altinn apps. Min Kommune, the vendors' apps and a possible Altinn app can all create dialogues, and parents get one combined inbox across the channels. The channels keep their own solution for the full overview over time, and the dialogue links there.

Dialogporten fits with flow B (see [Actors and information flow](/en/pilotering/pilot-6/aktoerer-og-informasjonsflyt/)): when a channel has retrieved new data via data.altinn.no, it can create or update a dialogue. Three common solutions thus get three clear roles: data.altinn.no for data, Altinn Events for events and Dialogporten for dialogue and notification.

It must be clarified how parents can see dialogues concerning the child, who owns the dialogue when there are several channels, and how duplicate notifications are avoided.

## Basis

The figures and text build on the presentation [Samt-BU and pilot 6 – concept and solution](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=en-US&rs=en-US) (in Norwegian, [download](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)). On data.altinn.no in general: the presentation [Data.altinn.no](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Flibrary%2Freusable-solutions%2Fnorway%2Fdigdir-dan%2FDAN%2520-%2520DD.pptx&ui=en-US&rs=en-US) from Digdir (in Norwegian, [download](https://github.com/samt-x/samt-bu-files/raw/main/library/reusable-solutions/norway/digdir-dan/DAN%20-%20DD.pptx)).
