# FAQ ISA -DevOps (2020-21)

aka ISA-DevOPS stacko

French only

## ISA

- **Mon équipe n'a pas eu de feedback sur l'aspect X de notre rapport?** On a focalisé le feedback sur les points les plus importants à améliorer pour chaque équipe. Si on n'a pas évoqué un point, c'est que plus de 80% de ce qui est fait est correct. Vous pouvez avancer (et on est toujours la pour répondre à des questions précises)

## DevOps



## Développement

- **Ou est le setup IntelliJ pour Arquilian ?** Il est la : [https://github.com/collet/4A_ISA_TheCookieFactory/tree/develop/ides/intelliJ](https://github.com/collet/4A_ISA_TheCookieFactory/tree/develop/ides/intelliJ)

- **Le setup IntelliJ n'a pas l'air de marcher sous Windows (erreur TODO) ?** TODO

- **Le choix des technos est-il imposé concernant les modules externes ?** oui (aka .Net pour la banque)

- **Peut-il être le même pour tous les modules externes (différents modules mais la même technologie) ?** oui

- **Est-il fortement recommandé d'utiliser les mêmes technos que CookieFactory ?** oui, c’est même pour ça qu’on l’a écrit !

## Méthode

- **Est-ce une bonne idée de se spécialiser dans l'équipe sur ISA / sur DevOps?** NON. S'il est raisonnable que certains fassent un setup d'exploration de telle ou telle partie, il est TRES important que toute l'équipe maitrise l'ensemble. Toutes les équipes avec des membres ultra-spécialisés se sont plantées les années précédentes.

- **Comment démarre-t-on le développement de notre MVP**? 
   - Il est important d’y aller incrémentalement. Faire un module qui contient une classe toute bête, sans main, sans web service, sans persistence, sans gadget, avec juste une méthode qui affiche un message. Et à côté, un test qui l’invoque. Juste ça déjà c’est pas mal, ça permet de poser les répertoires au bon endroit, d’écrire un pom, de voir que ça marche sur les machines de tout le monde.
   - Puis pareil pour un deuxième, qui dépend du premier
   - En essayant si possible d’écrire les poms à la main plutôt que d’utiliser les wizard d’IntelliJ qui vous génèrent plein de trucs pas toujours simples à comprendre et souvent inutiles.

- **Au niveau du backlog, doit-on reproduire le même schema qu'en PS7 ? C'est à dire jusqu'au Poker Sizing ?** Ce n'est pas obligatoire et cela ne sera pas évalué. Faites ce qui est au bon niveau de granularité pour piloter le développement progressif des fonctionnalités et la répartition des tâches dans l'équipe.
En revanche, comme vous allez automatiser dans la chaine DevOps l'ensemble des tests (TU, TI, TF), il peut être intéressant de bien piloter l'avancement par des tests et une démo fonctionnelle.