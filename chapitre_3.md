### Chapitre 3: L'algèbre relationnelle

#### 3.1. Opérations de base
L'algèbre relationnelle est un langage procédural utilisé pour manipuler et interroger les données stockées dans des bases de données relationnelles. Elle se compose d'opérations fondamentales qui permettent de manipuler les relations (ou tables) pour obtenir des résultats spécifiques. Les principales opérations de l'algèbre relationnelle sont la sélection, la projection et la jointure.

##### 3.1.1. Sélection (σ)
La sélection permet de filtrer les lignes d'une table en fonction d'une condition spécifiée. Elle extrait uniquement les lignes qui satisfont cette condition.

**Syntaxe :**  
\[ \sigma_{condition}(Relation) \]

**Exemple :**  
Sélectionner tous les employés dont le salaire est supérieur à 50 000 euros.

\[ \sigma_{salaire > 50000}(Employés) \]

**Explication :**  
Cette opération filtre les lignes de la table "Employés" où la colonne "salaire" est supérieure à 50 000.

**Exercice :**  
Sélectionner tous les étudiants ayant une note supérieure à 15.

**Tables :**  
- Étudiants(id, nom, prenom, note)

**Solution :**  
\[ \sigma_{note > 15}(Étudiants) \]

##### 3.1.2. Projection (π)
La projection est utilisée pour extraire des colonnes spécifiques d'une table, en supprimant les doublons.

**Syntaxe :**  
\[ \pi_{colonne1, colonne2, \ldots}(Relation) \]

**Exemple :**  
Projeter les colonnes nom et prénom de la table Employés.

\[ \pi_{nom, prenom}(Employés) \]

**Explication :**  
Cette opération crée une nouvelle relation contenant uniquement les colonnes "nom" et "prenom" de la table "Employés".

**Exercice :**  
Projeter les colonnes nom et date de naissance de la table Étudiants.

**Table :**  
- Étudiants(id, nom, prenom, date_naissance)

**Solution :**  
\[ \pi_{nom, date_naissance}(Étudiants) \]

##### 3.1.3. Jointure (⨝)
La jointure combine les lignes de deux relations basées sur une condition commune, permettant de relier des données provenant de plusieurs tables.

**Syntaxe :**  
\[ Relation1 \bowtie_{condition} Relation2 \]

**Exemple :**  
Joindre les tables Employés et Départements sur l'identifiant du département.

\[ Employés \bowtie_{Employés.id_dept = Départements.id} Départements \]

**Explication :**  
Cette opération combine les lignes de la table "Employés" avec celles de la table "Départements" où l'identifiant du département correspond.

**Exercice :**  
Joindre les tables Étudiants et Inscriptions sur l'identifiant de l'étudiant.

**Tables :**  
- Étudiants(id, nom, prenom)
- Inscriptions(id_etudiant, cours)

**Solution :**  
\[ Étudiants \bowtie_{Étudiants.id = Inscriptions.id_etudiant} Inscriptions \]

#### 3.2. Opérations avancées
En plus des opérations de base, l'algèbre relationnelle comprend des opérations avancées telles que l'union, l'intersection, la différence et la division, qui permettent des manipulations plus complexes des données.

##### 3.2.1. Union (∪)
L'union combine les lignes de deux relations similaires, éliminant les doublons.

**Syntaxe :**  
\[ Relation1 \cup Relation2 \]

**Exemple :**  
Combiner les tables Employés et Contractuels.

\[ Employés \cup Contractuels \]

**Explication :**  
Cette opération crée une nouvelle relation contenant toutes les lignes de "Employés" et "Contractuels", sans doublons.

**Exercice :**  
Combiner les tables Étudiants et Alumni.

**Tables :**  
- Étudiants(id, nom, prenom)
- Alumni(id, nom, prenom)

**Solution :**  
\[ Étudiants \cup Alumni \]

##### 3.2.2. Intersection (∩)
L'intersection extrait les lignes communes à deux relations similaires.

**Syntaxe :**  
\[ Relation1 \cap Relation2 \]

**Exemple :**  
Trouver les employés qui sont également des contractuels.

\[ Employés \cap Contractuels \]

**Explication :**  
Cette opération crée une nouvelle relation contenant uniquement les lignes présentes à la fois dans "Employés" et "Contractuels".

**Exercice :**  
Trouver les étudiants qui sont également des chercheurs.

**Tables :**  
- Étudiants(id, nom, prenom)
- Chercheurs(id, nom, prenom)

**Solution :**  
\[ Étudiants \cap Chercheurs \]

##### 3.2.3. Différence (-)
La différence extrait les lignes présentes dans la première relation mais pas dans la deuxième.

**Syntaxe :**  
\[ Relation1 - Relation2 \]

**Exemple :**  
Trouver les employés qui ne sont pas des contractuels.

\[ Employés - Contractuels \]

**Explication :**  
Cette opération crée une nouvelle relation contenant les lignes présentes dans "Employés" mais pas dans "Contractuels".

**Exercice :**  
Trouver les étudiants qui ne sont pas inscrits à un cours spécifique.

**Tables :**  
- Étudiants(id, nom, prenom)
- Inscriptions(id_etudiant, cours)

**Solution :**  
\[ Étudiants - \pi_{id}(Inscriptions) \]

##### 3.2.4. Division (÷)
La division est utilisée pour trouver les tuples d'une relation qui sont en relation avec tous les tuples d'une autre relation.

**Syntaxe :**  
\[ Relation1 \div Relation2 \]

**Exemple :**  
Trouver les employés qui connaissent toutes les technologies listées.

\[ Employés \div Technologies \]

**Explication :**  
Cette opération retourne les lignes de "Employés" qui sont en relation avec toutes les lignes de "Technologies".

**Exercice :**  
Trouver les étudiants qui ont suivi tous les cours requis.

**Tables :**  
- Étudiants(id, nom, prenom)
- CoursRequis(cours)
- Inscriptions(id_etudiant, cours)

**Solution :**  
\[ \pi_{id}(Inscriptions) \div CoursRequis \]

#### 3.3. Utilisation de l'algèbre relationnelle pour manipuler les données
L'algèbre relationnelle est fondamentale pour comprendre et manipuler les données dans les bases de données relationnelles. Elle sert de base théorique aux langages de requêtes tels que SQL.

**Exemple pratique 1 :**
Sélectionner les employés dont le département est "Informatique" et projeter les colonnes nom et salaire.

\[ \pi_{nom, salaire}(\sigma_{departement = 'Informatique'}(Employés)) \]

**Exemple pratique 2 :**
Trouver les départements qui n'ont pas d'employés.

\[ Départements - \pi_{id}(Employés) \]

### Exercices

#### Exercice 1:
Sélectionner tous les clients qui ont effectué un achat supérieur à 100 euros.

**Tables :**  
- Clients(id, nom, prenom)
- Achats(id, id_client, montant)

**Solution :**  
\[ \sigma_{montant > 100}(Achats) \]

#### Exercice 2:
Projeter les colonnes nom et date de naissance de la table Étudiants.

**Table :**  
- Étudiants(id, nom, prenom, date_naissance)

**Solution :**  
\[ \pi_{nom, date_naissance}(Étudiants) \]

#### Exercice 3:
Joindre les tables Étudiants et Inscriptions sur l'identifiant de l'étudiant.

**Tables :**  
- Étudiants(id, nom, prenom)
- Inscriptions(id_etudiant, cours)

**Solution :**  
\[ Étudiants \bowtie_{Étudiants.id = Inscriptions.id_etudiant} Inscriptions \]

#### Exercice 4:
Combiner les tables Clients et Fournisseurs pour obtenir une liste unique.

**Tables :**  
- Clients(id, nom, prenom)
- Fournisseurs(id, nom, prenom)

**Solution :**  
\[ Clients \cup Fournisseurs \]

#### Exercice 5:
Trouver les clients qui n'ont pas effectué d'achats.

**Tables :**  
- Clients(id, nom, prenom)
- Achats(id, id_client, montant)

**Solution :**  
\[ Clients - \pi_{id_client}(Achats) \]

### QCM

1. Quelle opération de l'algèbre relationnelle est utilisée pour filtrer les lignes d'une table selon une condition spécifique?
   a) Projection  
   b) Sélection  
   c) Jointure  
   d) Union  

2. Quelle opération de l'algèbre relationnelle extrait des colonnes spécifiques d'une table, éliminant les doublons?
   a) Sélection  
   b) Jointure  
   c) Projection  
   d) Différence  

3. Quelle opération combine les lignes de deux relations basées sur une condition commune?
   a) Union  
   b) Intersection  
   c) Différence  
   d) Jointure  

4. Quelle

 opération combine les lignes de deux relations similaires, éliminant les doublons?
   a) Union  
   b) Intersection  
   c) Différence  
   d) Division  

5. Quelle opération de l'algèbre relationnelle extrait les lignes communes à deux relations similaires?
   a) Différence  
   b) Union  
   c) Intersection  
   d) Division  

6. Quelle opération de l'algèbre relationnelle extrait les lignes présentes dans la première relation mais pas dans la deuxième?
   a) Différence  
   b) Union  
   c) Intersection  
   d) Division  

7. Quelle opération est utilisée pour trouver les tuples d'une relation qui sont en relation avec tous les tuples d'une autre relation?
   a) Différence  
   b) Union  
   c) Intersection  
   d) Division  

8. Quel est le résultat de l'opération suivante : \[ \pi_{nom, prenom}(\sigma_{age > 30}(Personnes)) \] ?
   a) Tous les noms et prénoms des personnes  
   b) Tous les noms et prénoms des personnes âgées de plus de 30 ans  
   c) Tous les âges des personnes de plus de 30 ans  
   d) Tous les noms des personnes âgées de plus de 30 ans  

9. Quelle opération retournerait les départements sans employés?
   a) Union  
   b) Différence  
   c) Jointure  
   d) Intersection  

10. Quelle opération est utilisée pour combiner les tables Étudiants et Inscriptions sur l'identifiant de l'étudiant?
    a) Sélection  
    b) Jointure  
    c) Projection  
    d) Différence