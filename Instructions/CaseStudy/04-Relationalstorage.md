---
casestudy:
  title: Conception d’une solution de stockage relationnel
  module: Relational storage solutions
---
# Conception d’une étude de cas de stockage relationnel

## Spécifications

Tailwind Traders cherche à migrer sa base de données de site web public existante sur Azure, à l’instar du front-end du site web.  Initialement, le front-end du site web ne sera déployé que dans 2 régions à des fins de redondance.  Il est toutefois prévu qu’à mesure que le trafic augmente, le site web soit répliqué dans d’autres régions du monde entier. La base de données à migrer contient le catalogue de produits et toutes les commandes en ligne.  Actuellement, la base de données s’exécute sur un seul groupe de disponibilité Always On Microsoft SQL Server local.

![Architecture de stockage non relationnel](media/relational%20storage.png)

Principales préoccupations de Tailwind Traders :

-   **Haute disponibilité**.  Une préoccupation principale pour Tailwind Traders est que cette base de données soit hautement disponible, car elle est essentielle pour leur activité.  Les pannes peuvent entraîner un recul des ventes ou une perte de confiance des clients.

-   **Performances du site web.**  Bien que l’expérience d’achat soit satisfaisante, la navigation ou la recherche de pages contenant de nombreux articles est  « lente ».

-   **Sécurité**.  Tailwind Traders attache une grande importance aux informations personnelles ou financières stockées dans la base de données publique.  En plus d’implémenter des mesures de sécurité appropriées, l’équipe de sécurité doit vérifier que les bonnes pratiques du secteur sont appliquées dans la mesure du possible.


## Tâches

1.  Concevez la solution de base de données. Votre conception doit inclure l’autorisation, l’authentification, la tarification, les performances et la haute disponibilité. 
2.  Étayez vos choix et décrivez votre solution. 

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?
