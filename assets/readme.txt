Initialiser SASS (installer l'extension "live sass compiler")

-Créer un dossier assets à la racine du projet.
-créer un fichier index.scss.
-cliquer sur watch Sass en bas (afin d'initialiser la compilation).
(le fichiers index.css et index.css.map se génèrent automatiquement).
-créer des sous-dossiers dans le dossier "styles" afin de mieux segmenter les différents fichiers de style.
(exemples sous dossiers: components, layout, pages...)
-chaque fichiers de styles crées doivent débuter par "_" de façon à être ignorés lors de la compilation.
(exemple de fichiers: "_header.scss, _footer.scss, _navbar, _button.....")
-appeler le fichier index.css sur la page html (c'est celui-ci qui est utilisé pour lire le style une fois compilé)
-créer un fichier _setting.scss au même endroit que les index qui servira à stocker les réglages généraux 
(exemple: la police, les différentes variables....).
-le fichier "index.scss" est le fichier ou doit être importé tous les fichiers de styles créés
 et doivent être déclarés de la manière suivante (à faire à la création du fichier pour éviter oublie):
 @import "./settings";
 @import "./layout/navbar";
 @import  "./layout/header";
 @import "./layout/section1";
 @import "./layout/_footer.scss";


-création de variables:

"//Settings regroupe touys les réglages généraux.

@font-face {
    font-family: 'font1';
    src: url(../fonts/GochiHand-Regular.ttf);
}

$font1: 'font1', sans-serif;
$color1: rgb(164, 18, 43);
$color2: rgba(255, 166, 0, 0.548);
$color3: black;

//MIXINS

@mixin center {
    display: flex;
    justify-content: center;
    align-items: center;
}

body {
    background: $color2;
    
}
"

