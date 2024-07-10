```markdown
# Séance 1 : Introduction à HTML

## Objectifs de la Séance
1. Comprendre la structure de base d'un document HTML.
2. Apprendre et utiliser les balises HTML essentielles.
3. Créer des pages web simples avec des éléments de base.

## Plan de la Séance
1. **Présentation du cours et des objectifs (15 minutes)**
    - Introduction au cours de programmation web
    - Objectifs et structure des séances
    - Présentation des outils nécessaires (éditeur de texte, navigateur web)

2. **Notions de base en HTML (30 minutes)**
    - Qu'est-ce que HTML ?
    - Structure d'un document HTML : `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
    - Balises de base : `<h1>` à `<h6>`, `<p>`, `<ul>`, `<ol>`, `<li>`, `<a>`, `<img>`, `<table>`, `<tr>`, `<th>`, `<td>`, `<iframe>`, `<style>`, `<video>`

### Contenu Théorique

#### Structure de Base d'un Document HTML
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
</body>
</html>
```

#### Balises Essentielles

- **Titres et sous-titres**
    ```html
    <h1>Titre de niveau 1</h1>
    <h2>Titre de niveau 2</h2>
    <h3>Titre de niveau 3</h3>
    <h4>Titre de niveau 4</h4>
    <h5>Titre de niveau 5</h5>
    <h6>Titre de niveau 6</h6>
    ```

- **Paragraphes**
    ```html
    <p>Ceci est un paragraphe.</p>
    ```

- **Listes non ordonnées et ordonnées**
    ```html
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
    ```

- **Images**
    ```html
    <img src="chemin/vers/image.jpg" alt="Description de l'image">
    ```

- **Liens hypertexte**
    ```html
    <a href="https://www.example.com">Cliquez ici pour visiter Example.com</a>
    ```

- **Tableaux**
    ```html
    <table>
        <tr>
            <th>En-tête 1</th>
            <th>En-tête 2</th>
        </tr>
        <tr>
            <td>Donnée 1</td>
            <td>Donnée 2</td>
        </tr>
    </table>
    ```

- **Iframes**
    ```html
    <iframe src="https://www.example.com" width="300" height="200" title="Exemple"></iframe>
    ```

- **Styles**
    ```html
    <style>
        body {
            background-color: lightblue;
        }
        p {
            color: red;
        }
    </style>
    ```

- **Vidéos**
    ```html
    <video width="320" height="240" controls>
        <source src="chemin/vers/video.mp4" type="video/mp4">
        Votre navigateur ne supporte pas la balise vidéo.
    </video>
    ```

### Exercices Pratiques (1h30)

#### Exercice 1 : Créer une page HTML simple avec un titre et un paragraphe
**Objectif** : Créer une page basique contenant un titre et un paragraphe.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Ma Première Page HTML</title>
</head>
<body>
    <h1>Bienvenue sur ma première page HTML</h1>
    <p>Ceci est mon premier paragraphe en HTML.</p>
</body>
</html>
```

#### Exercice 2 : Ajouter une liste à puces et une liste numérotée
**Objectif** : Compléter la page précédente en ajoutant des listes non ordonnées et ordonnées.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Liste des tâches</title>
</head>
<body>
    <h1>Bienvenue sur ma première page HTML</h1>
    <p>Ceci est mon premier paragraphe en HTML.</p>
    
    <h2>Liste de courses</h2>
    <ul>
        <li>Pomme</li>
        <li>Banane</li>
        <li>Orange</li>
    </ul>
    
    <h2>Liste des tâches</h2>
    <ol>
        <li>Aller au marché</li>
        <li>Faire le ménage</li>
        <li>Lire un livre</li>
    </ol>
</body>
</html>
```

#### Exercice 3 : Ajouter une image et un lien hypertexte
**Objectif** : Enrichir la page avec une image et un lien hypertexte.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mon Profil</title>
</head>
<body>
    <h1>Bienvenue sur ma page de profil</h1>
    <p>Ceci est un court paragraphe de présentation.</p>
    
    <h2>Ma photo</h2>
    <img src="chemin/vers/image.jpg" alt="Photo de profil">
    
    <h2>Me contacter</h2>
    <p>Pour plus d'informations, <a href="mailto:monemail@example.com">envoyez-moi un email</a>.</p>
</body>
</html>
```

#### Exercice 4 : Créer une page avec plusieurs sections
**Objectif** : Créer une page contenant plusieurs sections avec des titres et des paragraphes.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mon Blog</title>
</head>
<body>
    <h1>Bienvenue sur mon blog</h1>
    
    <h2>Section 1</h2>
    <p>Contenu de la section 1.</p>
    
    <h2>Section 2</h2>
    <p>Contenu de la section 2.</p>
    
    <h2>Section 3</h2>
    <p>Contenu de la section 3.</p>
</body>
</html>
```

#### Exercice 5 : Utiliser des balises sémantiques
**Objectif** : Créer une page en utilisant des balises sémantiques comme `<header>`, `<footer>`, `<section>`, `<article>`.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Site Web Sémantique</title>
</head>
<body>
    <header>
        <h1>En-tête du Site</h1>
    </header>
    
    <section>
        <article>
            <h2>Article 1</h2>
            <p>Contenu de l'article 1.</p>
        </article>
        <article>
            <h2>Article 2</h2>
            <p>Contenu de l'article 2.</p>
        </article>
    </section>
    
    <footer>
        <p>Pied de page du site.</p>
    </footer>
</body>
</html>
```

#### Exercice 6 : Ajouter une vidéo et un style
**Objectif** : Enrichir la page avec une vidéo et ajouter des styles CSS.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Page avec Vidéo et Style</title>
    <style>
        body {
            background-color: lightblue;
        }
        p {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Bienvenue sur ma page vidéo</h1>
    <p>Ceci est un paragraphe avec du style.</p>
    
    <h2>Vidéo</h2>
    <video width="320" height="240" controls>
        <source src="chemin/vers/video.mp4" type="video/mp4">
        Votre navigateur ne supporte pas la balise vidéo.
    </video>
</body>
</html>
```

### Discussion et Révision (30 minutes)
- Révision des concepts abordés
- Questions et réponses
- Préparation pour la séance suivante

## Arborescence des fichiers
- `index

.html` : Page principale de démonstration
- `styles.css` : Fichier de styles CSS
- `images/` : Dossier contenant les images
- `videos/` : Dossier contenant les vidéos
- `pages/` : Dossier contenant les pages HTML supplémentaires

---

 