# Système de couleurs

## Constantes globales

```js
BG      = "#f7f5f2"  // fond page
CARD    = "#ffffff"  // fond carte
BORDER  = "#e8e4de"  // bordures
TEXT    = "#18181b"  // texte principal
MUTED   = "#78716c"  // texte secondaire
XMUTED  = "#a8a29e"  // texte très atténué
```

## Color maps — structure commune

```js
{ light, text, border }         // KPI_C, PHASE_C
{ light, text, border, accent } // CAT_C
{ light, text, border, icon }   // TYPE_C (icon = unicode string)
```

## Maps disponibles

| Map | Clés |
|-----|------|
| CAT_C | Jugement, Decision, Social, Memoire, Perception, Cognition, Comportement, Motivation |
| TYPE_C | Piege, Levier, LesDeux, Loi, Principe, Concept |
| KPI_C | Conversion, Activation, Retention, Engagement, NPS, Velocite, ARPU |
| PHASE_C | Recherche, Ideation, Prototypage, Test, Presentation, Handoff |

## Règle absolue

Toute valeur de couleur dans un composant JSX vient d'une color map ou d'une constante globale.
Jamais de hex en dur dans le JSX.

```js
// ✓
style={{ background: c.light, color: c.text }}

// ✗
style={{ background: "#f5f0ff", color: "#6d28d9" }}
```
