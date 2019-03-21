# First Demonstration

  * Date: 22.03.19
  * Examiners: Philippe Collet (PC), Laureen Ginier (LG), Guilhem Molines (GM), Anne-Marie Pinna-Déry (AMD),

## Planning

  * Constraints: 
    * 15 minutes for the team, 15 minutes from the jury;
    * No slides;
    * Live demonstration (no video)
    
  * The evaluation will take into account the fact that teams presenting in the afternoon have more time to produce and prepare their demo.

| Timeslot      | E+142   | 
|---------------|---------|
| 09:00 - 09:30 | Team A  | 
| 09:30 - 10:00 | Team B  | 
| 10:00 - 10:30 | Team C  | 

| Timeslot      | E+142   |
|---------------|---------|
| 10:45 - 11:15 | Team E  | 
| 11:15 - 11:45 | Team D  |
| 11:45 - 12:15 | Team F  |

| Timeslot      | E+142   |
|---------------|---------|
| 14:00 - 14:30 | Team G  | 
| 14:30 - 15:00 | Team H  |
| 15:00 - 15:30 | Team I  |

| Timeslot      | E+142   |
|---------------|---------|
| 15:45 - 16:15 | Team J  | 
| 16:15 - 16:45 | Team K  |

## Expectations

You have to demonstrate a single product, covering both ISA & DevOps course contents. This single demo will be evaluated according to these two dimensions, leading to two different marks. *However*, the two courses expect the project to respect the _PolyDiploma_ call for bids and implement features related to this project.

### French version as published on the slack

* Partie ISA pour le MVP nous attendons que vous dérouliez un scénario  sur la partie du coeur de l'application qui va d'un client vers un service externe minimum en passant par plusieurs composants EJBs si possible qui interagissent entre eux. Pour la partie techno vous pouvez avoir un client minimaliste qui se contente de récupérer les parametres des services et de les appeler et pour le service externe mocker un Service .net en partant du code de TCF. Si l'imlémentation .net vous pose trop de difficultés; attaquez au min le meme service externe que TCF.

* Pour le MVP partie DevOps, on aimerait voir que chaque composant est peut être construit en ne connaissant que des binaires de ceux dont il dépend, et sans les sources. Binaires récupérés depuis une repository Artifactory. On voudrait voir que si on composant ne compile/test plus, le build des autres composants en aval n’est pas affecté. On voudrait aussi que les interfaces entre les composants soient testées. Enfin on voudrait voir la structure choisie pour les sources et leurs dépendances, et que vous expliquiez vos choix. Pour cette première soutenance, il n’est pas imposé de démontrer des plans de build dans Jenkins, cependant on accordera volontiers un bonus aux groupes qui y seront parvenus.
