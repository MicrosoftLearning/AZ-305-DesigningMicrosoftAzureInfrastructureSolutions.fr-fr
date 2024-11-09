---
casestudy:
  title: Fabrikam Residences
  module: Logging and monitoring solutions
---
# Étude de cas : Fabrikam Residences

## Spécifications

**Avant de commencer cette étude de cas, assurez-vous d’avoir terminé les modules et les études de cas suivants : calcul, données relationnelles, données non relationnelles, authentification, architecture d’application**

Un nouveau poste vous a été confié chez Fabrikam Residences, une entreprise prospère qui connaît une croissance fulgurante. Fabrikam Residences est une entreprise du bâtiment qui construit de nouvelles maisons et rénove des maisons existantes. Elle doit son succès à la qualité de ses constructions et à aux technologies domestiques intégrées plus récentes que celles de ses concurrents.  

Actuellement, ces technologies sont fournies et gérées par des sous-traitants distincts. Les propriétaires de Fabrikam Residences souhaitent proposer ces options technologiques améliorées en interne pour fournir une meilleure qualité, un support et des données sur les modèles et les besoins des clients. 
 
Initialement, l’entreprise souhaite proposer le contrôle et la surveillance du chauffage et de la climatisation (HVAC), la surveillance et les alertes du système de sécurité, ainsi que la domotique. Cela nécessite un nouveau site web, ainsi qu’une solution de stockage et d’ingestion de données.

L’entreprise a connu une croissance exceptionnelle au cours des 2 dernières années. L’entreprise estime qu’elle peut doubler de taille au cours des 12 à 18 prochains mois. Forte de cette croissance rapide sur le marché régional, l’entreprise n’envisage pas actuellement de conquérir d’autres marchés.

## Situation actuelle

Le siège de Fabrikam exploite un petit centre de données dans un emplacement unique. Le centre de données héberge le **logiciel de gestion de projets (PM)** de l’entreprise.

![Architecture logicielle de gestion de projets](media/fabrikam.png)

- Le logiciel PM utilise une application Windows tierce. L’application s’exécute sur un cluster d’équilibrage de charge réseau à 2 nœuds avec un seul serveur principal Microsoft SQL Server.  

- Les images et les documents sont stockés sur un lecteur mappé du serveur, qui est hébergé sur une appliance NAS dédiée.

- Les utilisateurs d’entreprise et le personnel de bureau utilisent un front-end web pour entrer des données telles que les planifications de livraison et les ordres de modification.

-   Les superviseurs sur le terrain utilisent des ordinateurs portables Windows et des tablettes hors ligne pour enregistrer en permanence la progression de la construction et d’autres détails.  Ces modifications, telles que les nouveaux ordres de travail, sont stockées dans un fichier de modification local.  À la fin de chaque journée, les superviseurs reviennent au bureau pour se connecter au réseau sans fil et exécuter un petit script afin de charger le fichier de modification sur un serveur FTP.  Un deuxième script s’exécute ensuite chaque nuit pour traiter les fichiers de modification et introduire leur contenu dans la base de données de gestion de projets (Microsoft SQL Server).

Le **logiciel Home Technology** est actuellement fourni et hébergé par des tiers. Pour l’obtenir, le client doit visiter la bagatelle de trois sites web différents.  Fabrikam Residences souhaite remplacer le logiciel par une solution unifiée et développée en interne.

![Diagramme de l’application HVAC, de sécurité et d’automatisation](media/software.png)

## Spécifications 

**Logiciel de gestion de projets**

- Migrez autant de systèmes vers un fournisseur de cloud public que possible.

- Remplacez les scripts existants pour tirer parti d’un système plus sécurisé que le FTP, afin de répondre aux exigences de sécurité actuelles. En outre, il vous a été demandé de vous assurer que les fichiers de modification sont traités dès leur chargement.

- Augmentez la résilience de la base de données de gestion de projets. Bien que les performances ne constituent pas un problème, l’entreprise souhaite éviter de perdre l’accès à la base de données en cas de défaillance matérielle unique.

**Nouvelle solution de technologie domestique**

- Ajoutez une nouvelle solution pour collecter des données en continu à partir des capteurs de surveillance domestique.
  - Base de données des relevés de capteurs pour l’analyse des tendances et la génération de rapports.
  - Fournissez des alertes en temps réel configurables en fonction des besoins du propriétaire.
  
- Concevez une solution de base de données relationnelle contenant les préférences et les paramètres des propriétaires.
  - Le système doit être évolutif.
  - La redondance est essentielle.
  
- Le nouveau site web unifié sera développé en interne et hébergé sur Linux.  Ce site web sera utilisé pour afficher les moniteurs et modifier les préférences d’éléments tels que la température ou les seuils d’alerte. Les charges peuvent varier considérablement et le système doit être en mesure d’y répondre rapidement.

-   Fournissez aux utilisateurs un moyen de se connecter au système sans créer de compte d’utilisateur ou de mot de passe.

- Implémentez des contrôles de sécurité et fournissez des rapports hebdomadaires démontrant la conformité de l’entreprise avec les bonnes pratiques du secteur.

## Tâches 

1. Concevez une solution pour le logiciel de gestion de projets. Préparez-vous à expliquer pourquoi vous avez choisi chaque composant de la conception et comment il répond aux exigences de la solution.

2. Concevez une architecture pour la nouvelle solution de technologie domestique. Préparez-vous à expliquer pourquoi vous avez choisi chaque composant de la conception et comment il répond aux exigences de la solution.

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?

