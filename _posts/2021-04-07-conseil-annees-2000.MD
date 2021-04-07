---
layout: post
title: De bons conseils ... des années 2000 ... pour un meilleur code
published: false
---

En parcourant mes flux RSS cette semaine, je suis tombé sur un article de 2000 qui était remonté dans Hacker News ... et qui donnait 12 conseils pour faire du meilleur code et donc mieux réussir ses projets.

On pourrait se dire que 20 ans après et des tsunamis de technologies aidant, cet article ne vaudrait plus grand chose ... Mais *que nenni*. A sa lecture, cet article nous renvoit aux fondamentaux et c'est pour celà qu'il faut la peine d'être remis en exergue.

On part donc d'un postulat simple. 12 questions à se poser, un point par question ou vous répondez *OUI*. Un 12 est parfait, 11 est tolérable mais 10 et moins et vous vous dirigez vers les problèmes.

D'après [Joel Spolsky](https://www.joelonsoftware.com) l'auteur de l'article, la majorité des entreprises qui font du développement sont à 2 ou 3 points !

### 1. Utilisez-vous un outil de gestion de versions

L'objectif est de permettre aux développeurs de mieux travailler en commun, de ne pas perdre de code et de faciliter les mises en production.

__Version 2000 :__
Ici il utilise CVS, qui est un système de gestion de version centralisée, dont la dernière version est sortie en 2008.

__Version 2021 :__
Aujourd'hui, les choses sont bien différentes, mais le principe reste le même. Les systèmes de contrôle de versions sont décentralisés permettant à chacun de travailler à son rythme et surtout sans être connecté au gestionnaire de versions en permanence.

Le logiciel qui a pris le plus de parts de marché est [Git](https://git-scm.com/), donc la première version est sortie en 2005. De nombreuses solutions comme [Github](https://www.github.com) ou [GitLab](https://www.gitlab.com) sont venus se greffer à Git permettant de faciliter et d'intégrer des outils complémentaires.

### 2. Pouvez-vous "compiler" en une étape

L'objectif est de mettre en production le plus simplement possible la dernière version stable contenue dans le gestion de versions.

__Version 2000 :__

L'auteur nous dit que l'idéal est d'avoir un script unique qui permet de récupérer du gestionnaire de version, recompiler, créer les executables, créer le package d'installation ...

Il nous dit que s'il faut de nombreuses étapes pour arriver à une livraison, on devient vite fou et surtout on a un potentiel d'erreur beaucoup plus élevé.

__Version 2021 :__

Ici on est passé un cran au dessus. On parle de CI/CD (Intégration Continue / Déploiement Continu) et l'optimisation est poussé a son extrême puisque qu'il n'y a même plus besoin de lancer un quelconque script manuellement.

En effet, un simple *pull request* dans la branche de production du gestionnaire de versions et tout le système se met en branle ...

L'intégration continue va par *builder*, lancer les tests et merger avec la branche de production si tout s'est passé correctement.

Le déploiement continu và quand à lui détecteer la nouveelle version et la déployer dans l'infrastructure de production automatiquement.

Des outils comme [Jenkins](https://www.jenkins.io/), [Teamcity](https://www.jetbrains.com/fr-fr/teamcity/), [Github Actions](https://github.com/features/actions) ou [Gitlab CI](https://about.gitlab.com/stages-devops-lifecycle/continuous-integration/) vous permettront de mettre en place votre flux d'intégration continue.

[DeployBot](https://deploybot.com/), [AWS CodeDeploy](https://aws.amazon.com/fr/codedeploy/) ou encore [Bamboo](https://www.atlassian.com/fr/software/bamboo) permettront quand à eux de déployer vos applications sur les différentes infrastructures de production.

### 3. Faites-vous une compilation journalière

Et bien ici c'est simple ... rendez-vous à la section précédente :)

### 4. Avez-vous une base de données pour vos bugs

L'objectif est de centraliser et surtout de recueillir le maximum d'informations pour : 

  - avoir toutes les étapes pour reproduire le bug
  - avoir le résultat attendu
  - assigner un responsable à la résolution du bug
  - savoir s'il est fixé ou pas

__Version 2000 :__

L'auteur ne recommande pas d'outil en particulier mais indique que si une solution de gestion de bugs semble trop compliquée (ce qui peut indiquer qu'il n'y avait pas vraiment de solution mature grand publique) une table ou un tableur avec quelques colonnes peuvent faire l'affaire.

__Version 2021 :__

Aujourd'hui nous avons de nombreux outils qui nous permettent de facilement regrouper les bugs et surtout interragir et suivre l'avancement et la résolution de façon fluide.

[Les Issues de Github](https://docs.github.com/en/github/managing-your-work-on-github/about-issues), [les Issues de GitLab](https://docs.gitlab.com/ee/user/project/issues/) ou des outils comme [Jira](https://www.atlassian.com/fr/software/jira) ou [YouTrack](https://www.jetbrains.com/fr-fr/youtrack/) sont rapidement mis en place et intégrés dans les habitudes des développeurs

### 5. Corrigez-vous les bugs avant d'écrire du nouveau code

### 6. Tenez-vous un planning à jour

### 7. Avez-vous des specifications

### 8. Est-ce que les développeurs ont des conditions de travail tranquilles

### 9. Utilisez-vous les meilleurs outils 

### 10. Avez-vous des testeurs

### 11. Est-ce que vos candidats écrivent du code durant les entretiens 

### 12. Faites vous des tests aléatoires d'*utilisabilité*

