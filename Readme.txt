# Mini Projet - Analyse de données géographiques du Burkina Faso

Ce projet vise à extraire et analyser des données géographiques du Burkina Faso à partir de la base de données GeoNames.

## Structure du projet
mini_projet_data_analysis/
├── data/ # Contient les données brutes téléchargées
│ ├── BF.txt # Fichier original des localités du Burkina Faso
│ ├── BF.zip # Archive téléchargée
│ ├-- readme # informations sur les donnés .zip
├── output/ # Contient les résultats des traitements
│ ├── burkina_location.csv
│ └── mini_projet.xlsx # Fichier Excel final
├── code/ # Contient le code source
│ └── code.ipynb # Notebook Jupyter avec le code complet
└── README.md # Ce fichier

## Objectifs du projet
1. Télécharger et traiter les données géographiques du Burkina Faso
2. Extraire un sous-ensemble de données spécifiques

## Étapes principales du code
1. **Configuration initiale**
   - Importation des bibliothèques nécessaires
   - Création de la structure de répertoires
   

2. **Téléchargement des données**
   - Récupération des informations sur les pays
   - Extraction du code ISO du Burkina Faso (BF)
   - Téléchargement des données géographiques spécifiques au Burkina Faso

3. **Prétraitement des données**
   - Nettoyage et sélection des colonnes pertinentes
   - Renommage des colonnes
   - Sauvegarde au format CSV

4. **Analyses et extractions**
   - Recherche de la localité "Gounghin"
   - Extraction des localités dont le nom commence par A-P
   - Identification des coordonnées extrêmes
   - Filtrage géographique (latitude ≥ 11 et longitude ≤ 0.5)

5.  Génération d'un fichier Excel avec plusieurs feuilles contenat les données de "Gounghin" et dont le nom commence par A-P

## Comment exécuter le code
1. Installer les dépendances :
```bash
pip install pandas requests 

Exécuter le notebook Jupyter :

Ouvrir code/code.ipynb dans Jupyter Notebook ou Jupyter Lab

Exécuter toutes les cellules dans l'ordre

Les résultats seront générés dans le répertoire output/

Fichiers générés
burkina_location.csv - Toutes les localités du Burkina Faso

mini_projet.xlsx - Fichier Excel avec deux feuilles :

gounghin : Données de la localité Gounghin

A_to_P : Localités de A à P



Détails techniques
Sources de données :

GeoNames (http://www.geonames.org/)

Fichier pays : https://download.geonames.org/export/dump/countryInfo.txt

Données BF : https://download.geonames.org/export/dump/BF.zip

Bibliothèques utilisées :

pandas pour la manipulation des données

requests pour les téléchargements HTTP

zipfile pour la décompression des archives

os pour la gestion des répertoires


Personnalisation
Pour adapter le projet à un autre pays :

Modifier le nom du pays dans la cellule de recherche du code ISO

Adapter les chemins de fichiers si nécessaire

Ajuster les paramètres des filtres géographiques



Auteur
[YAMEOGO Isaac]
[14/08/2025]

