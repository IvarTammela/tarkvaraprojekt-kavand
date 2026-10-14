# 4. Tarkvaraarhitektuur

Skeemi lähtefail: [diagrams/arhitektuur.puml](../diagrams/arhitektuur.puml) (PlantUML, muudetav tekstina).

## Rakenduse tüüp

Veebirakendus. Õpilane ja lapsevanem kasutavad seda nutitelefonis või arvutis, söökla töötaja arvutis. Eraldi mobiilirakendus ei ole vajalik, sest kasutus on lühike ja brauser katab kõik vajalikud seadmed.

## Valitud arhitektuur: monoliit

Kõik osad (autentimine, menüü, tellimused, söökla vaade) on ühes rakenduses ja ühes andmebaasis. Kihid on eraldatud: veebiliides, API kiht, teenused, andmebaas.

**Põhjendus:**
- Süsteem on väike: neli põhifunktsiooni ja mõned sadad kasutajad.
- Üks deploy ja üks andmebaas on lihtsam hallata, kui tegemist on kooli IT-meeskonnaga, kellel pole palju aega.
- Kihid tagavad, et hiljem saab teenuseid eraldada.

**Eelised:** lihtne arendada ja paigaldada, ühtne andmebaas, vähem liikuvaid osi.
**Puudused:** kui üks osa (näiteks tellimused) vajab rohkem ressurssi, peab kogu rakendust skaleerima. Ühe koodibaasi muudatused võivad mõjutada teisi osi.

## Alternatiiv: mikroteenused

Iga põhifunktsioon oleks eraldi teenus oma andmebaasiga, teenuseid ühendaks API lüüs.

**Eelised:** teenuseid saab eraldi skaleerida ja arendada, rike ühes osas ei peata kogu süsteemi.
**Puudused:** keerukam paigaldus ja jälgimine, rohkem infrastruktuuri, mis on väikesele kooli projektile ülemäärane.

**Miks mitte mikroteenused:** tellimuste maht söökla kohta on väike ja meeskond väike. Keerukus ei tasuks ära saadud paindlikkust.

## Andmevoog

1. Õpilane avab veebiliidese brauseris ja logib sisse. Veebiliides saadab kasutajanime ja parooli API kihile.
2. API kiht kontrollib kasutajat autentimise teenusega, mis loeb kasutajate andmed andmebaasist.
3. Õpilane valib menüüst toidu. Veebiliides küsib menüü teenuselt päeva menüü, mis tuleb andmebaasi menüü tabelist.
4. Õpilane kinnitab tellimuse. Veebiliides saadab tellimuse API kihile, tellimuste teenus salvestab andmebaasi tellimuste tabelisse.
5. Söökla töötaja avab päeva vaate. Söökla vaade loeb tellimuste teenuse kaudu päeva tellimused ja kuvab need loendina.

Andmevoog on ühesuunaline kihtide vahel: brauser → API → teenus → andmebaas. Vaated ei pääse andmebaasi otse.

## Pudelikael ja suur koormus

Kui rakendust peaks kasutama sada korda rohkem inimesi (näiteks kogu kool ja mitu söökla), oleks pudelikael tellimuste teenus ja andmebaas, eriti tipptunnil kell 8–9. Võimalikud muudatused:
- Andmebaasi replikatsioon lugemiseks (söökla vaade loeb replikast).
- Vahemälu menüü jaoks, sest menüü muutub harva.
- Tellimuste teenuse eraldamine eraldi teenuseks, kui tellimuste maht kasvab.
