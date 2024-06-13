# Projet-d-etude_BD_G4
Data link : https://www.kaggle.com/datasets/prasad22/retail-transactions-dataset/data

# Rapport du Projet : Application Interactive de Prédiction Non Supervisée
Objectif :
Développer une application interactive utilisant Streamlit pour effectuer une analyse non supervisée des données clients. L'application permet aux utilisateurs de sélectionner les caractéristiques, d'effectuer une analyse PCA (Analyse en Composantes Principales) et de réaliser un clustering KMeans.

**1. Chargement et Prétraitement des Données**
*Données Utilisées :*

Fichier CSV : RTD.csv
*Colonnes d'origine :*
Customer_Name
Transaction_ID
Date
Product
Payment_Method
City
Store_Type
Customer_Category
Season
Promotion
Total_Items
Total_Cost
Discount_Applied
*Étapes de Prétraitement :*

*Suppression de Colonnes :*

Customer_Name
Transaction_ID
Date
*Transformation de la Colonne Product :*

Conserver uniquement le premier élément de la liste et le convertir en chaîne de caractères.
*Encodage des Données :*

Colonnes catégorielles : Product, Payment_Method, City, Store_Type, Customer_Category, Season, Promotion
Utilisation de LabelEncoder.
Colonnes numériques : Total_Items, Total_Cost, Discount_Applied
Normalisation avec MinMaxScaler.
**2. Interface Utilisateur avec Streamlit**
Fonctionnalités Principales :

Titre de l'Application : "Interactive Unsupervised Prediction"
Sélection de la Colonne Cible pour la Prédiction :
Permet aux utilisateurs de choisir la colonne cible.
Sélection des Colonnes de Fonctionnalités :
Permet aux utilisateurs de sélectionner les colonnes à utiliser pour la prédiction parmi les colonnes disponibles.
Validation :

Vérification que toutes les colonnes sélectionnées sont bien catégorielles ou numériques.
Saisie des Valeurs des Fonctionnalités :

*Colonnes catégorielles :* Sélection parmi les valeurs uniques disponibles.
Colonnes numériques : Utilisation de curseurs pour sélectionner les valeurs.
**3. Analyse en Composantes Principales (PCA)**
*Étapes :*

*Application de PCA :*
Réduction des données à deux dimensions.
*Visualisation :*
Affichage des résultats de PCA avec un graphique scatterplot incluant les données d'entrée.
*Résultats :*

Affichage des résultats de PCA et visualisation des points de données sur deux axes principaux (PC1 et PC2).
**4. Clustering KMeans**
*Étapes :*

*Détermination du Nombre de Clusters :*
Utilisation du nombre de valeurs uniques dans la colonne cible.
*Application de KMeans :*
Création de clusters.
*Prédiction pour les Données d'Entrée :*
Affichage du cluster auquel appartiennent les données d'entrée.
*Correspondance des Clusters :*

Détermination de la correspondance entre les clusters et les valeurs cibles.
Affichage de la correspondance pour interpréter les résultats.
*Visualisation :*

Affichage des résultats de clustering avec PCA, en utilisant différentes couleurs pour représenter les clusters.
**Conclusion et Utilisation**
L'application interactive développée permet aux utilisateurs de charger des données, de sélectionner les caractéristiques pertinentes, et d'effectuer des analyses non supervisées en utilisant PCA et KMeans. Les utilisateurs peuvent visualiser les résultats sous forme de graphiques interactifs et comprendre la segmentation des données.

**Recommandations :**

Valider et tester l'application avec des ensembles de données variés pour assurer sa robustesse.
Intégrer des fonctionnalités supplémentaires telles que la sauvegarde des résultats et des rapports détaillés.
