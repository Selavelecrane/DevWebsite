Voici **3 mini-projets bonus de niveau 2** conçus pour prolonger l'apprentissage de ton élève. Ils reprennent la carte Pokémon qu'il vient de faire et y ajoutent des interactions ou des structures un peu plus poussées, toujours sans JavaScript, en exploitant les super-pouvoirs du CSS moderne.

---

### Mini-Projet 1 : "Le Menu Popover Secret" (Le Dashboard du Joueur)

* **Objectif pédagogique :** Utiliser l'API native `popover` pour créer un menu d'options qui s'ouvre au clic sans une seule ligne de JavaScript.
* **Le défi pour l'élève :**
1. Ajouter un bouton "⚙️ Options" en haut à droite de la carte.
2. Créer un petit menu déroulant caché par défaut.
3. Relier le bouton au menu grâce aux attributs magiques `popovertarget="id-du-menu"` et `popover` sur le menu.


* **Le code à lui faire écrire :**
```html
<!-- Dans l'en-tête de la carte -->
<button popovertarget="menu-options" class="btn-gear">⚙️</button>

<div id="menu-options" popover class="dropdown-menu">
    <a href="#">Modifier le profil</a>
    <a href="#">Changer de skin</a>
    <hr>
    <a href="#" class="danger">Supprimer</a>
</div>

```


```css
.btn-gear {
    background: none;
    border: none;
    cursor: pointer;
    font-size: 1.2rem;
}
.dropdown-menu {
    background: #0f172a;
    border: 1px solid #334155;
    padding: 0.5rem;
    border-radius: 8px;
    color: white;
}

```


* **Pourquoi c'est top :** Il découvre que le navigateur gère tout seul l'ouverture, la fermeture quand on clique à côté (*light-dismiss*) et la touche Échap, comme un grand.



---

### Mini-Projet 2 : "La Galerie de l'Inventaire" (Le Multi-cartes en Grid)

* **Objectif pédagogique :** Passer d'une seule carte isolée à une véritable grille responsive multi-éléments grâce à Grid et `auto-fit` / `minmax`.
* **Le défi pour l'élève :**
1. Dupliquer la carte Pokémon 3 ou 4 fois pour avoir une équipe complète.
2. Créer un conteneur global `.team-grid` et appliquer une grille intelligente qui s'adapte toute seule si on redimensionne la fenêtre.


* **Le code à lui faire écrire :**
```css
.team-grid {
    display: grid;
    /* Magie du responsive moderne : crée des colonnes d'au moins 300px qui s'étirent si besoin */
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    padding: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

```


* **Pourquoi c'est top :** C'est la transition parfaite vers le Responsive Design sans s'embêter avec des media queries compliquées. La grille s'organise toute seule selon la taille de l'écran.



---

### Mini-Projet 3 : "La Carte Holographique" (Les Effets Hover 3D & Transitions)

* **Objectif pédagogique :** Découvrir les transitions douces et les transformations CSS (`transform`, `scale`, `box-shadow`) pour donner vie à l'interface.
* **Le défi pour l'élève :**
1. Faire en sorte que la carte entière réagisse quand la souris passe dessus.
2. Appliquer un léger zoom et accentuer l'ombre portée pour donner l'impression qu'elle se soulève de l'écran (effet carte à jouer physique).


* **Le code à lui faire écrire :**
```css
.carte-profil {
    /* On ajoute une transition fluide sur tous les mouvements */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.carte-profil:hover {
    /* La carte grossit de 3% et se soulève */
    transform: translateY(-8px) scale(1.02);
    /* L'ombre devient beaucoup plus grande et intense */
    box-shadow: 0 20px 35px rgba(56, 189, 248, 0.2);
}

```


* **Pourquoi c'est top :** Visuellement, c'est ultra gratifiant pour un ado. En changeant deux lignes, sa carte plate se transforme en un objet interactif digne d'un vrai jeu vidéo.