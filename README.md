# Premier League Top Scorers – SQL Analysis Project

Et lille dataanalyseprojekt i PostgreSQL, hvor jeg indlæser og analyserer Premier League-topscorerdata fra sæsonen 2024/25.

---

## Struktur

- `data/Premier_League_Top_Scorers.csv` – Datagrundlaget (topscorere, assists, skud m.m.)
- `sql/create_table.sql` – Oprettelse af `top_scorers`-tabellen
- `sql/import_data.sql` – Import af CSV via `COPY`
- `sql/analysis_queries.sql` – Mine bedste SQL-analyser (se nedenfor)

---

## Eksempler på analyser

```sql
-- 1. Top 5 målscorere
SELECT name, goals FROM top_scorers ORDER BY goals DESC LIMIT 5;

-- 2. Spillere med flest assists
SELECT name, assists FROM top_scorers ORDER BY assists DESC LIMIT 5;

-- 3. Effektivitet pr. 90 minutter
SELECT name, goals_per_90 FROM top_scorers ORDER BY goals_per_90 DESC LIMIT 5;


