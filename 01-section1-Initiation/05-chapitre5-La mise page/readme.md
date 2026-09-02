C'est parti pour le **Chapitre 2 : Les Moteurs de Mise en Page (Flexbox & CSS Grid)**.

C'est l'étape où le site web passe d'une simple colonne de texte à une véritable interface de jeu vidéo moderne. Préparez la suite de votre manuel de cours :

---

# CHAPITRE 2 : Les Moteurs de Mise en Page (Flexbox & CSS Grid)

Jusqu'à présent, nos éléments s'empilaient bêtement les uns sous les autres comme des briques de Lego fatiguées. Pour construire de vraies interfaces (des barres de navigation, des grilles de personnages, des tableaux de score), le CSS moderne met à notre disposition deux supers-pouvoirs : **Flexbox** et **CSS Grid**.

---

## 1. La grande règle d'or : "Le Chef d'Orchestre et les Musiciens"

Avant de coder, retiens bien ce principe magique :

* Pour activer Flexbox ou Grid, on ne touche **PAS** aux éléments qu'on veut bouger.
* On applique la règle **uniquement sur le conteneur (le parent)**.
* Le parent devient le *Chef d'orchestre*, et les enfants à l'intérieur deviennent les *Musiciens* qui obéissent aux règles.

---

## 2. Flexbox (`display: flex`) : Le spécialiste d'un seul axe

Flexbox est idéal pour aligner des éléments **sur une seule ligne** (ou une seule colonne) et gérer l'espace entre eux.

### Comment ça marche ?

Dès que tu écris `display: flex` sur un conteneur, tous les blocs à l'intérieur se mettent magiquement côte à côte.

### Les propriétés magiques du Chef d'orchestre :

1. **`gap: 15px;`** : C'est l'arme anti-galère. Il crée automatiquement un espace régulier entre tes éléments, sans avoir besoin de s'embêter avec des marges complexes.
2. **`justify-content: space-between;`** : Idéal pour les barres de menus. Il colle le premier enfant tout à gauche, le dernier tout à droite, et répartit l'espace vide au milieu.
3. **`align-items: center;`** : Aligne parfaitement tout le monde au milieu sur la hauteur (verticalement).

### Exemple concret : La barre de menu Gamer

```html
<nav class="menu">
    <div class="logo">🎮 GAMER ZONE</div>
    <div class="liens">
        <a href="#">Accueil</a>
        <a href="#">Profil</a>
    </div>
</nav>

```

```css
.menu {
    display: flex;
    justify-content: space-between; /* Pousse le logo à gauche et les liens à droite */
    align-items: center;            /* Centre verticalement */
    background-color: #1e293b;
    padding: 1rem 2rem;
    border-radius: 12px;
}

.liens {
    display: flex;                  /* On peut même imbriquer du Flex dans du Flex ! */
    gap: 20px;                      /* Espace entre les liens */
}

```

---

## 3. CSS Grid (`display: grid`) : Le spécialiste du tableau à 2 dimensions

Si Flexbox est une ligne, **Grid est un damier (lignes et colonnes)**. C'est l'outil parfait pour faire des galeries d'images, des inventaires de jeux ou des tableaux de statistiques.

### La propriété magique : `grid-template-columns`

Pour dire au navigateur *"Je veux 3 colonnes de taille égale"*, on utilise l'unité `fr` (fraction de l'espace disponible) :

```css
.grille-stats {
    display: grid;
    /* Crée 3 colonnes de tailles strictement égales */
    grid-template-columns: repeat(3, 1fr); 
    gap: 10px; /* L'espace entre les cases de la grille */
}

```

* Si tu veux 2 colonnes : `grid-template-columns: 1fr 1fr;` (ou `repeat(2, 1fr)`).
* Si tu veux que la première colonne soit deux fois plus grande que la deuxième : `grid-template-columns: 2fr 1fr;`.

---

## 4. Le Grand Projet : Transformer la Carte avec Grid et Flex

Reprenons notre carte de profil du Chapitre 1 et améliorons-la en y ajoutant une belle ligne de statistiques en bas grâce à Grid et Flexbox !

### Le HTML mis à jour (Ajout de la section stats) :

```html
<div class="carte-profil">
    <img src="https://picsum.photos/400/250" alt="Avatar">
    
    <div class="carte-corps">
        <!-- En-tête aligné en Flexbox horizontal -->
        <div class="carte-header">
            <h1>CyberNinja</h1>
            <span class="badge">Niv. 42</span>
        </div>

        <p>Expert en infiltration numérique et en CSS.</p>

        <!-- Grille de statistiques en CSS Grid -->
        <div class="stats-grille">
            <div class="stat-box">
                <span>Attaque</span>
                <strong>95</strong>
            </div>
            <div class="stat-box">
                <span>Défense</span>
                <strong>80</strong>
            </div>
            <div class="stat-box">
                <span>Vitesse</span>
                <strong>110</strong>
            </div>
        </div>
    </div>
</div>

```

### Le CSS complet et commenté :

```css
body {
    background-color: #0f172a;
    color: #f8fafc;
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.carte-profil {
    background-color: #1e293b;
    width: 350px;
    border-radius: 16px;
    overflow: hidden; /* Empêche l'image de dépasser des coins arrondis */
    border: 2px solid #38bdf8;
}

.carte-profil img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    display: block; /* Supprime le bug des 4px sous l'image */
}

/* Le corps de la carte utilise Flexbox en mode colonne */
.carte-corps {
    padding: 1.5rem;
    display: flex;
    flex-direction: column; /* Empile les éléments du haut vers le bas */
    gap: 1rem;              /* Espacement automatique entre chaque bloc */
}

/* L'en-tête utilise Flexbox en mode ligne */
.carte-header {
    display: flex;
    justify-content: space-between; /* Titre à gauche, Badge à droite */
    align-items: center;            /* Centrage vertical */
}

.badge {
    background-color: #0284c7;
    padding: 0.2rem 0.6rem;
    border-radius: 20px;
    font-size: 0.75rem;
    font-weight: bold;
}

/* La Grille de statistiques (CSS Grid) */
.stats-grille {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 colonnes égales */
    gap: 0.5rem;                           /* Espacement de 8px */
}

.stat-box {
    background-color: #0f172a;
    padding: 0.5rem;
    border-radius: 8px;
    text-align: center;
    border: 1px solid #334155;
}

/* On utilise des sélecteurs imbriqués pour styliser l'intérieur des stats */
.stat-box span {
    display: block;
    font-size: 0.7rem;
    color: #64748b;
    text-transform: uppercase;
}

.stat-box strong {
    font-size: 1.1rem;
    color: #38bdf8;
}

```

---

## 🎯 Le Défi Final du Cours : Le Bouton "Action"

**Consigne pour l'élève :**
Ajoute un bouton "Sélectionner ce Héros" tout en bas de la carte (après la grille de stats).

1. Le bouton doit prendre toute la largeur.
2. Il doit avoir un fond vert (`#10b981`), des coins arrondis et pas de bordure.
3. **Bonus magique :** Fais en sorte que la couleur du bouton change pour un vert plus foncé (`#059669`) quand la souris passe dessus (`:hover`).