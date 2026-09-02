## 1. Les Fondations et l'Environnement

Avant d'écrire la moindre ligne de code, il faut comprendre ce que l'on manipule et préparer notre atelier de travail.

### Le duo HTML et CSS

Pour créer un site web, on utilise deux langages qui travaillent toujours en équipe :

* **HTML (HyperText Markup Language) :** C'est le **squelette** du site. Il dit au navigateur : *"Ceci est un titre, ceci est une image, ceci est un paragraphe"*. Sans lui, le site n'a pas de structure.
* **CSS (Cascading Style Sheets) :** C'est la **peinture et les vêtements**. Il dit au navigateur : *"Ce titre est bleu, cette image a des bords arrondis, ce texte est centré"*. Sans lui, le site ressemble à un document Word des années 90.

### Préparer l'atelier (VS Code)

Pour écrire notre code, on utilise un éditeur professionnel mais très simple : **Visual Studio Code (VS Code)**.

1. Crée un nouveau dossier sur le bureau de l'ordinateur et nomme-le `mon-premier-site`.
2. Ouvre ce dossier dans VS Code (Glisser-déposer le dossier dans la fenêtre de VS Code).
3. Crée deux fichiers vides à l'intérieur :
* `index.html` (La page principale de ton site).
* `style.css` (Le fichier qui contiendra toutes tes couleurs et tes styles).



> **Astuce du prof : Le pouvoir de "Live Server"**
> Normalement, à chaque fois qu'on modifie le code, il faut sauvegarder, aller sur le navigateur, et cliquer sur le bouton "Actualiser" (F5) pour voir le résultat. C'est long !
> Pour nous simplifier la vie, on va utiliser une extension VS Code appelée **Live Server**.
> * **Comment faire :** Va dans l'onglet Extensions de VS Code (les petits carrés à gauche), cherche "Live Server" et clique sur "Install".
> * **La magie :** En bas à droite de VS Code, clique sur **"Go Live"**. Ton site s'ouvre tout seul dans le navigateur. Dès que tu sauvegarderas ton code (Ctrl+S), la page se mettra à jour instantanément sous tes yeux !
> 
> 

---

## 2. La Structure de Base et la Magie du "!"

Le fichier `index.html` a besoin d'une structure de base obligatoire pour que le navigateur le comprenne. Autrefois, les développeurs devaient tout taper à la main. Aujourd'hui, on utilise un outil magique intégré à VS Code : **Emmet**.

### Générer le squelette instantanément

1. Ouvre ton fichier `index.html`.
2. Tape simplement le point d'exclamation **`!`** et appuie sur la touche **`Entrée`** (ou `Tab`).
3. Boum ! VS Code génère automatiquement tout le code de démarrage.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!--C'est ici qu'on écrit notre code-->
</body>
</html>

```

### Le décryptage ligne par ligne (Qu'est-ce qu'on vient d'écrire ?)

C'est très important de comprendre ce que ce texte barbare veut dire, car c'est la fondation de **tous** les sites du monde. Change le `lang="en"` en `lang="fr"` pendant qu'on lit la suite.

* **`<!DOCTYPE html>` :** C'est le signal d'alarme. On crie au navigateur : *"Attention, prépare-toi, on va parler le HTML5 moderne, pas une vieille version de 1999 !"*
* **`<html>` et `</html>` :** C'est la grande boîte qui contient absolument tout le site. Remarque bien : la majorité des balises s'ouvrent `<...>` et se ferment avec un slash `</...>`.
* **`<head>` :** C'est le **cerveau** de la page (les paramètres). Tout ce qui est écrit ici est **invisible** pour le visiteur, mais vital pour l'ordinateur.
* **`<meta charset="UTF-8">` :** C'est le dictionnaire du site. Ça dit au navigateur d'accepter tous les caractères spéciaux de la planète : les accents (é, à) et même les émojis 🚀 ! Sans ça, les accents se transforment en symboles bizarres.
* **`<meta name="viewport" content="width=device-width, initial-scale=1.0">` :** C'est la règle d'or du Web moderne. Ça ordonne au site de s'adapter automatiquement à la largeur de l'écran (smartphone, tablette, ou gros écran PC). Sans cette ligne, un site sur mobile serait affiché en miniature illisible.
* **`<title>Document</title>` :** C'est le nom qui s'affiche tout en haut de ton navigateur, sur l'onglet de la page. (Change "Document" par "Mon Super Site" !).


* **`<body>` :** C'est le **corps** visible du site. **Absolument tout** ce que le visiteur va voir à l'écran (les textes, les images, les boutons) devra être écrit à l'intérieur de cette boîte, entre `<body>` et `</body>`.