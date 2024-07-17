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