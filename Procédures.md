# Procédures

---

### 1. Processus de développement [Lien ...](#1-processus-de-développement)
### 2. Outil de configuration [Lien ...](#2-outil-de-configuration)
### 3. Teste de l'application [Lien ...](#3-test-de-lapplication)
### 4. Gestion des tickets [Lien ...](#4-gestion-des-tickets)
### 5. Gestion des livraisons [Lien ...](#5-gestion-des-livraisons)

---

### 1. Processus de Développement

- **Adoption du Modèle Agile** : L'approche agile et les cycles de travail en sprints de 3 à 4 semaines pour le développement vont permettre une adaptation flexible et rapide face aux changements, qu'ils soient liés aux besoins du client, aux conditions du marché ou aux retours de la communauté d'utilisateurs.

- **Revue** : À la fin de chaque sprint est organisé une revue pour évaluer le travail accompli.

- **Rétrospective** : Après la revue, la rétrospective est un bilan du sprint qui permet de proposer des axes d'améliorations des processus.

- **Sprint Planning** : C'est un temps pour valider avec toute l'équipe les objectifs et les tickets à embarquer en fonction de la capacité.

- **Réunion hebdomadaire** : Un point d'avancement tous les mardis à **9h45**.
  ```
  Le rendez-vous est composé des 4 points suivants
    1) Les informations à partager à l'équipe ou des questions à partager.
    2) Suivi des tickets du sprint, mise à jour des statuts et des relecteurs sur les ticket en review. Identifier les besoins d'aide
    3) Raffiner 3/4 tickets (dans une limite de temps)
    4) Démo / Atelier / Discutions
  ```

---

### 2. Outil de Configuration

- **Utilisation de Git** : Lire la documentation sur [l'utilisation de GIT](./Utilisation%20de%20GIT.md).

---

### 3. Test de l'Application

- **Tests Automatisés** : Mettre en place une suite de tests automatisés, y compris des tests unitaires, d'intégration
  et de système.
- **Intégration Continue pour les Tests** : Utiliser l'intégration continue pour exécuter les tests automatiquement à
  chaque push et pull request.
- **Tests End-to-End (E2E)** : Implémenter des tests end-to-end automatisés pour valider le flux complet de l'application en fonction de scénarios d'utilisation réels prédéterminés.
- **Feedback Interne** : Demander aux membres du groupe de faire des tests de la nouvelle fonctionnalité développée.

---

### 4. Gestion des Tickets

- **Outil de Suivi des Tickets** : Utiliser le dashboard GitHub Project pour suivre les tâches, les bugs et les
  demandes de fonctionnalités.
- **Catégorisation et Priorisation** : Catégoriser les tickets (par exemple, bugs, nouvelles fonctionnalités,
  améliorations) et les prioriser en fonction de l'urgence et de l'importance et de la [matrice Valeur vs Efforts](https://www.product-master.com/produit/prioriser-roadmap-backlog-matrice-valeur-effort/#:~:text=L'Objectif%20de%20la%20Matrice%20Valeur%20%2F%20Effort,-L'objectif%20de&text=Un%20%C3%A9l%C3%A9ment%20cl%C3%A9%20%C3%A0%20comprendre,les%20valeurs%20entre%20les%20items.).
- **Révisions Régulières** : Examiner régulièrement le backlog pour réévaluer et reprioriser les tickets en fonction de
  l'évolution des besoins.

> [!NOTE]
> [Lien vers le tableau de gestion](https://github.com/orgs/BarraDataSquad/projects/1/views/1)

---

### 5. Gestion des Livraisons

- **Tags** : Ajouter des tags sur les nouvelles livraisons importantes de l'application.
- **Planification des Releases** : Planifier les releases en fonction des objectifs du sprint et des priorités du
  projet.
- **Déploiements Automatisés** : Utiliser des outils de déploiement continu pour automatiser la livraison des versions
  dans les environnements de test et de production.
- **Feedback Post-Livraison** : Recueillir et analyser les retours des utilisateurs ou des membres de l'équipe après
  chaque livraison pour guider les développements futurs.
- **Gestion du changelog** : Documentater l'évolution du projet avec la mise à jour, à chaque nouvelle realease, manuel ou automatique du fichier CHANGELOG.md à la racine du projet. Il doit contenir toutes les modifications significatives (nouvelles fonctionnalités, améliorations, corrections de bugs..) et mentionner les contributeurs des changements. Le changelog doit aussi inclure la datation et le versionnement (majeur, mineur, patch), en suivant les principes du Semantic Versioning (SemVer).

---
