# FAQ ISA -DevOps (2020-21)

aka ISA-DevOPS stacko

French only

## ISA

### Mon équipe n'a pas eu de feedback sur l'aspect X de notre rapport?
On a focalisé le feedback sur les points les plus importants à améliorer pour chaque équipe. Si on n'a pas évoqué un point, c'est que plus de 80% de ce qui est fait est correct. Vous pouvez avancer (et on est toujours la pour répondre à des questions précises)


### Pensez-vous que modéliser des acteurs secondaires pour gérer le paiement/l'envoie de mails ou de notifications etc. est cohérent dans un diagramme de UC ?
En reprenant la définition d'un acteur dans le manuel référence UML : `An actor may be a human, another computer system, or some executable process`. S'il vous semble qu'ils jouent un rôle dans votre système et que modéliser ces acteurs facilite la lecture / compréhension, vous pouvez les ajouter ! 

### On a du mal à bien comprendre quelle est la différence entre classes et composants ?
Dans votre diagramme de classes, vos objets représentent des entités métier. Il s'agit de votre modèle de données métier, ex : customer, cart, etc. qui vous permet également de lier les objets aux informations qui leur sont associées, ex : identifiant, date, nom, mot de passe, etc. 
En revanche, vos composants sont des briques logicielles qui contiennent de la logique métier nécessaire afin de faire tourner votre système en fonction des contraintes que le sujet vous impose, ex : vérifier un paiement, envoyer des notifications de manière périodique, calculer un montant, etc. Ces composants vont donc réaliser un ensemble d'opérations en manipulant vos objets métier.

### Est-il nécessaire de développer une webapp (avec JSP, JSF... etc) pour le serveur ? En effet, nous avions dans l'idée que nos utilisateurs utilisaient seulement un client en CLI qui contactait le serveur au travers de web services. Est-il également possible d'utiliser Postman ?
La CLI (ex : TCF) est suffisante, l'important ici étant de montrer qu'elle appelle le Web service qui déclenche toutes les interactions entre les composants
Et vous pouvez commencer par du postman/newman/curl pour vous concentrer sur l'architecture. L'idée est de pouvoir avoir au moins une CLI qui facilite une démo intéressante, pour le MVP et pour le produit final. Le reste peut être du postman/newman/curl. 
Réfléchissez où il est intéressant d'avoir une CLI élaborée pour des interactions front (des données qui s'affichent, etc.), et peut être pour d'autres interactions front, un script curl/newman peut suffire à juste montrer l'enclenchement d'un scénario qui va ensuite se démontrer par : des logs au fur et à mesure du passage dans les session Beans, des logs sur les services externes en .NET ou des retours vers la CLI principale.

### Comment doit-on traiter les id des objets, est-ce mieux de les faire en String ou en Int en général ?
Les identifiants des objets sont là pour pouvoir les distinguer de manière unique, un mélange de lettres et chiffres est généralement conseillé pour ne pas se restreindre et garder des ids de taille raisonnable via des String. En général une façon simple de procéder est de générer des UUID. 
 Pour ce projet, n'ayant pas de contraintes particulières, vous pouvez également utiliser des Int/Long pour vos ids si cela vous convient mieux. L'essentiel est de garantir l'unicité de vos objets le plus facilement possible. Pensez simple afin de ne pas compliquer la manipulation et les vérifications liées à ces ids.


## DevOps

### Nous avons du mal à lancer plusieurs modules J2E sur TomEE :quand on lance un module sur TomEE, il n'est pas possible d'en lancer un deuxième sur la même adresse apparemment. Serait-il possible de compiler/lancer plusieurs modules J2E ensemble sur TomEE mais également indépendamment ? S'agit-il d'une configuration de Tomee Maven Plugin ?
Comme c'est un peu expliqué dans https://github.com/collet/4A_ISA_TheCookieFactory/blob/develop/chapters/Architecture.md le setup de TCF est simplifié en utilisant une version embarqué (embedded) de Tomee. C'est pratique pour exécuter des tests par exemple, mais ce n'est pas le bon setup pour laisser le serveur up et déployer/re-déployer. 
Avec un tomee:run, le plugin maven a récupéré un tomee complet, lance le serveur à la volée en lui passant en argument un package deployable (e.g., war, ear... ), et un seul. C'est un raccourci. Si vous avez plusieurs War, vous êtes coincés avec ce setup.
Vous pouvez soit :

- regarder comment faire un EAR (une archive faite pour en assembler plusieurs) à partir de vos modules et faire le tomee:run avec cet EAR : on prépare une seule application qui contient plusieurs web services et le raccourci fonctionne.
- ou installer un tomee "lourd" séparé (il a des scripts pour démarrer, se stopper...), et faire des deploy sur ce serveur, soit par des commandes tomee:deploy ou simplement en copiant les war dans le bon répertoire (que tomee surveille continuellement et charge automatiquement tout nouveau module).

Dans les deux cas, on peut préparer le tout par un plan de build dédié !

## Développement

### Où est le setup IntelliJ pour Arquilian ?
Il est la : [https://github.com/collet/4A_ISA_TheCookieFactory/tree/develop/ides/intelliJ](https://github.com/collet/4A_ISA_TheCookieFactory/tree/develop/ides/intelliJ)

### Je n'arrive à lancer les tests arquillians sur Intellij?

 - La première chose à vérifier dans la trace : les tests sont-ils bien exécutés avec Java 8 ?

#### Erreur liée à la version de tomee :

```
SEVERE: Unable to deploy collapsed ear in war StandardEngine[Tomcat].StandardHost[localhost].StandardContext[/7605c1c7-e3eb-486d-b585-8352ad982b10]
org.apache.xbean.recipe.ConstructionException: Error calling instance factory method: public org.apache.openejb.core.mdb.BaseMdbContainer org.apache.openejb.core.mdb.MdbContainerFactory.create()
```

La version de tomee embedded n'est certainement pas la bonne, se réferer au setup intellij et à la manière de forcer la version `7.0.2`.

#### Erreur liée à l'agent EJB

```
org.apache.openejb.OpenEJBRuntimeException: javax.transaction.NotSupportedException: Nested Transactions are not supported
```

Cette erreur est liée à une mauvaise configuration de l'agent openejb. Se référer au setup intellij en faisant attention au path utilisé selon si c'est le projet `j2e` qui est ouvert ou la racine `4A_ISA_TheCookieFactory`.

#### Erreur uniquement du job integrationBetweenCustomersAndOrders :

```
WARNING: Interceptor for {http://localhost:9090}WebClient has thrown exception, unwinding now
org.apache.cxf.interceptor.Fault: Could not send Message.
```

Ce test nécessite de pouvoir accèder à la banque, il faut donc la démarrer avant de lancer les tests.

### Je suis sur Windows et lors de l'exécution des tests arquillian, le test "performInternalCucumberOperations" est échoue avec un message du type "Malformed \uxxx encoding" ou "C:\Users\XXXX\XXXX\4A_ISA_TheCookieFactory\j2e\YYYY	argetcucumber-report"

Il s'agit d'une erreur lors de la génération du rapport des tests cucumber. Ces tests sont déployés et exécutés dans un serveur d'application (tomee) au moyen d'`Arquillian` et de `Cukespace`. Ce dernier présente un bug quelque soit la version que vous utilisez depuis maven central. Un contributeur a proposé un correctif qui n'a pas été mergé (et donc pas release sur maven central).

Pour corriger le problème, il faut récupérer la version du contributeur, builder en local le core (les tests des exemples sont en erreur), installer `cukespace-core 1.6.8-SNAPSHOT` dans votre repository maven local et changer la version dans le pom.xml du projet `j2e`.

```
$ git clone https://github.com/misterul/cukespace.git 
$ cd cukespace
$ mvn install -pl core  -am
```

Dans le pom.xml de j2e il faut remplacer : `<versions.cukespace>1.6.5</versions.cukespace>` par la version maintenant disponible dans votre repository maven : `<versions.cukespace>1.6.8-SNAPSHOT</versions.cukespace>`

### Le choix des technos est-il imposé concernant les modules externes ? 
oui (aka .Net pour la banque)

### Peut-il être le même pour tous les modules externes (différents modules mais la même technologie) ?
oui

### Est-il fortement recommandé d'utiliser les mêmes technos que CookieFactory ?
oui, c’est même pour ça qu’on l’a écrit !

## Méthode

### Est-ce une bonne idée de se spécialiser dans l'équipe sur ISA / sur DevOps?
NON. S'il est raisonnable que certains fassent un setup d'exploration de telle ou telle partie, il est TRES important que toute l'équipe maitrise l'ensemble. Toutes les équipes avec des membres ultra-spécialisés se sont plantées les années précédentes.

### Comment démarre-t-on le développement de notre MVP ? 
   - Il est important d’y aller incrémentalement. Faire un module qui contient une classe toute bête, sans main, sans web service, sans persistence, sans gadget, avec juste une méthode qui affiche un message. Et à côté, un test qui l’invoque. Juste ça déjà c’est pas mal, ça permet de poser les répertoires au bon endroit, d’écrire un pom, de voir que ça marche sur les machines de tout le monde.
   - Puis pareil pour un deuxième, qui dépend du premier
   - En essayant si possible d’écrire les poms à la main plutôt que d’utiliser les wizard d’IntelliJ qui vous génèrent plein de trucs pas toujours simples à comprendre et souvent inutiles.

### Au niveau du backlog, doit-on reproduire le même schema qu'en PS7 ? C'est à dire jusqu'au Poker Sizing ?
Ce n'est pas obligatoire et cela ne sera pas évalué. Faites ce qui est au bon niveau de granularité pour piloter le développement progressif des fonctionnalités et la répartition des tâches dans l'équipe.
En revanche, comme vous allez automatiser dans la chaine DevOps l'ensemble des tests (TU, TI, TF), il peut être intéressant de bien piloter l'avancement par des tests et une démo fonctionnelle.
