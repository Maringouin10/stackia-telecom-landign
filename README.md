# Stackia Telecom — Landing page

Page web (single-file `index.html`) pour **Stackia Telecom**, un firmware mesh
LoRa 915 MHz pour ESP8266 / ESP32. Le mesh fonctionne sans internet : les nœuds
communiquent en RF via un module LR20-A et les nœuds *home antenna* font le pont
vers un broker MQTT local pour s'intégrer à n8n.

Le design reprend l'identité visuelle Stackia (thème néon violet, fond noir,
particules, cartes glow, animations AOS), réorientée vers la téléphonie mesh —
dans l'esprit de Meshtastic / MeshCore.

## Aperçu

Le site est une page unique avec ancres :

- **Hero** — réseau mesh animé (SVG), accroche, stats clés (915 MHz, 5 sauts…)
- **Fonctionnalités** — sans internet, mesh auto-réparant, pont MQTT/n8n, web UI…
- **Types de nœuds** — `HANDHELD`, `HOME_ANTENNA`, `REPEATER` (cartes + tableau)
- **Comment ça marche** — câblage 3,3 V, commandes PlatformIO
- **Protocole** — format de paquet JSON, topics MQTT, fragmentation, API HTTP
- **Comparaison** — Stackia vs Meshtastic vs MeshCore

## Lancer en local

Aucune étape de build. Ouvrez simplement le fichier dans un navigateur :

```bash
# option 1 : ouvrir directement
xdg-open index.html      # Linux
open index.html          # macOS

# option 2 : petit serveur statique (recommandé)
python3 -m http.server 8000
# puis http://localhost:8000
```

## Dépendances (CDN, aucune installation)

- [Tailwind CSS](https://tailwindcss.com) — styles
- [AOS](https://github.com/michalsnik/aos) — animations au scroll
- [Lucide](https://lucide.dev) — icônes
- Google Fonts — *Inter* & *JetBrains Mono*

Une connexion internet est requise au chargement pour récupérer ces ressources.
