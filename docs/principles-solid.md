# Principes SOLID

## S — Single Responsibility

Une classe / module = une raison de changer.
Si tu décris le rôle avec "et", c'est deux responsabilités.

```ts
// ✗ UserService gère les users ET envoie des emails
// ✓ UserRepository + EmailService séparés
```

## O — Open / Closed

Ouvert à l'extension, fermé à la modification.
Préférer l'injection de comportement aux conditions croissantes.

```ts
// ✗ switch (type) { case 'A': ... case 'B': ... }
// ✓ interface Handler { handle(input): void } + registry
```

## L — Liskov Substitution

Un sous-type doit pouvoir remplacer son type parent sans casser le comportement.
Ne pas restreindre ou étendre le contrat de la classe parente.

## I — Interface Segregation

Interfaces ciblées, pas de méga-contrats.
Le consommateur ne doit pas dépendre de méthodes qu'il n'utilise pas.

```ts
// ✗ interface Repository { read(); write(); delete(); export(); notify(); }
// ✓ ReadRepository + WriteRepository séparés, combinés si besoin
```

## D — Dependency Inversion

Dépendre des abstractions, pas des implémentations.
Les modules de haut niveau ne doivent pas importer directement les modules bas niveau.

```ts
// ✗ class Service { db = new PostgresClient() }
// ✓ class Service { constructor(private db: DatabasePort) {} }
```
