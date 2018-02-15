## Introduction

> Les feuilles de style en cascade1, généralement appelées CSS de l'anglais Cascading Style Sheets, forment un langage informatique qui décrit la présentation des documents HTML et XML.
> Les standards définissant CSS sont publiés par le World Wide Web Consortium (W3C). Introduit au milieu des années 1990,
> CSS devient couramment utilisé dans la conception de sites web et bien pris en charge par les navigateurs web dans les années 2000. [^1]

Comme l'HTML nous a permis de structurer le texte présent dans votre page,
les CSS vont nous permettre de présenter ce contenu tant au niveau de l'esthétique que de son positionnement.

Les CSS attachés à une page ou plusieurs sont généralement appelés: {%em%}«les styles»{%endem%}.

Il y a plusieurs manières de mettre des styles dans un document HTML:

1. directement introduire le style dans la balise HTML (Feuille de style interne)
2. une feuille de style dans le body de la page HTML grâce à la balise `style` (Feuille de style interne)
3. une feuille de style séparée dans un fichier `*.css` (Feuille de style externe)

Nous concentrerons sur le troisième procédé car il nous permettra de réutiliser le style sur plusieurs pages et:

* D’éviter des duplications
* D’avoir un maintenance plus aisée
* D’utiliser le même contenu avec différents styles pour différents usages
* D’avoir des milliers de pages qui ont un aspect similaire.

Lorsqu’un visiteur affiche une page, son navigateur charge les informations de style en même temps que le contenu de la page.
Lorsqu’il imprime une page, vous fournissez des informations de style différentes qui rendent la page imprimée facile à lire.

Si vous cherchez un exemple sur Internet de balises HTML, vous en trouverez sûrement certaines qui comportent des éléments de style.

```html
Dans les anciennes versions d’html, vous pouviez faire ceci:

<H1 align="center"> How to Carve Wood </H1>
```

Ce ne sont pas des CSS à proprement parlé mais des attributs de cette balise qui permettent de lui rajouter un certain style.
Nous éviterons d’utiliser ce genre d’attributs car ils sont sur la voie de garage et ne permettent pas toute une série de choses listées plus haut.

## Que peut-on faire avec du css?

<p data-height="265" data-theme-id="0" data-slug-hash="JMxmgx" data-default-tab="css,result" data-user="borisrorsvort" data-embed-version="2" data-pen-title="Logo lacambre css" class="codepen">See the Pen <a href="https://codepen.io/borisrorsvort/pen/JMxmgx/">Logo lacambre css</a> by Rorsvort (<a href="https://codepen.io/borisrorsvort">@borisrorsvort</a>) on <a href="https://codepen.io">CodePen</a>.</p>

### Css zen garden

> En 2003, se lance CSS Zen Garden, un site de présentation des diverses possibilités CSS (Feuilles de style en cascade) qui s'offrent aux pages web.
> Les feuilles de styles sont proposées par des designers, puis sont appliquées sur le contenu du site.
> Ainsi on peut afficher la page d'une centaine de manières différentes.
> Le contenu de la page HTML reste quant à lui invariant. Le site est disponible dans de nombreuses langues.
> Lorsqu’il a été lancé en avril 2003, il ne contenait que cinq designs. [^2]

http://www.csszengarden.com/

D’autres exemples de ce que l’on peut réaliser avec des css:

* http://designm.ag/graphic-design/50-css-only-icon-graphics/
* https://picturepan2.github.io/devices.css/

## Comment cibler un élément?

![](../assets/images/css/class-id-attributes.png)

Nous avons à notre disposition deux attributs HTML qui nous permettent d'identifier une balise (ou plusieures) dans une règle css.

### L’attribut Id

il ne peut-être utilisé qu'une seule fois sur la page.  
Comme nous essayons de réutiliser différentes règles CSS sur plusieurs éléments, cet attribut ne nous est donc pas très utile.

### L’attribut class

Nous pouvons via cet attribut associer des règles CSS a une balise en ajoutant le nom de ces règles dans la valeur de l'attribut, séparé par une espace

```html
<p class="super cool nice">Hello</p>
```

et le css

```css
.super {
}

.cool {
}

.nice {
}
```

{%em%}Retenez: les id, c’est comme highlander, il ne peut en rester qu’un. Les classes «C’est la class!» donc c’est pour le style.{%endem%}

Plus d’info sur les sélecteurs css [ici](https://developer.mozilla.org/fr/docs/Web/CSS/S%C3%A9lecteurs_CSS)

## Anatomie d’une règle css

![Anatomie d’une règle css](../assets/images/css/regle-css.png)

## Les propiétés

Voici une liste complètes de toutes les propriétés que vous pouvez utiliser pour modifier l’apparence d’une balise html:

[https://tympanus.net/codrops/css_reference/#section_css-property](https://tympanus.net/codrops/css_reference/#section_css-property)

## Les unités des valeurs

Pour spécifier les unités de CSS vous avez la possibilité entre plusieurs unité de mesure.

| Unité | Description                                                                              |
| ----- | ---------------------------------------------------------------------------------------- |
| em    | Relative par rapport à la taille de police de l’élement courant                          |
| rem   | Relative par rapport à la taille de police du document                                   |
| vw    | Relative par rapport à la largeur de la fenêtre. 10vh == 10% de la largeur de la fenêtre |
| vh    | Relative par rapport à la hauteur de la fenêtre. 10vh == 10% de la hauteur de la fenêtre |
| %     | Pourcentage par rapport au conteneur                                                     |

## La cascade et héritage

<p data-height="265" data-theme-id="0" data-slug-hash="VygVXa" data-default-tab="css,result" data-user="borisrorsvort" data-embed-version="2" data-pen-title="Cascade & héritage" class="codepen">See the Pen <a href="https://codepen.io/borisrorsvort/pen/VygVXa/">Cascade & héritage</a> by Rorsvort (<a href="https://codepen.io/borisrorsvort">@borisrorsvort</a>) on <a href="https://codepen.io">CodePen</a>.</p>

Le style final d'un élément peut être spécifié à de nombreux endroits, qui peuvent interagir de manière complexe.
C’est ce qui rend CSS puissant, mais peut aussi le rendre déroutant et difficile à débuguer.

Trois sources principales d'information de styles forment une cascade.

Celles-ci sont:

* Le style par défaut du navigateur pour le langage de balisage
* Le style spécifié par l'utilisateur lisant le document
* Le style lié au document par son auteur

## Le positionnement

Tutoriel complet [http://fr.learnlayout.com/](http://fr.learnlayout.com/)

![Illustration du «Box model»](https://mdn.mozillademos.org/files/8685/boxmodel-3)

Pour plus d’info sur le «Box model» rendez-vous sur [Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model).

<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

---

[^1]: https://fr.wikipedia.org/wiki/Feuilles_de_style_en_cascade
[^2]: https://fr.wikipedia.org/wiki/CSS_Zen_Garden