# Projet de Séparation Éthanol-Eau - 2025-06

Ce dépôt Git contient les fichiers relatifs au projet de séparation d'un mélange éthanol-eau. L'objectif principal de ce projet est de simuler une unité de séparation pour produire de l'éthanol plus ou moins pur.

## Contexte

L'éthanol est un alcool incolore, inflammable et miscible à l'eau, utilisé dans de nombreux domaines tels que l'industrie agroalimentaire, la parfumerie, la pharmacie et la production de biocarburant. Les procédés de production d'éthanol génèrent des mélanges eau-éthanol qui nécessitent une concentration pour diverses applications.

Ce projet se concentre sur la séparation d'un flux d'alimentation de **10000 kg/h** constitué d'un mélange éthanol/eau avec une teneur en éthanol de **10% massique** à une température de **20°C**. La séparation est envisagée à pression atmosphérique dans un premier temps.

## Étapes du Projet

Le projet est structuré en plusieurs étapes, comme décrit dans l'énoncé :

1.  **Choix d’un modèle thermodynamique adéquat** : Sélection d'un modèle thermodynamique approprié pour traiter la séparation éthanol-eau.
2.  **Vérification du modèle thermodynamique** :
    *   Récupération des données du NIST (National Institute of Standards and Technology) via ASPEN+ (set de données « Binary VLE 167 »).
    *   Comparaison de ces données avec les résultats prédits par le modèle thermodynamique choisi.
    *   Amélioration de la qualité du modèle thermodynamique pour obtenir un bon accord avec les données expérimentales.
3.  **Analyse du diagramme d’équilibre liquide/vapeur thermodynamique** :
    *   Analyse du diagramme d'équilibre obtenu avec la méthode thermodynamique améliorée, en se concentrant sur la partie des concentrations élevées en éthanol (à partir de 70% de pureté).
    *   Tirer des conclusions sur la facilité à produire de l’éthanol pur.
4.  **Simulation de la colonne à distiller – Modèle simplifié (shortcut)** :
    *   Détermination des couples (nombre d’étages ; taux de reflux) permettant d'atteindre une séparation où le flux d ’éthanol contient 10% massique d’eau et le flux d’eau contient 1% d’éthanol.
    *   Détermination du nombre d’étages minimum.
    *   Détermination du taux de reflux minimum.
    *   Choix d'un couple de variables pour réaliser la séparation en pratique.
5.  **Simulation de la colonne à distiller – Modèle rigoureux** :
    *   Modélisation rigoureuse de la colonne en utilisant les valeurs initiales obtenues avec le modèle simplifié.
    *   Vérification de l'obtention des mêmes puretés que dans le modèle simplifié.
    *   Analyse de l'impact du passage au modèle rigoureux sur les coûts opératoires, notamment le paramètre le plus influencé.
    *   Réalisation d’une étude de sensibilité pour évaluer l’influence de l’étage d’alimentation sur la consommation énergétique du rebouilleur.
    *   Détermination de l’étage optimum d'alimentation et justification de ce choix.
6.  **Obtention d’éthanol pur (1% massique d’eau)** 
    *   Proposition et implémentation d'une approche pour traiter l’éthanol produit par la distillation afin d’obtenir une concentration en eau de seulement 1% massique.

## Unités

Pour l’ensemble des résultats, les unités suivantes seront utilisées :

*   Débit : kg/h
*   Température : °C
*   Pression : barg
*   Puissance : kW
*   Concentration : fractions massiques

## Logiciels Utilisés

Ce projet nécessite l'utilisation du logiciel **ASPENPLUS V11.0** pour la modélisation thermodynamique et la simulation de la colonne de distillation.
