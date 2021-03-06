# Projet de MiniT'Chat - II Le Retour

Le projet est une **application Web de T'Chat**, les groupes seront définis _aléatoirements_.
Ce dont vous avez besoin, c'est ce que vous avez déjà appris : `HTML`, `CSS`, `PHP`, `MySQL` et `JS` !

Vous utiliserez le framework [Material Design Light](https://getmdl.io/).
__Vous devez utiliser le fichier structure__ `index-skeleton.php` qui est disponible à la racine de ce dépôt, vous devez suivre le cahier des charges fonctionnel.

__Ce sujet est librement inspiré de [OpenClassrooms - TP : un mini-chat](https://openclassrooms.com/courses/concevez-votre-site-web-avec-php-et-mysql/tp-un-mini-chat) !__

## Cahier des charges fonctionnel (déjà rédigé)

* [Version française](https://docs.google.com/document/d/1AK9OQgLsr0Iv549YS3zUCoENvSVdm0H5RV2kMYpaeyc)
* [Version anglaise](https://docs.google.com/document/d/15xab7ijmKXCmGWooJcPr9Yp8X6TVPQ3CnYtqoKc297Q)

## Structure de la table MySQL

* `ID` (type `INT`) : il nous permettra de savoir dans quel ordre ont été postés les messages. Il faudra le mettre en `auto_increment` pour que les numéros s'écrivent tout seuls, et ne pas oublier de sélectionner "Primaire" (cela dit à MySQL que c'est le champ qui numérote les entrées);

* `pseudo` (type `VARCHAR`) : pensez à indiquer la taille maximale du champ (je vous conseille de mettre le maximum, "255");

* `message` (type `VARCHAR`) : de même, on indiquera une taille maximale de 255 caractères. Si vous pensez que vos messages seront plus longs, utilisez plutôt le type `TEXT`, beaucoup moins limité.

## Caractéristiques

C'est un t'chat, vous devez bien sûr laisser les gens discuter ensemble sur un canal global, __sans connexion avec mot de passe__, permettre aux utilisateurs de choisir un pseudo, les messages sont du texte brut.

## Bonus

### Niveau 1

* Retenir le pseudo. On doit actuellement saisir à nouveau son pseudo à chaque nouveau message. Comme vous le savez probablement, il est possible en HTML de pré-remplir un champ avec l'attribut `value`. Par exemple :

```php
<input type="text" name="pseudo" value="Alice" />
```

* Remplacez `Alice` par le pseudo du visiteur. Ce pseudo peut être issu d'un cookie par exemple : lorsqu'il poste un message, vous inscrivez son pseudo dans un cookie, ce qui vous permet ensuite de pré-remplir le champ.

### Niveau 2

* Le mini-chat ne s'actualise pas automatiquement s'il y a de nouveaux messages. En revanche, ce que vous pouvez facilement faire, c'est proposer un lien « Rafraîchir » qui charge à nouveau la page. Ainsi, s'il y a de nouveaux messages, ils apparaîtront après un clic sur le lien.

* Rafraichir automatiquement la page toute les 30 secondes à l'aide de __JavaScript__.

### Niveau 3

* N'afficher que les 10 derniers messages.

* Sauriez-vous trouver un moyen d'afficher les anciens messages ? Bien sûr, les afficher tous d'un coup sur la même page n'est pas une bonne idée. Vous pourriez imaginer un paramètre `$_GET['page']` qui permet de choisir le numéro de page des messages à afficher.

### Niveau 4

* Permettre aux utilisateurs d'utiliser des [Emojis](http://www.emoji-cheat-sheet.com/) ! Par exemple : `:smile_cat:` va être remplacé par `<img src="graphics/emojis/smile_cat.png"/>`.

* Permettre aux utilisateurs d'écrire en [Markdown](https://guides.github.com/features/mastering-markdown/) ! Par exemple :
```markdown
It's very easy to make some words **bold** and other words *italic* with Markdown.
You can even [link to Google!](http://google.com)
```
va être remplacé par
```html
It's very easy to make some words <strong>bold</strong> and other words <em>italic</em> with Markdown.
You can even <a href="http://google.com">link to Google!</a>
```

### Niveau 5

* Autoriser d'autres canaux comme des discussions privées.
