### TP 3 : Manipulation des Bases de Données avec SQL et l'Algèbre Relationnelle

**Responsable du TP :** [Ben-Jamin MK]

**Objectifs :**
- Comprendre les bases de la manipulation de bases de données avec SQL et l'algèbre relationnelle
- Pratiquer les bases de la manipulation de bases de données avec SQL et l'algèbre relationnelle    

#### Introduction
Ce TP est divisé en trois parties distinctes. Chaque partie représente un scénario pratique où vous devrez créer et manipuler des bases de données relationnelles. Vous utiliserez à la fois des opérations d'algèbre relationnelle et des requêtes SQL pour accomplir les tâches demandées. Chaque scénario représente 25% des opérations d'algèbre relationnelle, 65% des requêtes SQL et 10% des QCM sur la syntaxe SQL.

Pour chaque scénario, vous devrez :
1. Fournir le schéma des tables nécessaires et générer un jeu de données fictives pour chaque table (au moins 10 enregistrements par table).
2. Écrire et exécuter les requêtes d'algèbre relationnelle et SQL demandées.
3. Capturer les résultats des requêtes et fournir un fichier SQL contenant toutes les requêtes exécutées. Nb : vous pouvez utiliser un logiciel de gestion de base de données (par exemple, MySQL  XAMPP) pour exécuter les requêtes SQL. Les capture ne concernent qu'un enregistrement par requête d'insertion pour chacune des tables.
4. Répondre aux QCM.

Les manipulations seront effectuées sur XAMPP.

### Scénario 1 : Gestion d'une Bibliothèque

#### Schéma des tables à créer (suggestion, l'étudiant peut l'adapter) :
1. **Books** : BookID, Title, Author, Genre, PublishedYear, CopiesAvailable
2. **Members** : MemberID, FirstName, LastName, DateOfBirth, MembershipDate
3. **Borrowings** : BorrowingID, BookID, MemberID, BorrowDate, ReturnDate, IsReturned

#### Partie Algèbre Relationnelle (25%)
1. Listez les livres disponibles (CopiesAvailable > 0).
2. Trouvez les membres ayant emprunté plus de 5 livres.
3. Affichez les livres empruntés mais non retournés.

#### Partie SQL (65%)
1. Insérez au moins 10 enregistrements dans chaque table.
2. Sélectionnez tous les livres écrits par un auteur spécifique.
3. Mettez à jour le nombre de copies disponibles pour un livre après un emprunt.
4. Supprimez les membres qui n'ont jamais emprunté de livres.
5. Calculez le nombre total de livres empruntés par chaque membre.

#### QCM sur la syntaxe SQL (10%)
1. Quelle est la commande SQL pour ajouter une nouvelle colonne à une table ?
   - a) ADD COLUMN
   - b) ALTER TABLE ADD COLUMN
   - c) INSERT COLUMN
   - d) MODIFY TABLE ADD COLUMN

2. Quelle est la commande SQL pour créer une clé étrangère ?
   - a) FOREIGN KEY
   - b) ADD CONSTRAINT FOREIGN KEY
   - c) ALTER TABLE ADD CONSTRAINT FOREIGN KEY
   - d) None of the above

### Scénario 2 : Gestion des Commandes d'une Boutique en Ligne

#### Schéma des tables à créer (suggestion, l'étudiant peut l'adapter) :
1. **Products** : ProductID, Name, Category, Price, StockQuantity
2. **Customers** : CustomerID, FirstName, LastName, Email, RegistrationDate
3. **Orders** : OrderID, CustomerID, OrderDate, TotalAmount
4. **OrderDetails** : OrderDetailID, OrderID, ProductID, Quantity, SubTotal

#### Partie Algèbre Relationnelle (25%)
1. Listez les produits en rupture de stock.
2. Affichez les commandes passées par les clients depuis plus d'un an.
3. Trouvez les clients ayant dépensé plus de 1000€ en commandes.

#### Partie SQL (65%)
1. Insérez au moins 10 enregistrements dans chaque table.
2. Sélectionnez tous les produits d'une catégorie spécifique.
3. Mettez à jour le stock des produits après chaque commande.
4. Supprimez les commandes avec un montant total de 0€.
5. Calculez le total des ventes par produit.

#### QCM sur la syntaxe SQL (10%)
1. Quelle est la commande SQL pour renommer une table ?
   - a) RENAME TABLE
   - b) ALTER TABLE RENAME
   - c) RENAME TO
   - d) None of the above

2. Quelle est la commande SQL pour ajouter une contrainte unique à une colonne ?
   - a) ADD CONSTRAINT UNIQUE
   - b) ALTER TABLE ADD UNIQUE
   - c) ADD UNIQUE
   - d) None of the above

### Scénario 3 : Gestion des Transports Urbains

#### Schéma des tables à créer (suggestion, l'étudiant peut l'adapter) :
1. **Lines** : LineID, Name, Route, StartTime, EndTime, Frequency
2. **Drivers** : DriverID, FirstName, LastName, LicenseNumber, HireDate
3. **Buses** : BusID, LineID, Model, Capacity, ServiceDate, InService
4. **Trips** : TripID, BusID, DriverID, TripDate, PassengerCount

#### Partie Algèbre Relationnelle (25%)
1. Listez les lignes avec une fréquence supérieure à 15 minutes.
2. Affichez les chauffeurs ayant effectué plus de 5 trajets.
3. Trouvez les bus qui ne sont pas en service.

#### Partie SQL (65%)
1. Insérez au moins 10 enregistrements dans chaque table.
2. Sélectionnez tous les trajets effectués par un chauffeur spécifique.
3. Mettez à jour l'état de service d'un bus après un entretien.
4. Supprimez les lignes de bus sans trajets associés.
5. Calculez le nombre total de passagers transportés par ligne.

#### QCM sur la syntaxe SQL (10%)
1. Quelle est la commande SQL pour fusionner deux tables ?
   - a) JOIN TABLES
   - b) UNION TABLES
   - c) SELECT INTO
   - d) None of the above

2. Quelle est la commande SQL pour supprimer une colonne d'une table ?
   - a) DELETE COLUMN
   - b) REMOVE COLUMN
   - c) DROP COLUMN
   - d) None of the above

### Livrables
1. Schéma des tables (MCD et MLD) pour chaque scénario.
2. Jeu de données pour chaque table (au moins 10 enregistrements par table).
3. Requêtes d'algèbre relationnelle et résultats capturés.
4. Requêtes SQL et résultats capturés.
5. Fichier SQL contenant toutes les requêtes.
6. Réponses aux QCM.

### Instructions pour l'implémentation sur XAMPP
1. Installez XAMPP et démarrez le serveur MySQL.
2. Créez une base de données pour chaque scénario.
3. Créez les tables et insérez les données.
4. Exécutez les requêtes d'algèbre relationnelle et SQL.
5. Capturez les résultats des requêtes et compilez-les dans un rapport final.

---

Ce TP vous permettra de renforcer vos compétences en SQL et en algèbre relationnelle tout en vous offrant une expérience pratique dans la gestion de bases de données. Bonne concentration !