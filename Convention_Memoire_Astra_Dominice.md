# Projet de clauses - Mecanisme de compensation Astra / Dominice

## Avertissement
Ce document est un modele de travail operationnel et economique. Il doit etre revu, adapte et valide par un avocat avant signature.

## 1. Objet
Le present document fixe les regles economiques entre Dominice ("Dominice") et Astra ("Astra") pour:
- la repartition des revenus,
- la prise en charge des couts,
- la compensation des deficits de Dominice par les revenus d'Astra,
- le suivi du deficit cumule restant ("Astra cumulated deficit").

## 2. Definitions
- `Revenus Dominice`: part economique de Dominice issue des management fees et performance fees selon la grille step-down en vigueur.
- `Revenus Astra`: solde economique apres attribution des Revenus Dominice.
- `Couts de fonctionnement`: couts fixes et/ou variables definis annuellement au budget approuve.
- `Resultat net Dominice de base`: `Revenus Dominice - Couts de fonctionnement`.
- `Deficit cumule Dominice` (a afficher comme `Astra cumulated deficit`): montant de deficit Dominice restant a compenser a la fin de periode.
- `Compensation Astra`: part des Revenus Astra de la periode affectee en priorite a la reduction du Deficit cumule Dominice.
- `Resultat net Astra`: `Revenus Astra - Compensation Astra`.

## 3. Repartition des couts
Les Couts de fonctionnement sont supportes a 100% par Dominice et a 0% par Astra.

## 4. Mecanisme de compensation in-year
A chaque periode de calcul:
1. Calcul du resultat net Dominice de base.
2. Si ce resultat est negatif, son montant absolu alimente le Deficit cumule Dominice.
3. La Compensation Astra est calculee comme le minimum entre:
   - les Revenus Astra de la periode, et
   - le Deficit cumule Dominice avant compensation.
4. Le Deficit cumule Dominice est diminue de cette compensation.
5. Le resultat net Dominice de la periode est egal au resultat de base plus la compensation.
6. Le resultat net Astra de la periode est egal aux Revenus Astra moins la compensation.

## 5. Principe economique Astra
- Hors compensation active, `Resultat net Astra = Revenus Astra`.
- En cas de compensation active, `Resultat net Astra < Revenus Astra`.
- En toute hypothese, `Resultat net Astra` ne peut pas etre negatif dans ce mecanisme (la compensation est plafonnee aux Revenus Astra).

## 6. Suivi du deficit cumule
- Le champ `Astra cumulated deficit` correspond au Deficit cumule Dominice restant en fin de periode.
- Ce montant revient a zero des que le deficit a ete integralement compense.

## 7. Reporting et auditabilite
Un etat economique periodique est prepare et valide par les parties, comprenant au minimum:
- revenus bruts,
- partage de revenus,
- couts supportes par Dominice,
- deficit cumule d'ouverture,
- compensation Astra de la periode,
- deficit cumule de cloture (`Astra cumulated deficit`),
- resultats nets et cumules des parties.

## 8. Duree et revision
Le mecanisme entre en vigueur a la date d'effet contractuelle et demeure applicable jusqu'a accord contraire ecrit des parties.
Toute modification de ces regles doit faire l'objet d'un avenant signe.

## 9. Droit applicable et for
Sauf stipulation differente dans les contrats-cadres:
- droit applicable: droit suisse,
- for: Geneve.

## Annexe - Formules resumees
- `ResultatDominiceBase(t) = RevenusDominice(t) - CoutsFonctionnement(t)`
- `DeficitCumuleAvantComp(t) = DeficitCumuleFin(t-1) + max(-ResultatDominiceBase(t), 0)`
- `CompensationAstra(t) = min(RevenusAstra(t), DeficitCumuleAvantComp(t))`
- `DeficitCumuleFin(t) = DeficitCumuleAvantComp(t) - CompensationAstra(t)`
- `ResultatDominice(t) = ResultatDominiceBase(t) + CompensationAstra(t)`
- `ResultatAstra(t) = RevenusAstra(t) - CompensationAstra(t)`