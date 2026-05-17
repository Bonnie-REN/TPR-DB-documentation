---
icon: lucide/grid-2x2-check
---

# Data Tables (3.0)

The [TPR feature extraction](https://github.com/Critt-Kent/TPR-DB-web-app/tree/main/libs/tables) generates 14 summary tables, each of which describes the relation between the translation process and the translation product from a different angle. Each row in a TPR-DB table describes a process or product unit, while the columns contain the values of features (or attributes). The values can be categorical (strings or numbers), integers or real numbers.
Eleven of these tables are already part of the previous [TPR-DB version 2.0](https://drive.google.com/file/d/1FgOSNcpbjlxdo6MM_jf3Pw5wDS6S9-BB/view), and there described in some detail, albeit several features have changed. The documentation of [The CRITT Translation Process Research Database, pp. 18 ff](https://drive.google.com/file/d/1FgOSNcpbjlxdo6MM_jf3Pw5wDS6S9-BB/view) classifies the TPR-DB tables into:

1. Basic product unit tables: source token (ST), target token (TT)
2. Composed product unit tables: segment (SG) and session (SS) summary, alignment groups (AG)[^AG]
3. Basic process unit tables: keystroke data (KD), fixation data (FD)
4. Composed process unit tables: activity unit (AU), fixation unit (FU) production unit (PU)
5. Usage of external resources: external resources (EX)

[^AG]: in the original version we used the term 'alignment unit' (AU), which we then changed into alignment group (AG). The short form AU was then used as a short form for 'Activity Unit'.

With the new Python implementation, the [TPR Feature Extraction](https://github.com/Critt-Kent/TPR-DB-web-app/tree/main/libs/tables) generates three additional tables of process units: 

* KU: keystroke units, indicative of automated typing routines  
* HS: HORF states, states of hesitation, need for orientation, and fluent typing, indicative of affective-cognitive dynamics
* HC: HORF cycles, coordination of HORF states, indicative of affective-cognitive attumement 

Together with the AU and PU tables the three new processing units form a temporally nested hierarchy of behavioral units, each operating on a different timescale, which jointly span a [Behavioural Translation Style Space](https://arxiv.org/abs/2507.12208)[^newTables]:

[^newTables]: new tables are in bold

| Processing Unit          | Typical Timescale    | Primary Function                                                                                        |
| :----------------------- | :----------- | :-------------------------------------------------------------------------------------------------------------- |
| Activity Units (AU)      | ~500 ms–2 s  | Sensorimotor integration, characterized by recurring patterns of eye–hand coordination                          |
| **Keystroke Units (KU)** | **~1–2 s**   | **Automatized typing routines, characterized by short inter-keystroke intervals ([KUI](https://arxiv.org/pdf/2604.01410))**                        |
| Production Units (PU)    | ~3–5 s       | Reflective processing segments, characterized by extended inter-keystroke intervals ([PUBs](https://arxiv.org/pdf/2604.01410)) and local planning activity |
| **HORF States (HS)**     | **~10–30 s** | **Perception–action states, characterized by recurrent reading and typing configurations**                      |
| **HORF Cycles (HC)**     | **~1–3 min** | **Epistemic–pragmatic sequences, characterized by recurring transitions between HORF states**                   |

This hierarchy of embedded temporal units captures and structures the organization, control, and monitoring of [affective, behavioral, and cognitive](https://www.degruyterbrill.com/document/doi/10.1515/dsll-2025-0002/html) processes during translation.

Each unit consists of a number of product and process features, many of which are slightly differently computed in the TPR-DB 3.0, as discussed next.

