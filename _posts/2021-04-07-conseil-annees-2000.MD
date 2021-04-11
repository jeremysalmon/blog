---
layout: post
title: De bons conseils ... des années 2000 ... pour un meilleur code
published: false
---

En parcourant mes flux RSS cette semaine, je suis tombé sur un article de 2000 qui était remonté dans Hacker News ... et qui donnait 12 conseils pour faire du meilleur code et donc mieux réussir ses projets.

On pourrait se dire que 20 ans après et des tsunamis de technologies aidant, cet article ne vaudrait plus grand chose ... Mais *que nenni*. A sa lecture, l'auteur nous renvoit aux fondamentaux et c'est pour celà qu'il faut la peine d'être remis en exergue.

On part donc d'un postulat simple. 12 questions à se poser, un point par question ou vous répondez *OUI*. Un 12 est parfait, 11 est tolérable mais 10 et moins et vous vous dirigez vers les problèmes.

D'après [Joel Spolsky](https://www.joelonsoftware.com) l'auteur de l'article, la majorité des entreprises qui font du développement sont à 2 ou 3 points ... mais çà c'était en 2000.

### 1. Utilisez-vous un outil de gestion de versions

L'objectif est de permettre aux développeurs de mieux travailler en commun, de ne pas perdre de code et de faciliter les mises en production.

__Version 2000 :__
Ici il utilise CVS, qui est un système de gestion de version centralisée, dont la dernière version est sortie en 2008.

__Version 2021 :__
Aujourd'hui, les choses sont bien différentes, mais le principe reste le même. Les systèmes de contrôle de versions sont décentralisés permettant à chacun de travailler à son rythme et surtout sans avoir besoin d'être connecté au gestionnaire de versions en permanence.

Le logiciel qui a pris le plus de parts de marché est [Git](https://git-scm.com/), donc la première version est sortie en 2005. De nombreuses solutions comme [Github](https://www.github.com) ou [GitLab](https://www.gitlab.com) sont venus se greffer à Git permettant de faciliter et d'intégrer des outils complémentaires.

### 2. Pouvez-vous "compiler" en une étape

L'objectif est de mettre en production le plus simplement possible la dernière version stable contenue dans le gestionnaire de versions.

__Version 2000 :__

L'auteur nous dit que l'idéal est d'avoir un script unique qui permet de récupérer du gestionnaire de version, recompiler, créer les executables, créer le package d'installation ...

Pour lui, plus nombreuses sont les étapes pour arriver à une livraison, plus vite on devient fou et surtout on augmente les possibilités d'occurences d'erreurs humaines.

__Version 2021 :__

Ici on est passé un cran au dessus. On parle de CI/CD (Intégration Continue / Déploiement Continu) et l'optimisation est poussée à son extrême puisque qu'il n'y a même plus besoin de lancer un quelconque script manuellement.

En effet, un simple *pull request* dans la branche de production du gestionnaire de versions et tout le système se met en branle ...

L'intégration continue va *builder*, lancer les tests et merger avec la branche de production si tout c'est passé correctement.

Le déploiement continu và quand à lui détecter la nouvelle version et la déployer dans l'infrastructure de production automatiquement.

Des outils comme [Jenkins](https://www.jenkins.io/), [Teamcity](https://www.jetbrains.com/fr-fr/teamcity/), [Github Actions](https://github.com/features/actions) ou [Gitlab CI](https://about.gitlab.com/stages-devops-lifecycle/continuous-integration/) permettent de mettre en place votre flux d'intégration continue simplement.

[DeployBot](https://deploybot.com/), [AWS CodeDeploy](https://aws.amazon.com/fr/codedeploy/) ou encore [Bamboo](https://www.atlassian.com/fr/software/bamboo) permettent quand à eux de déployer vos applications sur les différentes infrastructures de production.

### 3. Faites-vous une compilation journalière

Et bien ici c'est simple ... rendez-vous à la section précédente :)

### 4. Avez-vous une base de données pour vos bugs

L'objectif est de centraliser et surtout de recueillir le maximum d'informations pour : 

  - avoir toutes les étapes pour reproduire le bug
  - avoir le résultat attendu
  - assigner un responsable à la résolution du bug
  - savoir s'il est fixé ou pas

__Version 2000 :__

L'auteur ne recommande pas d'outil en particulier mais indique que si une solution de gestion de bugs semble trop compliquée (ce qui peut indiquer qu'il n'y avait pas vraiment de solution mature grand publique en 2000) une table ou un tableur avec quelques colonnes peuvent faire l'affaire.

__Version 2021 :__

Aujourd'hui nous avons de nombreux outils qui nous permettent de facilement regrouper les bugs et surtout interragir et suivre l'avancement et la résolution de façon fluide.

[Les Issues de Github](https://docs.github.com/en/github/managing-your-work-on-github/about-issues), [les Issues de GitLab](https://docs.gitlab.com/ee/user/project/issues/) ou des outils comme [Jira](https://www.atlassian.com/fr/software/jira) ou [YouTrack](https://www.jetbrains.com/fr-fr/youtrack/) sont rapidement mis en place et intégrés dans les habitudes des développeurs.

### 5. Corrigez-vous les bugs avant d'écrire du nouveau code

Joel nous parle de la désastreuse mauvaise gestion du développement des premières versions de Microsoft Word. Des développeurs qui se ruent sur le code, pas de corrections de bugs. un planning de fonctionnalités basé sur une checklist de fonctionnalités *"a convertir en bug"*.

Puis ils sont passés à une méthode "Zéro Défaut" qui mettait la priorité sur la correction de bugs, avant l'implémentation de nouvelles fonctionnalités.

Corriger un bug *frais* prendra toujours moins de temps que d'entretenir une dette technique qui s'accumule, grossit et décourage tout le monde quand il faut se mettre à faire les corrections.

Et avoir une base de code en permanence exempte de bugs permet de réagir plus vite à un concurrent qui introduit une *killer* feature dans sa solution pour vous concurrencer.

__Version 2021 :__

Dans les années 2000 on faisait encore dans la majorité des cas des logiciels [comme des Cathédrales](https://fr.wikipedia.org/wiki/La_Cath%C3%A9drale_et_le_Bazar) et il était courant de développer pendant des mois voir des années avant de sortir une première version de production.

Aujourd'hui les [méthodes agiles](https://fr.wikipedia.org/wiki/M%C3%A9thode_agile), le [Release early, Release often](https://fr.wikipedia.org/wiki/Release_early,_release_often) rendent ce point 5 un peu caduque.

Les habitudes des développeurs, des managers et des clients sont maintenant orientés vers des mises en production rapide et des applications  qui s'améliorent pas incrément.

### 6. Tenez-vous un planning à jour

La planification des projets de développement était en 2000 et reste en 2021 une étape douloureuse, difficile et souvent râtée.

Toutefois, comme nous l'avons vu dans le point 5, les applications de 2021 ne sont plus des monolithes développés pendant des mois. 

La planification n'est donc plus vraiment placée au même niveau. Nous raisonnons en [sprints](https://searchsoftwarequality.techtarget.com/definition/Scrum-sprint) de courtes durées (de quelques jours à quelques semaines) et les premières versions arrivent généralement en moins d'une année ce qui facilite grandement le positionnement de jalons auprès des managers et des clients.

### 7. Avez-vous des specifications

__Version 2000 :__

Les spécifications reprenaient toutes les fonctionnalités que l'application devait implémenter. Des méthodes comme [Merise](https://fr.wikipedia.org/wiki/Merise_(informatique)) ou [UML](https://fr.wikipedia.org/wiki/UML_(informatique)) permettait de structurer son projet et de poser d'une façon précise l'ensemble des spécifications.

__Version 2021 :__

Les méthodes agiles ont changées la donne, en se basant plus sur des [Récits Utilisateurs](https://fr.wikipedia.org/wiki/R%C3%A9cit_utilisateur) que sur de longues spécifications crées en amont du lancement du projet de développement.

### 8. Est-ce que les développeurs ont des conditions de travail tranquilles

__Version 2000 :__

On parle déjà de la nécessité pour un développeur d'entrer *dans le Flow* ou "dans la zone", ce moment de super-concentration ou le temps n'existe plus et les idées sont fluides. C'est particulièrement vrai pour un développeur qui doit se mettre un *contexte* en tête et ne plus en sortir avant d'avoir résolu son problème.

Rappelons tout de même le contexte des années 2000. Pas de smartphone, un Internet très limité, pas de réseaux sociaux ... Je me souviens que ma productivité était meilleure en ces temps là ... mais c'était peut-être la jeunesse ;).

__Version 2021 :__

Ici nous avons plutôt été a reculons. Smartphone, réseaux sociaux omniprésents, outils de communication multicanaux, Internet a outrance ... font qu'*entrer dans la zone" est de plus en plus difficile même avec la meilleur volonté du monde.

Des méthodes comme [Pomodoro](https://fr.wikipedia.org/wiki/Technique_Pomodoro) essaye tant bien que mal de concentrer le flux d'attention des développeurs sur des périodes de 25 min.

De nouveaux objets comme les casques audio qui nous permettent de nous isoler font également parti des habitudes de travail actuelle ...

Mais sur ce point, je suis plutôt d'avis pessimiste et je pense qu'en 2000 les conditions étaient bien meilleures pour réussir une entrée dans le *Flow*

### 9. Utilisez-vous les meilleurs outils 

__Version 2000 :__

Dans l'article on parle de processeur un peu trop lent à la compilation et qui pousse les devs à faire autre chose, du fait de mettre un deuxième écran, d'acheter des logiciels pour par exemple faire des icônes, d'avoir des disques durs trop petits pour stocker toutes ses informations ... et de rendre les programmeurs malheureux et grincheux en ne leur mettant pas du bon matériel à disposition.

__Version 2021 :__

Aujourd'hui toutes les barrières en termes de coûts ont disparues, le matériel est surpuissant à des tarifs tout à faire abordables, le cloud nous permet d'avoir tout le volume de stockage, la puissance de calcul et les logiciels au meilleur prix.

### 10. Avez-vous des testeurs

__Version 2000 :__

Il est dommage de payer des développeurs à $100/h alors que le travail pourrait être fait par un test à $30/h.

__Version 2021 :__

Les développeurs ont de plus en plus l'habitude d'écrire des tests unitaires et des tests fonctionnels lorsqu'ils développent des applications. Parfois même, ce sont les tests qui guident le développement quand on utilise des méthodes comme [TDD](https://fr.wikipedia.org/wiki/Test_driven_development) par exemple.

Des outils comme [PHPUnit](https://phpunit.de/), [PYUnit](https://docs.python.org/3/library/unittest.html) ou encore [Selenium](https://www.selenium.dev/) permettent d'automatiser les tests en les intégrants dans votre flux d'intégration continue.

Et s'ils vous manque des tests, des plateformes comme [Fiverr](https://www.fiverr.com) ou [Upwork](https://www.upwork.com/) vous permettent d'embaucher des testeurs à la tâches et à des prix défiants toute concurrence.

### 11. Est-ce que vos candidats écrivent du code durant les entretiens 

Est-ce que vous embaucheriez un magicien sans qu'il vous montre un tour, ou un traiteur pour votre mariage sans goûter sa nourriture. Alors pourquoi embaucher un développeur sans lui demander de faire du code ?

__Version 2021 :__

Les entretiens pour les développeurs sont devenus depuis une dizaine d'années de plus en plus techniques. Des livres sont même dédiés à ce sujet comme [Cracking the coding interview](https://www.amazon.fr/Cracking-Coding-Interview-6th-Programming/dp/0984782850) ou bien encore [Elements of Programming Interview : The Inside's Guide](https://www.amazon.com/dp/1479274836/?tag=javamysqlanta-20).

Cette pratique est maintenant entrée dans les moeurs et ne surprend plus aucun candidat.

### 12. Faites vous des tests aléatoires d'*utilisabilité*

Attraper quelqu'un dans le couloir et faites lui tester votre application. Répétez celà sur 5 personnes et vous aurez 95% de vos problèmes d'interfaces qui ressortiront.

__Version 2021 :__

Les méthodes agiles nous permettent d'itérer et la prise en charge des modifications demandées par les utilisateurs au fur et à mesure du développement est maintenant une pratique communément admise.

Des outils de maquettage comme [Adobe XD](https://www.adobe.com/fr/products/xd.html) ou [Figma](https://www.figma.com/) permettent également de montrer facilement et de autorisent les futurs utilisateurs à naviguer.

Les interfaces se sont également beaucoup uniformisées autour de documents de référence comme le [Material Design](https://material.io/design) de Google ou le [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) de Apple.

Parrallèlement les frameworks et librairies comme [Tailwindcss](https://tailwindcss.com/), [Bootstrap](https://getbootstrap.com/) oue encore [Material-UI](https://material-ui.com) permettent d'utiliser des composants génériques que les utilisateurs voient sur l'ensemble des applications qu'ils utilisent.

# Conclusion 2021

En 20 ans les technologies et méthodologies ont complétement été transformées. L'informatique des années 2000 ne ressemble plus à l'informatique d'aujourd'hui. L'hyperconnectivité, l'abandon des clients lours au bénéfice d'applications fonctionnant dans des navigateurs web et les outils que nous utilisons facilitent grandement le développement.

Néanmoins la quasi totalité des points évoqués [dans l'article original](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/) restent d'actualité.

En analysant ces points on se rend bien compte que l'industrialisation des processus de développement est bien en train de se faire. Je ne sais combien d'années il a fallut pour avoir des process précis pour la construction immobilière, la gestion de la santé ou la mise en place de banques, mais on voit bien qu'en 20 ans, de solides méthodes se sont mise en place et nous donne des solutions utilisées par des millions (voir des milliards) d'utilisateurs.

Aujourd'hui il devient quasiment impossible a un développeur sérieux de ne pas utiliser de gestion de sources, de tests ou d'outils de déploiement. Cette situation  est récente (pour moi je pense moins de 8 ans) mais ne cesse de se démocratiser grâce à l'intégration dans les cursus des écoles ou à tous les tutoriels qui nous orientent vers ce genre de pratique.

Nous avons été tout de même secoués depuis une dizaine d'années par l'arrivée ultra rapide d'un foisonnement de technologies, de Framework et de méthodes qui ont pu donnéer le tournis (voir du découragement) à pas mal de personne.

Aujourd'hui les choses semblent se calmer (relativement), les languages utilisés ont dans la majorité des cas plusieurs dizaines d'années, les Frameworks se stabilisent autour de méthodes communes et les grosses *hypes* commencent a diminuer.

On ne peut, je pense, qu'être rassuré par l'avenir. J'espère que le métier de développeur deviendra plus standardisé (pour le bien mental et familial de tous) avec des méthodes qui viseront a polir un peu le flou artistique qu'il peut parfois y avoir au sein de projets de développement.

Il restera je l'espère de la place pour le côté "hacker" du métier de développeur avec des outils tels que les Raspberry, les outils d'intelligence artificielle (vision, analyse de données ...) et bien sûr la participation à des projets Open Source.
