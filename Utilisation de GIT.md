# Utilisation de GIT

---

# Introduction

Bienvenue dans le guide de bonnes pratiques pour l'utilisation de Git au sein de notre équipe. Ce document a été conçu
pour servir de référence commune à tous les membres de l'équipe de développement dans l'utilisation de Git et GitHub
pour notre projet.

---

# Objectif

L'objectif principal de ce document est de fournir des directives claires et concises sur :

1. **Conventions de Codage et Commit** : Nous établirons des normes pour les messages de commit, les noms de branches,
   et les commentaires de code pour assurer que notre historique de révision soit facile à suivre et à comprendre.

2. **Workflow Git** : Ce guide détaillera notre workflow Git spécifique, y compris la gestion des branches, les
   stratégies de fusion (merge) et de rebase, afin de maintenir un dépôt propre et organisé.

3. **Revue de Code et Collaboration** : Nous clarifierons le processus de revue de code, y compris comment créer et
   gérer des pull requests, pour favoriser une collaboration efficace et réduire les erreurs.

4. **Documentation et Commentaires** : Des lignes directrices sur la façon de documenter efficacement le code et
   d'utiliser des commentaires pour améliorer la lisibilité et la maintenabilité.

5. **Sécurité et Conformité** : Nous aborderons les meilleures pratiques pour assurer la sécurité de notre code et la
   conformité avec les standards de développement.

En suivant ces directives, nous visons à créer un environnement de développement harmonieux et productif, où chaque
membre de l'équipe peut contribuer efficacement et sans ambiguïté à notre projet commun.

---

## I. Conventions de Codage et Commit

L'objectif de cette section est de définir des normes claires pour le codage et les commits dans notre projet. Ces
conventions sont essentielles pour assurer la lisibilité, la maintenabilité et la traçabilité de notre code.

### 1. Format des Messages de Commit

Un bon message de commit doit être clair, précis et informatif. Il doit permettre à toute personne lisant l'historique
du projet de comprendre rapidement les changements effectués et leur raison. Il ne faut pas hésiter à faire de nombreux
commits.

#### Structure d'un Message de Commit :

- **Type** : Commencez par un des mots suivants décrivant le commit :
    - `fix`: un commit du type `fix` corrige un bug dans votre base de code
    - `feat`: un commit du type `feat` introduit une nouvelle fonctionnalité dans la base de code
    - `docs`: un commit de type `docs` introduit une modification ou un ajout de documentation
    - `build`: Utilisé pour des changements qui affectent le système de build ou les dépendances externes.
    - `chore`: Pour les modifications mineures qui n'affectent pas le code source ou la fonctionnalité de l'application.
    - `ci`: Pour les modifications de pipeline.
    - `perf`: Pour l'amélioration des performances.
- **Scope**: Références aux tickets d'issue ou de bug concernés.
- **Corps du Message** : Fournit des détails supplémentaires. Expliquez le changement.

#### Exemple de Message de Commit :

```text
feat(123): Ajouter une fonction de recherche avancée
docs(123): Documentation développeur pour la recherche avancée
```

### 2. Granularité des Commits

- Chaque commit doit représenter une unité logique de changement. Cela facilite la compréhension des modifications et la
  résolution des problèmes en cas de besoin.
- Évitez les commits trop larges qui incluent des changements non liés.

### 3. Commits Atomiques

- Un commit doit être "atomique", c'est-à-dire qu'il ne devrait pas causer de rupture dans la fonctionnalité existante.
  Testez votre code avant de commettre pour éviter les régressions.

---

## II. Workflow Git

Le workflow Git est un élément crucial pour assurer une gestion efficace et organisée du code source de notre projet. Un
workflow clairement défini aide à minimiser les conflits, facilite la collaboration et permet une meilleure traçabilité
des changements. Voici les aspects clés de notre workflow Git :

### 1. Organisation des Branches

- **Branches Principales** :
    - `main/master` : La branche principale où le code source reflète toujours un état prêt à la production.
    - `develop` : Branche de développement où toutes les fonctionnalités, corrections et autres branches sont fusionnées
      avant d'être déployées en production.

- **Branches Secondaires** :
    - `feature/` : Branches créées pour le développement de nouvelles fonctionnalités. Nommez-les de manière
      descriptive, par exemple `feature/nouvelle-authentification`.
    - `bugfix/` : Branches utilisées pour les corrections de bugs.
    - `hotfix/` : Branches pour les correctifs urgents en production.
    - `release/` : Branches préparant la prochaine version à déployer, permettant la correction de bugs et la
      documentation.

#### Exemple de Branches :

```text
🌱 feature/123-fonction-recherche-avancee
```

### 2. Stratégies de Fusion et de Rebase

- **Fusion (Merge)** :
    - Utilisez `merge` pour intégrer les changements des branches de fonctionnalités dans `develop`. Cela crée un
      historique de fusion qui peut être utile pour suivre les changements.
    - Avant de fusionner dans `develop`, assurez-vous que votre branche est à jour avec les derniers changements
      de `develop`.

- **Rebase** :
    - Préférez `rebase` pour les branches de fonctionnalité avant de les fusionner dans `develop`. Cela aide à maintenir
      un historique propre et linéaire.
    - `Rebase` est également recommandé pour intégrer les derniers changements de `develop` ou `main` dans votre branche
      de fonctionnalité.

### 3. Revue de Code et Pull Requests

- Toutes les modifications doivent être soumises sous forme de pull requests (PRs) pour permettre la revue de code.
- Les PRs doivent être liées aux tickets d'issues correspondants si applicable.
- Chaque PR doit être revue par au moins 2 ou 3 membres de l'équipe avant la fusion.
- Encouragez les commentaires constructifs dans les revues de PR pour améliorer la qualité du code.

### 4. Gestion des Releases

- Lorsqu'une release est prête dans `develop`, créez une branche `release/` pour les tests finaux et les ajustements
  mineurs.
- Une fois la release validée, fusionnez-la dans `main` et taggez avec un numéro de version.
- Après la fusion dans `main`, faites également un `merge` de `main` dans `develop` pour garder cette dernière à jour.

### 5. Résolution des Conflits

- En cas de conflits lors des merges ou rebases, résolvez-les immédiatement pour maintenir l'intégrité du code.
- Communiquez avec les membres de l'équipe concernés pour résoudre les conflits de manière collaborative.

### 6. Utilisation de Tags

- Utilisez des tags pour marquer les points de release dans l'historique Git. Les tags doivent suivre le versionnage
  sémantique (par exemple, v1.2.3).

---