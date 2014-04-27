<img class="alignleft" alt="IntellijIDEA 13" src="http://blog.jetbrains.com/idea/files/2013/12/splash13-1.png" width="213" height="118" />Hadi HARIRI (@hhariri) de chez Jetbrains a présenté durant cette conférence quelques astuces pratiques de leur IDE phare Intellij IDEA, un IDE polyglotte payant mais qui est aussi proposé en édition communautaire.

Il commence la séance avec une petite touche d’humour comme quoi ceux qui sont sur Eclipse migreront sur Intellij Idea à la fin de la séance. Après quelques questions pour savoir qui sont sur Intelij ou sur Eclipse, il commence par présenter des raccourcis basiques.

Il en a présenté une centaine tout au long de la conférence. Cependant, je ne vais juste présenter que celles qui m'ont vraiment surpris et que je trouve vraiment utiles.

Un PDF contenant tous les raccourcis sera disponible à la fin de cet article.

Si vous êtes un early adopter de cet IDE ou si vous voulez vous y mettre,

Voici les raccourcis et les astuces qui changeront peut-être votre utilisation quotidienne d'Intellij IDEA.


## Des raccourcis pour naviguer plus facilement dans un projet

Lors de mon utilisation de cet IDE, il m'arrive souvent d'utiliser la souris pour aller dans le panneau contenant la structure du projet.
Eh bien maintenant, on peut utiliser le raccourci <strong><kbd>CTRL</kbd> + <kbd>1 </kbd></strong>.

Maintenant, si on veut configurer notre projet, il existe un raccourci <strong><kbd>ALT</kbd> + <kbd>F7</kbd></strong> pour afficher rapidement la fenêtre de paramétrage du projet.

Pour maximiser l'espace de travail et pour naviguer plus facilement à travers les différents packages de votre projet, plusieurs options s'offrent à nous :

 - On peut tout d'abord désactiver la barre de navigation celle qui se trouve en haut de la fenêtre.
     - Pour ce faire, il faut aller
     - On pourra toujours l'afficher à la demande en saisissant :

 - On peut aussi faire de la place dans l'éditeur en utilisant la fonctionnalité 'Blank Screen' avec la commande : <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>F12</kbd></strong>.

 Voici une liste succinte de commandes pour afficher d'autres fenêtre d'accès aux fichiers:

 - <strong><kbd>CTRL</kbd> + <kbd>E</kbd></strong> pour afficher la liste des fichiers récemment utilisés.


## Lorsqu'on est dans une classe

Voici les actions disponibles lorsque l'on se trouve dans une classe:

- La commande <strong><kbd>CTRL</kbd> + <kbd>F12</kbd></strong> affiche un Pop-up contenant la structure de la classe.

- Sur une méthode, on peut faire <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd></strong> pour voir son contenu.

- Dans une méthode, on peut 'highlight' les 'exists points' comme les _return_ ou les _throw_ à l'aide de <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>F7</kbd></strong>.

- <strong><kbd>CTRL</kbd> + <kbd>W</kbd></strong> pour sélectionner un mot ou un bloc entier.

    - Remaque: la fonction de refactoring est 'Context-aware' par conséquent, ce n'est pas nécessaire de tout séléectionner.

- <strong><kbd>CTRL</kbd> + <kbd>Y</kbd></strong> affiche la définition de la classe, de la méthode ou de l'annotation.


## Pour rechercher plus vite

### Les classes

* <strong><kbd>CTRL</kbd> + <kbd>N</kbd> </strong>: affiche une popup pour pouvoir rechercher une classe.

Je pense que celle-ci tout le monde la connait, cependant savez-vous qu'il est possible d'être plus précis dans la recherche?

Voici les quelques extensions que cette fonctionnalités offre :

1. On sait tous qu'en saisissant *MSC* on peut retrouver notre classe *M*a*S*uperbe*C*lasse.
1. Savez-vous que pour aller à une ligne bien précise on peut lui ajouter MSC*:*leNumeroDeLaLigne?.
    1. Par exemple : _MSC:40_ affiche la classe MaSuperberbeClasse et positionne le curseur à la ligne _40_.
1. On peut aussi rechercher des répertoires dans le projet en commençant la recherche par un '/'.

### Les fichiers

* <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>N</kbd></strong> : affiche la fenêtre de recherche de fichiers.

### Symboles

On entend par symboles, les méthodes, les attributs de classes, etc ...

* Cette fonctionnalité est accessible via : <strong><kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>N</kbd></strong>.

On peut y rechercher des méthodes, des variables de classes ou d'instances.

### Structural Search

Cette fonctionnalité est très intéressante parce qu'elle permet de détecter et remplacer toutes les structures de code qui correspondent au patern que vous avez saisis.

L'exemple qui a été donné était de trouver tous les blocs de code qui récupèrent une exception sans la traiter.

Voici le type de code recherché, qui avouons-le est une mauvaise façn d'écrire du code :


~~~~java
try {
    get(toPrint);
} catch (Exception e) {

}
~~~~


Pour cela, on ajoute un pattern via le menu.

On met juste ce qui peut changer, c'est-à-dire le statement qu'il y a entre le try et le catch.

o Add search template

o Replace bad structure : try catch without handling exception
o Replace bad structure : try catch without handling exception


## Des fonctionnalités avancées

### Les inspections

<strong><kbd>ALT</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd></strong> : Inspecter une classe ou une méthode.

Cela permet de savoir ce qui ne va pas dans une classe ou méthode.

### Le guide de productivité

· Productivity guide : pour le fun on voit les touches, que l’on utilise le plus. On pourrait s’en servir pour créer des live templates adéquats. C’est de l’amélioration continue.

### Le TDD

Pour finir, il a montré une manière de faire du TDD:

1. On crée une classe de Test
2. On génère une méthode de Test avec <strong><kbd>CTRL</kbd> + <kbd>ENTREE</kbd></strong>.
3. On met dans cette méthode MaClasse maClasse = new Maclasse();
4. Si la classe n'existe pas on peut la créer en faisant <strong><kbd>CTRL</kbd> + <kbd>ENTREE</kbd></strong> pour générer cette classe.

Pour information, pour trouver une action, saisissez <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>A</kbd></strong>.


Hadi a dit que c’est mieux de connaître des raccourcis car on est plus productifs que d’utiliser la souris.

Il finit sur une pointe d’humour.

Vous allez me dire, on connaissait déjà. Moi je dis tant mieux mais après un an et demie d’utilisation intensive de l’IDE, il continue de me surprendre.

Ce fut une séance riches en raccourcis qui amélioreront nettement ma productivité et certainement la vôtre avec Intellij Idea.

J'espère que ces quelques astuces vous aidera dans votre utilisation quotidienne de cet excellent IDE qu'est Intellij IDEA.

## Conclusion

Adepte d'Intellij IDEA depuis un an et demi, il me reste encore beaucoup à apprendre sur ce fabuleux IDE. Accompagnée par des petits apartés d'humour, la conférence de Hadi Hariri ne m'a pas à un seul moment ennuyé.
Vive Intellij. En espérant que ces astuces et raccourcis augmenteront votre productivité.