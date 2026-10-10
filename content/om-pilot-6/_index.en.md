---
id: 37cab3af-72bf-4dc1-9dd6-c63aac96a862
# id: auto-generated – copied values are overwritten automatically on push
title: "About pilot 6"
linkTitle: "About pilot 6"
weight: 10
lastmod: 2026-10-10T14:41:03+02:00
last_editor: Erik Hagen

---
## INTRODUCTION

This is a description of the plan for carrying out pilot 6 – Parents' access to data. Although the plan describes the work as a phase-driven process, we expect to work iteratively, repeating some phases as needed.

## SCOPE AND DELIMITATION

### Background

The work is based on the case description [6. Centralised Access to Data Parents Need](https://docs.samt-bu.no/en/behov/use-cases/06-sentralisert-datatilgang/).

The case is about giving parents and guardians simple and clear access to data that are relevant for following the pupil's development, such as national tests, national assessments, final assessments and grades where relevant.

Today there is no central "place" where parents can find all relevant information about their child's academic development. Parents who want such an overview have to search in many places and piece the information together themselves. In such a process there is always a risk that information is lost, and it raises the threshold for engaging in the child's academic development. A single overview would probably make it easier for parents to follow and engage, including parents with fewer resources.

Relevant data are held in many different places: some in the specialist systems (school administration systems), some in the municipality's archive systems and some at the Norwegian Directorate for Education and Training (Udir), to name a few. There is no single overview showing the individual's development over time.

As far as SAMT-BU has been able to establish, there are also no standardised information models or common architecture principles that make it easy to build a coherent service meeting this need. It is also uncertain whether there are easy-to-use APIs that could form the basis for retrieving relevant data.

### Objective of the pilot

In its first phase, the pilot will focus on mapping the current situation and the opportunities that exist, and on examining the architecture needed to build end-user solutions.

The goal after three months is to:

- understand parents' need for information, and how they would like to access it if everything were perfect (dream journey)
- have an overview of the actors, where the relevant data are held and to what extent they are available (AS-IS description)
- have a target architecture in place, with a rulebook and information models that can support a future solution
- understand how this case relates to the other cases in SAMT-BU

To be clarified:

- Are there legal obstacles?
- Can the voluntary sector be invited in, for example by retrieving data from the Norwegian Olympic and Paralympic Committee and Confederation of Sports' data platform?
- Can the supplier market build the end-user solution based on a data product offered by SAMT-BU, either through a hackathon or a "startoff-like" procurement?

### Deliverables of the pilot

The pilot has the following deliverables:

1. A dream journey for parents' access to data about the pupil, with an overview of which data they want
2. An AS-IS description with an overview of the actors, the system landscape, relevant data and whether there are simple ways to access the data (API)
3. A target architecture with a rulebook and information models that can also form the basis for a data product
4. A proposal for the next phase

Carrying out the pilot will also provide a basis for updating the project's playbook for this type of project.

### Hypotheses

It is assumed that the solution must be realised using an event-driven architecture and a virtual knowledge graph over the source systems. Requirements for consent, legal basis, power of attorney, representation, data minimisation, access control and logging/traceability, among other things, should be incorporated into a separate rulebook in line with the EU data spaces.

Some of the key data to be shown are held in specialist systems. It will therefore also be necessary to establish contact with the existing system suppliers.

### Delimitation

The pilot will initially look at data within the school area and only for pupils under 18. Sports data may also become relevant. No solutions will be built in the first iteration.

### Benefit owners

It is primarily parents who will benefit if the pilot leads to a working solution. However, no public body "owns" parents' needs. The closest benefit owner is therefore the Norwegian Digitalisation Agency (Digdir), which has overall responsibility for digital solutions in the public sector.

## STAFFING

The pilot needs the following competencies:

- Project manager
- Domain knowledge for the AS-IS mapping (Udir, Sikt and others, and an overview of the supplier market)
- Service designer (for the dream journey)
- The architecture group and national architecture (target architecture)
- The modelling group (ontology and knowledge graph)
- Knowledge of Altinn and KS Digital's data platform, depending on where the data products are to be offered

Staffing has not yet been decided.

## EXECUTION

### Duration of the pilot

The start date has not yet been decided.

### Work packages

The following work packages have been defined:

1. A dream journey for parents' access to data about the pupil, with an overview of which data they want
2. An AS-IS description with an overview of the actors, the system landscape, relevant data and whether there are simple ways to access the data (API)
3. A target architecture with a rulebook and information models that can also form the basis for a data product
4. A proposal for the next phase

### Dependencies

It is essential that the pilot gains good insight into today's solutions. Good communication with Udir is therefore essential, as is communication with today's system suppliers.

### Key milestones

The pilot has the following key milestones:

- When the dream journey is available
- When the AS-IS description is available
- When the target architecture is available
- When the information model is ready
- When the rulebook is ready
- When there is a proposal for a possible continuation of the pilot

### Practical execution

The pilot is carried out iteratively according to agile principles, in sprints of two or three weeks. Each sprint starts with a planning meeting and ends with a demo. A joint demo for all pilots under SAMT-BU is being considered. Initially, a stand-up for the whole pilot every other day is desirable, but over time it may be sufficient to coordinate the work within each work package. At least one retrospective should be held during the pilot period.

The pilot's tasks are followed up as issues in [samt-bu-pilot-6](https://github.com/samt-x/samt-bu-pilot-6/issues).

### Communication

Communication activities are coordinated with the communication adviser in SAMT-BU's core team.
