# eikon parcel starter

## Prérequis

- Git installé
- NPM installé

## Installation

Cloner le repository git

```
git clone git@github.com:eikon-frontend/starterkit.git <nom du projet>
```

Se rendre dans le dossier du projet, puis installer les dépendances avec NPM

```
cd <nom-du-projet>
npm install
```

## Commandes

Compiler la SCSS, aggréger le JS, lancer le serveur et écouter les changements

```
npm run dev
```

Compiler pour la production

```
npm run build
```

## Utilisation

### HTML

Inclure un fichier _header.html_ depuis un fichier HTML

```html
<include src="components/header.html"></include>
```

### SCSS

Inclure un fichier _main.scss_ depuis un fichier HTML

```html
<link rel="stylesheet" href="scss/main.scss" />
```

Inclure un fichier _\_base.scss_ depuis un fichier SCSS

```scss
@import "base";
```

### JS

Inclure un fichier _main.js_ depuis un fichier HTML

```html
<script src="js/main.js" type="module"></script>
```

Inclure un fichier _carousel.js_ depuis un fichier JS

```js
import "./carousel.js";
```

## Exemples d'utilisation de packages externes

### [AOS](https://michalsnik.github.io/aos)

Installer le paquet avec NPM

```
npm install aos@next
```

Inclure le JS depuis un fichier JS

```js
import AOS from "aos";
```

Inclure la CSS depuis un fichier SCSS

```SCSS
@import "../../node_modules/aos/dist/aos.css";
```

### [Bootstrap](https://getbootstrap.com)

Installer le paquet avec NPM

```
npm install bootstrap
```

Inclure la SCSS depuis un fichier SCSS

```SCSS
@import "bootstrap/scss/bootstrap-grid";
```

### [Flickity](https://flickity.metafizzy.co)

Installer le paquet avec NPM

```
npm install flickity
```

Inclure le JS depuis un fichier JS

```js
import Flickity from "flickity";
```

Inclure la CSS depuis un fichier SCSS

```SCSS
@import "../../node_modules/flickity/dist/flickity.css";
```

### [Font Awesome](https://fontawesome.com/)

Installer le paquet avec NPM

```
npm install @fortawesome/fontawesome-free
```

Inclure le JS depuis un fichier JS

```js
import "@fortawesome/fontawesome-free/js/all.js";
```

### [GSAP](https://greensock.com/gsap/)

Installer le paquet avec NPM

```
npm install gsap
```

Inclure le JS depuis un fichier JS

```js
import gsap from "gsap";
```

Inclure les éventuels plugins

```js
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
```

### [Masonry](https://masonry.desandro.com)

Installer le paquet avec NPM

```
npm install masonry-layout
```

Inclure le JS depuis un fichier JS

```js
import Masonry from "masonry-layout";
```

### [ScrollMagic](https://scrollmagic.io)

Installer le paquet avec NPM

```
npm install scrollmagic
```

Inclure le JS depuis un fichier JS

```js
import ScrollMagic from "scrollmagic";
```

### [Swiper](https://swiperjs.com)

Installer le paquet avec NPM

```
npm install swiper@6
```

Inclure le JS depuis un fichier JS

```js
import Swiper from "swiper";
import { Navigation, Pagination } from "swiper/modules";

Swiper.use([Navigation, Pagination]);
```

Inclure la SCSS depuis un fichier SCSS

```SCSS
@import "swiper/swiper";
```

### [three.js](https://threejs.org)

Installer le paquet avec NPM

```
npm install three
```

Inclure le JS depuis un fichier JS

```js
import * as THREE from "three";
```

## Exemple

Un exemple avec l'installation des packages ci-desssus est disponible sur la branche _examples_

```
git checkout examples
```

---

## ✨ Série d'exercices CSS Grid

Ce repository inclut 5 pages HTML supplémentaires servant de support pédagogique progressif pour apprendre **CSS Grid**. Chaque exercice possède son propre fichier HTML et une feuille de styles dédiée contenant le code cible (solution) commenté. Tu peux fournir aux étudiant·e·s soit :

- la version avec uniquement la structure (en supprimant les blocs commentés),
- ou une version « guidée » en laissant quelques indices (TODO) dans le CSS.

### Liste des exercices

| #   | Fichier HTML                      | Thème              | Objectif principal                    | Concepts clés                                                                                    |
| --- | --------------------------------- | ------------------ | ------------------------------------- | ------------------------------------------------------------------------------------------------ |
| 1   | `exercice-1-recettes.html`        | Cuisine / Recettes | Placement basique dans une grille 3×2 | `display: grid`, `grid-template-columns/rows`, `grid-column`, `grid-row`, `span`, `gap`          |
| 2   | `exercice-2-portfolio.html`       | Portfolio d'agence | Nommer et structurer avec des zones   | `grid-template-areas`, `grid-area`, responsive simple                                            |
| 3   | `exercice-3-magazine-tech.html`   | Magazine tech      | Mélange d’unités et gestion de pistes | `px`, `%`, `fr`, `grid-auto-rows`, `gap`                                                         |
| 4   | `exercice-4-festival-cinema.html` | Festival de cinéma | Alignement & distribution des items   | `justify-items`, `align-items`, `justify-self`, `align-self`, `justify-content`, `align-content` |
| 5   | `exercice-5-concert.html`         | Salle de concert   | Grille fluide et adaptative           | `repeat()`, `auto-fill`, `auto-fit`, `minmax()`, `gap` fluide                                    |

### Détails rapides

#### Exercice 1 – Placement de base (Recettes)

Créer une grille 3 colonnes × 2 lignes, placer 6 cartes dont certaines fusionnent (span). Objectif : lire et manipuler les lignes numérotées.

#### Exercice 2 – Gabarit avec areas (Portfolio)

Définir un layout de page (header, nav, hero, sidebar, projets, footer) avec `grid-template-areas`. Ajouter une version mobile en une seule colonne.

#### Exercice 3 – Unités mixtes (Magazine Tech)

Composer des colonnes hétérogènes : fixe, pourcentage, unités fractionnaires. Ajuster les lignes et utiliser `grid-auto-rows` pour les suivantes.

#### Exercice 4 – Alignements (Festival)

Comparer l'effet des propriétés d’alignement au niveau conteneur et au niveau item. Tester plusieurs combinaisons et documenter les différences.

#### Exercice 5 – Grille fluide (Concert)

Passer d’une grille fixe à une grille responsive centrée sur `repeat(auto-fill|auto-fit, minmax())`. Observer la différence entre auto-fill et auto-fit lors du redimensionnement.

### Organisation des fichiers

Les feuilles de styles associées :

```
src/css/ex1.css
src/css/ex2.css
src/css/ex3.css
src/css/ex4.css
src/css/ex5.css
```

Chaque fichier contient un bloc de règles « solution » commenté. Exemple (extrait) :

```css
/* Placement cible (à retirer pour la version élève) */
/*
#carte-1 { grid-column: 1 / span 2; }
*/
```

### Préparer une version « élève »

1. Dupliquer le projet ou créer une branche `eleves`.
2. Dans chaque `exN.css`, supprimer (ou laisser partiellement) les blocs commentés de solution.
3. Ajouter éventuellement des commentaires TODO :
   ```css
   /* TODO: activer display:grid et définir 3 colonnes égales */
   ```
4. Vérifier que les pages restent lisibles sans la grille (contenu accessible empilé).
5. Option : fournir un PDF ou un énoncé séparé listant les objectifs.

### Lancement local des exercices

Parcel génère par défaut un serveur autour de `src/index.html`. Pour tester un exercice précis, ouvre l’URL correspondante manuellement (exemple) :

```
http://localhost:1234/exercice-1-recettes.html
http://localhost:1234/exercice-2-portfolio.html
...
```

Astuce : ajouter un mini index de navigation si besoin dans `index.html` (liens vers les 5 pages).

### Idées d'évaluation / prolongements

- Variante subgrid (si support navigateur : Firefox, Safari récent).
- Ajouter un mode sombre : variables CSS + `prefers-color-scheme`.
- Mesurer l’impact de `auto-fill` vs `auto-fit` avec des captures et un court commentaire.
- Transformer l’exercice 5 en galerie d’images, ajouter un `:hover` interactif.
- Ajouter un test d’accessibilité (tab order, focus visible, contrastes).
- Introduire `clamp()` pour gérer des largeurs maximales/minimales.
- Défi chrono : reproduire la grille d’un site réel choisi par l’étudiant·e.

### Grille de compétences (suggestion)

| Niveau        | Indicateurs                                                                             |
| ------------- | --------------------------------------------------------------------------------------- |
| Débutant      | Sait activer `display: grid`, définir colonnes/lignes simples                           |
| Intermédiaire | Utilise `areas`, mixe unités, maîtrise `gap` et fusion de cellules                      |
| Avancé        | Ajuste alignements fins, comprend distribution de l’espace, structure responsive fluide |
| Expert        | Combine `auto-fit/fill`, `minmax`, optimise lisibilité & accessibilité, documente choix |

### Astuces pédagogiques

- Encourager la verbalisation : « pourquoi cette unité plutôt qu’une autre ? »
- Faire comparer deux approches (areas vs placement explicite) pour un même layout.
- Introduire tôt la notion de « pistes implicites » (implicit tracks) en forçant un élément en dehors des lignes définies.
- Demander une fiche récap personnelle des propriétés après le dernier exercice.

---

Si tu souhaites ajouter un script pour générer automatiquement la version élève (suppression des blocs commentés), on peut l’automatiser (ex: petit script Node parcourant `src/css`). N’hésite pas à le demander.
