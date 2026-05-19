# OUTIL POINTAGE — UI Kit

## Vue d'ensemble

Interface mobile-first pour les **Team Leads** qui effectuent le pointage quotidien des animateurs terrain.

## Fonctionnalités principales

- **Login sécurisé** — Authentification par email/password
- **Liste des animateurs** — Vue par secteur avec statuts en temps réel
- **Pointage rapide** — Formulaire d'entrée/sortie avec géolocalisation
- **Vue carte** — Positions GPS des animateurs sur carte interactive
- **Historique** — Consultation des pointages passés

## Composants

- `LoginScreen.jsx` — Écran de connexion
- `AnimateursList.jsx` — Liste scrollable avec badges de statut
- `PointageForm.jsx` — Formulaire de pointage (entrée/sortie)
- `MapView.jsx` — Carte interactive avec pins géolocalisés
- `Navigation.jsx` — Bottom nav mobile

## Technologies

- React 18 + Babel standalone
- Leaflet.js pour les cartes (OpenStreetMap)
- Lucide Icons
- CSS Variables du design system

## Viewport

- Design width: 375px (iPhone SE)
- Optimisé pour 375-414px
- Touch-friendly (44px minimum hit targets)