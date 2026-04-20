# PROJET

Psychodesign — Référentiel public pour designers : biais cognitifs et principes de psychologie appliqués au design produit.
Audience : designers (junior à senior), accès libre, lecture et exploration.

# STACK

- Framework : React (JavaScript — pas TypeScript)
- Styles : Inline styles uniquement — zéro CSS class, zéro lib externe
- Persistance : window.storage (API custom de la plateforme)
- Navigation : aucune — single-page, sections par état React
- Fonts : Plus Jakarta Sans + Playfair Display (Google Fonts)

# RÈGLES ABSOLUES

1. JavaScript vanilla — pas de TypeScript
2. Inline styles uniquement — toutes les couleurs passent par les color maps
3. UI en français — labels, copy, messages, placeholders
4. Commits en anglais, format : `type(scope): message`
5. Pas de commentaires évidents dans le code
6. Jamais de valeur hex en dur dans un composant — utiliser les constantes ou color maps

# PRINCIPES DE CODE

Au démarrage de chaque session, appliquer @docs/principles-react.md

# ARCHITECTURE

Fichier principal : App.jsx (données + composants dans un seul fichier actuellement)

Structure interne :
- Color maps globales : CAT_C, TYPE_C, KPI_C, PHASE_C → voir @docs/color-system.md
- Données : arrays `biases[]` et `psychology[]` → voir @docs/data-schema.md
- Composants : DropFilter, Opt, Chip, Card, ExBox, App
- Labels localisés : CAT_LABEL, TYPE_LABEL, KPI_LABEL, PHASE_LABEL

# MODE DE RÉPONSE

Apply caveman full mode by default.
Switch to normal verbosity when:
- architectural decisions
- comparative analysis between approaches
- explicitly asked via `--explain`

# SURVEILLANCE DU CONTEXTE

Estime l'utilisation de la fenêtre de contexte en continu.
Quand tu estimes que le contexte approche 60% de capacité,
signale-le en début de réponse avec :
⚠️ CONTEXTE ~60% — /compact recommandé
