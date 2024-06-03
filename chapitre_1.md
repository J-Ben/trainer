## Conception des bases de données

### Chapitre 1: Introduction générale

#### 1.1. Historique et évolution des bases de données

L'histoire des bases de données commence dans les années 1960, lorsque les entreprises et les institutions ont ressenti le besoin croissant de stocker et de gérer de grandes quantités d'informations de manière efficace et organisée. Les premiers systèmes de gestion de bases de données (SGBD) étaient très spécifiques et souvent intégrés directement dans les applications qu'ils servaient. Ces systèmes étaient généralement hiérarchiques ou en réseau.

Avec le temps, les systèmes de bases de données sont devenus plus génériques et plus puissants. Dans les années 1970, le modèle relationnel, introduit par Edgar F. Codd, a révolutionné la manière dont les données étaient stockées et manipulées. Ce modèle permettait de représenter les données sous forme de tables, offrant une flexibilité et une simplicité accrues par rapport aux modèles hiérarchiques et en réseau.

**Exemple** : Imaginons une bibliothèque universitaire dans les années 1960 qui devait suivre les emprunts de livres. Initialement, cela aurait pu être fait avec des cartes en papier. Un SGBD rudimentaire aurait permis de créer une base de données électronique pour stocker les informations des étudiants et les livres empruntés. Par exemple, un système comme IMS (Information Management System) d'IBM permettait de structurer et de gérer ces informations de manière plus efficace.

**Exercice** : Recherchez des informations sur les premiers SGBD, tels que IMS (Information Management System) d'IBM. Quels étaient leurs avantages et leurs inconvénients par rapport aux systèmes modernes? Rédigez un court rapport comparatif.

#### 1.2. Concepts fondamentaux des bases de données

Une base de données est une collection organisée de données, stockée et accessible électroniquement. Les composants principaux sont les tables (ou relations), les lignes (ou enregistrements), les colonnes (ou champs), et les relations entre les tables.

- **Tables** : Une table est une collection de données organisées en lignes et colonnes. Chaque table représente une entité dans la base de données.
- **Lignes** : Une ligne, ou enregistrement, contient des informations sur un élément spécifique de l'entité représentée par la table.
- **Colonnes** : Une colonne, ou champ, représente un attribut de l'entité et contient une valeur pour chaque enregistrement.
- **Relations** : Les relations entre les tables sont établies à l'aide de clés primaires et étrangères pour lier les données de manière logique.

**Exemple** : Considérons une base de données pour une école. Une table "Étudiants" pourrait contenir les colonnes ID, Nom, Prénom, Date de naissance, et Classe. Une table "Cours" pourrait contenir les colonnes ID, Nom du cours, et Professeur. Une table "Inscriptions" pourrait lier les deux premières tables en associant les étudiants aux cours qu'ils suivent. Voici une représentation simple :

| Étudiants |
|-----------|
| ID | Nom  | Prénom | Date de naissance | Classe |
|----|------|--------|-------------------|--------|
| 1  | Dupont | Jean | 2005-04-12        | 5A     |
| 2  | Martin | Marie | 2006-07-23        | 5B     |

| Cours |
|-------|
| ID | Nom du cours  | Professeur  |
|----|---------------|-------------|
| 1  | Mathématiques | Mme Dupuis  |
| 2  | Histoire      | M. Leroy    |

| Inscriptions |
|--------------|
| ID | ID Étudiant | ID Cours |
|----|-------------|----------|
| 1  | 1           | 1        |
| 2  | 1           | 2        |
| 3  | 2           | 1        |

**Exercice** : Créez un schéma de base de données pour une petite entreprise de vente en ligne. Incluez au moins les tables "Clients", "Produits", et "Commandes". Décrivez les relations entre ces tables et les clés primaires et étrangères nécessaires.

#### 1.3. Avantages des bases de données relationnelles

Les bases de données relationnelles offrent plusieurs avantages clés :

- **Intégrité des données** : Les contraintes d'intégrité (comme les clés primaires et étrangères) assurent que les données sont précises et cohérentes.
- **Réduction de la redondance** : La normalisation permet de minimiser la duplication des données en structurant les informations de manière efficace.
- **Flexibilité** : Les systèmes de gestion de bases de données relationnelles (SGBDR) permettent des requêtes complexes pour extraire et manipuler les données.
- **Sécurité** : Les SGBDR fournissent des mécanismes pour contrôler l'accès aux données et protéger la confidentialité et l'intégrité des informations.
- **Accessibilité** : Les bases de données relationnelles permettent un accès concurrentiel aux données par plusieurs utilisateurs et applications.
- **Évolutivité** : Les bases de données relationnelles peuvent être facilement étendues pour gérer des volumes croissants de données.

**Exemple** : Dans une base de données relationnelle pour une bibliothèque, les informations sur les livres empruntés ne sont stockées qu'une seule fois, et toutes les autres tables se réfèrent à cette information via des clés étrangères, réduisant ainsi la redondance. Par exemple, la table "Livres" contient des informations sur chaque livre, et la table "Emprunts" utilise des clés étrangères pour associer chaque emprunt à un livre et à un emprunteur.

**Exercice** : Identifiez les avantages des bases de données relationnelles dans un contexte médical, par exemple, pour la gestion des dossiers des patients. Rédigez un court rapport expliquant comment ces avantages améliorent la gestion des données médicales.

#### QCM Chapitre 1

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

Voulez-vous continuer avec le Chapitre 2 sur le modèle relationnel?