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

**Version 2000 : **
Ici il utilise CVS, qui est un système de gestion de version centralisée, dont la dernière version est sortie en 2008.

**Version 2021 : **
Aujourd'hui, les choses sont bien différentes, mais le principe reste le même. Les systèmes de contrôle de versions sont décentralisés permettant à chacun de travailler à son rythme et surtout sans être connecté au gestionnaire de versions en permanence.

Le logiciel qui a pris le plus de parts de marché est [Git](https://git-scm.com/), donc la première version est sortie en 2005. De nombreuses solutions comme [Github](https://www.github.com) ou [GitLab](https://www.gitlab.com) sont venus se greffer à Git permettant de faciliter et d'intégrer des outils complémentaires.

### 2. Pouvez-vous "compiler" en une étape

L'objectif est de mettre en production le plus simplement possible la dernière version stable contenue dans le gestion de versions.

**Version 2000 : **

L'auteur nous dit que l'idéal est d'avoir un script unique qui permet de récupérer du gestionnaire de version, recompiler, créer les executables, créer le package d'installation ...

Il nous dit que s'il faut de nombreuses étapes pour arriver à une livraison, on devient vite fou et surtout on a un potentiel d'erreur beaucoup plus élevé.

**Version 2021 : **

Ici on est passé un cran au dessus. On parle de CI/CD (Intégration Continue / Déploiement Continu) et l'optimisation est poussé a son extrême puisque qu'il n'y a même plus besoin de lancer un quelconque script manuellement.

En effet, un simple push dans la branche de production est tout le système se met en branle ...
### 3. Faites-vous une compilation journalière

### 4. Avez-vous une base de données pour vos bugs

### 5. Corrigez-vous les bugs avant d'écrire du nouveau code

### 6. Tenez-vous un planning à jour

### 7. Avez-vous des specifications

### 8. Est-ce que les développeurs ont des conditions de travail tranquilles

### 9. Utilisez-vous les meilleurs outils 

### 10. Avez-vous des testeurs

### 11. Est-ce que vos candidats écrivent du code durant les entretiens 

### 12. Faites vous des tests aléatoires d'*utilisabilité*

