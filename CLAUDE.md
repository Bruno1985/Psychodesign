# PROJET

Psychodesign — [description fonctionnelle à compléter]

# STACK

- Framework : [à compléter]
- Backend : [à compléter]
- Langage : TypeScript strict
- Navigation : [à compléter]

# RÈGLES ABSOLUES

1. TypeScript strict — pas de `any`, pas de cast forcé
2. Commits en anglais, format : `type(scope): message`
3. Pas de commentaires évidents dans le code
4. Un composant = un fichier
5. Les types globaux sont dans `/types/index.ts`

# PRINCIPES DE CODE

Au démarrage de chaque session, lis le package.json ou l'équivalent du projet.
Si React / React Native détecté → appliquer @docs/principles-react.md
Si langage OO détecté (Node avec classes, Python, Java) → appliquer @docs/principles-solid.md
Si les deux coexistent → appliquer les deux fichiers sur leur périmètre respectif.

# ARCHITECTURE

Feature folders : `/features/[nom]/components|hooks|screens`
Shared : `/components`, `/hooks`, `/lib`

# RÉFÉRENCES

- Schéma base de données : @docs/schema.md
- Structure de navigation : @docs/navigation.md
- Design system tokens : @docs/design-tokens.md

# MODE DE RÉPONSE

Apply caveman full mode by default.
Switch to normal verbosity when:
- the task involves architectural decisions
- comparative analysis between two approaches
- code review requiring detailed reasoning
- explicitly asked via `--explain` in the message

# SURVEILLANCE DU CONTEXTE

Estime l'utilisation de la fenêtre de contexte en continu.
Quand tu estimes que le contexte approche 60% de capacité,
signale-le en début de réponse avec :
⚠️ CONTEXTE ~60% — /compact recommandé
