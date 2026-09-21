# FY27 CML France — Sleeping Accounts Dashboard

Tableau de bord interne pour suivre le programme **Sleeping Accounts** (CML France, FY27 Q2–Q3).

## Contexte

Programme piloté par Iona Guily (Sales owner : Yves Sechi) pour réactiver des comptes commerciaux répondant à 3 critères :
- AOV > $0
- Aucune ACV closée en FY26 ou FY27
- $0 de pipeline ouvert pour FY27/FY28

Le dashboard suit, pour ~282 comptes ciblés : PipeGen généré, ACV closée, activités (call connect), et taux de réveil, avec un classement des FLM et un filtre par équipe (Yves Sechi / Romain Fracchia / reste).

## Utilisation

Ouvrir `sleeping_accounts.html` dans un navigateur — aucune installation ni dépendance requise, les données sont intégrées directement dans le fichier.

## Sources des données

- **Data PipeGen** — Snowflake, `GDSO_CRT_PG_WV_VW`
- **Data ACV** — Snowflake, `GDSO_CRT_ACV_VW`
- **Data Call Co** — Org 62, activités FY27 CMRL (auto-refresh 4h)
- **Hubbl Scans** — suivi manuel

Dernière extraction : voir date de mise à jour dans le pied de page du dashboard.

## Confidentialité

⚠️ Ce fichier contient des données commerciales internes (noms de comptes, AE, FLM, montants). **Repo privé uniquement.**

## Mise à jour des données

Les données sont figées au moment de l'export du Google Sheet source. Pour rafraîchir : régénérer le fichier à partir du Sheet et remplacer `sleeping_accounts.html`, puis commit.
