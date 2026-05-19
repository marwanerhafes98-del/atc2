# OUTILS POINTAGE — Design System

## Vue d'ensemble

**OUTILS POINTAGE** est une plateforme web professionnelle de gestion de pointage et de suivi terrain avec géolocalisation en temps réel, inspirée de l'identité visuelle Atacadão.

Le système comprend **deux outils connectés** :

### 1. **Outil Pointage** (Team Lead)
Interface mobile-first pour les Team Leads qui effectuent le pointage quotidien des animateurs terrain :
- Pointage rapide (entrée/sortie)
- Géolocalisation en temps réel
- Validation des présences
- Vue liste des animateurs par secteur
- Statuts visuels (Disponible, En mission, Absent, Hors ligne)

### 2. **Outil Manager** (Dashboard de suivi)
Interface desktop/mobile pour les managers qui suivent les KPIs et l'activité globale :
- Dashboard avec statistiques en temps réel
- Nombre d'animateurs disponibles / absents
- Répartition par secteur et ville
- Pourcentages et taux de présence
- Carte interactive des positions
- Historique complet et rapports
- Graphiques d'analyse

---

## Sources et contexte

**Sources fournies :**
- Brief fonctionnel complet (document initial)
- Inspiration visuelle : Logo Atacadão (chaîne brésilienne de supermercados)
- Recherche web : identité Atacadão via Wikimedia Commons, seeklogo.com

**Contraintes métier :**
- Structure organisationnelle : Ville → Secteur → Animateurs
- Un Team Lead par ville
- Géolocalisation GPS obligatoire lors des pointages
- Traçabilité complète (historique, logs, positions)
- Multi-rôles : Super Admin, Team Lead, Animateur

**Choix de design validés :**
- Palette : Bleu professionnel (confiance, corporate)
- Style : Dashboard moderne et minimaliste
- Cartes : OpenStreetMap / Mapbox style
- Device : Mobile-first pour Pointage, Desktop+Mobile pour Manager
- Langue : Français uniquement
- Fonctionnalités visuelles : Notifications/alertes visuelles

---

## Structure du projet

```
/
├── README.md                          # Ce fichier
├── SKILL.md                           # Métadonnées pour Agent Skills
├── colors_and_type.css               # Variables CSS : couleurs + typographie
├── fonts/                            # Webfonts (Google Fonts)
├── assets/                           # Logo, icônes, illustrations
│   ├── logo.svg
│   ├── logo-white.svg
│   └── icons/
├── preview/                          # Cards pour l'onglet Design System
│   ├── colors-primary.html
│   ├── colors-semantic.html
│   ├── typography.html
│   ├── spacing.html
│   ├── components-buttons.html
│   ├── components-status.html
│   └── map-preview.html
├── ui_kits/
│   ├── pointage/                     # Outil Pointage (Team Lead)
│   │   ├── README.md
│   │   ├── index.html               # Vue principale
│   │   ├── LoginScreen.jsx
│   │   ├── PointageList.jsx
│   │   ├── PointageForm.jsx
│   │   └── MapView.jsx
│   └── manager/                      # Outil Manager (Dashboard)
│       ├── README.md
│       ├── index.html               # Dashboard principal
│       ├── Sidebar.jsx
│       ├── KPICards.jsx
│       ├── AnimateursTable.jsx
│       ├── MapDashboard.jsx
│       └── Charts.jsx
└── SKILL.md
```

---

## Index des fichiers clés

### Fondations visuelles
- **colors_and_type.css** — Variables CSS pour couleurs, typographie, spacing
- **assets/logo.svg** — Logo OUTILS POINTAGE (inspiré Atacadão)
- **fonts/** — Inter (UI) et Roboto Mono (données/code)

### Design System Cards (preview/)
Visible dans l'onglet **Design System** de l'interface :
- Couleurs primaires et neutres
- Couleurs sémantiques (succès, alerte, erreur, info)
- Échelle typographique
- Système de spacing et élévation
- Composants (boutons, badges de statut, cartes)
- Aperçu de carte interactive

### UI Kits
- **ui_kits/pointage/** — Interface mobile Team Lead (pointage rapide)
- **ui_kits/manager/** — Dashboard manager (analytics et suivi)

Chaque UI kit contient des composants React modulaires et un index.html interactif.

---

---

## CONTENT FUNDAMENTALS

### Ton et style rédactionnel

**Voix de la marque :** Professionnelle, efficace, claire et directe.

**Principes de rédaction :**
- **Clarté avant tout** — Terminologie métier précise sans jargon inutile
- **Verbes d'action** — "Pointer", "Valider", "Localiser", "Suivre"
- **Impératif et infinitif** — "Valider la présence", "Voir l'historique"
- **Langage inclusif** — Animateur·rice utilisé dans la documentation, mais "Animateur" dans l'UI pour économiser l'espace mobile

**Casse et ponctuation :**
- Titres principaux en **Title Case** : "Gestion des Animateurs"
- Boutons d'action en **Sentence case** : "Valider le pointage"
- Labels de formulaire : **Sentence case** avec deux-points : "Heure d'arrivée :"
- Pas de point final sur les boutons et labels courts
- Points sur les messages d'aide et notifications complètes

**Voix grammaticale :**
- **2ème personne implicite** — "Voir les animateurs" (pas "Vous pouvez voir")
- **Phrases courtes** — Max 15 mots pour les instructions mobiles
- **Numération** — Chiffres arabes pour les données (124 animateurs, 5 secteurs)

**Vocabulaire métier standardisé :**
- ✅ "Pointage" (pas "Check-in", "Émargement")
- ✅ "Animateur" (pas "Agent", "Employé")
- ✅ "Team Lead" (pas "Responsable", "Chef d'équipe")
- ✅ "Secteur" (pas "Zone", "Périmètre")
- ✅ "Disponible / En mission / Absent / Hors ligne" (statuts standards)

**Usage des emoji et symboles :**
- ❌ **Pas d'emoji** dans l'interface de production
- ✅ Icônes vectorielles SVG uniquement
- ✅ Symboles Unicode acceptables : ·, →, %, •

**Exemples de formulations :**
- ❌ "Vous devez autoriser la géolocalisation pour continuer"
- ✅ "Autorisation GPS requise"
- ❌ "Cliquez ici pour valider la présence de cet animateur"
- ✅ "Valider la présence"
- ❌ "Il n'y a pas de données à afficher pour le moment"
- ✅ "Aucune donnée disponible"

---

## VISUAL FOUNDATIONS

### Palette de couleurs

**Couleur principale : Bleu professionnel (#0052CC)**
- Évoque la confiance, la fiabilité, le professionnalisme
- Utilisé pour les CTA primaires, navigation active, liens
- Fort contraste avec blanc pour accessibilité mobile

**Couleur d'accent : Or (#FFD700)**
- Inspiration Atacadão
- Utilisée avec parcimonie : badges premium, alertes importantes
- Contraste avec le bleu principal

**Système de statuts :**
- 🟢 **Disponible** : Vert (#12A150)
- 🔵 **En mission** : Bleu (#0065FF)
- 🔴 **Absent** : Rouge (#EF4444)
- ⚪ **Hors ligne** : Gris (#8B949E)

### Typographie

**Police principale : Inter**
- Famille moderne, lisible sur petit écran
- Weights utilisés : 400 (Regular), 500 (Medium), 600 (Semibold), 700 (Bold), 800 (Extrabold)
- Excellent pour les interfaces data-heavy

**Police monospace : Roboto Mono**
- Pour les données numériques (heures, coordonnées GPS, IDs)
- Alignement vertical des chiffres
- Weights : 400, 500, 600

**Hiérarchie mobile-first :**
- H1 : 36px (extrabold) — Titres de page
- H2 : 30px (bold) — Sections principales
- H3 : 24px (bold) — Sous-sections
- Body : 16px (regular) — Texte courant
- Small : 14px — Métadonnées, timestamps
- Tiny : 12px — Labels minimaux, badges

**Minimum lisible mobile : 12px** (badges, pills)

### Spacing et layout

**Échelle de spacing : Multiple de 4px**
- Mobile : Padding minimal 16px (confort au pouce)
- Desktop : Padding de sections 24-48px
- Gap entre éléments : 8px (compact), 16px (confortable), 24px (aéré)

**Hit targets mobiles : Minimum 44×44px**
- Boutons : 48px hauteur par défaut
- Icons cliquables : 40×40px zone tactile
- Switches et checkboxes : 48px zone

### Élévation et profondeur

**Système de shadow à 6 niveaux :**
- Flat (élévation 0) : Éléments inline, badges
- xs/sm : Cartes simples, inputs
- md : Cartes interactives, dropdowns
- lg : Modals, sheets
- xl/2xl : Notifications flottantes, toasts

**Pas de neumorphisme ni glassmorphism** — Clarté et lisibilité avant tout.

### Backgrounds et textures

- **Fond principal** : Blanc pur (#FFFFFF)
- **Fond secondaire** : Gris très clair (#F6F8FA) pour sections alternées
- **Overlay modals** : Noir 75% opacité
- **Pas de gradients** sauf dans les cartes de statistiques (subtil)
- **Pas d'images de fond** sur les zones fonctionnelles
- **Carte interactive** : Fond Mapbox/OSM avec overlay bleu semi-transparent pour les zones

### Interactivité

**Hover states (desktop) :**
- Boutons : Assombrissement 10% + cursor pointer
- Cartes : Élévation +1 niveau
- Liens : Soulignement

**Press states (mobile) :**
- Opacité 70% pendant le tap
- Pas d'animation de shrink (mauvais pour précision)

**Focus states :**
- Ring bleu 2px offset 2px (accessibilité clavier)
- Pas de outline par défaut (supprimé sur mobile)

**Transitions :**
- Durée standard : 150ms
- Easing : ease-out pour entrées, ease-in pour sorties
- Properties animées : opacity, transform, background-color
- **Pas d'animations complexes** (économie batterie mobile)

### Borders et coins

**Border radius :**
- Boutons : 6px (--radius-md)
- Cartes : 8px (--radius-lg)
- Modals : 12px (--radius-xl)
- Badges : 4px ou full (pill)
- Avatars : full (circle)

**Borders :**
- Par défaut : 1px solid var(--neutral-200)
- Focus : 2px solid var(--primary-600)
- Error : 2px solid var(--error-500)

### Iconographie

**Système : Lucide Icons** (via CDN)
- Style : Stroke, 2px weight
- Taille mobile : 20px (small), 24px (default), 32px (large)
- Couleur : Hérite du parent ou explicit var(--neutral-600)

**Usage :**
- Navigation : Icons + labels (mobile)
- Boutons primaires : Label seul (pas d'icon pour CTA principal)
- Boutons secondaires : Icon + label ou icon seul si évident
- Status badges : Dot coloré + label (pas d'icon)

**Positions GPS sur carte :**
- Pin bleu pour animateur en mission
- Pin vert pour animateur disponible
- Pin gris pour dernière position connue (hors ligne)

---

## ICONOGRAPHY

### Système d'icônes

**Source : Lucide Icons** (https://lucide.dev)
- Bibliothèque open-source, style cohérent stroke 2px
- CDN : `https://unpkg.com/lucide@latest/dist/umd/lucide.min.js`
- Usage : `<i data-lucide="icon-name"></i>` puis `lucide.createIcons()`

**Palette d'icônes utilisées :**

**Navigation et actions :**
- `home` — Accueil
- `users` — Gestion animateurs
- `map-pin` — Géolocalisation
- `calendar` — Historique
- `bar-chart-3` — Statistiques
- `settings` — Paramètres
- `log-out` — Déconnexion

**Pointage :**
- `clock` — Horaires, pointage
- `check-circle` — Valider présence
- `x-circle` — Marquer absence
- `map` — Voir sur carte
- `navigation` — GPS actif

**Statuts :**
- Pas d'icônes pour les statuts — uniquement dot coloré + label

**Data et actions :**
- `search` — Recherche
- `filter` — Filtres
- `download` — Export
- `upload` — Import
- `refresh-cw` — Actualiser
- `more-vertical` — Menu contextuel
- `chevron-down` — Dropdown

**Alertes et feedback :**
- `alert-circle` — Alerte
- `info` — Information
- `alert-triangle` — Avertissement

### Règles d'usage

1. **Toujours accompagner d'un label** sur mobile (accessibilité)
2. **Taille cohérente** : 20px ou 24px (jamais mélanger)
3. **Couleur sémantique** : Hériter du contexte ou var(--color-fg-secondary)
4. **Pas d'icônes décoratives** — Seulement fonctionnelles
5. **Éviter les icônes trop abstraites** — Préférer labels texte si ambiguïté

### Assets graphiques

**Logo :**
- `assets/logo.svg` — Logo couleur sur fond clair
- `assets/logo-white.svg` — Logo blanc sur fond sombre
- Usage : Header, écrans de login, exports PDF

**Illustrations :**
- Aucune illustration custom dans V1
- États vides : Icon + texte simple (pas d'empty state illustration)
- Privilégier la clarté fonctionnelle aux ornements

**Photos de profil :**
- Format : Cercle, 32px (liste), 48px (détail), 80px (profil complet)
- Fallback : Initiales sur fond coloré dérivé du nom (hash)
- Pas de photo par défaut générique

---

**Statut :** ✅ Fondations complètes
