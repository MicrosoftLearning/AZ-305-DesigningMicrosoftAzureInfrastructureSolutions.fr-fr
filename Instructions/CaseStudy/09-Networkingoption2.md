---
casestudy:
  title: Conception d’une solution réseau -Application d’entreprise BI
  module: Network infrastructure solutions
---
# Conception d’une solution d’infrastructure réseau  

## Spécifications

À mesure que l’équipe informatique de l’entreprise Tailwind Traders se prépare à définir la stratégie de migration des charges de travail de l’entreprise vers Azure, elle doit identifier les composants réseau requis et concevoir une infrastructure réseau nécessaire pour les prendre en charge. Compte tenu de l’étendue globale de ses opérations, Tailwind Traders utilisera plusieurs régions Azure pour héberger ses applications. La plupart de ces applications ont des dépendances vis-à-vis des services d’infrastructure et de données, qui résideront également dans Azure. Les applications internes migrées vers Azure doivent rester accessibles aux utilisateurs de Tailwind Traders. Les applications accessibles sur Internet migrées vers Azure doivent rester accessibles à n’importe quel client externe. 

Pour mettre en place la conception réseau initiale, l’équipe informatique de l’entreprise Tailwind Traders a choisi deux applications clés, qui sont représentatives des catégories les plus courantes de charges de travail qui sont censées être migrées vers Azure.  

## Conception - Application d’entreprise BI 

![Architecture d’application d’entreprise BI](media/compute.png)

-   Une application d’entreprise BI (Business Intelligence) interne basée sur Windows et à trois couches avec la couche front-end exécutant des serveurs web IIS, la couche intermédiaire hébergeant a logique métier basée sur .NET Framework et la couche principale implémentée en tant que base de données du groupe de disponibilité Always On SQL Server. 

-   Cette application est classée comme stratégique et nécessite des dispositions de haute disponibilité avec le contrat SLA de disponibilité de 99,99 % et des dispositions de récupération d’urgence, avec un RPO de 10 minutes et un RTO de 2 heures.

-   Pour fournir une connectivité aux applications internes migrées vers Azure, Tailwind Traders devra établir une connectivité hybride à partir de leurs centres de données locaux. Le groupe informatique d’entreprise a déjà établi que cette connectivité sera implémentée à l’aide du circuit ExpressRoute à partir de son centre de données principal de Seattle. Toutefois, à ce stade, la solution de basculement en cas d’indisponibilité du circuit n’est pas encore claire. Le directeur financier de Tailwind Traders souhaite éviter de payer pour un autre circuit ExpressRoute redondant. 

- Des considérations supplémentaires s’appliquent à la connectivité locale aux applications internes migrées vers Azure. Étant donné que l’environnement Azure de Tailwind Traders se compose de plusieurs abonnements et, effectivement, de plusieurs réseaux virtuels, pour réduire le coût, il est important de réduire le nombre de ressources Azure requises pour implémenter les fonctionnalités de mise en réseau principales. Ces fonctionnalités incluent la connectivité hybride aux emplacements locaux ainsi que le filtrage du trafic. En outre, cette nécessité de réduire les coûts s’aligne sur les exigences en matière de sécurité et de risque des informations, qui indiquent que tout le trafic entre les emplacements locaux et les réseaux virtuels Azure doit circuler via un seul réseau virtuel, qui hébergera des composants responsables de la connectivité hybride et du filtrage du trafic. 

-   Conformément aux exigences définies par les équipes en charge de la sécurité et du risque des informations de Tailwind Traders, toutes les communications entre les machines virtuelles Azure de différentes couches qui font partie de la même application doivent autoriser uniquement les ports nécessaires à l’exécution et à la maintenance de l’application. Toutefois, en raison des limitations de l’espace d’adressage IP, l’allocation de sous-réseaux dédiés à chaque couche peut ne pas être possible. Le groupe informatique d’entreprise doit identifier le moyen optimal de configurer la source et la destination pour le filtrage du trafic qui ne nécessiterait pas de référencer directement des adresses IP ou des plages d’adresses IP.


## Tâches - Application d’entreprise BI 

1. Concevez une solution réseau à 3 couches pour l’application BI. Votre conception peut inclure Azure ExpressRoute, des passerelles VPN, des passerelles d’application, le pare-feu Azure et des équilibreurs de charge Azure. Vos composants réseau doivent être regroupés en réseaux virtuels et les groupes de sécurité réseau doivent être pris en compte. Préparez-vous à expliquer pourquoi vous avez choisi chaque composant de la solution. 

2. En fonction de votre solution d’architecte de l’étude de cas de calcul, comment cela affecterait la conception du réseau ? Auriez-vous besoin de ressources réseau supplémentaires pour sécuriser l’accès à l’application modernisée ? N’auriez-vous plus besoin de certaines des solutions recommandées implémentées dans votre conception de réseau d’origine ? 

3. En fonction de votre étude de cas (relationnelle) de stockage, comment mettriez-vous à jour la conception du réseau pour sécuriser l’accès au compte de stockage et vous assurer que seuls les utilisateurs sélectionnés ont accès au compte de stockage ?

4. En fonction de la modernisation du back-end SQL, comment prévoyez-vous d’activer l’accès pragmatique à la base de données afin que le front-end n’ait pas de secrets codés en dur dans sa base de code ?

Comment intégrez-vous les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?
