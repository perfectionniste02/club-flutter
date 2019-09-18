# club-flutter

#1 Stack

>Stack est une Widget pouvant contenir plusieurs widgets enfants, 
>ils positionne ses enfants par rapport aux bords de sa boîte.
>Cette classe est utile si vous souhaitez superposer plusieurs enfants de manière simple, 
>par exemple, avoir du texte et une image, superposés avec un dégradé et un bouton attaché au bas.

>Chaque enfant d'un widget Stack est positionné ou non. 
>Les enfants positionnés sont ceux encapsulés dans un widget positionned qui a au moins une propriété non nulle. 
>La pile elle-même se redimensionne pour contenir tous les enfants non positionnés, qui sont positionnés selon 
>un alignement (défini par défaut sur le coin supérieur gauche des environnements gauche à droite et le coin 
>supérieur droit des environnements situés de droite à gauche). Les enfants positionnés sont ensuite placés 
>par rapport à la pile en fonction de leurs propriétés top(supérieure), right(droite), bottom(inférieure) et left(gauche).

#2 Spacer

>Spacer crée un espaceur vide ajustable pouvant être utilisé pour ajuster l'espacement entre les widgets d'un conteneur Flex,
>tel que Ligne ou Colonne.
>Le widget Spacer occupera tout l'espace disponible. 
>Par conséquent, définissez Flex.mainAxisAlignment sur un conteneur flex contenant un Spacer sur MainAxisAlignment.spaceAround,
> MainAxisAlignment.spaceBetween ou MainAxisAlignment.spaceEvenly n'aura aucun effet visible: 
>le Spacer n'aura aucun effet visible. de l'espace supplémentaire, il n'y a donc plus rien à redistribuer.

#3 Semantics

>Un widget qui annote l’arborescence des widgets avec une description de la signification des widgets.
>Utilisé par les outils d'accessibilité, les moteurs de recherche et d'autres logiciels 
>d'analyse sémantique pour déterminer la signification de l'application.
>MergeSemantics, qui marque un sous-arbre comme étant un seul nœud à des fins d'accessibilité.
>ExcludeSemantics, qui exclut un sous-arbre de l’arborescence de la 
>sémantique (qui peut être utile s’il est, par exemple, totalement décoratif et n’a pas d’importance pour l’utilisateur).
>RenderObject.semanticsAnnotator, l'API de bibliothèque de rendu à travers laquelle le widget Sémantique est réellement implémenté.
>SemanticsNode, l'objet utilisé par la bibliothèque de rendu pour représenter la sémantique dans l'arbre sémantique.
>SemanticsDebugger, une superposition permettant de visualiser l’arborescence de la sémantique. Peut être activé à l'aide de WidgetsApp.
>showSemanticsDebugger ou MaterialApp.showSemanticsDebugger.


#4 RichText

>Le widget RichText affiche du texte qui utilise plusieurs styles différents. 
>Le texte à afficher est décrit à l'aide d'une arborescence d'objets TextSpan, 
>chacun ayant un style associé utilisé pour cette sous-arborescence.
>Le texte peut se répartir sur plusieurs lignes ou être affiché sur la même ligne,
>en fonction des contraintes de présentation.
>Le texte affiché dans un widget RichText doit être explicitement stylé. 
>Lorsque vous choisissez le style à utiliser, envisagez d'utiliser DefaultTextStyle.of du BuildContext actuel pour fournir les valeurs par défaut. 
>Pensez à utiliser le widget Texte pour intégrer automatiquement le DefaultTextStyle. 
>Lorsque tout le texte utilise le même style, le constructeur par défaut est moins détaillé. 
>Le constructeur Text.rich vous permet de styliser plusieurs étendues avec le style de texte par défaut tout en autorisant les styles spécifiés par étendue.

#5 ReaoderableListView

>Liste dont les éléments peuvent être réorganisés de manière interactive par l'utilisateur en les faisant glisser.
>Cette classe est appropriée pour les vues avec un petit nombre d'enfants car la construction de la liste nécessite un travail pour chaque
>enfant susceptible de s'afficher dans la vue liste plutôt que uniquement les enfants réellement visibles.

#6 Placeholder

>Un widget qui dessine une boîte qui représente l'endroit où d'autres widgets seront un jour ajoutés.
>Ce widget est utile pendant le développement pour indiquer que l'interface n'est pas encore complète.
>Par défaut, l'espace réservé est dimensionné pour s'adapter à son conteneur. Si l'espace réservé se trouve dans un espace non limité, 
>il se dimensionnera lui-même en fonction des valeurs fallbackWidth et fallbackHeight données.

#7 MediaQuery

>Établit une sous-arborescence dans laquelle les requêtes de média résolvent les données données.
>Établit une sous-arborescence dans laquelle les requêtes de média résolvent les données données.

>Par exemple, pour connaître la taille du média actuel (la fenêtre contenant votre application, par exemple), 
>vous pouvez lire la propriété MediaQueryData.size à partir du MediaQueryData renvoyé par MediaQuery.of: MediaQuery.of (context) .size.
>Si vous interrogez le média actuel à l'aide de MediaQuery.of, votre widget sera reconstruit automatiquement à chaque modification de 
>MediaQueryData (par exemple, si l'utilisateur fait pivoter son périphérique).
>Si aucun MediaQuery n'est dans la portée, la méthode MediaQuery.of lève une exception, 
>sauf si l'argument null est défini sur true, auquel cas elle renvoie la valeur null.

#8 LimitedBox

>Une boîte qui limite sa taille uniquement lorsqu'elle n'est pas contrainte.
>Si la largeur maximale de ce widget n'est pas contrainte, la largeur de son enfant est limitée à maxWidth.
>De même, si la hauteur maximale de ce widget n'est pas contrainte, la hauteur de son enfant est limitée à maxHeight.
>Cela a pour effet de donner à l'enfant une dimension naturelle dans des environnements sans limites. Par exemple, 
>en fournissant un maxHeight à un widget qui essaie normalement d'être aussi grand que possible, le widget se redimensionne
>lui-même pour s'adapter à son parent, mais placé dans une liste verticale, il prendra la hauteur donnée.
>Ceci est utile lors de la composition de widgets qui tentent normalement de correspondre à la taille de leurs parents,
>de sorte qu'ils se comportent raisonnablement dans des listes (qui ne sont pas limitées).

#9 IndexedStack

>Une pile qui montre un seul enfant parmi une liste d’enfants.
>L'enfant affiché est celui avec l'index donné. La pile est toujours aussi grosse que le plus grand des enfants.
>Si la valeur est null, rien n'est affiché.

#10 InheritedWiget

>Classe de base pour les widgets qui propagent efficacement les informations dans l'arborescence.
>Pour obtenir l'instance la plus proche d'un type particulier de widget hérité à partir d'un contexte de construction,
>utilisez BuildContext.inheritFromWidgetOfExactType.
>Les widgets hérités, lorsqu'ils sont référencés de cette manière,
>vont entraîner la reconstruction du consommateur lorsque le widget hérité lui-même changera d'état.

#11 draggable

>Un widget qui peut être déplacé vers un DragTarget.

>Lorsqu'un widget déplaçable reconnaît le début d'un geste de glisser, il affiche un widget de commentaire qui suit le doigt de l'utilisateur sur l'écran. 
>Si l'utilisateur lève le doigt alors qu'il se trouve au-dessus d'un DragTarget, cette cible se voit offrir la possibilité d'accepter les données transportées par l'objet déplaçable.
>Sur les périphériques multitouch, plusieurs déplacements peuvent se produire simultanément, car il peut y avoir plusieurs pointeurs en contact avec le périphérique à la fois. 
>Pour limiter le nombre de déplacements simultanés, utilisez la propriété maxSimultaneousDrags. La valeur par défaut consiste à autoriser un nombre illimité de déplacements simultanés.
>Ce widget affiche enfant lorsque zéro glissement est en cours. Si childWhenDragging est non-null, ce widget affiche à la place childWhenDragging lorsqu'un ou plusieurs déplacements sont en cours. 
>Sinon, ce widget affiche toujours enfant.

#12 ConstrianeBox

>Un widget qui impose des contraintes supplémentaires à son enfant.
>Par exemple, si vous souhaitez que l'enfant ait une hauteur minimale de 50,0 pixels logiques,
>vous pouvez utiliser const BoxConstraints (minHeight: 50.0) comme contrainte.

#13 AspectRatio

>Un widget qui tente de dimensionner l'enfant à un rapport d'aspect spécifique.
>Le widget essaie d'abord la plus grande largeur autorisée par les contraintes de présentation. 
>La hauteur du widget est déterminée en appliquant le rapport de format donné à la largeur, exprimé 
>en tant que rapport largeur / hauteur.
>Par exemple, un rapport hauteur / largeur 16: 9 aurait une valeur de 16,0 / 9,0. Si la largeur maximale est infinie, la largeur initiale est déterminée en appliquant le rapport de format à la hauteur maximale.

>Considérons maintenant un deuxième exemple, cette fois-ci avec un rapport de format de 2,0 et des contraintes d’agencement nécessitant une largeur comprise entre 0,0
>et 100,0 et une hauteur comprise entre 0,0 et 100,0. Nous choisirons une largeur de 100,0 (la plus grande autorisée) et une hauteur de 50,0 (pour correspondre au rapport de format).
>Dans cette même situation, si le format de l’image est égal à 0,5, nous sélectionnons également une largeur de 100,0 (le plus grand permis) et nous essayons d’utiliser une hauteur de 200,0.
>Malheureusement, cela ne respecte pas les contraintes car l’enfant peut avoir une hauteur maximale de 100,0 pixels. Le widget prendra alors cette valeur et appliquera à nouveau le rapport de format pour obtenir une largeur de 50,0.
>Cette largeur est autorisée par les contraintes et l'enfant reçoit une largeur de 50,0 et une hauteur de 100,0. Si la largeur n'était pas autorisée, le widget continuerait à parcourir les contraintes. 
>Si le widget ne trouve pas de taille réalisable après avoir consulté chaque contrainte, il sélectionnera finalement une taille pour l'enfant qui respecte les contraintes de présentation mais ne respecte pas les contraintes de rapport de format.

#14 AnimatedPadding

>Version animée de Padding qui transforme automatiquement l'indentation sur une durée donnée à chaque changement d'inset.

#15 AnimatedPositioned 

>Version animée de Positionné qui transforme automatiquement la position de l'enfant sur une durée donnée à chaque changement de position.
>Ce widget est un bon choix si la taille de l’enfant finit par changer à la suite de cette animation. Si la taille doit rester la même et que seule la position change au fil du temps,
>envisagez plutôt SlideTransition. SlideTransition ne déclenche que de repeindre chaque image de l'animation, 
>alors que AnimatedPositioned déclenchera également un relayout.

#16 AnimatedOpacity 
>Version animée de l'opacité qui fait automatiquement passer l'opacité de l'enfant sur une durée donnée, chaque fois que l'opacité donnée change.

#17 AnimatedList 

Conteneur de défilement qui anime les éléments lorsqu'ils sont insérés ou supprimés.
AnimatedListState de ce widget peut être utilisé pour insérer ou supprimer des éléments de manière dynamique.
Pour faire référence à AnimatedListState, fournissez une clé GlobalKey ou utilisez la méthode static de à partir du rappel d'entrée d'un élément.

#18 animatedIcon

>il permet Affiche u
>ne icône animée à une progression d'animation donnée.

#19 Flexible

>Un widget qui contrôle le comportement d'un enfant d'une ligne, d'une colonne ou d'un flex.
>L’utilisation d’un widget Flexible donne à l’enfant d’une rangée, d’une colonne ou d’un Flex la possibilité de se développer
>pour remplir l’espace disponible dans l’axe principal (par exemple, horizontalement pour une rangée ou verticalement pour une colonne), 
>mais contrairement à Expanded, Flexible ne fonctionne  n'oblige pas l'enfant à remplir l'espace disponible.

#20 AnimatedSwitcher 

>Un widget qui effectue par défaut une FadeTransition entre un nouveau widget et le widget précédemment défini sur le AnimatedSwitcher en tant qu'enfant.
>S'ils sont permutés assez rapidement (c'est-à-dire avant la fin de la durée), plusieurs enfants précédents peuvent exister et effectuer la transition pendant
>que le dernier en arrive à la transition.
>Si le "nouveau" enfant est du même type et de la même clé que le "vieux" enfant, mais avec des paramètres différents, AnimatedSwitcher n'effectuera pas de transition entre eux car,
>s'agissant du cadre, ils sont le même widget et le widget existant peut être mis à jour avec les nouveaux paramètres. Pour forcer la transition, définissez une clé sur chaque widget
>enfant que vous souhaitez considérer comme unique (en règle générale, une valeur ValueKey sur les données du widget permettant de distinguer cet enfant des autres).

