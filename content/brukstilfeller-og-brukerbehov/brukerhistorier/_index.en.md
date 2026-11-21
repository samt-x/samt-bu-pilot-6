---
id: 34bd5d8b-c124-43c0-bb51-08ffd6505cf4
title: "User stories"
linkTitle: "User stories"
weight: 10
lastmod: 2026-11-21T00:22:24+01:00
last_editor: Erik Hagen

---

{{< i-arbeid >}}

The roles and actors in pilot 6, some personas, and the needs broken down into user stories in the form "As a … I want … so that …". The user stories are the basis for prioritising what the pilot should show, and for testing the solution.

Everything on this page is a first draft. The roles are kept here until there is a common role register across the cases. They should then be moved there, and this page should link to the register.

## Roles and actors

The roles are taken from [case 6](/en/behov/use-cases/06-sentralisert-datatilgang/), [About pilot 6](/en/pilotering/pilot-6/om-pilot-6/) and the [solution concept](/en/pilotering/pilot-6/loesningsvalg/valgt-loesning-naa/). One actor can have several roles, and one role can be filled by several actors.

### End users

| Role | Who | What the role does in pilot 6 |
|---|---|---|
| **Parent or guardian** | Person with parental responsibility for the pupil | Follows the pupil's academic progress. The most important user and the one who benefits. |
| **Pupil** | Child in primary or lower secondary school, under 18 | Sees their own information in pupil mode, and has the right to participate. |
| **Other carer** | For example foster parents, a guardian, or a parent without parental responsibility | May need access, but does not necessarily have the right to it. Must be clarified legally. |

### Public actors and data holders

| Role | Who | What the role does in pilot 6 |
|---|---|---|
| **School** | Contact teacher, subject teacher, head teacher | Records assessments and absence, and follows up the pupil together with the parents. |
| **School owner** | The municipality | Responsible for the school, the school systems and the archive. Controller for much of the data. |
| **Norwegian Directorate for Education and Training (Udir)** | National data holder | Holds results from national tests and assessments. |
| **Population Register** | The Norwegian Tax Administration | Source of who has parental responsibility. |
| **Other data holders** | For example sports | Possible sources later. Outside the scope at first. |

### Vendors and common solutions

| Role | Who | What the role does in pilot 6 |
|---|---|---|
| **School system vendor** | Vendors of school administration systems (OAS) | Holds much of the data and must be able to pass it on. |
| **Channel provider** | KS (Min Kommune), app developers, Altinn | Builds the end-user service. Is the organisation that asks for the data. |
| **Broker** | Digdir (data.altinn.no, Altinn Events, Dialogporten) | Brokers data, events and dialogues between the sources and the channels. |
| **Rule owner** | SAMT-BU, later a permanent manager | Manages the information model and the rulebook. |

## Personas

The personas are made up. They are not based on user research, and must be validated, for example through interviews with parents, as case 6 suggests. Amir is taken from the presentation of the solution concept.

| Persona | Role | Situation | What matters most |
|---|---|---|---|
| **Amir**, 12 | Pupil | In year 7. Likes maths, struggles with reading. | Seeing his own results, and knowing what his parents see. |
| **Mona**, Amir's mother | Parent | Works full time, used to digital services, uses Min Kommune. | One overview, and a notification when something new arrives. |
| **Piotr**, father of two | Parent | Shift work, Norwegian as a second language, does not know the school system well. | Understanding what the results mean, and what he can do. |
| **Lise and Erlend** | Parents | Divorced, the children live with both. Both have parental responsibility. | That both see the same thing, without going through each other. |
| **Nora**, 15 | Pupil | In year 10. | Having more say in what is shared with her parents. |

## User stories

The **Source** column shows where the story comes from: *Case 6*, *About pilot 6*, *Concept* (the presentation of the solution concept) or *Proposal* (our own, not in the sources). Priority will be set later.

### Parent or guardian

| Id | As a … | I want … | so that … | Source |
|---|---|---|---|---|
| F1 | parent | to see results from national tests and assessments, evaluations and grades for my child in one place | I do not have to search several systems and put the picture together myself | Case 6 |
| F2 | parent | to see progress over time, also across school years and changes of school | I understand whether my child is progressing as expected | Case 6 |
| F3 | parent | to see my child's absence in the same overview | I see absence and results together | Concept |
| F4 | parent | to be notified when new results are ready | I can follow up while it is relevant | Concept |
| F5 | parent | to log in with ID-porten and only see children I have parental responsibility for | I can trust that nobody else sees my child's data | Concept |
| F6 | parent | to get the overview in a service I already use, for example Min Kommune | I do not have to start using yet another service | Case 6 |
| F7 | parent who does not know the school system well | to have the results explained in plain language | I can follow up my child as well as other parents | Case 6, Proposal |
| F8 | parent with shared custody | both parents with parental responsibility to see the same information | we have the same basis when following up our child | Proposal |
| F9 | parent | to see who has retrieved my child's data, and when | I can trust that the data is not misused | About pilot 6 |
| F10 | parent | to see where each piece of information comes from, and where to report errors | errors are corrected at the source | Proposal |

### Pupil

| Id | As a … | I want … | so that … | Source |
|---|---|---|---|---|
| E1 | pupil | to see my own results and progress | I can keep track of how I am doing | Case 6 |
| E2 | pupil | to know what my parents can see about me | I know what is shared | Case 6 |
| E3 | older pupil | to have more say in what is shared with my parents as I get older | my right to participate is taken seriously | Concept, to be clarified legally |

### School and school owner

| Id | As a … | I want … | so that … | Source |
|---|---|---|---|---|
| S1 | contact teacher | parents to have the overview before the progress meeting | the meeting can be about follow-up, not about going through results | Proposal |
| S2 | school owner | the data to be shared from the school systems we already have | schools do not have to record the same thing in several places | Proposal |
| S3 | school owner | access to the data to follow the same rules in all channels | we meet our responsibility as controller | About pilot 6 |

### Data holders and vendors

| Id | As a … | I want … | so that … | Source |
|---|---|---|---|---|
| D1 | data holder (Udir) | to share the data once through data.altinn.no | I do not need separate integrations with each channel | Concept |
| D2 | data holder | only organisations with legal authority or consent to retrieve data, and the retrieval to be logged | I know who has received the data, and on what basis | Concept |
| D3 | school system vendor | a common information model and API description | I can deliver data in the same format to everyone | About pilot 6 |
| D4 | channel provider | one API for all the sources | I can build the service without integrating with each source | Concept |
| D5 | channel provider | to subscribe to events about new results | I can notify parents without constantly asking for new data | Concept |
| D6 | rule owner | the requirements for legal authority, consent, representation, data minimisation and logging to be in one rulebook | all channels follow the same rules | About pilot 6 |

## Next steps

- Validate roles, personas and stories with parents, pupils and schools.
- Prioritise the stories and link them to the [user journeys in the target picture](/en/pilotering/pilot-6/maalbilde/brukerreiser/).
- Clarify the legal questions: the role other carer, F8 and E3.
- Consider a common role register across the cases.
