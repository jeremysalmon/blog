---
layout: post
title: Pourquoi développer en Go
published: false
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

Go permet à un appel de fonction de s'exécuter en concurrence avec le thread courant. 

### Go est facile à lire ... facile à maintenir

La communauté Go travaille sur le même Guideline et le code des projets Go est donc formaté de la même façon. Et pour les récalcitrants [go-fmt](https://blog.golang.org/go-fmt-your-code) les remet sur le bon chemin ;)

Le language ne contient qu'une trentaine de mots clés, et la librairie standard pouvant être utilisée pour faire des projets "standards" (style API REST), on se retrouve donc sur du code sans avoir à comprendre les obscurs appels à des librairies externes.

### Go est performant



Si vous avez envie d'aller plus loin dans l'analyse du "pourquoi Go est performant je vous invite à lire l'excellente présentation de [Dave Cheney](https://dave.cheney.net/2014/06/07/five-things-that-make-go-fast).

### Go nous rapproche des racines :) tout en étant moderne


## Quand utiliser Go ?

### Pour vos API

### Pour vos outils

### Pour le Machine Learning

### Pour se faire plaisir !!!


## Par ou commencer ?

