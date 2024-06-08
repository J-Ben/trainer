### Chapitre 1: Introduction générale

#### 1.1. Historique et évolution des bases de données

L'histoire des bases de données commence dans les années 1960, lorsque les entreprises et les institutions ont ressenti le besoin croissant de stocker et de gérer de grandes quantités d'informations de manière efficace et organisée. Les premiers systèmes de gestion de bases de données (SGBD) étaient très spécifiques et souvent intégrés directement dans les applications qu'ils servaient. Ces systèmes étaient généralement hiérarchiques ou en réseau.

Avec le temps, les systèmes de bases de données sont devenus plus génériques et plus puissants. Dans les années 1970, le modèle relationnel, introduit par Edgar F. Codd, a révolutionné la manière dont les données étaient stockées et manipulées. Ce modèle permettait de représenter les données sous forme de tables, offrant une flexibilité et une simplicité accrues par rapport aux modèles hiérarchiques et en réseau.

**Exemple** : Imaginons une bibliothèque universitaire dans les années 1960 qui devait suivre les emprunts de livres. Initialement, cela aurait pu être fait avec des cartes en papier. Un SGBD rudimentaire aurait permis de créer une base de données électronique pour stocker les informations des étudiants et les livres empruntés. Par exemple, un système comme IMS (Information Management System) d'IBM permettait de structurer et de gérer ces informations de manière plus efficace.

**Exercice** : Recherchez des informations sur les premiers SGBD, tels que IMS (Information Management System) d'IBM. Quels étaient leurs avantages et leurs inconvénients par rapport aux systèmes modernes? Rédigez un court rapport comparatif.

#### 1.2. Du passage des systèmes de fichiers aux SGBD

Les systèmes de fichiers traditionnels étaient utilisés pour stocker des données dans des fichiers séparés. Chaque fichier contenait des données relatives à une application ou à une partie d'une application. Cependant, ces systèmes avaient plusieurs inconvénients :

- **Redondance et incohérence des données** : Les mêmes données pouvaient être stockées dans plusieurs fichiers, ce qui entraînait des duplications et des incohérences.
- **Difficulté de gestion des données** : Chaque application devait gérer ses propres fichiers, ce qui compliquait l'accès et la mise à jour des données.
- **Absence de standardisation** : Les formats de fichiers variaient d'une application à l'autre, rendant difficile l'intégration et l'interopérabilité.
- **Manque de sécurité et de contrôle d'accès** : Les systèmes de fichiers ne fournissaient pas de mécanismes robustes pour contrôler l'accès aux données.

Les systèmes de gestion de bases de données (SGBD) ont été développés pour surmonter ces limitations. Ils offrent une interface commune pour gérer et accéder aux données, tout en assurant l'intégrité, la cohérence, et la sécurité des données.

**Avantages des SGBD** :
- **Réduction de la redondance et de l'incohérence** : Les SGBD centralisent les données, réduisant ainsi la duplication et assurant la cohérence.
- **Gestion facilitée des données** : Les SGBD offrent des outils pour gérer les données de manière centralisée, simplifiant l'accès et les mises à jour.
- **Standardisation** : Les SGBD utilisent des formats standardisés, facilitant l'intégration et l'interopérabilité.
- **Sécurité et contrôle d'accès** : Les SGBD fournissent des mécanismes robustes pour contrôler l'accès aux données et protéger la confidentialité.

**Inconvénients des SGBD** :
- **Coût** : Les SGBD peuvent être coûteux à mettre en place et à maintenir.
- **Complexité** : Les SGBD peuvent être complexes à administrer, nécessitant des compétences spécialisées.
- **Performances** : Les SGBD peuvent être moins performants pour certaines applications spécifiques en raison de leur complexité et de la surcharge de gestion.

**Exemple** : Considérons un système de gestion des employés. Dans un système de fichiers, les informations des employés pourraient être réparties dans plusieurs fichiers (par exemple, un fichier pour les informations personnelles, un autre pour les informations salariales). Avec un SGBD, toutes ces informations peuvent être centralisées dans une base de données, réduisant ainsi la redondance et facilitant la gestion des données.

**Exercice** : Comparez les avantages et les inconvénients des systèmes de fichiers et des SGBD dans le contexte d'une entreprise de vente au détail. Rédigez un court rapport expliquant pourquoi une entreprise pourrait préférer utiliser un SGBD plutôt qu'un système de fichiers.

#### 1.3. Types de systèmes de gestion de bases de données (SGBD)

Il existe plusieurs types de SGBD, chacun ayant ses propres caractéristiques et étant adapté à différents types d'applications :

1. **SGBD hiérarchiques** :
   - Les données sont organisées en une structure arborescente.
   - Chaque enregistrement a un parent et peut avoir plusieurs enfants.
   - **Avantages** : Accès rapide aux données, structure simple.
   - **Inconvénients** : Difficulté de modification de la structure, redondance des données.
   - **Exemple** : IMS (Information Management System) d'IBM.

2. **SGBD en réseau** :
   - Les données sont organisées en une structure de graphe.
   - Les enregistrements peuvent avoir plusieurs parents et enfants.
   - **Avantages** : Flexibilité accrue par rapport aux SGBD hiérarchiques.
   - **Inconvénients** : Complexité de gestion, difficultés de mise à jour.
   - **Exemple** : IDMS (Integrated Database Management System).

3. **SGBD relationnels** :
   - Les données sont organisées en tables, avec des lignes et des colonnes.
   - Les relations entre les tables sont établies via des clés primaires et étrangères.
   - **Avantages** : Flexibilité, normalisation, facilité d'utilisation.
   - **Inconvénients** : Performance moins optimale pour certaines applications spécifiques.
   - **Exemple** : MySQL, PostgreSQL, Oracle.

4. **SGBD orientés objet** :
   - Les données sont représentées sous forme d'objets, comme dans la programmation orientée objet.
   - Les objets peuvent contenir des données et des méthodes.
   - **Avantages** : Modélisation naturelle des données complexes, réutilisabilité du code.
   - **Inconvénients** : Complexité, courbe d'apprentissage plus élevée.
   - **Exemple** : db4o, ObjectDB.

5. **SGBD NoSQL** :
   - Les données sont stockées dans des formats non relationnels (documents, colonnes, clés-valeurs, graphes).
   - Adaptés aux grandes quantités de données non structurées.
   - **Avantages** : Scalabilité, flexibilité, performance pour les applications web et les big data.
   - **Inconvénients** : Manque de normalisation, intégrité des données plus difficile à assurer.
   - **Exemple** : MongoDB, Cassandra, Redis.

**Exemple** : Imaginons une entreprise de construction de maisons. Un SGBD relationnel pourrait être utilisé pour gérer les informations sur les clients, les projets de construction, et les employés. Les relations entre les tables permettraient de lier les clients aux projets, et les projets aux employés responsables.

**Exercice** : Identifiez les types de SGBD qui seraient les plus appropriés pour les scénarios suivants : une application bancaire, un réseau social, et un système de gestion d'inventaire pour un grand magasin. Justifiez votre choix pour chaque scénario.

#### 1.4. Concepts fondamentaux des bases de données

Une base de données est une collection organisée de données, stockée et accessible électroniquement. Les composants principaux sont les tables (ou relations), les lignes (ou enregistrements), les colonnes (ou champs), et les relations entre les tables.

- **Tables** : Une table est une collection de données organisées en lignes et colonnes. Chaque table représente une entité dans la base de données.
- **Lignes** : Une ligne, ou enregistrement, contient des informations sur un élément spécifique de l'entité représentée par la table.
- **Colonnes** : Une colonne, ou champ, représente un attribut de l'entité et contient une valeur pour chaque enregistrement.
- **Relations** : Les relations entre les tables sont établies à l'aide de clés primaires et étrangères pour lier les données de manière logique.

**Exemple 1** : Considérons une base de données pour une école. Une table "Étudiants" pourrait contenir les colonnes ID, Nom, Prénom, Date de naissance, et Classe. Une table "Cours" pourrait contenir les colonnes ID, Nom du cours, et Professeur. Une table "Inscriptions" pourrait lier les deux premières tables en associant les étudiants aux cours qu'ils suivent. Voici une représentation simple :

| ID | Nom     | Prénom | Date de naissance | Classe |
|----|---------|--------|-------------------|--------|
| 1  | Dupont  | Jean   | 2005-04-12        | 5A     |
| 2  | Martin  | Marie  | 2006-07-23        | 5B     |

| ID | Nom du cours | Professeur |
|----|--------------|------------|
| 1  | Mathématiques | M. Durand |
| 2  | Français      | Mme. Leroy |

| ID étudiant | ID cours |
|-------------|----------|
| 1           | 1        |
| 2           | 2        |


**Exemple 2** : Pour une entreprise de construction de maisons, la base de données pourrait inclure :
- Une table "Clients" contenant les colonnes ID, Nom, Prénom, Adresse, et Numéro de téléphone.
- Une table "Projets" contenant les colonnes ID, Nom du projet, Adresse du chantier, et Date de début.
- Une table "Employés" contenant les colonnes ID, Nom, Prénom, Poste, et Salaire.
- Une table "Attributions" pour gérer les affectations d'employés à des projets, contenant les colonnes ID, ID de l'employé, ID du projet, et Date d'affectation.

| ID | Nom     | Prénom | Adresse            | Numéro de téléphone |
|----|---------|--------|--------------------|---------------------|
| 1  | Duval   | Pierre | 123 Rue de la Paix | 0123456789          |
| 2  | Lefèvre | Anne   | 456 Avenue des Champs | 0987654321        |

| ID | Nom du projet | Adresse du chantier      | Date de début |
|----|---------------|--------------------------|---------------|
| 1  | Maison A      | 789 Boulevard Victor Hugo | 2023-01-10    |
| 2  | Maison B      | 101 Rue de Rivoli         | 2023-02-15    |

| ID | Nom     | Prénom | Poste         | Salaire |
|----|---------|--------|---------------|---------|
| 1  | Martin  | Luc    | Maçon         | 2500    |
| 2  | Petit   | Claire | Électricien   | 2200    |

| ID | ID de l'employé | ID du projet | Date d'affectation |
|----|-----------------|--------------|--------------------|
| 1  | 1               | 1            | 2023-01-12         |
| 2  | 2               | 2            | 2023-02-16         |

#### 1.5. Avantages des bases de données relationnelles

Les bases de données relationnelles offrent plusieurs avantages clés :

- **Intégrité des données** : Assure que les données sont précises et cohérentes.
- **Réduction de la redondance** : Minimise la duplication des données grâce à la normalisation.
- **Flexibilité** : Permet des requêtes complexes pour extraire et manipuler les données.
- **Sécurité** : Fournit des mécanismes pour contrôler l'accès aux données et protéger la confidentialité.

**Exemple** : Dans une base de données relationnelle pour une bibliothèque, les informations sur les livres empruntés ne sont stockées qu'une seule fois, et toutes les autres tables se réfèrent à cette information via des clés étrangères, réduisant ainsi la redondance.

**Exercice** : Identifiez les avantages des bases de données relationnelles dans un contexte médical, par exemple, pour la gestion des dossiers des patients. Décrivez comment la normalisation peut améliorer la précision et la cohérence des données.

### QCM Chapitre 1

1. Quel est le principal avantage des bases de données relationnelles?
   a) Réduction de la sécurité  
   b) Augmentation de la redondance  
   c) Flexibilité des requêtes  
   d) Difficulté de mise en œuvre  

2. Quel composant de base de données stocke les enregistrements?  
   a) Tables  
   b) Colonnes  
   c) Lignes  
   d) Relations  

3. Qui a introduit le modèle relationnel?  
   a) Edgar F. Codd  
   b) Charles Bachman  
   c) Bill Gates  
   d) Larry Ellison  

4. Quel est le rôle d'une clé primaire?  
   a) Créer une copie des données  
   b) Assurer l'unicité des enregistrements  
   c) Relier différentes bases de données  
   d) Définir les types de données  

5. Quelle est la principale caractéristique des données en 1NF?  
   a) Atomicité  
   b) Redondance  
   c) Intégrité  
   d) Durabilité  

6. Les SGBD des années 1960 étaient souvent:  
   a) Très génériques  
   b) Spécifiques aux applications  
   c) Basés sur des réseaux  
   d) Inutilisés  

7. Qu'est-ce que SQL signifie?  
   a) Structured Query Language  
   b) Sequential Query Language  
   c) Simple Query Language  
   d) Secure Query Language  

8. Une base de données est une collection de:  
   a) Programmes  
   b) Algorithmes  
   c) Données organisées  
   d) Fichiers PDF  

9. Quel type de données pourrait être stocké dans une colonne BOOLEAN?  
   a) Texte  
   b) Numéros  
   c) Vrai/Faux  
   d) Dates  

10. La normalisation des bases de données vise à:  
    a) Augmenter la redondance  
    b) Diminuer l'intégrité  
    c) Réduire la duplication  
    d) Simplifier les requêtes  

---
 