# Praticidade Index 2026.1 (Índice Praticidade 2026.1)

Open data from the **Praticidade Index 2026.1**, published by [Praticidade.com](https://praticidade.com). The edition measures everyday walkable convenience ("praticidade a pé") — the services infrastructure available within walking distance — for **806 areas** (districts, neighbourhoods, territorial units, *freguesias* and zones) in **10 cities in Brazil and Portugal**, with **10 thematic rankings** published in **81 city–ranking slices**.

> **Only ranking extracts are published here.** The full interactive index — every area, all category scores and the address map — lives at **https://praticidade.com**.

- Edition: 2026.1 (`2026-07`)
- Frozen: **15 July 2026** (`2026-07-15T21:04:08.405Z`); values are not revised
- Methodology version: `commit-977201a`
- Permanent reference page: https://praticidade.com/indice/2026-07
- Methodology: https://praticidade.com/metodologia
- Licence: scores © 2026 Praticidade.com, **CC BY 4.0** (code and algorithms are not included and remain reserved)

## Files

| File | Description |
|---|---|
| `data/praticidade-indice-2026-07.csv` | Official CSV download (https://praticidade.com/indice/2026-07.csv), 1,150 rows × 9 columns, unmodified |
| `data/praticidade-indice-2026-07.json` | Official JSON download (https://praticidade.com/indice/2026-07.json), 81 ranking snapshots plus edition metadata, unmodified |

**Scope note:** the published files contain the ranking lists (the 81 city–ranking slices, 1,150 entries, 397 distinct city/area names). They do not contain one row per each of the 806 areas evaluated, nor the 14 category scores per area.

SHA-256:
- CSV `8be9e28cec846af765748f3d7cb86c5b777c480357af75c8d9bb7fcb8702874e`
- JSON `9307db678ad67a6682cc570411a2f17fb2586f27c02815c856c3c34ae52ae7bf`

## Data dictionary (CSV)

| Column | Type | Description |
|---|---|---|
| `cidade` | string | City slug (e.g. `sao-paulo`) |
| `cidade_nome` | string | City name |
| `ranking` | string | Ranking slug (e.g. `mais-seguros`) |
| `ranking_titulo` | string | Ranking title in Portuguese |
| `posicao` | integer | Position in the ranking (ties share a position) |
| `ex_aequo` | 0/1 | 1 if the entry is tied with the previous one |
| `nome` | string | Area name |
| `score` | number (0–10) | Score for the ranking's theme |
| `score_geral` | number (0–10) | Overall Praticidade score of the area |

The JSON has the same entries under `snapshots[].top[]` (`rank`, `exAequo`, `name`, `score`, `overallScore`) and edition metadata: `edition`, `frozenAt`, `methodologyVersion`, `sourceCommit`, `cities`, `cityNames`, `cityFramingNotes`, `rankingTypes`, `totalRankings`.

Rankings: `mais-seguros`, `melhor-transporte`, `mais-caminhaveis`, `mais-ciclaveis`, `melhor-restauracao`, `mais-tranquilos`, `melhor-para-familias`, `melhor-para-jovens`, `mais-completos`, `mais-acessiveis`.

## Cities (areas evaluated, from the index page)

| City | Country | Areas |
|---|---|---|
| São Paulo | Brazil | 95 districts |
| Rio de Janeiro | Brazil | 152 neighbourhoods |
| Belo Horizonte | Brazil | 163 neighbourhoods |
| Curitiba | Brazil | 68 neighbourhoods |
| Porto Alegre | Brazil | 83 neighbourhoods |
| Fortaleza | Brazil | 112 neighbourhoods |
| Brasília | Brazil | 39 territorial units |
| Salvador | Brazil | 59 neighbourhoods |
| Lisboa | Portugal | 24 freguesias |
| Porto | Portugal | 11 zones |
| **Total** | | **806** |

## Methodology summary (from https://praticidade.com/metodologia)

1. **Analysis grid:** each city is divided into a 200 m grid (over 135,000 analysis points in total).
2. **Walking radius:** for each point, points of interest (POIs) within a 10-minute walk (~800 m) are identified, using the pedestrian network via OSRM.
3. **Category scoring:** eight POI-based categories (transport, services, food, health, shopping, leisure, sport, education) are scored by quantity, proximity and sub-type diversity. Six others — safety (official statistics), walkability, tranquillity (noise + vegetation + heat island), environmental risk, air quality and cyclability — come from specialised grids and datasets.
4. **Scale 0–10:** intended mainly for within-city reading; equal scores in different cities do not prove equivalent conditions.
5. **Weighted overall score:** 80% categories, 10% density, 10% diversity, with a penalty when safety is below 3.

Category weights (editorial choice, not a scientific consensus): Safety 16%, Public transport 13%, Services 11%, Food 10%, Health 10%, Shopping 7%, Walkability 5%, Leisure & culture 5%, Environmental risk 5%, Tranquillity 5%, Air quality 4%, Cyclability 3%, Education 3%, Sport & fitness 3%.

Sources: OpenStreetMap contributors, a licensed commercial POI database (DataForSEO) + OpenStreetMap, public-safety authorities, environmental monitoring (e.g. CETESB, QUALAR), IBGE, and official GTFS feeds where approved. Coverage and vintage vary by category and city. **A cell without coverage is not a zero value.** The site describes the index as provisional and not a validated academic measurement; see the methodology page for limitations and what the index does not measure.

## How to cite

> Praticidade.com (2026). Índice Praticidade 2026.1. Congelado em 15 de julho de 2026. https://praticidade.com/indice/2026-07

The index is produced by Ricardo Carapeto, founder of Praticidade.com. See `CITATION.cff`.

## Licence

Data: [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (`LICENSE`). Attribute to "Praticidade.com".

---

## Português

Dados abertos do **Índice Praticidade 2026.1**, de [Praticidade.com](https://praticidade.com): praticidade a pé de 806 áreas em 10 cidades do Brasil e de Portugal, com 10 rankings temáticos em 81 recortes cidade-ranking. Números congelados a 15 de julho de 2026 e não revistos. Os ficheiros são os downloads oficiais em CSV e JSON da página https://praticidade.com/indice/2026-07, sem alterações; contêm as listas dos rankings, não uma linha por cada uma das 806 áreas. Metodologia: https://praticidade.com/metodologia. Licença CC BY 4.0, com atribuição a «Praticidade.com».
