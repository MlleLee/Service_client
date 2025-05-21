# Le projet Customer First Company

## Contexte

La société Customer First Company est une société fictive basée aux Etats-Unis spécialisée dans la vente de Hardware, Software, téléphonie
Plusieurs canaux sont disponibles pour contacter son service client.

Nous avions 10 jours pour finaliser le projet :
- Faire une analyse de la donnée existante 
- Identifier les KPIs
- Ebaucher un plan d’action pour améliorer ces KPIs
- Proposer des pistes d’amélioration pour optimiser le support


## Objectifs

Identifier des KPIs
Evaluer la performance du service client
Améliorer le service client

## Les données

Le jeu de données est constitué de 8469 tickets et 17 colonnes.

Ces données nous on permis d'analyser les KPIs suivants :
- Le volume des tickets qui va compter le nombre de Tickets IDs
- Le temps de première réponse qui permet d’évaluer la réactivité d’un service client.
- Le taux de réponse, soit la proportion de réponse par rapport à tous les tickets.
- Le temps de résolution: même principe que le temps de première réponse, mais pour la résolution d’un ticket.
- Le taux de résolution
- La Customer satisfaction (CSAT): une note donnée par un client à la suite d’un échange avec le support.

## Insights

### Démographie

Globalement c’est très équilibré, même si la catégorie 18-30 ans est la plus représentée.

### Volume de tickets

Globalement c’est encore une fois bien réparti sur les canaux, et sur la priorité, ce qui n’est pas une bonne nouvelle!
Par exemple, le téléphone représente ¼ des tickets. 
Or au téléphone :  un agent traite 1 ticket à la fois.
A l’écrit : 1 agent traite 7 tickets à la fois.
On perd donc en efficacité.

### First Response Time te le taux de réponse

Le temps moyen de première réponse est de 35 heures : il devrait être de 24 heures maximum pour les emails et les réseaux sociaux, de quelques minutes pour le tchat et le téléphone.
Il n'y a pas de changement en fonction de la priorité du ticket, alors qu'un ticket de type Critical devrait être pris en charge très rapidement.

Pour ce qui est du taux de réponse, celui-ci est bas : il devrait excéder les 90%.

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

- Viser une CSAT à 4,00 minimum
- FRT < 24H
- “Pending for Customer Response” en “Closed” au bout de 3 semaines
- Des équipes support spécialisées 
- Des FAQ claires pour maximiser le Self Care
- Limiter au maximum le téléphone pour privilégier l’écrit
- Mettre en place Harvestr
- Développer des Saved Replies
- Développer un chatbot
- Accès à un historique de tickets




