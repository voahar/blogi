<a href="http://blog.soat.fr/wp-content/uploads/2014/04/double_xx_texte.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/double_xx_texte.png" alt="double_xx_texte" width="128" height="124" class="alignleft size-full wp-image-25646" /></a>

Hadi HARIRI (@hhariri) de chez Jetbrains a présenté durant cette conférence quelques astuces pratiques de leur IDE phare Intellij IDEA, un IDE polyglotte payant mais qui est aussi proposé en édition communautaire.

Il commence la séance avec une petite touche d’humour comme quoi ceux qui sont sur Eclipse migreront sur Intellij Idea à la fin de la séance. Après quelques questions pour savoir qui sont sur Intelij ou sur Eclipse, il commence par présenter des raccourcis basiques.

Il en a présenté une centaine tout au long de la conférence. Cependant, je ne vais juste présenter que celles qui m'ont vraiment surpris et que je trouve vraiment utiles.

Si vous êtes un early adopter de cet IDE ou si vous voulez vous y mettre, voici les raccourcis et les astuces qui changeront peut-être votre utilisation quotidienne d'Intellij IDEA.


## Des raccourcis pour naviguer plus facilement dans un projet

Lors de mon utilisation de cet IDE, il m'arrive souvent d'utiliser la souris pour aller dans le panneau contenant la structure du projet.
Eh bien maintenant, on peut utiliser le raccourci <strong><kbd>CTRL</kbd> + <kbd>1</kbd></strong> pour l'atteindre.

Maintenant, si on veut configurer notre projet, il existe un raccourci <strong><kbd>ALT</kbd> + <kbd>F7</kbd></strong> pour afficher rapidement la fenêtre de paramétrage du projet.

Pour maximiser l'espace de travail et pour naviguer plus facilement à travers les différents packages de votre projet, plusieurs options s'offrent à nous :

 - La barre de navigation :
    - On peut tout d'abord désactiver la barre de navigation celle qui se trouve en haut de la fenêtre. Pour ce faire, il faut aller **View>Navigation Bar**.
    - Ensuite, on pourra toujours l'afficher à la demande en saisissant : <strong><kbd>ALT</kbd> + <kbd>DEBUT</kbd></strong>.

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/nav_bar.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/nav_bar.png" alt="nav_bar" width="540" height="28" class="aligncenter size-full wp-image-26124" /></a>

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

### Une classe

* <strong><kbd>CTRL</kbd> + <kbd>N</kbd> </strong>: affiche une popup pour pouvoir rechercher une classe.

Je pense que celle-ci tout le monde la connait, cependant savez-vous qu'il est possible d'être plus précis dans la recherche?

Voici les quelques extensions que cette fonctionnalités offre :

1. On sait tous qu'en saisissant *MSC* on peut retrouver notre classe *M*a*S*uperbe*C*lasse.
1. Savez-vous que pour aller à une ligne bien précise on peut lui ajouter MSC*:*leNumeroDeLaLigne?.
    1. Par exemple : _MSC:40_ affiche la classe MaSuperberbeClasse et positionne le curseur à la ligne _40_.
1. On peut aussi rechercher des répertoires dans le projet en commençant la recherche par un '/'.

### Des fichiers

* <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>N</kbd></strong> : affiche la fenêtre de recherche de fichiers.

### Des symboles

On entend par symboles, les méthodes, les attributs de classes, etc ...

* Cette fonctionnalité est accessible via : <strong><kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>N</kbd></strong>.

On peut y rechercher des méthodes, des variables de classes ou d'instances.

### Structural Search & Replace

Cette fonctionnalité est très intéressante parce qu'elle permet de détecter et remplacer toutes les structures de code qui correspondent au patern que vous avez saisis.

Elle permet de rechercher un bloc de code donné suivant un pattern. Des pattern par défaut sont déjà fournis.

Pour y accéder, il faut activer l'option.

1. Tout d'abord, activer l'option en accédant aux paramètres de l'IDE.
2. Ensuite rechercher "Structural Search Inspection", l'activer si elle ne l'est pas déjà

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search_inspection.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search_inspection-1024x756.png" alt="structural_search_inspection" width="640" height="472" class="aligncenter size-large wp-image-26105" /></a>


#### Recherche des try/catch qui ne font rien de l'exception attrappée

J'ai une classe comme ceci :

~~~~java
public class HelloController {

    public void print(final String toPrint) {

        try {
            get(toPrint);
        } catch (Exception e) {

        }

    }


    public void get(String s) throws Exception {
        throw new NotImplementedException();
    }

}
~~~~

1. Entrer la commande <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>S</kbd></strong>.
2. Copier et coller le code suivant dans le champ "Search template" :

~~~~java
try {
  $TryStatement$;
} catch($ExceptionType$ $ExceptionDcl$) {

}
~~~~

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search.png" alt="structural_search" width="652" height="529" class="aligncenter size-full wp-image-26109" /></a>

3. En appuyant sur "Find", on obtient ceci :

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search_result.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/structural_search_result-1024x619.png" alt="structural_search_result" width="640" height="386" class="aligncenter size-large wp-image-26111" /></a>

L'exemple qui a été donné était de trouver tous les blocs de code qui récupèrent une exception sans la traiter.

#### Recherche et remplacer les try/catch qui ne font rien de l'exception attrappée

De la même manière que la recherche, on peut remplacer des blocs de codes par un autre.
Cela est possible avec la fonctionnalité "Structural Replace" accessible via <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>M</kbd></strong>.

On réalisant cette combinaison de touches, on obtient ceci :

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/structural_replace.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/structural_replace.png" alt="structural_replace" width="635" height="732" class="aligncenter size-full wp-image-26114" /></a>

## Des fonctionnalités avancées

### Les inspections

La combinaison <strong><kbd>ALT</kbd> + <kbd>SHIFT</kbd> + <kbd>I</kbd></strong> permet d'inspecter une classe ou une méthode.

Cela permet de savoir ce qui ne va pas dans une classe ou méthode. C'est un complément à PMD et Checkstyle.

### Le guide de productivité

Le **Productivity guide** donne des statistiques sur notre utilisation de l'IDE et comment grâce à l'assistance de l'IDE, on devient plus productif. 

On y voit par exemple le nombre de fois que l'on utilise une fonctionnalité.

On y accède en faisant <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>A</kbd></strong>.
Puis on y saisi : Productivity Guide.

On obtient ceci :

<a href="http://blog.soat.fr/wp-content/uploads/2014/04/productivity_guide.png"><img src="http://blog.soat.fr/wp-content/uploads/2014/04/productivity_guide.png" alt="productivity_guide" width="731" height="560" class="aligncenter size-full wp-image-26116" /></a>

### Le TDD

Pour finir, il a montré une manière de faire du TDD:

1. On crée une classe de Test
2. On génère une méthode de Test avec <strong><kbd>CTRL</kbd> + <kbd>ENTREE</kbd></strong>.
3. On met dans cette méthode MaClasse maClasse = new Maclasse();
4. Si la classe n'existe pas on peut la créer en faisant <strong><kbd>CTRL</kbd> + <kbd>ENTREE</kbd></strong> pour générer cette classe.

Pour information, pour trouver une action, saisissez <strong><kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>A</kbd></strong>.

## Conclusion

Adepte d'Intellij IDEA depuis un an et demi, il me reste encore beaucoup à apprendre sur ce fabuleux IDE. Accompagnée par de petits moments d'humour, la conférence de Hadi Hariri a été très riche en découvertes.

J'espère que ces quelques astuces vous aidera à augmenter votre productivité dans votre utilisation quotidienne de cet excellent IDE qu'est Intellij IDEA.

Vive Intellij IDEA.