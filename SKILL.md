---
name: outils-pointage-design
description: Use this skill to generate well-branded interfaces and assets for OUTILS POINTAGE, either for production or throwaway prototypes/mocks/etc. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.

If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy assets out and create static HTML files for the user to view. If working on production code, you can copy assets and read the rules here to become an expert in designing with this brand.

If the user invokes this skill without any other guidance, ask them what they want to build or design, ask some questions, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.

## Design System Overview

OUTILS POINTAGE is a professional time-tracking and field monitoring platform with GPS geolocation for Team Leads and Managers.

**Visual Identity:**
- Professional blue palette (#0052CC primary) inspired by Atacadão brand
- Gold accent (#FFD700) for premium elements
- Inter font family for UI, Roboto Mono for data
- Clean, modern, mobile-first design
- OpenStreetMap/Mapbox style maps

**Two Core Tools:**
1. **Outil Pointage** — Mobile-first interface for Team Leads to check in/out field workers (animateurs)
2. **Outil Manager** — Desktop dashboard for managers to track KPIs, attendance rates, and real-time GPS positions

**Status System:**
- 🟢 Disponible (Available) — Green
- 🔵 En mission (On mission) — Blue  
- 🔴 Absent — Red
- ⚪ Hors ligne (Offline) — Gray

**Key Components Available:**
- Login screens
- KPI cards with statistics
- Status badges
- Interactive maps (Leaflet.js)
- Data tables with filters
- Charts (Chart.js)
- Mobile bottom navigation
- Desktop sidebar navigation

**Organizational Structure:**
- Ville (City) → Secteur (Sector) → Animateur (Field worker)
- One Team Lead per city
- GPS tracking mandatory for all check-ins

Explore `colors_and_type.css` for the complete design token system, and `ui_kits/` folders for full working prototypes.