---
layout: post
title: Pourquoi développer en Go
published: true
---

Quand il s'agit de choisir le language de développement d'un projet on peut facilement arriver à des guerres de clochers oû chacun campe sur ses propres convictions.

C pour être au plus près du métal, JAVA parce que c'est le language du monde professionnel (... !!!), PHP parce qu'il faut vite livrer une maquette ...

Depuis maintenant deux ans je m'intéresse de près à [GO](https://golang.org/) et je suis majoritairement content quand je développe dans ce language.

Vous avez peut-être vu dans mon [résumé des lectures 2017-2018](https://www.jsalmon.net/recap-lecture-web-2017-2018/) que ca a été un de mes principal pôle d'intérêt ces derniers mois.

## Go ?

Go nous vient de nos chers amis de chez Google, c'est un language qui s'inspire du C (non ne paniquez pas :) ). Go est écrit en ... Go depuis sa version 1.5. Il ne sort pas du cerveau d'illustres inconnus mais d'une équipe composée de [Rob Pike](https://fr.wikipedia.org/wiki/Rob_Pike) (UTF-8, Unix 8 aux Laboratoires Bell, Co-auteur avec Kernighan de The Practice of Programming, ...), [Ken Thompson](https://fr.wikipedia.org/wiki/Ken_Thompson) (Language B, début des travaux sur Unix, Prix Turing 1983, ...) et Robert Grisemer (Google V8, Java HotSpot).

Sur la page Wikipedia de Go on peut trouver une phrase qui résume bien toute la philosophie de ce language : "*Go veut faciliter et accélérer la programmation à grande échelle : en raison de sa simplicité il est donc concevable de l'utiliser aussi bien pour écrire des applications, des scripts ou de grands systèmes. Cette simplicité est nécessaire aussi pour assurer la maintenance et l'évolution des programmes sur plusieurs générations de développeurs.*"

## Pourquoi choisir Go ?

### Go est "cross-compilable" 

A partir de macOS vous pouvez compiler un .exe pour Windows, de Windows vous pouvez compiler un executable Linux ...

Un ```GOOS=windows GOARCH=386 go build test.go``` sous macOS compilera un .exe que vous pourrez executer sous Windows.

On est donc proche de la promesse de la portabilité du C ... mais sans avoir à mettre en place une "toolchain" complexe pour compiler.

### Go Compile Statiquement

Go compile statiquement ses executables, c'est à dire qu'il ne nécessite aucun runtime (comme par exemple la JVM de Java ou le Framework .Net). Ceci vous permet de facilement distribuer vos applications sans trop vous soucier du système hôte.

### Go est "Cloud Native"

Avec la librairie standard de Go (sans aucune librairie externe donc ... une pensée aux adorateurs de NPM install) vous pouvez développer des programmes pour le cloud (gérant nativement HTTP et autres joyeuseté ...).

La majorité des provider de Cloud ([Google Cloud Platform](https://cloud.google.com/go/home), [Azure](https://docs.microsoft.com/en-us/go/azure/), [Amazon Web Service](https://aws.amazon.com/fr/sdk-for-go/), [Rackspace](https://developer.rackspace.com/sdks/golang/), [Heroku](https://devcenter.heroku.com/articles/getting-started-with-go)) gère nativement Go.

### Go gère la concurrence

Go permet à un appel de fonction de s'exécuter en concurrence avec le thread courant grâce aux goroutines. Les goroutines fournissent une abstraction sur les threads et le langage (et son contexte d'exécution) tire parti de la topologie de l'ordinateur qui exécute le programme pour choisir la stratégie de simultanéïté idéale. Donc une goroutine ne consommera pas
spécialement un nouveau thread.

### Go est facile à lire ... facile à maintenir

La communauté Go travaille sur le même Guideline et le code des projets Go est donc formaté de la même façon. Et pour les récalcitrants [go-fmt](https://blog.golang.org/go-fmt-your-code) les remet sur le bon chemin ;)

Le language ne contient qu'une trentaine de mots clés, et la librairie standard pouvant être utilisée pour faire des projets "standards" (style API REST), on se retrouve donc sur du code sans avoir à comprendre les obscurs appels à des librairies externes.

### Go est performant

Si vous avez envie de savoir pourquoi, je vous invite à lire l'excellente présentation de [Dave Cheney](https://dave.cheney.net/2014/06/07/five-things-that-make-go-fast).

## Quand utiliser Go ?

### Pour vos API

Comme nous l'avons déjà vu, Go se veut le language "Cloud Native". Sa librairie standard inclut tout ce qu'il faut pour écrire serveur Web, routeur et toutes les joyeusetés qui permettent de mettre en place une API.

### Pour vos outils

Vous écrivez un code, vous utilisez des fonctions portables et vous compilez pour n'importe quelle plateforme. Alors suivez l'exemple de Docker, Kubernetes et autres choses du genre pour écrire vos propres outils.

### Pour le Machine Learning

Go est performant, go est lisible, go gère la concurrence ... un outils idéal pour le machine learning donc. Généralement on entends Python comme référence dans le domaine. Mais le petit poucet Go avance vite :) ([Si vous avez des doutes, c'est par ici](https://medium.com/sourcedtech/machine-learning-on-go-code-829e85e2d2c6)).

### Pour se faire plaisir !!!

Sa simplicité d'écriture, ses outils facilitant la mise en forme et le fait que Go compile rapidement font qu'il est vraiment très agréable de travailler avec ce language.

Et en plus on se rapproche du métal (c'est vraiment autre chose que ce #&#--$# de Node) :).

## Par ou commencer ?

Pas la peine de chercher 12h à 14h. Le site [tour.golang.org](https://tour.golang.org/) vous donnera vos premières armes pour commencer à apprécier le language.

Concernant les livres pour vraiment faire un tour complet je recommande ["The Go Programming Language"](https://www.amazon.com/dp/0134190440/) de Donovan et Kernighan.

Pour avancer rapidement dans la création d'API et/ou de Microservices, [Building RESTful Web services with Go: Learn how to build powerful RESTful APIs with Golang that scale gracefully](https://www.amazon.com/Building-RESTful-Web-services-gracefully-ebook/dp/B072QB8KL1/ref=sr_1_fkmr0_1?keywords=builing+restful+webservice+with+go&qid=1553266992&s=books&sr=1-1-fkmr0)

Amusez-vous bien !
