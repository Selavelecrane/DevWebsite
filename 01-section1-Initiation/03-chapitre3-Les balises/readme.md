## 3. Le Dictionnaire des Balises HTML

Maintenant que le squelette est en place dans `<body>`, il faut le remplir ! En HTML, on utilise des **balises** pour indiquer le rôle de chaque élément.

La majorité des balises fonctionnent par paires : une **balise ouvrante** `<nom>` et une **balise fermante** `</nom>`. Tout ce qui se trouve entre les deux sera transformé par le navigateur.

### 1. Les Titres : `<h1>` à `<h6>`

Pour organiser ton texte, tu as accès à 6 niveaux de titres :

* `<h1>` : Le titre principal de la page (il ne doit y en avoir **qu'un seul** par page !).
* `<h2>` à `<h6>` : Les sous-titres, du plus important (`<h2>`) au plus petit (`<h6>`).

```html
<h1>Mon Pseudo de Gamer</h1>
<h2>Mes Statistiques</h2>
<h3>Saison 2026</h3>

```

### 2. Les Paragraphes : `<p>`

C'est la balise que tu utiliseras le plus souvent. Elle sert à écrire des phrases, des explications ou des histoires. Le navigateur ajoute automatiquement un petit espace au-dessus et en dessous de chaque paragraphe pour rendre le texte lisible.

```html
<p>Bienvenue sur ma toute première page web ! Je l'ai codée moi-même de A à Z.</p>

```

### 3. Les Boîtes : `<div>` et `<span>`

Ces deux balises ne changent rien au texte à elles seules : ce sont des **conteneurs neutres** qu'on utilise pour regrouper des éléments et les styliser plus tard en CSS.

* **`<div>` (Division) :** C'est un **gros carton**. Il prend toute la largeur de l'écran et saute automatiquement à la ligne. On l'utilise pour créer des blocs (des cartes, des sections, des grilles).
* **`<span>` (Étiquette) :** C'est une **petite étiquette**. Elle ne saute PAS à la ligne. On l'utilise pour isoler un ou deux mots au milieu d'une phrase afin de leur donner une couleur ou un style particulier (comme un badge de niveau).

```html
<div>
    <p>Joueur : CyberNinja <span class="badge">Niv. 42</span></p>
</div>

```

### 4. Les Listes : `<ul>`, `<ol>` et `<li>`

Pour afficher une liste d'éléments (des compétences, des jeux préférés, une recette) :

* **`<ul>` (Unordered List) :** Une liste à puces classiques (des puces rondes).
* **`<ol>` (Ordered List) :** Une liste numérotée (1, 2, 3...).
* **`<li>` (List Item) :** Chaque élément à l'intérieur de la liste.

```html
<h2>Mes 3 jeux préférés :</h2>
<ul>
    <li>Minecraft</li>
    <li>Zelda</li>
    <li>Rocket League</li>
</ul>

```

### 5. Les Liens : `<a>`

Pour envoyer le visiteur vers un autre site web, on utilise la balise `<a>` (pour "Ancre"). Elle a besoin d'un **attribut** appelé `href` qui contient l'adresse du site (URL).

```html
<a href="https://www.youtube.com">Visiter ma chaîne YouTube</a>

```

### 6. Les Images : `<img>`

La balise `<img>` est spéciale : **elle ne se ferme pas !** Elle n'a pas de `</img>`.
Elle utilise deux attributs obligatoires :

* `src` (Source) : Le lien ou le chemin vers la photo.
* `alt` (Texte alternatif) : Une description de la photo (très important si l'image ne charge pas ou pour les personnes malvoyantes).

```html
<img src="https://picsum.photos/300/200" alt="Avatar de mon personnage">

```

---

## 4. Pratique : Le Code de ton Premier Site (Version brute)

On va maintenant rassembler toutes ces balises à l'intérieur de ton fichier `index.html`.

Copie (ou mieux : retape) ce code complet à l'intérieur de ton fichier `index.html`.

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil de CyberNinja</title>
</head>
<body>

    <!-- Conteneur principal de la carte -->
    <div>
        
        <!-- Image de profil -->
        <img src="https://picsum.photos/400/250" alt="Avatar Gamer">

        <!-- Titre principal avec un badge -->
        <h1>CyberNinja <small>(Joueur Pro)</small></h1>
        
        <!-- Courte biographie -->
        <p>
            Bienvenue sur mon profil ! Passionné de jeux vidéo et de code CSS. 
            Mon objectif : créer le jeu vidéo du siècle.
        </p>

        <!-- Sous-titre -->
        <h2>Mes Jeux Favoris</h2>

        <!-- Liste des jeux -->
        <ul>
            <li>Minecraft</li>
            <li>Pokémon</li>
            <li>Fortnite</li>
        </ul>

        <!-- Un lien vers un site externe -->
        <p>
            Retrouve mes vidéos sur 
            <a href="https://www.youtube.com" target="_blank">ma chaîne YouTube</a>.
        </p>

    </div>

</body>
</html>

```

> **Observation avec Live Server :**
> Si tu regardes ton écran avec **Live Server**, tu vas voir ton contenu s'afficher.
> Pour l'instant, c'est **tout noir et blanc, plaqué à gauche, avec des puces noires**. C'est totalement normal ! C'est le comportement brut du HTML.
> Dans la partie suivante, on va ajouter notre fichier CSS pour transformer cette page brute en une vraie carte moderne stylisée !