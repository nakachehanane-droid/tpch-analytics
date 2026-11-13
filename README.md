# TPC-H Sales Analytics

Lernprojekt mit **Snowflake**, **dbt Cloud** und **Git**.
Rohdaten aus `SNOWFLAKE_SAMPLE_DATA.TPCH_SF1` werden in Staging-, Intermediate- und Mart-Schichten modelliert.

## Architektur

```
source (TPCH_SF1) -> staging (views) -> intermediate (ephemeral) -> marts (tables)
```

| Ordner | Inhalt |
| --- | --- |
| `models/staging/tpch` | 1 Model pro Quelltabelle, umbenennen + casten |
| `models/intermediate` | Joins und Geschaeftslogik |
| `models/marts` | `fct_orders`, `dim_customers` fuer BI |
| `seeds` | kleine CSV-Referenzdaten |
| `macros`, `tests`, `snapshots` | eigene Macros, Singular-Tests, SCD2 |

## Start

1. Snowflake-Setup-Skript ausfuehren (siehe Lernanleitung).
2. Repo in dbt Cloud verbinden.
3. In der IDE: `dbt deps` und dann `dbt build`.

## Fortschritt

- [ ] Phase 1 - Staging
- [ ] Phase 2 - Intermediate & Marts
- [ ] Phase 3 - Tests & Doku
- [ ] Phase 4 - Deployment & CI
- [ ] Phase 5 - Seeds, Macros, Incremental, Snapshots
- [ ] Phase 6 - Snowflake vertiefen
