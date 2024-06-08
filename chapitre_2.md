# Chapitre 2: Le modèle relationnel

## 2.1. Introduction au modèle relationnel

### Rappels

Le modèle relationnel a été proposé par Edgar F. Codd en 1970 alors qu'il travaillait chez IBM. Ce modèle repose sur une structure de données basée sur des tables (ou relations) pour représenter les données et leurs relations. Avant le modèle relationnel, les bases de données étaient principalement hiérarchiques ou en réseau, ce qui rendait les relations entre les données plus complexes et moins flexibles.

#### Exemple

Considérons une base de données d'une bibliothèque :

- **Table "Livres"** : contient les informations sur les livres.
  - Colonnes : ID, Titre, Auteur, Genre, Date de publication
- **Table "Auteurs"** : contient les informations sur les auteurs.
  - Colonnes : ID, Nom, Prénom, Date de naissance

*Exemple de données pour la table "Livres"* :

| ID  | Titre                  | Auteur        | Genre       | Date de publication |
|-----|------------------------|---------------|-------------|---------------------|
| 1   | "1984"                 | George Orwell | Fiction     | 1949                |
| 2   | "To Kill a Mockingbird"| Harper Lee    | Fiction     | 1960                |

### Concepts de base (tables, lignes, colonnes)

- **Table** : Représente une relation dans la base de données. Elle est constituée de lignes et de colonnes.
- **Ligne** : Aussi appelée n-uplet ou enregistrement, représente une instance de la relation.
- **Colonne** : Aussi appelée attribut, représente une propriété de la relation.

#### Exemple

Table "Étudiants" avec les colonnes ID, Nom, Prénom, Date de naissance.

| ID  | Nom      | Prénom  | Date de naissance |
|-----|----------|---------|-------------------|
| 1   | Dupont   | Jean    | 1995-05-20        |
| 2   | Martin   | Sophie  | 1993-07-15        |

#### Exercices

1. **Exercice 1** : Dessinez un diagramme de relations pour une base de données de gestion de cours incluant les tables "Cours", "Étudiants", et "Inscriptions". Indiquez les clés primaires et les clés étrangères.
2. **Exercice 2** : Définissez un schéma de relation pour une table "Employés" dans une entreprise, incluant au moins cinq attributs différents (par exemple, ID, Nom, Prénom, Poste, Salaire).

## 2.2. Structure des données relationnelles

### Schéma de relation

Le schéma de relation définit la structure d'une table, incluant ses attributs et leurs types de données. Il décrit comment les données sont organisées et les relations entre elles.

#### Exemple

Table "Produits" :

- ID (INTEGER)
- Nom (VARCHAR)
- Prix (DECIMAL)
- Date d'ajout (DATE)

### Domaines et types de données
Le domaine d'un attribut dans une base de données définit l'ensemble des valeurs autorisées pour cet attribut. Cela permet de restreindre les données pouvant être stockées dans une colonne donnée, assurant ainsi l'intégrité et la cohérence des données.

Voici quelques points importants à retenir sur les domaines en base de données :

1. **Définition du Domaine** : Chaque attribut d'une table est associé à un domaine qui spécifie le type de données pouvant être stocké dans cette colonne. Par exemple, une colonne "Âge" peut avoir un domaine de type INTEGER pour ne stocker que des nombres entiers.

2. **Contraintes de Domaine** : Les domaines peuvent inclure des contraintes pour limiter les valeurs acceptables. Par exemple, une colonne "Genre" peut avoir un domaine restreint aux valeurs "Homme" ou "Femme", assurant ainsi que seules ces deux options peuvent être stockées.

3. **Types de Données** : Les domaines peuvent être associés à différents types de données, tels que INTEGER, VARCHAR, DATE, etc. Chaque type de données a ses propres règles et restrictions quant aux valeurs qu'il peut contenir.

4. **Gestion des Erreurs** : Lorsqu'une valeur enfreint les contraintes de domaine, le système de gestion de base de données (SGBD) peut générer une erreur ou appliquer une action spécifiée, comme rejeter la valeur ou la remplacer par une valeur par défaut.

5. **Uniformité des Données** : En définissant des domaines appropriés pour chaque attribut, il est possible de garantir que les données stockées dans une colonne donnée sont cohérentes et uniformes, ce qui facilite la manipulation et l'analyse ultérieure de ces données.

6. **Exemple** : Pour une colonne "Code Postal", le domaine peut être défini comme VARCHAR(10) pour accepter des chaînes de caractères de longueur maximale 10, correspondant aux codes postaux. Les contraintes peuvent également spécifier un format spécifique pour les codes postaux, comme "XXXXX" pour les codes postaux américains à 5 chiffres.

En résumé, les domaines jouent un rôle crucial dans la définition et la gestion des types de données en base de données, contribuant à assurer l'intégrité, la cohérence et la qualité des données stockées.


Les types de données spécifient le genre de valeurs que chaque attribut peut contenir. Les types de données courants incluent :

- **NUMÉRIQUES** : INTEGER, DECIMAL, FLOAT
- **CHAÎNES DE CARACTÈRES** : VARCHAR, CHAR, TEXT
- **DATES ET HEURES** : DATE, TIME, TIMESTAMP
- **AUTRES TYPES** : BOOLEAN, BLOB (Binary Large Object), ENUM

#### Exemple

Table "Commandes" :

| ID  | Client   | Date de commande | Total     | Payée |
|-----|----------|------------------|-----------|-------|
| 1   | Dupont   | 2024-01-15       | 150.75    | TRUE  |
| 2   | Martin   | 2024-01-20       | 75.50     | FALSE |

#### Exercices

1. **Exercice 1** : Créez le schéma pour une table "Ventes" dans une base de données de magasin, incluant les types de données appropriés pour chaque attribut.
2. **Exercice 2** : Définissez un schéma de relation pour une table "Patients" dans une base de données hospitalière avec au moins cinq attributs différents, incluant différents types de données (INTEGER, VARCHAR, DATE, BOOLEAN, etc.).

## 2.3. Contraintes d'intégrité

### Contraintes d'entité

Les contraintes d'entité assurent que chaque enregistrement dans une table est unique. La clé primaire est un exemple de contrainte d'entité.

#### Exemple

Dans la table "Clients", l'ID client doit être unique pour chaque enregistrement.

### Contraintes de domaine

Les contraintes de domaine limitent les valeurs que les attributs peuvent prendre. Elles assurent que les données respectent certaines règles définies.

#### Exemple

Dans la table "Employés", le salaire doit être un nombre positif.

### Contraintes de clé primaire et étrangère

- **Clé primaire** : Assure l'unicité des enregistrements dans une table.
- **Clé étrangère** : Établit une relation entre deux tables en référant la clé primaire d'une autre table.

#### Exemple

Table "Inscriptions" :

| ID | Étudiant_ID (FK) | Cours_ID (FK) |
|----|------------------|---------------|
| 1  | 1                | 101           |
| 2  | 2                | 102           |

Ici, Étudiant_ID et Cours_ID sont des clés étrangères référant respectivement les clés primaires des tables "Étudiants" et "Cours".

### Risques liés à la non prise en compte des contraintes d'intégrité

Ne pas respecter les contraintes d'intégrité peut entraîner :

- **Incohérences dans les données** : Par exemple, des entrées dupliquées pour des clients.
- **Données invalides** : Par exemple, des valeurs de salaire négatives ou des dates incorrectes.
- **Références brisées** : Par exemple, des clés étrangères pointant vers des enregistrements inexistants, ce qui rend difficile le maintien de la cohérence des données entre les tables.

#### Exercices

1. **Exercice 1** : Imaginez une table "Factures" avec une contrainte de clé étrangère reliant l'ID du client de la table "Clients". Expliquez comment cela assure l'intégrité des données.
2. **Exercice 2** : Définissez des contraintes de domaine pour une table "Produits" où le prix doit être supérieur à zéro et la quantité en stock doit être un entier positif.

## QCM de fin de chapitre

1. Qui a développé le modèle relationnel ?
    - a) Charles Bachman
    - b) Bill Gates
    - c) Edgar F. Codd
    - d) Larry Ellison

2. Quelle est la principale structure de données dans le modèle relationnel ?
    - a) Graphes
    - b) Arbres
    - c) Tables
    - d) Listes chaînées

3. Quel terme décrit une ligne dans une table relationnelle ?
    - a) Attribut
    - b) Tuple
    - c) Domaine
    - d) Clé

4. Une clé primaire assure :
    - a) La duplication des enregistrements
    - b) L'unicité des enregistrements
    - c) La suppression des enregistrements
    - d) La modification des enregistrements

5. Quelle contrainte assure que les valeurs d'un attribut sont valides ?
    - a) Contrainte de domaine
    - b) Contrainte d'entité
    - c) Clé primaire
    - d) Clé étrangère

6. Les attributs d'une table sont également connus sous le nom de :
    - a) Lignes
    - b) Colonnes
    - c) Tuples
    - d) Relations

7. Une clé étrangère :
    - a) Est toujours unique
    - b) Relie deux tables
    - c) Est toujours vide
    - d) Est une contrainte de domaine

8. Une table "Clients" avec une clé primaire sur l'ID client garantit :
    - a) Que chaque client a un identifiant unique
    - b) Que les clients peuvent partager des identifiants
    - c) Que les identifiants sont séquentiels
    - d) Que les identifiants sont aléatoires

9. Les données relationnelles sont stockées sous forme de :
    - a) Documents
    - b) Graphes
    - c) Tables
    - d) Listes

10. Une contrainte d'intégrité garantit :
    - a) La redondance des données
    - b) La cohérence des données
    - c) La perte des données
    - d) La duplication des données