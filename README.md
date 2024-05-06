# booki-starter-pack

## Couleurs

* firstColor `#0065FC`;
* secondColor: `#DEEBFF`;
* thirdColor: `#D9D9D9`;
* fourthColor: `#F2F2F2`;

## Spécifications fonctionnelles

### Fonction recherche

* Les usagers pourront rechercher des hébergements dans la ville de leur choix.
* Le **champ de recherche** est un **champ de saisie**, le texte doit donc pouvoir être édité par l’utilisateur.
* Il faut **englober ce champ dans un formulaire**. La **partie Recherche ne doit pas être fonctionnelle** - il s’agit d’une **première version** pour valider l’interface.

### Liens “Hébergements” et “Activités”

* Les textes **“Hébergements”** et **“Activités”**, situés dans l’en-tête, sont des **liens**. Ils doivent **mener** respectivement vers la section “**Hébergements à Marseille**” et “**Activités à Marseille**”.

  * **IMPORTANT** *DONC POSER ANCRE (utiliser les id) pour faire liens du menu vers les sections plus bas*

### Cartes hébergements et activités

* Chaque carte d’hébergement ou d’activité devra être cliquable dans son intégralité (pas uniquement le titre).

  * **IMPORTANT** *Englober chaques cartes dans 1 balise ``<a>``*

* Pour l’instant, les **liens sont vides**. On peut **utiliser un attribut `href=”#”` pour simuler** la présence d’un lien.

### Filtres de recherche

* **Les hébergements peuvent être filtrés par thématique, comme le budget**

  * **??? QUOI ??? Pas compris ???**

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

### Desktop first

* Il faut d’abord réaliser l’intégration pour les ordinateurs (autrement dit, en **desktop first**), **puis** les tablettes et **enfin** les téléphones. L’utilisation des Media Queries nous permettra de réaliser l’intégration pour les différents supports.

### Bibliothèque d’icônes

* Les icônes proviennent de la bibliothèque **Font Awesome**.

### Couleurs

* Les couleurs de la charte sont le bleu (#0065FC), le bleu clair (#DEEBFF) et le gris pour le fond (#F2F2F2).

### Police

* La police du site est Raleway. Nous pouvons passer par [Google Fonts pour importer facilement cette police dans le code](https://fonts.google.com/specimen/Raleway).

### Mise en page

* Il est recommandé d'utiliser Flexbox.

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

* Le **code doit être** valide aux **validateurs** ``W3C`` ``HTML`` et ``CSS``.
* Le code ``HTML`` ne doit pas contenir de propriété ``CSS``.
* Lors du passage du desktop au mobile et à la tablette, **ne pas dupliquer le code** ``HTML`` *(exception faite dans le formulaire avec le mot “Rechercher” et l’icône de la loupe)*.
* Privilégier **l’utilisation des classes CSS** pour cibler un élément, **plutôt que d’utiliser le nom de l’élément** lui-même.
* Ne pas dupliquer des classes CSS inutilement. Exemple : *si 4 éléments sont identiques du point de vue de la mise en forme, alors utiliser une seule et même classe CSS, et non pas 4*.

### Compatibilité navigateurs

* La maquette doit être compatible avec les dernières versions de **Google Chrome** et de **Mozilla Firefox**. Il faudra **tester** la page web sur **ces deux navigateurs**.

### Restrictions

* Aucun framework CSS (type BootStrap ou Tailwind CSS) ou préprocesseur CSS (type Sass ou Less) ne doit être utilisé.
* Aucun autre langage ne doit être utilisé (comme JavaScript, par exemple).

## Notes

* code de l'[icon loupe](https://fontawesome.com/icons/magnifying-glass?f=classic&s=solid)

* des icones stylisés en CSS direectement ds le HTML, non conforme à la direction de la maquette, mais tel que fontawsome gère les changements de couleurs de ces icônes

```html
<!-- 1ère <section> du <main>-->
<section>
    <form>
        <i class="fa-solid fa-location-dot" style="color: #050505;"></i>
        <input type="text" placeholder="Marseille, France" />
        <button type="submit">Rechercher</button>
    </form>
</section>
<!-- 3ème <section> du <main> -->
<i class="fas fa-info fa-stack-1x" style="color: #0065FC;"></i>
```

## Todo

* voir à quoi correspond l'attribut `aria-hidden` dans les icônes, ds la base de code, on retrouve cet attribut avec une valeur `true` tel que `aria-hidden="true"`.

* placer des ancres sur les 2 liens de la section menu, rappel:

```html
<!-- la valeur de l'attribut "href" doit débuter par le caractère "#" suivi de la valeur de l'id inclus ds la balise ciblée par l'ancrage -->
<a href='#ancre'>Lien du menu de navigation</a>
<div id='ancre'>Cible à atteindre au click sur le lien du menu de navigation</div>
```

* ordre de balises `HTML`

```html
<!-- balise <a> et <h3> ds le bonne ordre? 
  je suppose que oui ...(le lien semble fonctionnel)-->
<a href="#"><h3></h3></a>
```

* concernant la description des images, faut-il faire 1 description + détaillée & + précise? par exemple, `alt='Image de la chambre d'hôtel montrant un lit'` pour une image où on voit 2 lit?

* ajuster les balises de textes h1, H2, h2, p ... pour être au plus proche de celle la maquette avec <font-size> <font-weight> ...

* propriété "webkit"? ....

* trouver les bonnes valeurs des propriétés "margin" qui séparent les différentes sections

* utiliser des unités pr tailles relatives

  * donner taille a un element par rapport a la taille de la fenetre (relatif par rapport à la fenetre et non au parent):
    * 100`vh` (viewport height) : 100% de la hauteur de l'espace visible
    * 100`vw` (viewport width) : 100% de la largeur de l'espace visible
  * `vmin`
  * `vmax`

  * unités de mesures liés à la police
    * `em` par rapport à la taille de la police de l'élément ou du parent,  (exemple:

      ```css
        html, body {
          
        }
        
        button {
          color: white;
          background-color: blue;
          text-decoration: none;
          font-size: 30px;
          padding: 0.4em 0.5em; 
          /* soit la moitié de la taille de la police, sur les côtés */
        }
      ```

    )

    * `rem` lié à la police définie ds la racine (`body` ou `html`),
    à utiliser pr fixer 1 valeur relative à la taille de la police générale (exemple:

      ```css
        html, body {
          font-size: 20px;
        }
        
        .card {
          padding: 1rem; /* 1 rem est alors égal à 20px */
        }
      ```

    )

## Sections à finir

* **header**: rapprocher ``<nav>`` du haut de page

* **section recherche**: voir différences avec maquette

* **section hebergements**: aligner titre + haut des cards avec titre et haut de la section **populaire**

* **section activités**: voir différences avec maquette

* **footer**: derniere colonne...

## QUESTIONS

* **section recherche**: pr les *bouttons icone*:
  * mettre une balise ``<p>`` ds la balise ``<button>`` ?
  * pr différencier partie **texte** de partie **icone** des bouttons...

## NOTES SPECIFICITE

* sélécteur universel (*) : 0
* element : 1
* classe, attributs, pseudo-classe: 10
* id: 100
* : 1000
* !important (suis valeur de propriété): 10 000

* VISUALISATION
  * id - classe - element
