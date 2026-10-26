# Ferrate-365 — Semantic Web Ontology

An OWL 2 ontology modelling Italian *ferrate* (via ferrata climbs): difficulty grades, complexity dimensions, GPS coordinates, and route durations. Built in 2020 with Protégé as part of a "Modellazione per il Web Semantico" course (with collaborators from the University of Bologna's Semantic Web group).

## Contents

| File | Description |
|------|-------------|
| `ferrate_final.owl` | Main ontology: 18 classes, ~8 object properties, datatype properties for geo/score data |
| `ferrate_export.owl` | Protégé export with the time period content-ontology pattern import |
| `Ferrata-365.html` | Rendered documentation of the ontology |
| `Modellazione_Semantica_Relazione.pdf` | Project report (Italian) |

## Key classes & relations

- `Ferrata` — the core concept, with subclasses like `FerrataAltaMontagna`, `FerrataImpegnativa`
- `Difficoltà`, `Complessità` — graded scale hierarchy (environmental, exposure, physical, technical)
- Object properties: `haDifficoltà`, `haComplessità`, `haDurata`, `haAvvicinamento`, plus inverse properties (`èDifficoltàDi`, `èComplessitàDi`)
- Datatype properties: GPS lat/long/altitude, duration in hours, route length
- Reasoning: SWRL rules + Protégé inference for `FerrataImpegnativa` classification (complexity scores → class assignment)

Open any `.owl` file with [Protégé](https://protege.stanford.edu/) to explore the class hierarchy, run the reasoner, and query.
