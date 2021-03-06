
# Too Long; Didn’t read

Ces règles de conduite sont assez longues, par conséquent il est de bon ton d’avoir une version plus concise. Voici un résumé.

## Principes fondamentaux

* L’intérêt principal d’un guide de style est la cohérence. Il est normal de ne pas se trouver en accord avec l’intégralité de Sass Guidelines, du moment que la cohérence est maintenue. [↩](#pourquoi-un-guide-de-style)
* Il est important de garder le code Sass aussi simple qu’il puisse être et éviter de bâtir des systèmes complexes à moins d’y être contraint. [↩](#principes-fondamentaux)
* Gardez en tête que bien souvent *KISS* (Keep It Simple, Stupid) est préférable à *DRY* (Don’t Repeat Yourself). [↩](#principes-fondamentaux)

## Syntaxe & Formatage

* Indentation à 2 espaces, pas de tabulations. [↩](#syntaxe--formatage)
* La longueur des lignes doit être inférieure à 80 caractères autant que faire se peut. N’hésitez pas à diviser les lignes trop longues en plusieurs lignes plus courtes quand cela s’avère nécessaire. [↩](#syntaxe--formatage)
* Le code CSS doit être écrit de manière propre et évidente, si possible suivant les [CSS Guidelines](https://cssguidelin.es) de Harry Roberts. [↩](#syntaxe--formatage)
* Les lignes vides ne coûtent rien ; servez-vous en pour séparer les éléments, règles et déclarations. [↩](#syntaxe--formatage)

### Chaînes De Caractères

* Déclarer la directive `@charset` en haut de la feuille de styles est fortement encouragé. [↩](#encodage)
* À moins d’être utilisées comme identifiants CSS, les chaînes de caractères doivent être mises entre guillemets simples. De même pour les URLs. [↩](#chanes-comme-valeurs-css)

### Nombres

* Sass ne fait pas de distinction entre les nombres, les entiers, les flottants, par conséquent les zéros (0) inutiles après le point sont à éviter. En revanche, les zéros (0) avant le point dans le cas de nombres entre 0 et 1 sont à écrire dans un souci de lisibilité. [↩](#zros)
* Une longueur valant zéro (0) ne devrait pas avoir d’unité. [↩](#units)
* Les manipulations d’unités devraient être considérées comme des opérations mathématiques standards, pas comme des manipulations de chaînes de caractères. [↩](#units)
* Afin d’améliorer la lisibilité du code, les calculs doivent être encerclés de parenthèses. De plus, les opérations mathématiques complexes peuvent être éclatées en plusieurs morceaux. [↩](#calculs)
* Les nombres magiques sont problématiques pour la maintenance du code et doivent être évités coûte que coûte. Quand cela n’est pas possible, pensez à expliquer la valeur douteuse dans un commentaire. [↩](#nombres-magiques)

### Couleurs

* Les couleurs devraient être exprimées au format HSL si possible, puis RGB et enfin hexadécimal (bas-de-casse et forme raccourcie quand possible). Les mots clés sont à éviter. [↩](#formats-de-couleurs)
* Préférez `mix(..)` au lieu de `darken(..)` et `lighten(..)` pour éclaircir ou obscurcir une couleur. [↩](#claircir-et-obscurcir-les-couleurs)

### Listes

* À moins d’être utilisées comme associations directes avec des valeurs CSS utilisant des listes séparées par des espaces, les listes Sass doivent être séparées par des virgules. [↩](#listes)
* Entourer les listes avec des parenthèses doit être considéré pour faciliter la lecture. [↩](#listes)
* Les listes mises sur une ligne unique n’ont pas de virgule finale, mais les listes s’étendant sur plusieurs lignes en ont. [↩](#listes)

### Maps

* Les maps contenant au moins deux paires sont écrites sur plusieurs lignes. [↩](#maps)
* Pour faciliter la maintenance, la dernière paire d’une map doit avoir une virgule finale. [↩](#maps)
* Les clés d’une map qui se trouvent être des chaînes de caractères doivent être mises entre guillemets, comme toutes les autres chaînes. [↩](#maps)

### Ordre des déclarations

* Le système utilisé pour déterminer l’ordre des déclarations (alphabétique, par type, etc.) importe peu du moment qu’il est cohérent et utilisé partout. [↩](#ordre-des-dclarations)

### Imbrication des sélecteurs

* Évitez l’imbrication des sélecteurs quand elle n’est pas nécessaire (ce qui représente la majorité des cas). [↩](#imbrication-des-slecteurs)
* Utilisez l’imbrication des sélecteurs pour les pseudo-classes et les pseudo-éléments. [↩](#imbrication-des-slecteurs)
* Les media queries peuvent également être imbriquées dans le sélecteur auquel elles se rattachent. [↩](#imbrication-des-slecteurs)

## Conventions de nommage

* Il est préférable de s’en tenir aux conventions de nommage de CSS qui sont (à l’exception de quelques erreurs) bas-de-casse et séparation par un tiret [↩](#conventions-de-nommage)

## Commentaires

* CSS est un langage délicat ; n’hésitez pas à écrire des commentaires approfondis pour expliquer toute chose qui paraît douteuse. [↩](#crire-des-commentaires)
* Pour les variables, fonctions, mixins et placeholders constituant une API publique, utilisez les commentaires de SassDoc. [↩](#documentation)

## Variables

* Utilisez le flag `!default` pour toute variable faisant partie d’une API publique pouvant être changée sans crainte. [↩](#le-flag-default)
* N’utilisez pas le flag `!global` à la racine car il est possible que cela constitue une violation de la syntaxe Sass à l’avenir. [↩](#le-flag-global)

## Extend

* Contentez-vous d’étendre des placeholders et évitez d’étendre les sélecteurs CSS existants. [↩](#extend)
* Étendez un même placeholder aussi peu que possible afin d’éviter les effets de bord. [↩](#extend)
