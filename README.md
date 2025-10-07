# Le projet Customer First Company

## Introduction

Le but de ce projet est d'analyser des données fictives afin de démontrer comment, à partir de données brutes, de précieux insights peuvent être livrés aux équipes métiers : ici, le service client de 'Customer First', basée aux Etat-sUnis et spécialisé dans la vente de produits hardware, logiciels, et dans la téléphonie.

Le défi à relever est donc d'explorer les données et de les corriger si besoin, de comprendre les process business en place pour les challenger une fois des KPIs identifiés et les données analysées. 
L'objectif est d'améliorer la satisfaction des clients en identifiant des axes d'amélioration.

A l'issue de cette étude qui durera 10 jours, un rapport Power BI doit être livré aux équipes métiers, ainsi que des recommandations pour améliorer le fonctionnement du service client.

Le code utilsé pour l'exploration des données est public, et le rapport final peut être téléchargé.

## Objectifs

1) Identifier des KPIs pour les équipes métiers
2) Evaluer la performance du service client
3) Livrer un rapport Power BI pour aider les équipes métiers à piloter l'activité

## Les données

Le jeu de données est un constitué de 8469 tickets et 17 colonnes.

Ces données nous on permis d'analyser les KPIs suivants :
- Le volume des tickets qui va compter le nombre de Tickets IDs
- Le temps de première réponse qui permet d’évaluer la réactivité d’un service client.
- Le taux de réponse, soit la proportion de réponse par rapport à tous les tickets.
- Le temps de résolution: même principe que le temps de première réponse, mais pour la résolution d’un ticket.
- Le taux de résolution
- La Customer satisfaction (CSAT): une note donnée par un client à la suite d’un échange avec le support.

## Les process Business

Grâce à l'exploration des données, un business process a pu être cartographié, mais nécessite des entretiens avec le service client pour mieux détailler son fonctionnement.



## Insights

### Démographie

Pour ce qui est des données démographiques, on remarque que la catégorie 18-30 ans est la plus représentée (de peu). Si ce segment est le plus représenté dans les ventes, cela peut expliquer pourquoi il est plus représenté dans l'échantillon : en revanche, un écart important entre les ventes et le taux de contact par catégorie démographique peut illustrer un besoin non adressé, qu'il s'agisse du produit, du tunnel de conversion, du service client.

Par ailleurs, croiser les données démographiques du service client avec  les département des ventes et du marketint permet d'identifier les canaux où concentrer les agents du service client pour prendre en charge rapidement et efficacement les demandes. 

### Volume de tickets

Si  le volume de ticket est bien réparti sur l'ensemble des canaux, il l'est aussi sur la priorité : or certains canaux devraient permettre de traiter plus des demandes, plus rapidement (en particulier les tickets à haute priorité).
Par exemple ici, le téléphone représente ¼ des tickets. Or au téléphone, un agent traite un ticket à la fois : à l'écrit, un agent traite sept tickets à la fois.
Le service pourrait gagner en efficacité en privilégiant l'écrit, et en réservant le téléphone aux tickets urgents pour proposer une résolution rapide et une expérience client personnalisée.

### First Response Time et le taux de réponse

Le temps moyen de première réponse est de 35 heures : il devrait être de 24 heures maximum pour les emails et les réseaux sociaux, de quelques minutes pour le tchat et le téléphone.
De plus, il n'y a pas de changement en fonction de la priorité du ticket, alors qu'un ticket de type Critical devrait être pris en charge très rapidement.

Pour ce qui est du taux de réponse, celui-ci est bas : il devrait excéder les 90%.

Le temps de première réponse et le taux de réponse sont en-deça des standards pour un service client. Le process devrait changer afin que les tickets soient pris en charge par ordre de priorité

### Temps de Résolution et taux de résolution

On ne sait pas si le taux de résolution est décompté à partir de la date de création du ticket ou  du temps de première réponse : il est donc difficile de mesurer si les objectifs sont atteints. 
On remarque que les Refund et Product inquiries mettent du temps à être traitées par rapport à un Technical Issue donc:
1) il faut que le process de remboursement soit clair, simple, rapide
2) pour les product inquiries, il faut de la documentation claire à destination des clients,  et des Saved Replies pour le support (voire un chatbot)

### Customer Satisfaction

Avec un FRT moyen de 35h et un TTR moyen de 35h aussi, on peut anticiper une CSAT assez basse.

C’est le cas ici où elle est de 2.99 : nous avons fixé un objectif à 4 qui est le minimum recommandé pour un service support.

La  CSAT la plus basse concerne surtout  les problèmes techniques: il faut impérativement améliorer le traitement de ce type de ticket en spécialisant les équipes et/ou en développant une FAQ  pour aider les utilisateurs à résoudre un incident sans contacter le support.
Le canal le plus à mal globalement reste le téléphone : il faut donc réévaluer le plan de charge sur ce canal, et réfléchir à eds automatisations, ou à l'abandon du service téléphonique au bénéfice du tchat.

Les produits triés par CSAT devraient être comparé avec un Net Promoter Score pour recueillir un meilleur feedback sur nos produits.

## Recommandations

### 10 recommandations data

- Créer une colonne Creation Date
- First Response Time = Datetime de première réponse
- Time to resolution = Datetime de résolution
- Créer une colonne Client ID
- Créer une colonne Agent ID
- Créer une colonne State 
- Créer une colonne Product Category
- Créer une colonne Product Brand
- Créer une colonne Ticket Channel avec sources de données
- Mettre en place du shadow avec le support pour mieux mapper le flux de données

### 10 recommandations opérationnelles

- Viser une CSAT à 4,00 minimum pour garantir une expérience client optimale
- Viser un FRT de moins de 24 heures pour améliorer la réactivité
- Changer le statut des tickets “Pending for Customer Response” en “Closed” au bout de 3 semaines (automatisation à envisager)
- Spécialiser les équipes support pour répondre  efficacement aux demandes
- Rédiger des FAQ claires et engageantes pour maximiser le Self Care
- Limiter au maximum le téléphone pour privilégier l’écrit
- Mettre en place Harvestr pour récupérer et expoiter les retours client
- Développer des Saved Replies pour répondre rapidement aux demandes écrites (Intercom offre cette fonctionnalité)
- Développer un chatbot pour gérer un volume de demandes important
- Accéder à un historique de tickets

### Propositionn de Process

## Conclusion


