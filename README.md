Programmation Java @ Et3
<br>
Polytech Paris-Saclay | 2019-20

 
___

# TP1

Le but de ce TP est de créer un programme de conversion de températures.
Ce programme devra contenir :

  - deux titres (cf. (*Label*)[https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/Label.html]), "Celsius" et "Fahrenheit";
  - deux champs de texte (cf. (*TextField*)[https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/TextField.html]), pour entrer et afficher des températures;
  - deux boutons (cf. (*Button*)[https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/Button.html]), "Close" (pour fermer l'application) et "Reset" (pour vider les champs de texte).

<br><div align="center"><img src="images/tempconvH.jpg" width="300"></img></div><br>

1. Importez ce projet dans votre IDE.

> Pour importer ce projet dans Eclipse, suivez les étapes suivantes :
>   1) Allez dans *File* > *Import...*;
>   2) Sélectionnez *Git* > *Projects from Git*;
>   3) Sélectionnez *Clone URI*;
>   4) Dans *URI:*, entrez "https://github.com/polytech-ihm-et3/TP1_squelette.git" (les autres champs devraient se remplir automatiquement);
>   5) Cliquez sur "*Next >*" pour toutes les étapes suivantes, puis sur "*Finish*".
>   
> Pour visualiser les tâches à réaliser dans ce projet avec Eclipse, allez dans "*Window*" > "*Show View*" > "*Tasks*".

> Pour importer ce projet dans IntelliJ, suivez les étapes suivantes :
>   1) Allez dans *File* > *New* > *Project from Version Control...*;
>   2) Sur la droite, sélectionnez *GitHub*;
>   3) Dans la barre de recherche, en haut, inscrivez "https://github.com/polytech-ihm-et3/TP1_squelette.git";
>   4) Cliquez sur "*Clone*".
>   
> Pour visualiser les tâches à réaliser dans ce projet avec IntelliJ, allez dans "*View*" > "*Tool Windows*" > "*TODO*".

2. Dans le fichier *TemperatureConverter.java*, complétez la fonction `initGUI()` pour qu'elle agence correctement les différents éléments graphiques (la disposition finale doit être proche de celle de la photo). Utilisez la classe (FlowPane)[https://docs.oracle.com/javase/8/javafx/api/javafx/scene/layout/FlowPane.html] pour le contenant principal puis d'autres (Panes)[https://docs.oracle.com/javase/8/javafx/api/javafx/scene/layout/Pane.html] de votre choix pour les autres éléments.

3. Assurez-vous que les éléments graphiques sont correctement alignés et que leurs positions sont cohérentent avec la photo suivante lorsque vous changez la taille de la fenêtre.

<br><div align="center"><img src="images/tempconvV.jpg" width="300"></img></div><br>

4) The `textFieldCListener` reads a floating value in the Celsius text box when the user press "enter", converts it from Celsius to Fahrenheit, and writes the result in the Fahrenheit text box. Associate this event handler to the text box of the Celsius value.
5) Fill in the `textFieldFListener` in order to do the conversion from Fahrenheit to Celsius. Associate it with the text box of the Fahrenheit value.

> *The temperature conversion occurs when the user presses enter. Use a `EventHandler<KeyEvent>()` (that you attach with `TextField.setOnKeyPressed`). The `EventHandler<KeyEvent>()` will be notified at each key press.*

6) The `buttonCloseListener` closes the window. Associate it to the "Close" button.
7) Fill in the `buttonResetListener` in order to empty both text boxes. Associate it to the "Reset" button.
8) (Going furhter) Associate a `TextFormatter` to `textFieldF` to ensure a valid character input (e.g., 23, 23.345, -21, 3E -02).
