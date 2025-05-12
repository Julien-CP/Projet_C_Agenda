# Projet C - Gestion d’un agenda avec listes à niveaux

Projet réalisé dans le cadre du cours *Algorithmes et structures de données* — L2 Informatique à EFREI Paris

## Présentation

Ce projet consiste à développer en C un programme de gestion d’agenda utilisant des **listes à niveaux** pour optimiser les opérations de recherche, d’insertion et de suppression. Cette structure permet une amélioration significative des performances par rapport aux listes chaînées simples, tout en maintenant un tri logique des éléments.

L’agenda permet de stocker des **contacts** et **rendez-vous** avec un accès rapide grâce à la recherche hiérarchique.

## Membres du projet

- Adrien ASSOUAD
- Thibault BIAL
- Julien CHAN PENG

## Contenu du projet

- `main.c` – Point d’entrée du programme
- `list.c / list.h` – Gestion des listes à niveaux
- `cell.c / cell.h` – Structure des cellules et opérations de base
- `agenda.c` – Création et gestion des contacts et rendez-vous
- `timer.c / timer.h` – Outils de mesure de performance
- `Rapport SDD.docx` – Rapport complet du projet

## Concepts et structures

### Listes à niveaux

- Inspirées des **skip lists**, les listes à niveaux permettent une recherche rapide en sautant des portions de la liste.
- Chaque cellule peut exister sur plusieurs niveaux et pointer vers la suivante au même niveau.
- La recherche commence au niveau le plus haut et descend progressivement.

### Structures utilisées

- `t_d_cell` : structure d’une cellule (valeur, niveau, pointeurs)
- `t_d_list` : structure de la liste à niveaux (niveau max, pointeur tête)
- `Contact` / `RendezVous` : structures pour l’agenda (nom, prénom, date, etc.)

## Fonctionnalités implémentées

- Insertion triée dans la liste à niveaux
- Recherche classique (niveau 0 uniquement)
- Recherche hiérarchique (multi-niveaux)
- Création et affichage de rendez-vous et contacts
- Comparaison de performance des deux méthodes de recherche
- Utilisation de chaînes de caractères dynamiques avec `scanString()`

## Résultats obtenus

- **Recherche par niveau** : très performante, temps d’exécution constant même avec des données croissantes
- **Recherche classique** : temps d’exécution exponentiel avec la taille des données
- Tests de performance réalisés avec `timer.c`, montrant l’efficacité claire de la recherche hiérarchique
- Stockage fonctionnel des contacts avec insertion dynamique

## Limites et difficultés

- La **retri automatique** des éléments après modification d’un contact n’a pas pu être finalisée
- Quelques fonctionnalités restent instables ou incomplètes, notamment sur les modifications dans la liste triée
- Difficultés rencontrées sur les chaînes de pointeurs multiples et gestion dynamique

## Enseignements

Ce projet nous a permis de :
- Comprendre et manipuler les **listes à niveaux**, structure intermédiaire entre liste chaînée et tableau trié
- Approfondir la gestion dynamique en C (allocations, pointeurs, structures imbriquées)
- Expérimenter la **comparaison algorithmique** entre différentes méthodes
- Travailler en équipe sur la répartition des modules et la mise en commun des idées
- Appliquer des méthodes de test et de mesure des performances

