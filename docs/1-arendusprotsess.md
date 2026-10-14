# 1. Arendusprotsess

## Etapid idee tekkimisest hoolduseni

| Etapp | Eesmärk | Väljund |
|---|---|---|
| Idee ja analüüs | Selgitada, mis probleemi lahendame ja kellele | probleemi kirjeldus, sihtrühmad (õpilane, söökla töötaja, lapsevanem) |
| Nõuete kogumine | Koos kooli esindaja ja söökla töötajaga kokku leppida, mida süsteem teeb | nõuete loend, kasutajalood, prioriteedid |
| Kavandamine | Otsustada arhitektuur, andmed, liidesed ja kasutatavad vahendid | arhitektuuriskeem, andmemudel, tehnoloogiavalik |
| Arendus | Ehitada süsteem väiksemate osade kaupa | töötav tarkvara, testid |
| Testimine | Kontrollida, kas süsteem täidab nõudeid ja on kasutatav | testjuhud, kasutajatesti tulemused |
| Kasutuselevõtt | Viia süsteem koolisöökla kasutusse, õpetada kasutajaid | paigaldatud versioon, juhendid |
| Hooldus | Parandada vigu, lisada väiksemaid muudatusi, jälgida kasutust | väljalasked versioonidega, tugi |

## Mudelite võrdlus

**Koskmudel (waterfall).** Etapid järjestikused: nõuded, kavandamine, arendus, testimine, kasutuselevõtt. Iga etapp lõpeb enne järgmise algust.
- Plussid: lihtne planeerida, dokumenteeritud, sobib kindlate nõuetega projektile.
- Miinused: nõuete muutmine on kallis, kasutajaga suhtlemine jääb algusesse ja lõppu, viga tuleb kätte alles testimisel.

**Iteratiivne ja inkrementaalne mudel.** Süsteem arendatakse väikeste tsüklitena. Iga tsükkel lisab töötava osa ja selle üle antakse tagasiside.
- Plussid: kasutaja näeb varakult töötavat osa, muudatused on odavamad, riske saab varakult märgata.
- Miinused: nõuab rohkem koordineerimist, lõppmaht ei pruugi olla kohe selge, vajab head backlog’i haldamist.

## Valitud mudel: iteratiivne

Valisin iteratiivse mudeli, sest:
1. Söökla tellimissüsteemi nõuded selguvad alles siis, kui söökla töötajad näevad esimest versiooni. Näiteks, kas tellimine peab olema päeva või nädala kaupa.
2. Süsteemi lihtsaim versioon (õpilane tellib ühe toidu ja söökla näeb tellimusi) on kiiresti kasutatav ja annab tagasisidet.
3. Tähtaeg ei ole range enne kooliaasta algust, seega on võimalik teha mitu tsüklit.

Esimene tsükkel (MVP) on ühe päeva tellimine ilma maksmiseta. Maksmine lisatakse teises tsüklis, kui tellimine on kasutatav.

## Kliendi nõuete muutmine arenduse keskel

Olukord: söökla juhataja ütleb pärast esimest tsüklit, et tellimus peab olema lubatud kuni kella 9 samal päeval, mitte eelmisel päeval.

Käitumine:
1. Muudatus lisatakse backlog’i kasutajalooga, mitte koodi muutes. Lugu saab prioriteedi ja selgitatakse, mis osa see mõjutab.
2. Kui muudatus puudutab tellimise loogikat, kontrollin, millised teised lood sõltuvad tähtajast (näiteks päevane toidunimekiri). Need märgitakse hõlmatuks.
3. Muudatus läheb järgmisesse sprinti ja selle mõju hinnatakse sprinti planeerimisel. Kui see on kiireloomuline, asendab see mõne sama suuruse loo sprinti.
4. Klient saab näha, mis muutus ja mis sellega kaasneb, enne kui ta otsustab, kas muudatus tehakse praegu või hiljem.

Iteratiivse mudeli eelis siin on see, et muudatus on väike ja sprintide vahel saab seda ümber seada. Koskmudeli puhul oleks see tähendanud kogu kavandi ümbertegemist.
