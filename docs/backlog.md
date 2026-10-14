# Backlog: koolisöökla toitude tellimine

Prioriteedid: 1 = kõige tähtsam (MVP), 2 = esimesse versiooni, kui aega on, 3 = hiljem.

| # | Prioriteet | Sprint | Kasutaja lugu | Kriteeriumid |
|---|---|---|---|---|
| 1 | 1 | sprint-1 | Õpilasena soovin sisse logida kooli kontoga, et tellida toitu oma nime all. | Sisselogimisvormil on kasutajanime ja parooli väljad. Vale parooli korral kuvatakse veateade. Õige logimise järel avaneb menüü. |
| 2 | 1 | sprint-1 | Õpilasena soovin näha päeva menüüd, et teada, mis söögikordi on saadaval. | Menüü lehel on päeva kuupäev. Iga toidu juures on nimi ja hind. Menüü kuvatakse nimekirjana. |
| 3 | 1 | sprint-1 | Õpilasena soovin valida toidu ja kinnitada tellimuse, et söökla teaks, mida valmistada. | Toidu valimisel ilmub kinnitusnupp. Pärast kinnitamist on tellimus salvestatud. Kinnitus näitab valitud toidu nime. |
| 4 | 1 | sprint-1 | Söökla töötajana soovin näha päeva tellimuste loendit, et teada, kui palju mida valmistada. | Vaates kuvatakse päeva kõik tellimused. Iga tellimuse juures on toidu nimi ja tellija. Loendit saab filtreerida toidu järgi. |
| 5 | 2 | sprint-2 | Õpilasena soovin tellida toitu nädalaks ette, et mitte iga päev eraldi tellida. | Tellimus saab valida mitu päeva. Iga päeva kohta kuvatakse valitud toit. Tellimuse saab tühistada enne kella 9. |
| 6 | 2 | sprint-2 | Lapsevanemana soovin näha lapse tellimusi, et teada, mida ta sööb. | Vanem näeb lapse tellimusi kuupäeva järgi. Tellimuste loendis on näha kõik viimase 30 päeva tellimused. |
| 7 | 3 | hiljem | Söökla töötajana soovin maksta tellimuse eest veebis, et vähendada sularaha käsitlemist. | Maksmise nupp on tellimuse kinnitamisel. Edukal maksmisel saab õpilane kinnituse. Ebaõnnestunud makse korral tellimust ei salvestata. |

## Märkused

- Lood 1–4 moodustavad MVP-joone: ilma nendeta ei saa esimest kasutatavat voogu läbida.
- Lood 5–6 lisatakse teises sprindis, kui esimene versioon on söökla juures testitud.
- Lugu 7 on prioriteet 3, sest maksmine nõuab lepingut teenusepakkujaga ja see ei ole kooli sisemine otsus.
- Lugude 1–4 kriteeriumid on jah/ei kontrollitavad. Kriteeriumide sõnastamisel jälgisin, et ei oleks hinnangulisi sõnu (kiire, lihtne, mugav).

Kõik lood on GitHubi issue’d: https://github.com/IvarTammela/tarkvaraprojekt-kavand/issues
