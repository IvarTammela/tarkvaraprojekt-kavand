# 3. CASE-vahendid

Kasutasin kahte vahendit: PlantUML (modelleerimine, tekstipõhine) ja GitHub Issues (tööde planeerimine ja jälgimine). Võrdluseks vaatlen veel diagrams.net-i, mida ma selles kavandis ei kasutanud.

## Kasutatud vahendid

**PlantUML (modelleerimine).** Diagrammid kirjeldatakse tekstina, mis salvestatakse Giti. Kasutasin komponendidiagrammi arhitektuuri jaoks (`diagrams/arhitektuur.puml`).
- Toetab: komponentide ja nende seoste kujutamist, versioonihaldust (diagramm on Giti failis), muudatuste tegemist tekstiredaktoriga.
- Piirang: paigutust ei saa lohistades muuta, paigutuse eest vastutab PlantUML.

**GitHub Issues (tööde planeerimine).** Iga kasutajalugu on issue, prioriteet ja sprint on märgised.
- Toetab: backlog’i haldust, prioriteete, sprindi valikut, seost koodi ja commit’idega (issue number commit’is).
- Piirang: Issues ei anna Kanban-tahvlit ega burndown-diagrammi ilma GitHub Projects’ita. Projects vajab kontoga lisa-õigust, mida ma selles kavandis ei seadistanud.

## Võrdlus: PlantUML vs diagrams.net

| Omadus | PlantUML | diagrams.net |
|---|---|---|
| Lähtefail | tekst (`.puml`), hästi Giti sobiv | XML (`.drawio`) või pilt; XML on Giti sobiv, aga diff on lugematu |
| Muutmine | tekstiredaktor, kiire, koodilik | visuaalne lohistamine, sobib paigutamiseks |
| Standardid | UML ja muud diagrammitüübid | UML, BPMN, võrgu skeemid, vabam kujund |
| Koostöö | ühine tekstifail, konfliktid lahendatakse Giti kaudu | reaalajas koostöö veebis |
| Sobib kavandamisse, kus | struktuur on tähtsam kui paigutus | paigutus ja visuaal on tähtsad |

Valisin PlantUML-i, sest arhitektuuri muudatused on tekstipõhised ja neid on mugav Giti diff-ina üle vaadata. Kui kaitsmisel peaks skeemi muutma diagrams.net-is, on lähtefaili võimalik ümber ehitada, aga see nõuab käsitsi tööd.

## Vahendi toetatud arendustegevused

- Arhitektuur: PlantUML toetab kavandamist ja dokumenteerimist.
- Planeerimine: GitHub Issues toetab backlog’i, prioriteetide ja sprindi haldust.
- Versioonihaldus: mõlemad on Giti repositooriumis, muudatused on jälgitavad commit’idega.
