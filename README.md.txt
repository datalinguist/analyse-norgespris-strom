# ⚡ Analyse av Norske Strømpriser og Norgespris

Dette prosjektet inneholder en tidsserieanalyse av historiske strømpriser i Norge for å vurdere lønnsomheten av den statlige ordningen **Norgespris** (40 øre/kWh ekskl. mva.). Analysen bruker reelle historiske data for å beregne en **vektet gjennomsnittspris** basert på et typisk husholdningsforbruk, i tillegg til å bygge en enkel prediksjonsmodell for fremtidige prisestimater.

### Utførte Hovedsteg:
1.  **Datalasting og Rensing:** Excel-data ble lastet inn, og tidsstempler samt priskolonner ble konvertert og renset for å sikre datakvalitet.
2.  **Områdematching:** Postnummeret ble koblet til riktig prisområde (f.eks. NO5).
3.  **Vektet Analyse:** Det ble regnet ut en vektet gjennomsnittlig spotpris. Denne prisen reflekterer hva en husholdning faktisk betaler, da det antas høyest forbruk i dyre perioder (morgen 06-09 og kveld 16-22).
4.  **Prediksjonsmodell:** En Lineær Regresjonsmodell (OLS) ble trent på månedlig data, inkludert en lineær trend- og sesongkomponent (dummy-variabler for måned), for å estimere snittprisene de neste 6 månedene.
5.  **Vurdering av Norgespris:** Både historisk vektet pris og fremtidige estimater ble sammenlignet med grensen på 40 øre/kWh.

## Illustrasjon og Eksempel på Resultat

Nedenfor vises et eksempel på den grafiske analysen for et gitt prisområde.

### 1. Døgnvariasjon (Gjennomsnittlig timepris)
Denne grafen viser at selv om snittprisen varierer gjennom døgnet, er de dyreste tidspunktene (rød linje) konsistent i morgen- og kveldsrushet – de samme tidene husholdningen har høyest forbruk.



### 2. Historisk Utvikling og Fremtidig Estimat
Denne grafen viser den historiske månedlige utviklingen (blå linje) og de estimerte prisene for de neste 6 månedene (rød stiplet linje).

Den oransje linjen representerer **Norgespris-grensen på 40 øre/kWh**. Prisestimater over denne linjen indikerer at det kan være lønnsomt å velge Norgespris i den perioden.