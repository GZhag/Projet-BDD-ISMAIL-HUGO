# Conception

# Dictionnaire des données

- Dictionnaire des données
    - Type de safran
    - Description du type de safran
    - Année
    - QuantiteProduite
    - QuantiteVendue
    - Nom client
    - Prenom client
    - Nationalite client
    - Entreprise cliente
    - Prix de la commande
    - Quantité de safran commandée
    - Type de livraison
    - Frais de livraison
    - Pays de livraison
    - Taxe d’envoie
    

- Type de safran
- Description du type de safran
- Année
- QuantiteProduite
- QuantiteVendue
- Nom client
- Prenom client
- Nationalite client
- Entreprise cliente
- Prix de la commande
- Quantité de safran commandée
- Type de livraison
- Frais de livraison
- Pays de livraison
- Taxe d’envoie

# Modèle entitée association (MEA)

![Untitled](Conception%20c82048e5fa5048c2aec448f1bd2be228/Untitled.png)

---

![DiagrammeMEAReduit.png](Conception%20c82048e5fa5048c2aec448f1bd2be228/DiagrammeMEAReduit.png)

# Shéma relationnel

Client (***NumCl***, Nom, Prénom, Nationalité, Entreprise)

Commande (***NumCo***, Prix, Date, **#NumCl, #TypeL, #Pays**)

Frais (***Pays***, Taxe)

Livraison (***TypeL***, Frais)

Produit (***TypeP***, Description)

Panier (***#TypeP,#NumCo**,* Quantité)

HistoriqueProduction (***Année**,* TypeP, QuantitéProduite, QuantitéVendue)

# Contraintes particulières

- Tout les prix, taxes , quantités et frais doivent être strictement positifs

# Liste des fonctionnalités prises en charge

- fonction calcul prix de la commande selon la qte
- Trigger qui update du stock après chaque commande ou Production:
- Trigger qui estime la fidelité des clients selon le nombre de commandes passées