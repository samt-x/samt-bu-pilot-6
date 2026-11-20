---
id: 87e27b2c-0de7-469c-9ac9-7ed0d5c59ad9
title: "Alternative solutions"
linkTitle: "Alternative solutions"
weight: 10

---

{{< i-arbeid >}}

Which solution alternatives have been considered for giving parents and guardians combined access to the data, and what distinguishes them. What has been chosen, and why, is described under [Chosen solution now](/en/pilotering/pilot-6/loesningsvalg/valgt-loesning-naa/).

The solution concept builds on data.altinn.no as a common broker. Within the concept, two choices are open: where the transformation to the common information model happens, and which channels offer the end-user service.

## Where does the transformation happen?

![Three places where the transformation from the source's format to the common model can happen: 1) in the source, where Udir or the school systems deliver in the common model – the target, but a high threshold for the vendors; 2) in data.altinn.no, where the datasets are defined in the common model and the source integration translates – one transformation, many consumers, a pragmatic start to be clarified with the data.altinn.no team; 3) at the consumer, where each channel maps on its own – should be avoided because it recreates the point-to-point problem, and contradicts the concept.](hvor-skjer-transformasjonen-en.svg)

In principle, the transformation from the source's format to the common model can happen in three places:

1. **In the source:** Udir or the school system vendor delivers data in the common model. This is the target, but it means a high threshold.
2. **In data.altinn.no:** The datasets in the service are defined in the common model, and the source integration translates. This gives one transformation and many consumers, and is a pragmatic start. Whether and how data.altinn.no can carry this mapping must be clarified with the team.
3. **At the consumer:** Each channel maps on its own. This should be avoided, because it recreates the point-to-point problem the concept is meant to solve.

## Channels for the end-user service

![Three channels for the end-user service. A) Min Kommune: closest to the dream journey and a channel parents already use; to be clarified: KS as the organisation that asks, and controller responsibility. B) Vendor apps: market and innovation, several front ends on the same data product; to be clarified: opening the service to private consumers and look-ups on behalf of others. C) Altinn app in the workspace: built in Altinn Studio, pre-filling from data.altinn.no, fastest to a prototype; to be clarified: it is form-oriented and weak as a lasting overview, and parents as representatives of the child. All channels use the same API from data.altinn.no.](kanaler-for-sluttbrukertjenesten-en.svg)

All the channels use the same API from data.altinn.no, so the choice is not either–or, and no channel integrates directly with the sources.

- **A) Min Kommune** (the municipal app) is closest to the dream journey and is a channel parents already use. KS becomes the organisation that asks.
- **B) Vendors** bring market and innovation. The access requirements in data.altinn.no are set per dataset, and many currently require a public-sector consumer. The service must therefore be opened deliberately, and the rule on look-ups on behalf of others must be clarified.
- **C) Altinn:** an Altinn app is built in Altinn Studio and used in the Altinn workspace. This is fastest for a prototype and gives pre-filling from data.altinn.no, but the app is form-oriented and poorly suited as a lasting overview over time. Whether parents can act for the child in Altinn must be clarified.

Services outside Altinn can also show dialogues and notifications in the workspace via Dialogporten.

## Basis

The figures and text build on the presentation [Samt-BU and pilot 6 – concept and solution](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2Fsamt-x%2Fsamt-bu-files%2Fmain%2Fprojects%2Fsamt-bu%2Fsubproject%2Fpilot-6%2FSamt-BU-pilot6-konsept-og-losning.pptx&ui=en-US&rs=en-US) (in Norwegian, [download](https://github.com/samt-x/samt-bu-files/raw/main/projects/samt-bu/subproject/pilot-6/Samt-BU-pilot6-konsept-og-losning.pptx)).
