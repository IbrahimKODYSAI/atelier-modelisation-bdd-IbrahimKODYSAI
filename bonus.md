# Bonus

## MEAE (aussi appelé _schéma Workbench_)

Il s'agit d'un schéma beaucoup plus complet que le MCD, qui représente la structure de la BDD de façon fidèle.

### Avantages

- Il représente les clés et les contraintes de la BDD ;
- L'outil utilisé pour le dessiner permet aussi de générer le script SQL de création de la BDD :heart_eyes:.

### Inconvénients

- Son exhaustivité le rend moins clair, moins lisible qu'un MCD, qui ne représente que "l'essentiel" :dizzy_face: ;
- Ce n'est pas gênant dans notre cas mais il ne fonctionne qu'avec MySQL : autre SGBD, autres spécificités.

### Comment procéder

- installer MySQLWorkBench si ce n'est pas déjà fait
  - en ligne de commande : `sudo apt-get install mysql-workbench`
- lancer MySQLWorkBench
- Créer un _Model_
- Ajouter un _EER Diagram_
- Créer les tables
- Pour chaque table, définir les champs, leur type, leurs attributs (UNSIGNED, NULL, etc.) et leur valeur par défaut
- Lier les tables entre elles avec les relations `1:n` ou `n:m` **non identifying**
  - attention à l'ordre du click (commencer par la table côté 1 de la relation)
  - les clés étrangères sont automatiquement créées (en rouge) :tada:
  - la relation `n:m` a une conséquence bizarre, mais logique ! :nerd_face:

## Export PNG

- Menu > File > Export > Export as PNG

## Export SQL

- Menu > File > Export > Forward Engineering SQL Create Script
- Sélectionner un fichier SQL
- Cocher uniquement :
  - Skip creation of Foreign Keys
  - Ommit schema qualifier in Object Names
  - Generate INSERT statements for tables
- Next
- Next
- Finish

## Création database

- créer un utilisateur dans phpMyAdmin
  - en cochant "créer une base de données du même nom également et lui donner tous les droits"
- aller dans cette nouvelle base de données dans phpMyadmin
- onglet _Opérations_
- changer _Interclassement_ ou _Collation_ en `ut8_general_ci`

## Import

- dans phpMyAdmin
- onglet _Import_
- sélectionner le fichier SQL exporté via MySQLWorkBench
- Valider