
# 📋 Fiche Mémo : HTML & CSS (Les Fondamentaux)

## 1. Les Balises HTML Indispensables

| Balise | Rôle / Description | Exemple |
| --- | --- | --- |
| `<!DOCTYPE html>` | Déclare le document en HTML5 moderne | `<!DOCTYPE html>` |
| `<html>` / `<body>` | Racine du site / Corps visible de la page | `<body> ... </body>` |
| `<head>` | Le cerveau (méta, titre, lien CSS) | `<title>Mon Site</title>` |
| `<h1>` à `<h6>` | Titres (H1 = le titre principal unique) | `<h1>CyberNinja</h1>` |
| `<p>` | Paragraphe de texte standard | `<p>Bonjour le monde</p>` |
| `<div>` | Boîte conteneur neutre (prend 100% de large) | `<div class="carte">...</div>` |
| `<span>` | Petite étiquette de texte (ne saute pas de ligne) | `<span>Niv. 42</span>` |
| `<ul>` / `<li>` | Liste à puces et ses éléments | `<ul><li>Item</li></ul>` |
| `<a>` | Lien hypertexte | `<a href="url">Lien</a>` |
| `<img>` | Image (pas de balise fermante) | `<img src="img.jpg" alt="desc">` |

---

## 2. Le Modèle de Boîte (*Box Model*) & Unités

| Propriété / Unité | Rôle / Effet | Exemple / Syntaxe |
| --- | --- | --- |
| `box-sizing` | Empêche le padding d'élargir la boîte | `box-sizing: border-box;` |
| `padding` | Coussin d'air interne (Sens des aiguilles : Haut/Droite/Bas/Gauche) | `padding: 1.5rem;` |
| `margin` | Espace externe (repousse les autres éléments) | `margin-top: 1rem;` |
| `border` | Contour de la boîte (`taille`, `style`, `couleur`) | `border: 2px solid #38bdf8;` |
| `border-radius` | Arrondit les coins | `border-radius: 12px;` |
| `rem` | Unité élastique ($1\text{rem} = 16\text{px}$ par défaut) | `font-size: 1.2rem;` |

---

## 3. Flexbox (L'alignement sur 1 axe)

> **Règle d'or :** Tout se pilote sur le **parent** (sauf `flex: 1` sur l'enfant).

| Propriété (Sur le Parent) | Rôle / Effet |
| --- | --- |
| `display: flex;` | Active Flexbox (met les enfants en ligne par défaut) |
| `flex-direction: column;` | Bascule les enfants à la verticale (du haut vers le bas) |
| `gap: [valeur];` | Crée un espace régulier entre les enfants |
| `justify-content: center;` | Centre les enfants horizontalement |
| `justify-content: space-between;` | Pousse le 1er à gauche, le dernier à droite |
| `align-items: center;` | Centre les enfants verticalement |
| **Propriété (Sur l'Enfant)** |  |
| `flex: 1;` | Force l'enfant à occuper une part égale de l'espace |

---

## 4. CSS Grid (Le damier à 2 dimensions)

> **Règle d'or :** Idéal pour structurer des colonnes et des lignes parfaites.

| Propriété (Sur le Parent) | Rôle / Effet | Exemple |
| --- | --- | --- |
| `display: grid;` | Active la grille | `display: grid;` |
| `grid-template-columns` | Définit la taille et le nombre de colonnes | `grid-template-columns: repeat(3, 1fr);` *(3 colonnes égales)* |
| `gap: [valeur];` | Espace entre les cases de la grille | `gap: 10px;` |