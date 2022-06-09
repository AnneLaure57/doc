```
Je vous retranscris une discussion que j’ai eu avec Guillaume à propos de la librairie Moment.js


À l’avenir, il est recommandé de **ne plus l’utiliser** dans les nouveaux projets pour les raisons suivantes :

- API mutable

- Prise en charge trop importante dans le cas d’un développement d’applications avec des fuseaux horaires ou l'internationalisation.

 

Il existe **des alternatives** :

 

* luxon (API immutable, plus évoluée que Moment.js) : [Luxon](https://moment.github.io/luxon/#/)
* day.js (similaire à Moment.js) : [Day.js](https://day.js.org/)
* date-fns (utilise l’objet Date du langage JS) : [date-fns](https://date-fns.org/)
* Intl : [Intl](https://blog.logrocket.com/4-alternatives-to-moment-js-for-internationalizing-dates/) qui est l’API ECMAScript pour les paramètres régionaux, les fuseaux horaires ou les deux.
 

Comparaison des différentes librairies :

* [Lien Github (avec tableau de comparaison, tips)](https://github.com/you-dont-need/You-Dont-Need-Momentjs/blob/master/README.md)
* [Article (avec schémas, explications etc)](https://inventi.studio/en/blog/why-you-shouldnt-use-moment-js)


Je vous donne mes sources :

* [Moment.js](https://momentjs.com/docs/)

* [4 Alternatives to Moment.js](https://blog.logrocket.com/4-alternatives-to-moment-js-for-internationalizing-dates/)

* [Autre](https://dockyard.com/blog/2020/02/14/you-probably-don-t-need-moment-js-anymore)

```
