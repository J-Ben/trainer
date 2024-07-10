```markdown
# Programme du Cours de Programmation Web 
## Licence 2

Par M. Ben-Jamin MAMFOUMBI

## Séance 1 : Introduction à HTML
- Présentation du cours et des objectifs
- Notions de base en HTML
- Balises essentielles
- Structure d'un document HTML
- Exercices pratiques

## Séance 2 : HTML Intermédiaire
- Tables en HTML
- Formulaires en HTML
- Balises sémantiques (header, footer, section, article, etc.)
- Exercices pratiques

## Séance 3 : Introduction à CSS
- Notions de base en CSS
- Sélecteurs et propriétés CSS
- Mise en forme de texte
- Exercices pratiques

## Séance 4 : Mise en Page avec CSS
- Modèle de boîte (box model)
- Positionnement (static, relative, absolute, fixed)
- Flexbox
- Exercices pratiques

## Séance 5 : CSS Avancé et Media Queries
- CSS Grid
- Media Queries
- Réalisation d'une mise en page responsive
- Exercices pratiques

## Séance 6 : Introduction à JavaScript
- Concepts de base en JavaScript
- Variables, types de données, et opérateurs
- Fonctions et événements
- Exercices pratiques

## Séance 7 : Manipulation du DOM avec JavaScript
- Sélection et modification d'éléments
- Ajout et suppression d'éléments
- Gestion des événements
- Exercices pratiques

## Séance 8 : Interactions Utilisateur et Validation de Formulaires
- Validation de formulaires
- Interactions utilisateur
- Manipulation de classes CSS avec JavaScript
- Exercices pratiques

## Séance 9 : Projet de Gestion de Tramway - Partie 1
- Introduction au projet
- Création de la structure HTML
- Mise en place des styles de base avec CSS
- Exercices pratiques

## Séance 10 : Projet de Gestion de Tramway - Partie 2
- Ajout de fonctionnalités interactives avec JavaScript
- Intégration des formulaires et validation
- Finalisation du projet
- Exercices pratiques
```

## Séance 1 : Introduction à HTML

### Plan de la Séance
1. **Présentation du cours et des objectifs (15 minutes)**
2. **Notions de base en HTML (30 minutes)**
    - Structure d'un document HTML
    - Balises essentielles : titres, paragraphes, listes
3. **Exemples de code et explications (45 minutes)**
4. **Exercices pratiques (1h30)**
    - Créer une page HTML simple avec un titre et un paragraphe
    - Ajouter une liste à puces et une liste numérotée
    - Ajouter une image et un lien hypertexte
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!DOCTYPE html>
<html>
<head>
    <title>Ma Première Page HTML</title>
</head>
<body>
    <h1>Bienvenue sur ma page</h1>
    <p>Ceci est un paragraphe.</p>
    <ul>
        <li>Élément de liste 1</li>
        <li>Élément de liste 2</li>
        <li>Élément de liste 3</li>
    </ul>
    <ol>
        <li>Élément numéroté 1</li>
        <li>Élément numéroté 2</li>
        <li>Élément numéroté 3</li>
    </ol>
    <img src="image.jpg" alt="Une image">
    <a href="https://www.example.com">Lien vers un site</a>
</body>
</html>
```

### Exercices
1. Créer une page HTML simple avec un titre et un paragraphe.
2. Ajouter une liste à puces et une liste numérotée.
3. Ajouter une image et un lien hypertexte.

---

## Séance 2 : HTML Intermédiaire

### Plan de la Séance
1. **Tables en HTML (30 minutes)**
2. **Formulaires en HTML (45 minutes)**
3. **Balises sémantiques (header, footer, section, article, etc.) (45 minutes)**
4. **Exercices pratiques (1 heure)**
    - Créer un tableau pour afficher des données
    - Créer un formulaire d'inscription
    - Utiliser des balises sémantiques pour structurer une page
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Tableau HTML -->
<table border="1">
    <thead>
        <tr>
            <th>Nom</th>
            <th>Prénom</th>
            <th>Âge</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Doe</td>
            <td>John</td>
            <td>30</td>
        </tr>
        <tr>
            <td>Smith</td>
            <td>Jane</td>
            <td>25</td>
        </tr>
    </tbody>
</table>

<!-- Formulaire HTML -->
<form>
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom"><br><br>
    <label for="email">Email :</label>
    <input type="email" id="email" name="email"><br><br>
    <input type="submit" value="Soumettre">
</form>

<!-- Balises sémantiques -->
<header>
    <h1>Bienvenue sur ma page</h1>
</header>
<section>
    <h2>À propos</h2>
    <p>Voici une section avec du texte.</p>
</section>
<footer>
    <p>Contactez-nous à info@example.com</p>
</footer>
```

### Exercices
1. Créer un tableau pour afficher une liste de lignes de tramway.
2. Créer un formulaire d'inscription pour les conducteurs de tramway.
3. Utiliser les balises `<header>`, `<section>`, et `<footer>` pour structurer une page.

---

## Séance 3 : Introduction à CSS

### Plan de la Séance
1. **Notions de base en CSS (30 minutes)**
    - Qu'est-ce que le CSS ?
    - Ajouter du CSS à une page HTML
2. **Sélecteurs et propriétés CSS (45 minutes)**
    - Sélecteurs de type, classe, et ID
    - Propriétés CSS courantes
3. **Mise en forme de texte (45 minutes)**
    - Polices, tailles, couleurs
4. **Exercices pratiques (1 heure)**
    - Ajouter du style à une page HTML
    - Utiliser des sélecteurs et des propriétés CSS
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- CSS en ligne -->
<p style="color: red;">Ceci est un paragraphe rouge.</p>

<!-- CSS interne -->
<style>
    p {
        color: blue;
    }
</style>

<!-- CSS externe -->
<link rel="stylesheet" href="styles.css">
```

### Exercices
1. Ajouter du style à une page HTML en utilisant du CSS en ligne.
2. Utiliser des sélecteurs de type, classe, et ID pour appliquer des styles.
3. Modifier la police, la taille, et la couleur du texte.

---

## Séance 4 : Mise en Page avec CSS

### Plan de la Séance
1. **Modèle de boîte (box model) (30 minutes)**
2. **Positionnement (45 minutes)**
    - Positionnement static, relative, absolute, fixed
3. **Flexbox (45 minutes)**
    - Introduction à Flexbox
    - Alignement et disposition des éléments
4. **Exercices pratiques (1 heure)**
    - Utiliser le modèle de boîte pour créer des mises en page
    - Utiliser Flexbox pour aligner des éléments
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Modèle de boîte -->
<style>
    .box {
        width: 100px;
        height: 100px;
        padding: 10px;
        border: 5px solid black;
        margin: 20px;
    }
</style>

<!-- Flexbox -->
<style>
    .container {
        display: flex;
        justify-content: space-between;
    }
</style>
```

### Exercices
1. Utiliser le modèle de boîte pour créer une carte de profil.
2. Utiliser Flexbox pour créer une barre de navigation responsive.

---

## Séance 5 : CSS Avancé et Media Queries

### Plan de la Séance
1. **CSS Grid (45 minutes)**
    - Introduction à CSS Grid
    - Création de grilles
2. **Media Queries (45 minutes)**
    - Introduction aux media queries
    - Création de mises en page responsives
3. **Exercices pratiques (1h30)**
    - Créer une mise en page en utilisant CSS Grid
    - Utiliser des media queries pour rendre une page responsive
4. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- CSS Grid -->
<style>
    .grid-container {
        display: grid;
        grid-template-columns: auto auto auto;
    }
    .grid-item {
        border: 1px solid black;
        padding: 20px;
    }
</style>

<!-- Media Queries -->
<style>
    @media screen and (max-width: 600px) {
        .responsive {
            font-size: 14px;
        }
    }
</style>
```

### Exercices
1. Créer une grille pour organiser les horaires de tramway.
2. Utiliser des media queries pour rendre la grille responsive.

---

## Séance 6 : Introduction à JavaScript

### Plan de la Séance
1. **Concepts de base en JavaScript (30 minutes)**
    - Qu'est-ce que JavaScript ?
    - Ajouter du JavaScript à une page HTML
2. **Variables, types de données, et opérateurs (45 minutes)**
3. **Fonctions et événements (45 minutes)**
4. **Exercices pratiques (1 heure)**
    - Créer et utiliser des variables en JavaScript
    - Créer et appeler des fonctions
    - Réagir à des événements utilisateur
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- JavaScript en ligne -->
<script>
    alert("Bienvenue sur ma page !");
</script>

<!-- Variables et types de données -->
<script>
    let nom = "John";
    let age = 30;
    let estConducteur = true;
</script>

<!-- Fonctions et événements -->
<script>
    function saluer() {
        alert("Bonjour !");
    }
    document.getElementById("bouton").addEventListener("click", saluer);
</script>
```

### Exercices
1. Créer et afficher une alerte JavaScript.
2. Créer une fonction qui affiche une alerte.
3. Ajouter un bouton et réagir à son clic avec une alerte.

---

## Séance 7 : Manipulation du DOM avec JavaScript



### Plan de la Séance
1. **Sélection et modification d'éléments (45 minutes)**
2. **Ajout et suppression d'éléments (45 minutes)**
3. **Gestion des événements (45 minutes)**
4. **Exercices pratiques (1h30)**
    - Sélectionner et modifier des éléments du DOM
    - Ajouter et supprimer des éléments dynamiquement
    - Gérer des événements utilisateur
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Sélection et modification d'éléments -->
<script>
    document.getElementById("titre").textContent = "Nouveau Titre";
</script>

<!-- Ajout et suppression d'éléments -->
<script>
    let nouveauParagraphe = document.createElement("p");
    nouveauParagraphe.textContent = "Ceci est un nouveau paragraphe.";
    document.body.appendChild(nouveauParagraphe);
</script>

<!-- Gestion des événements -->
<script>
    document.getElementById("bouton").addEventListener("click", function() {
        alert("Bouton cliqué !");
    });
</script>
```

### Exercices
1. Sélectionner un élément et changer son texte.
2. Ajouter un nouveau paragraphe au document.
3. Réagir au clic d'un bouton en affichant une alerte.

---

## Séance 8 : Interactions Utilisateur et Validation de Formulaires

### Plan de la Séance
1. **Validation de formulaires (45 minutes)**
2. **Interactions utilisateur (45 minutes)**
3. **Manipulation de classes CSS avec JavaScript (45 minutes)**
4. **Exercices pratiques (1h30)**
    - Valider un formulaire en JavaScript
    - Créer des interactions utilisateur
    - Manipuler des classes CSS avec JavaScript
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Validation de formulaire -->
<script>
    function validerFormulaire() {
        let email = document.getElementById("email").value;
        if (email === "") {
            alert("Veuillez entrer un email.");
            return false;
        }
        return true;
    }
</script>

<!-- Manipulation de classes CSS -->
<script>
    document.getElementById("bouton").addEventListener("click", function() {
        document.getElementById("texte").classList.toggle("highlight");
    });
</script>
```

### Exercices
1. Valider un formulaire d'inscription.
2. Changer la couleur d'un élément au clic.
3. Ajouter une classe CSS à un élément lorsque l'utilisateur interagit avec.

---

## Séance 9 : Projet de Gestion de Tramway - Partie 1

### Plan de la Séance
1. **Introduction au projet (30 minutes)**
2. **Création de la structure HTML (45 minutes)**
3. **Mise en place des styles de base avec CSS (45 minutes)**
4. **Exercices pratiques (1h30)**
    - Créer la structure HTML pour le projet
    - Ajouter les styles de base avec CSS
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Structure de base du projet -->
<!DOCTYPE html>
<html>
<head>
    <title>Gestion de Tramway</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Gestion de Tramway</h1>
    </header>
    <section>
        <h2>Horaires des Tramways</h2>
        <table>
            <thead>
                <tr>
                    <th>Ligne</th>
                    <th>Départ</th>
                    <th>Arrêt</th>
                    <th>Heure</th>
                </tr>
            </thead>
            <tbody id="tableauHoraires">
                <tr>
                    <td>AKANDA</td>
                    <td>Libreville</td>
                    <td>Arrêt 1</td>
                    <td>08:00</td>
                </tr>
                <tr>
                    <td>OWENDO</td>
                    <td>Libreville</td>
                    <td>Arrêt 2</td>
                    <td>09:00</td>
                </tr>
            </tbody>
        </table>
    </section>
    <footer>
        <p>&copy; 2024 Compagnie de Tramway</p>
    </footer>
</body>
</html>
```

### Exercices
1. Créer la structure HTML pour afficher les horaires des tramways AKANDA, OWENDO et NKOK.
2. Ajouter des styles de base pour la page de gestion de tramway.

---

## Séance 10 : Projet de Gestion de Tramway - Partie 2

### Plan de la Séance
1. **Ajout de fonctionnalités interactives avec JavaScript (45 minutes)**
2. **Intégration des formulaires et validation (45 minutes)**
3. **Finalisation du projet (45 minutes)**
4. **Exercices pratiques (1h30)**
    - Ajouter des fonctionnalités interactives avec JavaScript
    - Intégrer et valider des formulaires
    - Finaliser le projet de gestion de tramway
5. **Discussion et révision (30 minutes)**

### Contenu Théorique

```html
<!-- Ajouter des fonctionnalités interactives -->
<script>
    function ajouterHoraire() {
        let ligne = document.getElementById("ligne").value;
        let depart = document.getElementById("depart").value;
        let arret = document.getElementById("arret").value;
        let heure = document.getElementById("heure").value;

        let nouvelleLigne = document.createElement("tr");
        nouvelleLigne.innerHTML = `<td>${ligne}</td><td>${depart}</td><td>${arret}</td><td>${heure}</td>`;
        document.getElementById("tableauHoraires").appendChild(nouvelleLigne);
    }

    document.getElementById("ajouterHoraire").addEventListener("click", ajouterHoraire);
</script>
```

### Exercices
1. Ajouter une fonctionnalité pour ajouter des horaires de tramway.
2. Intégrer et valider un formulaire d'ajout de conducteur.
3. Finaliser la mise en page et les fonctionnalités du projet.

