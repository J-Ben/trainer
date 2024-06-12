### Travaux Pratiques (TP) Enoncé 1 : Gestion de la Production dans une Usine

**Objectifs :**
1. Concevoir un modèle conceptuel de données (MCD) pour une usine.
2. Traduire le MCD en modèle logique de données (MLD).
3. Créer des schémas de relations à partir du MLD.
4. Appliquer des opérations d'algèbre relationnelle pour extraire des informations pertinentes.

### 1. Modèle Conceptuel de Données (MCD)

#### Étape 1 : Identification des Entités et des Relations
Identifiez les entités et les relations nécessaires pour modéliser la gestion de la production dans une usine. Voici quelques suggestions :

- **Produits**
- **Machines**
- **Employés**
- **Départements**
- **Commandes**
- **Production**

#### Étape 2 : Définition des Attributs
Pour chaque entité, définissez des attributs pertinents de base.

#### Étape 3 : Diagramme MCD
Dessinez un diagramme MCD montrant les relations et les cardinalités entre les entités.

### 2. Modèle Logique de Données (MLD)

#### Traduction du MCD en MLD
Transformez le MCD en MLD en définissant les relations entre les tables, les clés primaires et étrangères.

### 3. Schéma de Relations
Créez des schémas de relations à partir du MLD pour représenter les tables et les relations entre elles. Chaque schéma de relation doit contenir au moins 8 champs différents en type (chaîne de caractères, entiers, booléens, etc.).

### 4. Exercices sur l'Algèbre Relationnelle

#### Exercices de Sélection : 
**Attention : vous devez afficher le résultat de chaque selection d'après les enregistrements fournis pour chacune des tables table. Notez que les données et attributs fournis sont indépendants de ceux de votre propre analyse.**

**Table Produits :**
1. Sélectionnez tous les produits dont le prix est supérieur à 1000.
2. Sélectionnez tous les produits dont le type est 'Électronique'.
3. Sélectionnez tous les produits fabriqués avant une certaine date.


Table Produits

| ID | Nom            | Type         | Prix   | Date Fabrication | Stock |
|----|----------------|--------------|--------|------------------|-------|
| 1  | Téléviseur     | Électronique | 1200   | 2023-05-10       | 50    |
| 2  | Smartphone     | Électronique | 800    | 2023-04-15       | 100   |
| 3  | Ordinateur     | Électronique | 1500   | 2023-06-20       | 30    |
| 4  | Machine à Café| Électroménager| 200    | 2023-03-05       | 80    |
| 5  | Imprimante     | Électronique | 300    | 2023-07-12       | 60    |
| 6  | Tablette       | Électronique | 600    | 2023-05-30       | 40    |
| 7  | Réfrigérateur  | Électroménager| 1000  | 2023-02-18       | 20    |
| 8  | Micro-ondes    | Électroménager| 150    | 2023-09-25       | 90    |
| 9  | Aspirateur     | Électroménager| 400    | 2023-08-10       | 70    |
| 10 | Console de jeux| Électronique | 700    | 2023-07-05       | 50    |


**Table Machines :**
1. Sélectionnez toutes les machines où la date d'acquisition est après le 1er janvier 2020.
2. Sélectionnez toutes les machines où le type est 'Automatique'.
3. Sélectionnez toutes les machines avec un coût supérieur à 50,000.
4. On veut connaitre les machines inactives afin de les remettre en marche.

 Table Machines

| ID | Nom            | Type       | Coût   | Date Acquisition | Statut |
|----|----------------|------------|--------|------------------|--------|
| 1  | Robot 1        | Automatique| 60000  | 2022-12-10       | Actif  |
| 2  | Machine 1      | Automatique| 80000  | 2023-02-20       | Inactif|
| 3  | Presse 1       | Manuelle   | 40000  | 2023-05-15       | Actif  |
| 4  | Machine 2      | Automatique| 70000  | 2023-01-05       | Actif  |
| 5  | Imprimante 3D  | Automatique| 90000  | 2023-04-30       | Actif  |
| 6  | Perceuse 1     | Manuelle   | 30000  | 2023-03-25       | Inactif|
| 7  | Machine 3      | Automatique| 75000  | 2023-06-10       | Actif  |
| 8  | Scie Circulaire| Manuelle   | 35000  | 2023-08-20       | Inactif|
| 9  | Machine 4      | Automatique| 85000  | 2023-07-15       | Actif  |
| 10 | Robot 2        | Automatique| 65000  | 2023-09-05       | Actif  |

**Table Employés :**
1. Sélectionnez tous les employés où le poste est 'Technicien' ou 'Ouvrier'.
2. Sélectionnez tous les employés ayant plus de 10 ans d'expérience.
3. Montrez tous les employés travaillant dans la Maintenance.
Table Employés

| ID | Nom            | Prénom | Poste       | Salaire | Date Embauche | Département |
|----|----------------|--------|-------------|---------|---------------|-------------|
| 1  | Dupont         | Jean   | Technicien  | 2500    | 2022-10-01    | Production  |
| 2  | Durand         | Pierre | Ingénieur   | 3500    | 2022-11-15    | Recherche   |
| 3  | Martin         | Marie  | Opérateur   | 2000    | 2023-01-20    | Production  |
| 4  | Dubois         | Sylvie | Responsable | 4000    | 2023-02-10    | Administration |
| 5  | Bernard        | Sophie | Technicien  | 2400    | 2023-03-05    | Maintenance |
| 6  | Thomas         | Lucas  | Ingénieur   | 3800    | 2023-04-15    | Recherche   |
| 7  | Petit          | Émilie | Opérateur   | 2100    | 2023-06-20    | Production  |
| 8  | Robert         | Marc   | Responsable | 4200    | 2023-07-12    | Administration |
| 9  | Simon          | Claire | Technicien  | 2600    | 2023-08-30    | Maintenance |
| 10 | Lefebvre       | Thomas | Ingénieur   | 3900    | 2023-09-25    | Recherche   |


**Table Départements :**
1. Sélectionnez tous les départements avec plus de 20 employés.
2. Sélectionnez tous les départements où le budget est supérieur à 100,000.
3. Sélectionnez tous les départements où le nom commence par 'R'.

Table Départements

| ID | Nom            | Budget | Nombre Employés | Localisation |
|----|----------------|--------|-----------------|--------------|
| 1  | Production     | 500000 | 50              | Usine 1      |
| 2  | Recherche      | 300000 | 20              | Centre R&D   |
| 3  | Maintenance    | 100000 | 10              | Usine 1      |
| 4  | Administration | 200000 | 5               | Siège Social |


**Table Commandes :**
1. Sélectionnez toutes les commandes passées avant le 1er janvier 2024.
2. Quels sont les commandes dont les clés produits sont des multiple de 3 ?
3. Sélectionnez toutes les commandes où la quantité commandée est supérieure ou égale à 100.
4. Sélectionnez toutes les commandes pour un produit spécifique.
Table Commandes

| ID | Date Commande | Produit ID | Quantité | Prix Total | Statut   |
|----|---------------|------------|----------|------------|----------|
| 1  | 2023-05-10    | 1          | 10       | 12000      | En Cours  |
| 2  | 2023-07-15    | 3          | 5        | 7500       | Terminée  |
| 3  | 2023-08-20    | 5          | 8        | 2400       | En Cours  |
| 4  | 2023-09-05    | 2          | 12       | 9600       | En Cours  |
| 5  | 2023-09-30    | 6          | 15       | 9000       | En Cours  |
| 6  | 2023-10-05    | 8          | 3        | 450        | En Attente|
| 7  | 2023-11-20    | 4          | 7        | 1400       | En Cours  |
| 8  | 2023-12-01    | 7          | 4        | 4000       | Terminée  |
| 9  | 2024-01-10    | 9


**Table Production : A vous de fournir le jeu de données de cette table en fonction du shema que vous avez défini de manière à ce que les selections demandées soient possibles et renvoient des résultats.**
1. Sélectionnez toutes les productions réalisées par l'employé Marc Robert.
2. Sélectionnez toutes les productions où la quantité produite est supérieure à 500 mais inférieur à 750.
3. Sélectionnez toutes les productions réalisées sur une Imprimante 3D.
 
