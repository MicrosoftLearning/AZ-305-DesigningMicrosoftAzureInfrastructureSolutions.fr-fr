---
casestudy:
  title: Conception d’une solution de stockage non relationnel
  module: Non-relational storage solutions
---
# Conception d’une solution de stockage non relationnel

## Spécifications

Tailwind Traders souhaite réduire les coûts de stockage en réduisant le contenu dupliqué et, le cas échéant, en le migrant vers le cloud. L’entreprise recherche une solution qui centralise la maintenance tout en offrant un accès mondial aux clients qui parcourent les fichiers multimédias et les supports marketing. Elle souhaite également résoudre le problème de stockage des fichiers de données d’entreprise. 

![Architecture de stockage non relationnel](media/Nonrelational%20storage.png)

 

* **Fichiers multimédias**. Les fichiers multimédias incluent des photos de produits et des vidéos de fonctionnalités qui sont affichées sur le site web public de l’entreprise, qui est développé et géré en interne. Lorsqu’un client consulte un article, les fichiers multimédias correspondants s’affichent. Les fichiers multimédias existent dans différents formats, notamment JPEG et MP4. 

* **Supports marketing**. Les supports marketing incluent des témoignages de clients, des brochures de vente, des tableaux de tailles et des informations sur la fabrication respectueuse de l’environnement. Les utilisateurs marketing internes accèdent aux supports via un lecteur mappé sur leurs stations de travail Windows. Les clients accèdent directement aux supports à partir du site web public de l’entreprise.

* **Documents d’entreprise**. Il s’agit de documents internes destinés aux services tels que les ressources humaines et les finances. Ces documents sont accessibles et gérés via une application web développée en interne. La loi exige que certains documents soient conservés pendant une période spécifique. Les documents doivent parfois être conservés plus longtemps en cas de problèmes juridiques ou de ressources humaines. La plupart des documents d’entreprise datant de plus d’un an ne sont conservés que pour des raisons de conformité et sont rarement consultés.

* **Emplacement des fichiers**. Tous les fichiers sont stockés localement dans le centre de données du siège de l’entreprise. De nombreux fichiers sont utilisés par différents services ou gammes de produit. Les serveurs de données ont du mal à fournir des fichiers pour le site web. Pendant les périodes de forte affluence, les pages du site web s’affichent lentement. 

* **Fréquence d’accès aux fichiers**. Certains produits sont plus populaires et leurs données sont donc consultées plus fréquemment. Certains produits, comme les équipements de ski, ne sont toutefois consultés qu’à l’approche de l’hiver. Les articles en promotion connaissent une augmentation du trafic. 

## Tâches

1. Concevez une solution de stockage pour Tailwind Traders. 

      * Quel type de données est représenté ? 

      * Quels sont les facteurs à prendre en compte dans votre conception ?

      * Utiliserez-vous des niveaux d’accès aux objets blob ?

      * Allez-vous utiliser un stockage immuable ?

      * Comment allez-vous faire pour que le contenu soit accessible en toute sécurité ?

2.  Votre solution doit tenir compte des médias, des supports marketing et des documents d’entreprise. Vos recommandations peuvent être différentes en fonction des données. Préparez-vous à étayer vos décisions. 

Comment allez-vous intégrer les piliers d’Azure Well-Architected Framework pour produire une architecture cloud de haute qualité, stable et efficace ?
