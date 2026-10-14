# 5. Versioonimine (SemVer)

Versioonid on kujul **MAJOR.MINOR.PATCH**, näiteks 1.2.3.

## Reeglid rakenduse jaoks

- **MAJOR** (1.x.x → 2.0.0): muudatus, mis katkestab olemasoleva kasutuse. Näiteks API vorming muutub, või tellimuse andmemudel vahetub nii, et vana andmed ei sobi.
- **MINOR** (1.1.x → 1.2.0): uus funktsioon, mis on tagasiühilduv. Näiteks lugu 5 (nädala tellimine) lisatakse ilma et olemasolev tellimine muutuks.
- **PATCH** (1.2.2 → 1.2.3): veaparandus, mis ei lisa funktsionaalsust. Näiteks tellimuse kinnitusteate tekst valesti kuvatakse.

## Versiooniplaan

| Versioon | Sisu | Sprint |
|---|---|---|
| 0.1.0 | esimene töötav versioon: sisselogimine, menüü, tellimine, söökla vaade | sprint 1 |
| 0.1.1 | veaparandused pärast söökla testi | sprint 1 |
| 0.2.0 | nädala tellimine ja tühistamine (lood 5) | sprint 2 |
| 0.3.0 | lapsevanema vaade (lugu 6) | sprint 2 |
| 1.0.0 | esimene kasutuselevõtt kooli kasutajatele; API ja andmemudel on stabiilne | pärast sprinti 2 |
| 1.1.0 | maksmine (lugu 7), tagasiühilduv | hiljem |
| 2.0.0 | näiteks, kui tellimuse andmemudel muudetakse ja vana tellimus ei sobi enam | hiljem, vajadusel |

Versiooni 0.x.x kasutatakse arendusperioodil, sest API ei ole veel stabiilne. Alates 1.0.0 järgitakse SemVer-it rangelt.

## Kuidas versioonid väljalaskmisel kasutatakse

1. Iga väljalase on Giti tag (näiteks `v1.0.0`) ja GitHubi release.
2. Söökla saab teada, mis versioon on kasutusel, kuvamise kaudu rakenduse päises.
3. PATCH-versioonid paigaldatakse ilma söökla juhatajalt kinnitust küsimata, sest need ei muuda kasutust.
4. MINOR-versioonid tutvustatakse söökla juhatajale enne paigaldust.
5. MAJOR-versioon nõuab kokkulepet söökla ja kooli IT-ga, sest kasutajad peavad oma harjumusi muutma.

## Näited

- Parandasin tellimuse kinnitusnupu, mis ei töötanud Safaris → **0.1.0 → 0.1.1** (PATCH).
- Lisasin lapsevanema vaate, mis ei muuda olemasolevat tellimist → **0.2.0 → 0.3.0** (MINOR).
- Muutsin tellimuse andmemudelit nii, et toidu ID läks nimest koodiks ja vana tellimus ei loe enam → **1.4.0 → 2.0.0** (MAJOR).
