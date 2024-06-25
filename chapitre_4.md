### Chapitre 4: Le langage SQL

#### 4.1. Introduction à SQL (Structured Query Language)

SQL (Structured Query Language) est un langage de programmation standard utilisé pour gérer et manipuler les bases de données relationnelles. Il permet de définir des structures de données, de manipuler les données et de contrôler l'accès aux données.

**Objectifs :**
1. Comprendre l'utilité de SQL dans la gestion des bases de données.
2. Apprendre les commandes de base de SQL.
3. Maîtriser les commandes SQL avancées.
4. Appliquer les contraintes et gérer l'intégrité des données avec SQL.

#### 4.2. Commandes SQL de base

Les commandes de base en SQL incluent les opérations de sélection, insertion, mise à jour et suppression de données.

**4.2.1. Commande SELECT**

La commande `SELECT` est utilisée pour extraire des données d'une table.

**Exemple :**
```sql
SELECT * FROM Tramways;
```

**Exercices :**
1. Sélectionnez tous les tramways dont le modèle est 'Alstom'.
   ```sql
   SELECT * FROM Tramways WHERE Modèle = 'Alstom';
   ```

2. Sélectionnez les tramways ayant une capacité supérieure à 150.
   ```sql
   SELECT * FROM Tramways WHERE Capacité > 150;
   ```

**4.2.2. Commande INSERT**

La commande `INSERT` est utilisée pour ajouter de nouvelles lignes dans une table.

**Exemple :**
```sql
INSERT INTO Tramways (TramwayID, LigneID, Modèle, AnnéeFabrication, Capacité, DateEntretien, EnService, ConducteurID)
VALUES (4, 1, 'CAF', 2018, 220, '2024-09-01', TRUE, 4);
```

**Exercices :**
1. Insérez un nouveau tramway avec les détails de votre choix.
   ```sql
   INSERT INTO Tramways (TramwayID, LigneID, Modèle, AnnéeFabrication, Capacité, DateEntretien, EnService, ConducteurID)
   VALUES (5, 2, 'Hyundai', 2019, 180, '2024-10-01', TRUE, 5);
   ```

2. Ajoutez un tramway qui est hors service.
   ```sql
   INSERT INTO Tramways (TramwayID, LigneID, Modèle, AnnéeFabrication, Capacité, DateEntretien, EnService, ConducteurID)
   VALUES (4, 3, 'Bombardier', 2017, 150, '2024-11-01', FALSE, 4);
   ```

**4.2.3. Commande UPDATE**

La commande `UPDATE` est utilisée pour modifier les données existantes dans une table.

**Exemple :**
```sql
UPDATE Tramways SET Capacité = 210 WHERE TramwayID = 1;
```

**Exercices :**
1. Mettez à jour le modèle de tramway avec l'ID 2 pour 'Siemens'.
   ```sql
   UPDATE Tramways SET Modèle = 'Siemens' WHERE TramwayID = 2;
   ```

2. Changez l'état de service du tramway avec l'ID 3 à FALSE.
   ```sql
   UPDATE Tramways SET EnService = FALSE WHERE TramwayID = 3;
   ```

**4.2.4. Commande DELETE**

La commande `DELETE` est utilisée pour supprimer des lignes d'une table.

**Exemple :**
```sql
DELETE FROM Tramways WHERE TramwayID = 4;
```

**Exercices :**
1. Supprimez tous les tramways fabriqués avant 2015.
   ```sql
   DELETE FROM Tramways WHERE AnnéeFabrication < 2015;
   ```

2. Supprimez les tramways qui ne sont pas en service.
   ```sql
   DELETE FROM Tramways WHERE EnService = FALSE;
   ```

#### 4.3. Commandes SQL avancées

Les commandes SQL avancées incluent des opérations de regroupement, de filtrage et de tri des données.

**4.3.1. Commande GROUP BY et HAVING**

La commande `GROUP BY` est utilisée pour regrouper des lignes qui ont les mêmes valeurs dans des colonnes spécifiées. La clause `HAVING` est utilisée pour filtrer les groupes.

**Exemple :**
```sql
SELECT LigneID, COUNT(*) AS NombreTramways
FROM Tramways
GROUP BY LigneID
HAVING COUNT(*) > 1;
```

**Exercices :**
1. Groupez les tramways par modèle et affichez le nombre de tramways pour chaque modèle.
   ```sql
   SELECT Modèle, COUNT(*) AS NombreTramways
   FROM Tramways
   GROUP BY Modèle;
   ```

2. Affichez les lignes qui ont plus de 2 tramways en service.
   ```sql
   SELECT LigneID, COUNT(*) AS NombreTramwaysEnService
   FROM Tramways
   WHERE EnService = TRUE
   GROUP BY LigneID
   HAVING COUNT(*) > 2;
   ```

**4.3.2. Commande ORDER BY**

La commande `ORDER BY` est utilisée pour trier les résultats.

**Exemple :**
```sql
SELECT * FROM Tramways ORDER BY Capacité DESC;
```

**Exercices :**
1. Affichez tous les tramways triés par année de fabrication en ordre croissant.
   ```sql
   SELECT * FROM Tramways ORDER BY AnnéeFabrication ASC;
   ```

2. Affichez les tramways en service triés par date d'entretien en ordre décroissant.
   ```sql
   SELECT * FROM Tramways WHERE EnService = TRUE ORDER BY DateEntretien DESC;
   ```

**4.3.3. Fonctions d'agrégation (SUM, AVG, COUNT, etc.)**

Les fonctions d'agrégation sont utilisées pour effectuer des calculs sur un ensemble de valeurs et retourner une valeur unique.

**Exemple :**
```sql
SELECT AVG(Capacité) AS CapacitéMoyenne FROM Tramways;
```

**Exercices :**
1. Calculez le nombre total de tramways.
   ```sql
   SELECT COUNT(*) AS NombreTotalTramways FROM Tramways;
   ```

2. Calculez la capacité totale des tramways en service.
   ```sql
   SELECT SUM(Capacité) AS CapacitéTotale FROM Tramways WHERE EnService = TRUE;
   ```

#### 4.4. SQL et les contraintes

Les contraintes en SQL sont utilisées pour spécifier des règles pour les données dans une table. Elles aident à maintenir l'exactitude et l'intégrité des données.

**4.4.1. Clé primaire**

Une clé primaire est un champ ou un ensemble de champs qui identifie de manière unique chaque enregistrement dans une table.

**Exemple :**
```sql
CREATE TABLE Tramways (
    TramwayID INT PRIMARY KEY,
    LigneID INT,
    Modèle VARCHAR(50),
    AnnéeFabrication INT,
    Capacité INT,
    DateEntretien DATE,
    EnService BOOLEAN,
    ConducteurID INT
);
```

**Exercices :**
1. Créez une table Conducteurs avec une clé primaire sur ConducteurID.
   ```sql
   CREATE TABLE Conducteurs (
       ConducteurID INT PRIMARY KEY,
       Nom VARCHAR(50),
       Prénom VARCHAR(50),
       DateNaissance DATE,
       DateEmbauche DATE
   );
   ```

2. Ajoutez une clé primaire à une table existante Lignes.
   ```sql
   ALTER TABLE Lignes
   ADD PRIMARY KEY (LigneID);
   ```

**4.4.2. Clé étrangère**

Une clé étrangère est un champ ou un ensemble de champs dans une table qui crée un lien entre les données de deux tables.

**Exemple :**
```sql
CREATE TABLE Tramways (
    TramwayID INT PRIMARY KEY,
    LigneID INT,
    Modèle VARCHAR(50),
    AnnéeFabrication INT,
    Capacité INT,
    DateEntretien DATE,
    EnService BOOLEAN,
    ConducteurID INT,
    FOREIGN KEY (LigneID) REFERENCES Lignes(LigneID)
);
```

**Exercices :**
1. Créez une clé étrangère dans la table Tramways reliant ConducteurID à Conducteurs.
   ```sql
   ALTER TABLE Tramways
   ADD CONSTRAINT FK_Conducteur
   FOREIGN KEY (ConducteurID) REFERENCES Conducteurs(ConducteurID);
   ```

2. Ajoutez une clé étrangère à une table Emplois reliant EmployéID à Employés.
   ```sql
   ALTER TABLE Emplois
   ADD CONSTRAINT FK_Employé
   FOREIGN KEY (EmployéID) REFERENCES Employés(EmployéID);
   ```

### QCM

1. Quel est le principal avantage des bases de données relationnelles?
   - a) Réduction de la sécurité
   - b) Augmentation de la redondance
   - c) Flexibilité des requêtes
   - d) Difficulté de mise en œuvre

2. Quel composant de base de données stocke les enregistrements?
   - a) Tables
   - b) Colonnes
   - c) Lignes
   - d) Relations

3. Qui a introduit le modèle relationnel?
   - a) Edgar F. Codd
   - b) Charles Bachman
   - c) Bill Gates
   - d)

 Larry Ellison

4. Quel est le rôle d'une clé primaire?
   - a) Créer une copie des données
   - b) Assurer l'unicité des enregistrements
   - c) Relier différentes bases de données
   - d) Définir les types de données

5. Quelle est la principale caractéristique des données en 1NF?
   - a) Atomicité
   - b) Redondance
   - c) Intégrité
   - d) Durabilité

4. Les SGBD des années 1940 étaient souvent:
   - a) Très génériques
   - b) Spécifiques aux applications
   - c) Basés sur des réseaux
   - d) Inutilisés

7. Qu'est-ce que SQL signifie?
   - a) Structured Query Language
   - b) Sequential Query Language
   - c) Simple Query Language
   - d) Secure Query Language

8. Une base de données est une collection de:
   - a) Programmes
   - b) Algorithmes
   - c) Données organisées
   - d) Fichiers PDF

9. Quel type de données pourrait être stocké dans une colonne BOOLEAN?
   - a) Texte
   - b) Numéros
   - c) Vrai/Faux
   - d) Dates

10. La normalisation des bases de données vise à:
    - a) Augmenter la redondance
    - b) Diminuer l'intégrité
    - c) Réduire la duplication
    - d) Simplifier les requêtes

### Conclusion

Ce chapitre vous a permis de découvrir les commandes SQL de base et avancées ainsi que les contraintes utilisées pour assurer l'intégrité des données. Vous avez appris à manipuler les données dans une base de données relationnelle et à appliquer des règles de gestion des données. Vous êtes maintenant capable d'écrire des requêtes SQL pour extraire, insérer, mettre à jour et supprimer des données, ainsi que d'assurer l'intégrité des données grâce aux clés primaires et étrangères.