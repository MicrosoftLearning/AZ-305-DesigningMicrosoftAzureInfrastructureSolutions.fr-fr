---
casestudy:
  title: Concevoir une solution de calcul
  module: Compute solutions
---

# Concevoir une solution de calcul

## Spécifications

Tailwind Traders souhaite migrer son application de catalogue de produits vers le cloud. Cette application a une configuration traditionnelle à 3 couches et utilise SQL Server comme magasin de données. L’équipe informatique espère que vous pouvez l’aider à moderniser l’application. Elle a fourni ce diagramme et identifié plusieurs domaines qui pourraient être améliorés. 

![architecture de calcul](media/compute.png)

* L’application front-end est une application web basée sur .NET Core. Pendant les périodes de forte affluence, 1 750 clients visitent le site web chaque heure. 

* L’application s’exécute sur des serveurs web IIS à un niveau frontal. Ce niveau gère toutes les demandes d’achat de produits par les clients. Au cours de la dernière période promotionnelle, les serveurs front-end ont atteint leurs limites de performances et les chargements de page étaient longs. L’équipe informatique a envisagé d’ajouter d’autres serveurs, mais pendant les heures creuses, les serveurs sont souvent inactifs.

* Le niveau intermédiaire héberge la logique métier qui traite les demandes des clients. Ces demandes sont souvent adressées au support technique. Les demandes de support sont mises en file d’attente et les temps d’attente sont très longs. Les clients se voient proposer une réponse par e-mail plutôt que d’attendre l’intervention d’un agent. De nombreux clients semblent toutefois frustrés et se déconnectent plutôt que d’attendre. Les demandes des clients sont au nombre de 75 à 125 par heure. 

* Le niveau back-end utilise la base de données SQL Server pour stocker les commandes des clients. Actuellement, les serveurs de base de données back-end fonctionnent bien.

* Bien que la haute disponibilité soit une préoccupation, en raison des exigences légales, l’entreprise doit conserver toutes les ressources dans une seule région.

## Tâches

* **Niveau frontal**. Quel service de calcul Azure recommanderiez-vous pour le niveau frontal ? Expliquez la raison pour laquelle vous avez choisi cette solution. 

* **Niveau intermédiaire**. Quel service de calcul Azure recommanderiez-vous pour le niveau intermédiaire ? Expliquez la raison pour laquelle vous avez choisi cette solution. 

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?
