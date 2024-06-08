# booki-starter-pack

## Repo Code Source

* [URL du Repo. du projet (code source)](https://github.com/gouttebroze/booki-starter-code/tree/master)
* [URL du projet Booki](https://gouttebroze.github.io/booki-starter-code/) en déploiement continu (GitHub pages)

## Spécifications fonctionnelles

### Fonction recherche

### Liens “Hébergements” et “Activités”

* Les textes **“Hébergements”** et **“Activités”**, situés dans l’en-tête, sont des **liens**. Ils doivent **mener** respectivement vers la section “**Hébergements à Marseille**” et “**Activités à Marseille**”.

### Cartes hébergements et activités

* Chaque carte d’hébergement ou d’activité devra être cliquable dans son intégralité (pas uniquement le titre).

  * **IMPORTANT** *Englober chaques cartes dans 1 balise ``<a>``*

* Pour l’instant, les **liens sont vides**. On peut **utiliser un attribut `href=”#”` pour simuler** la présence d’un lien.

## Spécifications techniques

### Maquettes

* Trois maquettes ont été réalisées : **desktop**, **tablette** et **mobile**.

### Breakpoints

* Nous avons convenu avec le designer UI d’utiliser **1024 px** et **768 px** :
  * **>1024 px** pour les écrans d’ordinateurs
  * **>=768** px pour les tablettes
  * et tout ce qui est **en dessous de 768** pour les téléphones portables.

### Largeur min - max

* Pour éviter d’étirer la page web sur la largeur de façon excessive, il va falloir déterminer une **largeur maximum de 1440 px**. Au-delà, une marge blanche doit apparaître sur les côtés et le contenu doit se limiter à **1440 px de large**.

* La **largeur minimum est fixée à 320 px**, en-deçà de cette largeur, le comportement n’est pas garanti.

### Bibliothèque d’icônes

* Les icônes proviennent de la [bibliothèque **Font Awesome**](https://docs.fontawesome.com/)

### Police

* La police du site est Raleway. Nous pouvons passer par [Google Fonts pour importer facilement cette police dans le code](https://fonts.google.com/specimen/Raleway).

### Balises sémantiques

* Il est important d’utiliser des **balises sémantiques**, au **minimum**:

  `header`
  `nav`
  `h1-h2-h3`
  `main`
  `section`
  `article`
  `footer`

### Validité du code

* Le **code HTML** à valider [ici](https://validator.w3.org/) sur ``W3C`` * **Validateurs code CSS**  ````````.

### Compatibilité navigateurs

* La maquette doit être compatible avec les dernières versions de **Google Chrome** et de **Mozilla Firefox**. Il faudra **tester** la page web sur **ces deux navigateurs**.

### Restrictions

* Aucun framework CSS &/ou autre langage ne doit être utilisé.
