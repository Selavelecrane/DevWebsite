## 5. Habiller le Site avec CSS : Couleurs et Polices

Ton squelette HTML est prêt, il est temps de lui donner des couleurs et du style. Pour cela, nous allons utiliser le fichier `style.css` que tu as créé au tout début.

### 1. Brancher le fichier CSS au HTML

Si tu écris du CSS maintenant, le navigateur ne le saura pas. Il faut "brancher" ton fichier CSS dans le "cerveau" de ta page HTML (la balise `<head>`).

Ajoute cette ligne juste en dessous de ta balise `<title>` dans `index.html` :

```html
<link rel="stylesheet" href="style.css">

```

* `rel="stylesheet"` : Indique qu'il s'agit d'une feuille de style.
* `href="style.css"` : Indique le nom exact du fichier à charger.

### 2. La Syntaxe du CSS (Comment donner un ordre)

En CSS, on n'utilise plus les chevrons `< >` mais des accolades `{ }`. L'écriture fonctionne toujours en 3 étapes :

1. **Le Sélecteur :** "Qui je veux modifier ?" (ex: `body`, `h1`, `p`).
2. **La Propriété :** "Qu'est-ce que je veux changer ?" (ex: la couleur, la taille).
3. **La Valeur :** "Quel est le nouveau réglage ?" (ex: rouge, 20px).

```css
sélecteur {
    propriété: valeur;
}

```

### 3. Le fond et la police globale (`body`)

Ouvre ton fichier `style.css`. Nous allons d'abord changer l'allure générale de toute la page en ciblant la grande boîte `body`.

```css
body {
    background-color: #0f172a; /* Un fond bleu nuit très sombre */
    color: #f8fafc;            /* Le texte par défaut en blanc cassé */
    font-family: Arial, sans-serif; /* Une police moderne sans empattements */
}

```

> **Astuce du prof : Les codes couleurs Hexadécimaux**
> En web, on n'écrit pas juste "blue" ou "red". On utilise des codes précis à 6 lettres/chiffres précédés d'un hashtag (comme `#0f172a`). Dans VS Code, si tu survoles le code couleur avec ta souris, une palette s'affiche pour te laisser choisir la nuance exacte !

### 4. Le Modèle de Boîte (Rappel des métaphores)

Pour transformer notre `<div>` en une jolie carte, il faut utiliser le modèle de boîte :

* **`padding` (Le coussin d'air) :** L'espace *à l'intérieur* de la boîte pour que le texte ne colle pas aux bords. On utilise l'unité élastique `rem` (`1.5rem` = environ 24 pixels).
* **`border-radius` :** Pour arrondir les angles tranchants des boîtes.
* **`border` (La commande Fast-Food) :** L'épaisseur, le style, la couleur (`2px solid blue`).

---

## 6. Le Grand Assemblage et Test

C'est le moment de vérité ! Nous allons transformer ta liste brute en une véritable "Carte de Profil" centrée au milieu de l'écran.

### Étape 1 : Ajoute une "classe" dans ton HTML

Pour dire au CSS de cibler *cette* `<div>` en particulier et pas une autre, on lui donne un nom de classe. Modifie la balise `<div>` de ton `index.html` comme ceci :

```html
<div class="carte-profil">

```

### Étape 2 : Le code CSS final

Copie ce code complet dans ton fichier `style.css`. Lis bien les commentaires pour comprendre chaque ligne.

```css
/* 1. Style global de la page */
body {
    background-color: #0f172a; 
    color: #f8fafc;
    font-family: Arial, sans-serif;
    
    /* Les 3 lignes magiques pour centrer la carte au milieu de l'écran */
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

/* 2. La boîte de la carte */
.carte-profil {
    background-color: #1e293b; /* Un bleu légèrement plus clair que le fond */
    width: 350px;              /* Largeur fixe */
    padding: 2rem;             /* Le coussin d'air interne */
    border-radius: 16px;       /* Coins arrondis */
    border: 2px solid #38bdf8; /* Bordure cyan de 2px */
}

/* 3. L'image de profil */
.carte-profil img {
    width: 100%;               /* Prend toute la largeur de la carte */
    border-radius: 8px;        /* Coins arrondis pour l'image aussi */
}

/* 4. Les textes */
.carte-profil h1 {
    color: #38bdf8;            /* Titre en cyan brillant */
    margin-top: 1rem;
}

.carte-profil h2 {
    font-size: 1.1rem;
    margin-top: 1.5rem;
    color: #94a3b8;            /* Sous-titre en gris clair */
}

/* 5. Les liens */
.carte-profil a {
    color: #38bdf8;
    text-decoration: none;     /* Enlève le soulignement par défaut */
    font-weight: bold;
}

.carte-profil a:hover {
    color: #f8fafc;            /* Le lien devient blanc quand la souris passe dessus */
}

```

### Étape 3 : Admire le résultat

Sauvegarde tes deux fichiers (`Ctrl + S`). Si **Live Server** est toujours activé, regarde ton navigateur : tu viens de coder ta toute première interface moderne de A à Z !

Maintenant que nous avons validé ce manuel complet de la première leçon, voulez-vous que nous préparions le chapitre 2 axé exclusivement sur Flexbox et CSS Grid, ou préférez-vous aborder des concepts d'animation pour rendre la carte interactive ?