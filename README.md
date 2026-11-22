# Fortnite VMAF / CRF & Throughput Analysis

A szakmai gyakorlati feladathoz tartozó elemző notebook (`vmaf_throughput_analysis.ipynb`), amely a `Fortnite-l1` adathalmaz alapján vizsgálja a sávszélesség-igényt, az SCC-görbéket és az időbeli váltásokat.

## Mit csinál a notebook?

- Betölti a VMAF (`50–95` tartomány) és a CRF (`fortnitel1-crf`) méréseket, majd kiszámolja a bitráta- / sávszélesség-igényt.
- Legenerálja és elmenti az SCC-adatokat (`scc_master_data.pkl`), majd kirajzolja a VMAF és CRF alapú összehasonlító ábrákat.
- Kiszűri az alacsony aktivitású időablakokat (`CRF=20` mellett `2 Mbps` küszöb alatt), és megvizsgálja az egymást követő időszeletek profiljai közötti különbségeket (kiemelve a Top 10 legnagyobb váltást).

## Mappák és adatok

A notebook az `Adatok` mappán belüli `fortnitel1-vmaf` és `fortnitel1-crf` könyvtárakkal dolgozik. A futtatás során keletkező `scc_master_data.pkl` fájl és a nagyobb nyers adatállományokat `.gitignore`-ban kizártam.
