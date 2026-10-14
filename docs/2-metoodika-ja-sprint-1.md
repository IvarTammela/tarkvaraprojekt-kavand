# 2. Arendusmetoodika ja esimene arendusperiood

## Valitud metoodika: Scrum

Valisin Scrumi, sest:
- Söökla tellimissüsteem on väike meeskonna projekt, kus on selge tellija (söökla juhataja) ja selge ülesande omanik (product owner roll on minul).
- Scrumi sprindid (2 nädalat) sobivad kooliaastaga, kus söökla tagasiside tuleb regulaarselt.
- Backlog ja sprinti planeerimine annavad selge ülevaate, mis on esimeses versioonis ja mis hiljem.

Kanban oleks sobinud pidevama tööga, aga söökla vajab kindlaid kuupäevi tutvustuseks, mis Scrumis on loomulikum.

## Rollid ja sündmused (kavandatud)

- **Product owner:** mina (prioriteedid, backlog).
- **Arendaja:** mina, koos õpetajaga kui tagasiside andjaga. Kavand ei eelda suuremat meeskonda.
- **Tellija:** söökla juhataja (ülevaatus sprindi lõpus).
- **Sprint planning:** sprindi algul valitakse lood backlog’ist.
- **Daily:** lühike enesekontroll, mis on blokeeritud ja mis järgmisena.
- **Sprint review:** söökla näeb tööd ja annab tagasiside.
- **Retrospective:** mis töötas ja mida muuta.

## Esimene arendusperiood (sprint 1, 2 nädalat)

**Eesmärk:** õpilane saab tellida ühe päeva ühe toidu ja söökla näeb tellimusi lehel.

Sprinti kuuluvad lood (vt [backlog.md](backlog.md)):
1. Õpilane logib sisse kooli kontoga (lugu 1).
2. Õpilane näeb päeva menüüd (lugu 2).
3. Õpilane valib toidu ja kinnitab tellimuse (lugu 3).
4. Söökla näeb päeva tellimuste loendit (lugu 4).

Sprinti ei kuulu: maksmine, nädala menüü, teavitused, administraatori paneel.

**Planeeritud tegevused nädalate kaupa:**
- Nädal 1: andmemudel, kontoga sisselogimine, menüü kuvamine.
- Nädal 2: tellimise salvestamine, söökla vaade, testimine söökla töötajaga.

**Sprindi lõpu kriteerium (Definition of Done):** lood on kaetud kontrollitavate kriteeriumidega, testitud käsitsi söökla keskkonnas, ja söökla töötaja on vaadanud tulemust.

## Tööde jälgimine

Backlog ja sprint 1 lood on GitHubi Issues’is. Iga lugu on issue, mille staatus liigub kolme seisu vahel: avatud (backlog), sprint-1 (valitud), suletud (valmis). Märgised näitavad prioriteedi ja sprindi.
