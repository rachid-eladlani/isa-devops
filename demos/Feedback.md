# Feedback demo finale

# Group A

## ISA

Très bonne présentation, bien préparée. Bonnes réponses aux questions.

## DevOps

Bonne démo, bien rattrapée malgré le plantage. Pas de plan de tests d'intégration, mais vous avez su dire comment vous auriez fait aux questions. Bonne maitrise de Docker et Compose

# Group B

## ISA

Présentation complète, je n'ai pas eu besoin d'aller chercher les réponses. Ceci dit, il y a eu moins d'investissements sur la partie ISA comparé au dernier rendu (complétion des fonctionnalités - déjà très avancées au dernier rendu - mais MOM/intercepteur et persistence peu poussés). La présentation faisait un peu moins préparée que d'autres groupes : des hésitations/flottements, la présentation du diagramme aurait été mieux au début. Mais ça reste très bon !

## DevOps

RIen à dire côté DevOps, vous êtes allés au bout de l'attendu, et même couvert un bonus difficile avec Kubernetes déployé sur Google Cloud, c'est parfait

# Group C

## ISA

Très bonne présentation ISA compléte qui montre une maitrise du traval accompli

## DevOps
Rien à dire, vous avez fait tout ce qui était attendu en allant chercher à chaque fois à comprendre en profondeur, et vous avez su démontrer votre maitrise du sujet. Vous avez aussi réalisé plusieurs bonus qui vous augmente une note déjà bonne, bien joué !

# Group D

## ISA

Malgré la prise en compte de la constitution de l'équipe, le travail fournit n'est pas assez aboutit et les justifications peu probantes

## DevOps
Une partie DevOps sans démonstration, ni même une visualisation d'un dashboard Jenkins. Juste deux minutes de discussion sur ce qui a été fait. Quand on creuse, on se rend compte que le Jenkins est cassé, par un docker push qui échoue, il y a un seul TI qui vérifie l'invitation avec inscription, mais tout est dépend de services externes lancés séparément et qui ne sont pas les mêmes que ceux qui sont dockerisés et lancer dans le compose. C'est vraiment un état très incohérent pour une chaine DevOps. Rien ne semble perdu, mais vous devez vraiment corriger tous ces défauts pour revenir à un état stable, faire des tests d'intégration propres et un compose bien paramétré dans Docker.

# Group E

## ISA
C'est vraiment dommage d'avoir fait une démonstration client en ISA. On a vu l'architecture independament des fonctionnalités implémentées. Vous n'êtes pas assez à l'aise dans les justifications. Vous manquez d'assurance à l'oral en esperant que ce ne soit qu'un problème de forme.

## DevOps
Côté DevOps, vous avez fait le minimum, sauf sur la partie Test d'Intégration qui pêche un peu, ça marche un peu par hasard, on n'a pas de TI depuis Jenkins, ni de déploiement. Pas de Volume non plus dans le Compose, on perd donc la persistence entre deux exécutions.

# Group F

## ISA
Bonnes explications et illustrations lors de la démo, avec schéma d'architecture, dommage qu'il n'y ait pas de log serveur visible (sauf pour le mail)

## DevOps
La démo DevOps a été trop rapide et n'a pas pu montré l'étendue de ce qui a été fait sur la chaine d'intégration. Il manque de vrais tests d'intégration, une démonstration de ce qui se passe quand on casse le build. Coté Docker, cela a progressé, il faut finaliser la configuration du compose.

# Group G

## ISA
Très bonne démo d'archi

## DevOps
Trop de temps passé sur la démo ISA. En 2 minutes, vous avez montré vos dépendances de build, la cascade de build, mais c'est dommage de faire si peu de démonstration. Un travail raisonnable a été fait sur chaque aspect, mais tout est améliorable : il y a des test d'intégration, mais il faudrait les automatiser avec docker. Pour le docker compose, il faudrait aller au dela du simple lancement en parallèle de tous les exécutables.

# Group H

## ISA
Bonne présentation, mais problème de lisibilité sur les petits écrans + difficulté à suivre le déroulé (une prénsetation de l'archi globale au début aurait pu aider). Manque de réflexion sur la partie MOM et intercepteur (logging mis en place par "manque de temps").

## DevOps
L'organisation de la démo est intéressante, en lancant des jobs Jenkins au début pour voir le résultat vers la fin, mais ça aurait été mieux avec un build en partie cassé, avec un scénario qui montre plus de choses. Il y a un travail raisonnable côté tests d'intégration et docker mais tout est améliorable : les TI pourraient se lancer séparément dans jenkins, le docker compose pourrait être plus qu'un simple lancement en parallèle des 2 services externes et du serveur j2e.

# Group I

## ISA
Bonne présentation, démo bien scénarisée et bonnes justifications.

## DevOps
Peu de temps passé sur la partie DevOps, et pas de vraie démo de la chaine, ni de scénario associé, c'est dommage. Il y a bien des éléments attendus avec un TF cucumber, une dockerisation et un compose pour lancer le tout. En revanche, c'est faible sur les tests d'intégration, il faut en faire quelques uns et les automatiser. Coté compose, il faudrait aller au dela du simple lancement en parallèle des éléments.

# Group J

## ISA
Bon travail dans l'ensemble mais... Votre démonstration n'a pas bien montré les composants impactés par les fonctionnalités choisies, vous avez plus raconté que démontré. Il a fallu aller chercher les informations BD aux questions. Votre couverture fonctionnelle n'a pas été assez bien défendue. Le choix de l'intercepteur n'a pas non plus été  bien argumenté. 

## DevOps
Bonne utilisation de Jenkins, ainsi que de la registry de docker hub, avec une bonne gestion des tests d'intégration. Manque de recul sur Compose. Scénario DevOps expliqué avec les mains et peu démonstratifs, on aurait bien voulu voir casser des tests

# Group K

## ISA
Bel achèvement compte tenu du parcours, bonne couverture fonctionnelle. Manque de recul ou de justifications sur ce qui a été fait. Les réponses aux questions n'ont pas toujours convaincu.

## DevOps
La démo manque de clarté. C'est bien d'avoir insisté sur les tests, par contre il n'y a que du fonctionnel, pas de tests d'intégration. Côté Docker et Compose, bonne maitrise.


