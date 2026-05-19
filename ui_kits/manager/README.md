# OUTIL MANAGER — UI Kit

## Vue d'ensemble

Interface desktop/mobile pour les **Managers** qui suivent les KPIs et l'activité globale de tous les animateurs.

## Fonctionnalités principales

- **Dashboard statistiques** — KPI cards avec métriques en temps réel
- **Vue tableau** — Liste complète des animateurs avec filtres avancés
- **Carte interactive** — Positions GPS de tous les animateurs
- **Graphiques** — Visualisations des taux de présence par secteur/ville
- **Historique** — Exports et rapports détaillés

## Composants

- `Sidebar.jsx` — Navigation latérale
- `KPICards.jsx` — Cartes de statistiques
- `AnimateursTable.jsx` — Tableau avec tri et filtres
- `MapDashboard.jsx` — Carte avec overlay statistiques
- `Charts.jsx` — Graphiques de présence

## Technologies

- React 18 + Babel standalone
- Leaflet.js pour les cartes
- Chart.js pour les graphiques
- Lucide Icons
- CSS Variables du design system

## Viewport

- Design width: 1440px (desktop)
- Responsive: 768px+ (tablette), 1024px+ (desktop)
- Grid layout adaptatif