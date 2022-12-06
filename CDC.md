# Cahier des charges

## Titre 

"Réalisation d’une application web pour la documentation de détails sur les clients les ventes et le stock d’un agriculteur exportateur de safran."

## Contexte (ou Introduction)

Ahmed est un agriculteur de safran Marocain qui possède une entreprise d’export  vers l’étranger appelée SCorp. Il vend son safran en poudre ou en stigmates. Grâce à la très bonne qualité de son produit,  le nombre de commandes et de clients a grandement augmentés . Il rencontre ainsi des difficultés à bien noter sur papier les informations sur ses clients étrangers et son business d’exportation à cause du volume important. Par conséquent , il souhaite avoir toutes les informations concernant son stock, ses clients étrangers et ses ventes enregistrées proprement quelque part pour mieux gérer son business et lui faciliter la vie .

Le contexte est donc celui de la gestion des cours et des emplois du temps que l'Université Pierre-Marie de Saint-Martin-la-Plaine souhaiterait améliorer.

## Problématiques

Ahmed est le seul gérant de son commerce de safran vers le marché interne et étranger . Il remarque qu’il a des soucis d’organisation et de lisibilité avec sa manière traditionnelle de gestion . Ce qui le pousse à exprimer plusieurs problématiques:

- Problème de changement de stock en permanence . Suivre le changement de son stock est essentiel .
- Mauvaise organisation sur papier avec le grand nombre de clients.
- Difficulté de se rappeler des clients les plus fidèles .


## Besoins

- La liste de tous ses clients ainsi que leur nombre d’achat pour voir leur fiabilité
- La liste de chacune des ventes et de leur détail
- Les données de son stock actuel
- Sa production/Vente par année

> **Contraintes particulières**
> 
- La solution devra être accessible depuis une interface Web.
- Elle devra fonctionner dans un environnement WINDOWS.

## Livrables

2 livrables sont attendus :

- La solution *packagée* dans des conteneurs type Docker
- La documentation contenant les procédures d'installation et de déploiement, le guide utilisateur et le guide administrateur.
- La solution devra fonctionner sur un serveur local.

# Réponse au besoin

## Solutions

Pour répondre aux besoins de Ahmed , nous avons identifié les solutions fonctionnelles et techniques adequates pour une gestion plus facile et rapide d’un commerce d’export.

### Solutions fonctionnelles

- Possibilité de contrôler le restant du stock de produit qui se met à jour automatiquement.
- Système de gestions de clients et de leurs  commandes.
- Un classement de clients basé sur leurs nombre de commandes pour prioriser les plus fidèles.

### Solutions techniques

- Le langage PHP pour la génération dynamique de la page web.
- Docker pour le packaging de l'application dans un environnement maîtrisée et cloisonné.
- Serveur Web Apache pour la délivrance des pages Web.
- Une base de données PostgreSQL pour la gestion et la manipulation des données.

# Livrables

- Un environnement *Docker* contenant l'ensemble des services, base de données et IHMs. Le livrable pourra s'installer sur une machine WINDOWS avec *Docker* et *docker-compose* installés.
- Un fichier [README](https://github.com/vincentmartin/demo-postgresql-php/blob/master/README.md) décrit la procédure d'installation de l'application.

Les mises à jour se font en téléchargeant la dernière version de l'application sur *github*. Lors des mises à jours, l'administrateur du système devra suivre la procédure suivante :

- Stopper les services
    
    `docker-compose down`
    
- Télécharger les mises à jours
    
    `git pull`
    
- Redémarrer les services
    
    `docker-compose up`
