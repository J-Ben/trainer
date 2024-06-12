### TP 1 Enoncé 2 : Gestion de Transport Urbain - Tramway

#### Contexte

Vous êtes chargé de la conception d'un système de gestion pour une nouvelle voie de tramway dans le grand Libreville. Le projet comprend plusieurs aspects de la gestion des tramways, notamment les tramways eux-mêmes, les arrêts, les lignes de tramway, les conducteurs, les horaires, les tickets, et les passagers.

#### Règles de Gestion

1. Chaque tramway est assigné à une ligne de tramway spécifique, mais peut changer de ligne après des périodes d'entretien.
2. Chaque ligne de tramway a plusieurs arrêts et un arrêt peut appartenir à plusieurs lignes.
3. Les conducteurs peuvent conduire plusieurs tramways, mais un tramway ne peut être conduit que par un seul conducteur à la fois.
4. Les passagers achètent des tickets pour des trajets spécifiques qui incluent un point de départ et un point d'arrivée sur une ligne de tramway particulière.


#### QCM de Compréhension des Règles de Gestion

1. **Chaque tramway est assigné à :**
   a) Une seule ligne de tramway en permanence
   b) Une ligne de tramway spécifique mais peut changer après des périodes d'entretien
   c) Plusieurs lignes de tramway en même temps
   d) Aucun lien fixe

2. **Un arrêt de tramway peut :**
   a) Appartenir à une seule ligne
   b) Appartenir à plusieurs lignes
   c) Ne pas appartenir à une ligne
   d) Être réservé à des véhicules privés

3. **Un conducteur peut :**
   a) Conduire un seul tramway à la fois
   b) Conduire plusieurs tramways simultanément
   c) Conduire plusieurs tramways, mais un tramway ne peut être conduit que par un seul conducteur à la fois
   d) Ne pas conduire de tramways

4. **Les passagers achètent des tickets pour :**
   a) Des trajets spécifiques avec un point de départ et un point d'arrivée sur une ligne de tramway particulière
   b) Accéder à n'importe quel tramway sans spécifier de trajet
   c) Des abonnements mensuels uniquement
   d) Des trajets sans restriction de lignes

#### Travaux Demandés

1. **Modélisation Conceptuelle (MCD)**
   - Identifiez et créez les tables nécessaires pour modéliser ce système. Pensez aux entités principales découlant de l'enoncé.
   - Définissez les relations entre ces entités, en respectant les règles de gestion mentionnées.

2. **Modélisation Logique (MLD)**
   - Transformez votre MCD en MLD.
   - Ajoutez les clés primaires et étrangères nécessaires pour définir les relations entre les tables.

3. **Schéma des Relations**
   - Détaillez le schéma des relations entre les tables avec tous les champs requis. 
   - Assurez-vous que chaque table contient au moins 9 champs de types différents (string, integer, boolean, etc.).

4. **Algèbre Relationnelle**
   - Formulez au moins 5 requêtes en algèbre relationnelle par table. Utilisez un langage naturel pour les formuler.
 
### Exercice d'Algèbre Relationnelle

Formulez les requêtes suivantes en algèbre relationnelle pour chaque table mentionnée.

**Table Tramways**
1. On souhaite connaître tous les tramways en opération sur la ligne 1.
2. Affichez les tramways nécessitant un entretien dans le mois à venir.
3. Listez tous les tramways avec plus de 10 ans d'âge.
4. Affichez les tramways conduits par le conducteur 'John Doe'.
5. Listez les tramways qui ont été en service pendant les 5 dernières années sur plus de deux lignes différentes.

| TramwayID | LigneID | Modèle     | AnnéeFabrication | Capacité | DateEntretien | EnService | ConducteurID |
|-----------|---------|------------|------------------|----------|---------------|-----------|--------------|
| 1         | 1       | Alstom     | 2015             | 200      | 2024-07-01    | True      | 1            |
| 2         | 2       | Bombardier | 2016             | 150      | 2024-06-15    | True      | 2            |
| 3         | 3       | Siemens    | 2014             | 180      | 2024-08-10    | True      | 3            |
| 4         | 1       | Alstom     | 2017             | 200      | 2024-07-20    | True      | 4            |
| 5         | 2       | Bombardier | 2013             | 150      | 2024-09-01    | True      | 1            |
| 6         | 3       | Siemens    | 2012             | 180      | 2024-05-05    | False     | 2            |
| 7         | 1       | Alstom     | 2011             | 200      | 2024-06-25    | True      | 3            |
| 8         | 2       | Bombardier | 2015             | 150      | 2024-07-30    | True      | 4            |
| 9         | 3       | Siemens    | 2010             | 180      | 2024-08-15    | False     | 1            |
| 10        | 1       | Alstom     | 2018             | 200      | 2024-09-10    | True      | 2            |


**Table Lignes**
1. Affichez toutes les lignes qui ont au moins 10 arrêts.
2. On souhaite connaître la longueur totale des lignes en opération.
3. Affichez les lignes desservies par les tramways fabriqués après 2015.
4. Listez toutes les lignes qui passent par l'arrêt 'Central Station'.
5. Affichez les lignes qui ont une fréquence de passage de moins de 10 minutes aux heures de pointe.

| LigneID | NomLigne           | Longueur | Fréquence | DateOuverture | EnService | NumArrets |
|---------|---------------------|----------|-----------|---------------|-----------|-----------|
| 1       | Ligne Rouge         | 20       | 10        | 2015-01-01    | True      | 15        |
| 2       | Ligne Verte         | 25       | 15        | 2016-06-15    | True      | 20        |
| 3       | Ligne Bleue         | 30       | 12        | 2014-08-20    | True      | 18        |


**Table Arrêts**
1. Affichez tous les arrêts desservis par plus de 3 lignes différentes.
2. On souhaite connaître les arrêts les plus fréquentés aux heures de pointe.
3. Listez les arrêts situés dans le quartier 'Downtown'.
4. Affichez les arrêts qui ont été ajoutés dans les deux dernières années.
5. Listez les arrêts où le tramway n° 5 s'arrête.


| ArretID | NomArret           | Quartier       | LigneID | DateAjout  | Frequentation | EnService |
|---------|---------------------|----------------|---------|------------|---------------|-----------|
| 1       | Central Station     | Downtown       | 1       | 2015-01-01 | 1000          | True      |
| 2       | West End            | West           | 1       | 2015-01-01 | 800           | True      |
| 3       | East Park           | East           | 2       | 2016-06-15 | 600           | True      |
| 4       | North Gate          | North          | 3       | 2014-08-20 | 900           | True      |
| 5       | South Terminal      | South          | 1       | 2015-01-01 | 500           | True      |
| 6       | University Avenue   | University     | 2       | 2016-06-15 | 1200          | True      |
| 7       | Airport             | Airport        | 3       | 2014-08-20 | 1500          | True      |
| 8       | Central Plaza       | Downtown       | 1       | 2015-01-01 | 700           | True      |
| 9       | Parkside            | East           | 2       | 2016-06-15 | 400           | True      |
| 10      | Highland            | North          | 3       | 2014-08-20 | 300           | True      |


**Table Conducteurs**
1. Affichez les conducteurs qui conduisent plus de deux tramways différents.
2. On souhaite connaître les conducteurs avec plus de 10 ans d'expérience.
3. Listez les conducteurs qui ont travaillé sur la ligne 1 en janvier 2024.
4. Affichez les conducteurs dont le permis expire dans les 6 mois.
5. Listez les conducteurs qui ont conduit le tramway 'T123' au moins une fois.



| ConducteurID | Nom             | Prenom    | DateNaissance | Experience | PermisExpire | EnService |
|--------------|-----------------|-----------|---------------|------------|--------------|-----------|
| 1            | Doe             | John      | 1980-05-15    | 15         | 2024-12-31   | True      |
| 2            | Smith           | Jane      | 1985-11-20    | 10         | 2024-06-30   | True      |
| 3            | Brown           | Michael   | 1990-03-10    | 5          | 2024-09-15   | True      |
| 4            | Johnson         | Emily     | 1992-07-25    | 7          | 2024-11-01   | True      |
| 5            | Williams        | Robert    | 1988-02-05    | 12         | 2024-05-20   | True      |
| 6            | Miller          | Patricia  | 1979-08-30    | 20         | 2024-04-10   | True      |
| 7            | Davis           | James     | 1983-12-12    | 18         | 2024-07-25   | True      |
| 8            | Garcia          | Maria     | 1987-09-18    | 11         | 2024-08-05   | True      |
| 9            | Martinez        | David     | 1981-01-23    | 14         | 2024-10-30   | True      |
| 10           | Hernandez       | Linda     | 1995-06-27    | 3          | 2024-03-18   | True      |


**Table Tickets : A vous de donner un jeu de données.**
1. Affichez les tickets vendus pour le trajet entre 'Central Station' et 'West End'.
2. On souhaite connaître le nombre de tickets vendus par jour pour la ligne 2.
3. Listez tous les tickets achetés par le passager 'Alice Johnson'.
4. Affichez les tickets dont le tarif est supérieur à 10 unités.
5. Listez les tickets achetés dans les 24 heures précédant un jour férié.

**Table Passagers: Idem, donner un jeu de données, au moin 5 lignes comme le précédent**
1. Affichez les passagers qui ont acheté plus de 10 tickets le mois dernier.
2. On souhaite connaître les passagers qui utilisent régulièrement la ligne 3.
3. Listez les passagers qui ont des abonnements mensuels.
4. Affichez les passagers ayant des tickets pour des trajets sur plusieurs lignes.
5. Listez les passagers qui ont acheté des tickets pour le trajet 'Downtown' à 'Airport'.

Ce TP vous permettra de maîtriser la modélisation conceptuelle et logique, ainsi que l'algèbre relationnelle appliquée à un cas concret de gestion de transport urbain.

   
