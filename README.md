# FFF-data

Données football (FFF) au format **JSON**, servies par CDN **jsDelivr** pour une
intégration web rapide et sans backend.

## Propriété

- **Propriétaire / auteur :** Koffi Frédéric SESSIE — <sessiekoffifrederic@gmail.com>
- **En collaboration avec :** <seedinho.contact@gmail.com>

© 2026 Koffi Frédéric SESSIE. Tous droits réservés. Voir [LICENSE](LICENSE).

## Contenu

Ce dépôt **public** ne contient **que les données JSON** (équipes, compétitions,
classements, matchs, index de recherche). Le code de génération (pipeline de scraping)
reste **privé**.

```
seasons/{saison}/
├── indexes/                     # index globaux (recherche, autocomplétion)
│   ├── equipes_autocomplete.json   # liste complète des équipes (recherche)
│   ├── clubs.json                  # clubs + logos
│   ├── competitions.json           # toutes les compétitions
│   ├── equipes.json / equipes_light.json
│   ├── regions.json / districts.json
│   └── equipes/{clNo}.json         # fiche détaillée par équipe (avec matchs)
├── regions/{region}/…/competitions/{type}/{cpNo}/   # données par compétition
└── competitions-nationales/{type}/{slug}/           # compétitions nationales
```

## Accès via jsDelivr

```
https://cdn.jsdelivr.net/gh/SEEDINHO-FOOT/FFF-data@main/seasons/2025-2026/indexes/equipes_autocomplete.json
```

## Mise à jour

Données rafraîchies **quotidiennement** (automatisé). Les données ne sont jamais
remplacées par du vide en cas d'incident de collecte (garde-fou).
