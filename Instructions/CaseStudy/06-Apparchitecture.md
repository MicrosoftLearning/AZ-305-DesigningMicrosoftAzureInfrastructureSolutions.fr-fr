---
casestudy:
  title: Conception d’une solution d’architecture d’applications
  module: App architecture solutions
---
# Conception d’une solution d’architecture d’applications

## Spécifications

Tailwind Traders souhaite mettre à jour son site web pour inclure des images de produits fournies par le client, en plus des photos déjà existantes ajoutées par l’équipe marketing. Ils espèrent ainsi qu’un plus large éventail de photos permettra aux clients potentiels de se faire une meilleure idée de la manière dont les clients précédents ont apprécié leurs produits après les avoir achetés. Ils ont certaines exigences, comme indiqué ci-dessous :

* Les images chargées doivent être analysées avant d’être publiées sur le site web. Les services juridique et marketing demandent qu’après le téléchargement initial, les images soient vérifiées afin de détecter tout problème susceptible de nuire à l’image de l’entreprise ou d’entraîner des problèmes juridiques. Une API interne capable d’effectuer l’analyse nécessaire a déjà été développée et déployée. 

* En fonction des modèles existants, Tailwind Traders s’attend à ce que les chargements d’images soient très irréguliers tout au long de la journée. Certaines périodes peuvent connaître plus de chargements que le logiciel d’analyse n’est en mesure de traiter, tandis que d’autres peuvent n’avoir que très peu de chargements, voire aucun.

* Une fois qu’une image chargée a été analysée et approuvée par le système, Tailwind Traders souhaite envoyer un e-mail au client pour le remercier d’avoir partagé son image.

* Le coût et la gestion de la solution sont un problème, plus particulièrement du fait que Tailwind Traders n’est pas sûr de l’accueil qui sera réservé à cette fonctionnalité. Réduisez les coûts et tirez parti de solutions serverless dans la mesure du possible.

 

![Architecture d’application](media/Apparchitecture.png)

 

## Tâche

Concevez une architecture pour les images clients à ajouter au site web de l’entreprise. 

* Où les images doivent-elles être stockées ?

* Comment s’assurer que toutes les images sont analysées, même lorsque les chargements dépassent la capacité d’analyse ?

* Une fois les images approuvées et la base de données du catalogue mise à jour, comment le client sera-t-il averti ? 

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?

 
