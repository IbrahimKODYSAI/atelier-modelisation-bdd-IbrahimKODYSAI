# Modéliser la base de données

La base de données est la pierre angulaire de toute application.

## Références

Pour modéliser notre projet _oKanban_, vous pouvez vous baser sur le travail effectué en cours, en S05E05.  
On a d'ailleurs placé dans le répertoire [S05](S05) 3 documents d'exemple de cette journée S05E05.

## Etapes

### #1 MCD

**Outils** => [Mocodo](http://mocodo.wingi.net/)  
**Récap** => [Conception d'un MCD](https://github.com/O-clock-Alumni/fiches-recap/blob/master/bdd/conception-03-mcd.md)

#### Entités

- un nom unique
- deux points `:`
- les attributs, séparés par une virgule `,`
- exemples :  
`AUTHOR: pen name, real name, date of birth, language`  
`BOOK: title, number of pages, type, release date`

#### Relations

- rappels : https://github.com/O-clock-Alumni/fiches-recap/blob/master/bdd/conception-03-mcd.md#cardinalit%C3%A9s
- définir les cardinalités en se posant les bonnes questions :
  - _1 entité `A` est liée à combien d'entité `B` minimum ?_
      - 0 ou 1
  - _1 entité `A` est liée à combien d'entité `B` maximum ?_
      - 1 ou n
  - _1 entité `B` est liée à combien d'entité `A` minimum ?_
      - 0 ou 1
  - _1 entité `B` est liée à combien d'entité `A` maximum ?_
      - 1 ou n
  - au final, on a 1  cardinalité pour chaque "sens" de la relation
      - exemple : `A` => `B` = `0,n`
      - exemple : `B` => `A` = `0,1`
      - => on parle alors de relation de type `1:n` (on prend le max de chaque cardinalité)
- pour représenter cela sur _Mocodo_
  - écrire sur une seule ligne (comme pour une entité)
    - un nom unique pour la relation
    - une virgule `,`
    - minimum et maximum d'une des deux cardinalités, collés l'un à l'autre, ex : `11`, `0N` (:warning: c'est zéro-N, pas `on` en majuscules) etc.
    - le nom de l'entité visée par la cardinalité
    - une virgule `,`
    - min et max de l'autre cardinalité
    - le nom de l'autre entité
  - exemple : `writes, 11 AUTHOR, 0N BOOK` (:warning: zéro-N)

#### Positionnement

Mocodo utilise un système de grille très simple _(Pensez aux tableaux HTML, le fonctionnement est assez identique !)_

- Écrivez chaque élément (entité ou relation) sur une ligne dédiée
  - Mocodo va les positionner côte à côte horizontalement (comme des `<td>`)
- Sautez une ligne dans le script pour passer à la ligne suivante dans le schéma
  - Mocodo dessinera le prochain élément tout à gauche, en dessous de la ligne précédente (comme si vous aviez changé de `<tr>`)
- Écrivez simplement `:` sur une ligne pour laisser la "case" vide (comme une `<td> </td>` avec un simple espace dedans)

### #2 Dictionnaire de données

- compléter le dictionnaire de données fourni (à la racine) :
  - lister les données nécessaires
  - définir à quelle entité sont attachées les données
  - définir le type de chaque donnée

## Bonus

[Ca se passe ici :wink:](bonus.md)
