# Explication relation N en maximum entre deux entités

## Données

- Carte 1
- Carte 2
- Carte 3

- Label 1
- Label 2
- Label 3
- Label 4

## Relations

- Carte 1 <-> Label 1
- Carte 1 <-> Label 2

- Carte 3 <-> Label 4

- Carte 2 <-> Label 3
- Carte 2 <-> Label 1

## Exemple clé étrangère sur la carte

- id: 1, label_ids: 1, 2
- id: 2, label_ids: 3, 1
- id: 3, label_ids: 4

## Exemple clé étrangère sur le label

- id: 1, card_ids: 1, 2
- ...

## Table intermédiaire stockant la relation

- card_id: 1, label_id: 1
- card_id: 1, label_id: 2
- card_id: 2, label_id: 3
