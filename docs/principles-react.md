# Principes React / React Native

## Composants

- Un composant = un fichier, un seul niveau de responsabilité
- Fonctionnel uniquement, pas de classes
- Props typées explicitement — pas d'inférence implicite
- Pas de logique métier dans le rendu — extraire dans un hook

## Hooks

- Un hook = une logique (pas de hooks fourre-tout)
- Préfixe `use` obligatoire
- Retourner uniquement ce qui est consommé à l'extérieur
- Effets de bord isolés dans `useEffect`, nettoyés si nécessaire

## Composition

- Préférer la composition à l'héritage
- Éviter le prop drilling au-delà de 2 niveaux — context ou state manager
- `children` pour les slots génériques, props nommées pour les slots sémantiques

## Types

- Props : interface nommée `[ComponentName]Props`
- Hooks : type de retour explicite si non trivial
- Éviter `React.FC` — typer directement les props
- `as const` pour les énumérations de valeurs

## Performance

- `useMemo` et `useCallback` uniquement si profileé ou cas évident (liste longue, re-render coûteux)
- Pas de mémo prématuré
- `key` stables sur les listes — jamais l'index si la liste est réordonnée
