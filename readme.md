<<<<<<< HEAD
# Lab Mise en Pratique des Tables Incrémentales dans Dataform
### Objectif du Lab
Ce lab a pour objectif de démontrer la mise en pratique des tables incrémentales dans Dataform. Nous allons construire une nouvelle table incrémentale `fct_transactions` à partir de la table `stg_transactions`, ce qui permettra d'optimiser le traitement des données en ne traitant que les nouvelles données ajoutées depuis la dernière exécution.

### Contexte
Nous disposons actuellement de la table `stg_transactions` qui contient des enregistrements de transactions de ventes. Cette table est alimentée en continu par les transactions générées par la source. Pour faire de l'analytics, nous avons besoin d'une table qui contienne les données les plus fraîches. Pour améliorer l'efficacité, cette table ne traitera que les nouvelles transactions depuis la dernière mise à jour.

### Étapes du Lab
1. **Connexion à Dataform et Création du Projet**
   * Connectez-vous à votre compte Dataform.
   * reprenez le lab3
2. **Création d'une Table Incrémentale**
   * Créez une nouvelle table `fct_transactions` en utilisant la table source `stg_transactions`.
   * Configurez la table pour qu'elle soit incrémentale.
   * Utilisez `transaction_id` comme clé unique.
   * Filtrez les données pour ne prendre que les transactions de la veille.
=======
# Introduction
L'objectif de ce lab est de définir les sources que nous allons utiliser dans notre projet. Pour ce faire, nous allons simuler trois sources de données :

* **Transactions** : des données qu'une autre équipe ou un partenaire nous a partagées (la table transactions).
* **Customers** : une table alimentée par un flux dans notre dataplateform (la table customers).
* **Products** : une table que nous allons charger depuis un stockage (la table products).

Les objectifs du lab sont :

1. **Créer la source transactions** : se baser sur la table transactions définie dans `formation-dataform.raw_data.transactions`.
2. **Créer la table customers** : l'alimenter avec les données du fichier `customers.csv`.
   1. télécharger le fichier `cutomers.csv` en local
   1. dans bigquery créer une dataset, par exemple lab2
   2. dans la dataset lab2 créer une table
   3. choisir `upload` et récupérer le fichier depuis le local
   4. utilisez le schema suivant :  
      * customer_id: STRING, 
      * first_name: STRING, 
      * last_name: STRING, 
      * email: STRING, 
      * phone_number: STRING, 
      * address: STRING, 
      * city: STRING, 
      * state: STRING, 
      * postal_code: STRING, 
      * country: STRING, 
      * created_at: STRING, 
      * updated_at: STRING
3. **Créer la table products** : charger les données depuis le fichier products.csv.
   1. télécharger le fichier `products.csv`.
   2. créez une bucket gcs
   3. mettre le fichier `products.csv`.dans le bucket
   4. loader le fichier depuis le bucket en utilisant le schema suivant 
      * product_id: STRING,
      * product_name: STRING,
      * description: STRING,
      * price: STRING,
      * category: STRING,
      * supplier_id: STRING,
      * created_at: STRING,
      * updated_at: STRING
>>>>>>> refs/heads/main
