# Astra BP Simulator

App web interactive basée sur les hypothèses du board paper et de la présentation Astra.

## Fichiers source utilisés
- `Astra.pdf`
- `Board_Paper_RV_Derives_Project_Detailed (1).pdf`

## Hypothèses intégrées
- Seed initial: `50m CHF`
- Coûts fixes annuels: `1.6m CHF` (modifiable)
- Fee structure: `2% management fee` + `20% performance fee`
- Step-down économique Dominicé (selon AUM de fin d'année):
  - Phase 1 (<= 300m): `100% MF` et `40% PF`
  - Phase 2 (300m - 600m): `80% MF` et `30% PF`
  - Phase 3 (> 600m): `70% MF` et `25% PF`
- Revenus Astra = part résiduelle après partage Dominicé.

## Scénarios disponibles
- Pas de perf / pas de collecte
- Perf moyenne (10%) + collecte moyenne
- Super perf + forte collecte

## Sorties
- KPIs (AUM final, cumul revenus/résultat Dominicé, ROIC)
- Graphes AUM + revenus annuels Dominicé/Astra
- Tableau annuel et cumulé (revenus + bilan)

## Lancement
- Ouvrir `index.html` dans un navigateur.
