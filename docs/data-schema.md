# Schéma des données

## Item Biais

```js
{
  id:      number,        // identifiant unique (1–33 actuellement)
  name:    string,        // nom du biais en français
  cat:     BiasCategory,  // "Jugement"|"Decision"|"Social"|"Memoire"
  tagline: string,        // phrase-clé courte, format : "Sujet + verbe."
  type:    BiasType,      // "Piege"|"Levier"|"LesDeux"
  kpis:    KPI[],         // sous-ensemble de ALL_KPIS (1–3 éléments)
  phases:  Phase[],       // sous-ensemble de ALL_PHASES (1–3 éléments)
  pattern: string,        // pattern design associé (préfixé "Pattern :" ou "Anti-pattern :")
  def:     string,        // définition neutre et factuelle
  prod:    string,        // exemple concret produit numérique
  proj:    string,        // exemple concret équipe/projet
  actD:    string,        // action immédiate pour le designer
  actE:    string,        // action immédiate pour l'équipe ou le PM
  counter: string,        // contre-mesure ou principe à retenir
}
```

## Item Psychologie

Même structure que Biais, avec des types différents :

```js
cat:  PsychCategory  // "Perception"|"Cognition"|"Comportement"|"Motivation"
type: PsychType      // "Loi"|"Principe"|"Concept"
```

IDs commencent à 101 pour éviter les collisions avec les biais.

## Constantes de filtres

```js
BIAS_CATS  = ["Jugement","Decision","Social","Memoire"]
PSYCH_CATS = ["Perception","Cognition","Comportement","Motivation"]
BIAS_TYPES = ["Piege","Levier","LesDeux"]
PSYCH_TYPES = ["Loi","Principe","Concept"]
ALL_KPIS   = ["Conversion","Activation","Retention","Engagement","NPS","Velocite","ARPU"]
ALL_PHASES = ["Recherche","Ideation","Prototypage","Test","Presentation","Handoff"]
```

## Ajout d'un item

1. Ajouter à `biases[]` ou `psychology[]` avec un id unique
2. `cat` et `type` doivent être dans les constantes de filtres de la section
3. `kpis` et `phases` : clés JS sans accents (ex: "Retention", "Ideation")
4. Tester les filtres après ajout
