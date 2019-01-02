---
layout: post
title: Dépendance au Cloud
published: true
---
Des dizaines de mails d'[Amazon SES](https://aws.amazon.com/fr/ses/) depuis quelques minutes ... \"Too many connections\" ...

Oupss. Des dizaines de notifications de mon application ne partent pas ... et bouclent.

Impossible qu'[Amazon](https://aws.amazon.com/fr/) soit en panne, je mets donc immédiatement en cause mon code. Quelque chose doit clocher. PostgreSQL semble OK. Le code tourne depuis des mois, pourquoi il se mettrait à ne plus fonctionner. Je commente, je **error_log()**, je check les fichiers de logs ...

Une bonne dizaines de minutes passent, les mails continuent d'affluer, j'arrête le service de notification par mail.

Je me connecte à la [surveillance des services Amazon](https://status.aws.amazon.com/) et là ... **41** services en erreur. Amazon en panne ?!!!

Un petit 'googlage' sur **Amazon outage** et là déjà plusieurs dizaines d'articles disant qu'un pan entier de l'Internet estt en panne suite aux anomalies chez Amazon (ex : [Engadget](https://www.engadget.com/2017/02/28/amazon-aws-outage/)).

Bon pour la nuit j'utiliserai un autre service SMTP pour envoyer mes notifications...

Le problème me tracasse tout de même. Je compte de plus en plus sur Amazon, de la [gestion du DNS](https://aws.amazon.com/fr/route53/), au [stockage des backups](https://aws.amazon.com/fr/s3/), en passant par les [serveurs hébergeant mes applications](https://aws.amazon.com/fr/ec2/).

La panne de cette nuit n'a pas eu un impact énorme sur mes quelques centaines d'utilisateurs mais m'**a montré à quel point je suis dépendant d'Amazon**.

Amazon fonctionne bien c'est sur! Mais si un changement brutal intervient ? Blocage en Europe, nouvelle tarification, ou ne sais je quoi d'autre ? Combien de temps me faudrait-il pour migrer vers autre chose ?

Je vais essayer de passer un peu de temps ces prochaines semaines à préparer des alternatives ...

* Des machines dédiées chez un hébergeur comme [OVH](https://www.ovh.com/fr/serveurs_dedies/) 

* Un mix d'opérateurs cloud comme [Microsoft Azure](https://azure.microsoft.com/fr-fr/), [Google Cloud](https://cloud.google.com/)

* Des machines en propre hébergées dans mes locaux

* Une combinaison de tout ceci dans un environnement de [containers](https://www.docker.com/) orchestrés avec [Kubernetes](https://kubernetes.io/) par exemple.

	
