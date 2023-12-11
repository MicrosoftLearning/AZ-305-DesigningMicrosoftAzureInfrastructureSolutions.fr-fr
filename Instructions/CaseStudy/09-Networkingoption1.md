
# Conception d’une solution d’infrastructure réseau  

## Spécifications

À mesure que l’équipe informatique de l’entreprise Tailwind Traders se prépare à définir la stratégie de migration des charges de travail de l’entreprise vers Azure, elle doit identifier les composants réseau requis et concevoir une infrastructure réseau nécessaire pour les prendre en charge. Compte tenu de l’étendue globale de ses opérations, Tailwind Traders utilisera plusieurs régions Azure pour héberger ses applications. La plupart de ces applications ont des dépendances vis-à-vis des services d’infrastructure et de données, qui résideront également dans Azure. Les applications internes migrées vers Azure doivent rester accessibles aux utilisateurs de Tailwind Traders. Les applications accessibles sur Internet migrées vers Azure doivent rester accessibles à n’importe quel client externe. 

Pour mettre en place la conception réseau initiale, l’équipe informatique de l’entreprise Tailwind Traders a choisi deux applications clés, qui sont représentatives des catégories les plus courantes de charges de travail qui sont censées être migrées vers Azure.  

### Conception - Application d’entreprise du catalogue de produits

![Architecture de catalogue de produits](media/catalog.png)

- Une application web Windows .NET Core à deux couches accessible sur Internet qui fournit l’accès au catalogue de produits, hébergée dans une base de données du groupe de disponibilité Always On SQL Server. Cette application est classée comme stratégique, avec un contrat SLA de disponibilité de 99,99 %, un RPO de 10 minutes et un RTO de 2 heures. 

-   Les prospects professionnels souhaitent bénéficier d’une expérience client optimale lorsqu’ils consultent des applications Internet. Les temps de chargement des pages web et de téléchargement du contenu statique doivent donc être réduits au minimum. De même, en cas de défaillance de serveurs individuels hébergeant des composants d’application web et leurs dépendances, l’impact sur la disponibilité de l’application web doit être minime pour les clients. Certes, une défaillance au niveau régional peut entraîner une interruption des sessions web existantes, mais le basculement vers un site de récupération d’urgence doit être automatique.

- Pour tirer parti des avantages offerts par les services PaaS Azure, l’équipe informatique d’entreprise a décidé d’implémenter la base de données de l’application d’entreprise du catalogue de produits à l’aide d’Azure SQL Database. 

- Les équipes en charge de la sécurité et du risque des informations de Tailwind Traders nécessitent que toutes les communications entre les machines virtuelles Azure et les services PaaS qui font partie de la même application doivent transiter par le réseau principal Azure, plutôt que via un point de terminaison public des services PaaS. 

## Tâches - Application d’entreprise du catalogue de produits

1. Concevez une solution réseau à deux couches pour le catalogue de produits. Le cas échéant, votre conception peut inclure Azure Front Door, WAF, Pare-feu Azure et Azure Load Balancer. Vos composants réseau doivent être regroupés en réseaux virtuels et les groupes de sécurité réseau doivent être pris en compte. Préparez-vous à expliquer pourquoi vous avez choisi chaque composant de la conception. 

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?

