# EstiMATHeur

## Comment ça marche ?

L'estiMATHeur est un outil au service de la construction du nombre. Comme son nom l'indique, il permet de travailler l'estimation. Chez les enfants, le SNA (Système Numérique Approximatif) s'améliore avec l'âge mais il est intéressant de l'entraîner.

Très inspiré de l’outil « Estimateur » issu du dispositif ACE il "est conçu pour mettre en relation les représentations analogiques de la ligne numérique mentale".

L'estiMATHeur permet de créer un ou plusieurs exercices de placement de nombre et d'en permettre l'accès aux élèves via un QR code.

## Exemples d'exercices

- Pour découvrir l'estimatheur de 1 à  5, puis de 1 à  10 avec les chiffres arabes :

[https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:5,e:2,n:1,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:n&m=g](https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:5,e:2,n:1,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:n&m=g)

- Avec le dés ou les doigts de 1 à  5, puis de 1 à  10 :

[https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:,g:,t:5,T:10p,d:d_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:d_m:0,M:5,e:2,n:,g:,t:5,T:10p,d:h_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:h&m=g](https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:,g:,t:5,T:10p,d:d_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:d_m:0,M:5,e:2,n:,g:,t:5,T:10p,d:h_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:h&m=g)

Si vous voulez récupérer un des ces exercices pour le modifier ou récupérer son QRCode, copier l'URL de ce dernier et modifier la partie ***&m=g*** par ***&m=m***. Par exemple pour la première série d'exercices :
[https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:5,e:2,n:1,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:n&m=m](https://matthieusalvat.github.io/estiMATHeur/?e=m:0,M:5,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:5,e:2,n:1,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:esu,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:eu,t:5,T:10p,d:n_m:0,M:10,e:2,n:,g:,t:5,T:10p,d:n&m=m)


## Une version tablette est-elle prévue ?

Oui c'est en cours !

Si vous avez besoin d'une version "hors-ligne" rapidement vous pouvez directement télécharger le contenu de ce dépôt au format Zip (appuyer sur le bouton "Clone or download" puis "Donwload ZIP"). Vous aurez à dézipper ce fichier sur votre tablette/téléphone/PC. Il suffira ensuite de cliquer sur le fichier "index.html" pour lancer l'estiMATHeur dans votre navigateur web préféré. 

Les liens de lecture de QRCode intégrés à la page de l'estiMATHeur vous permettont de charger un exercice sans avoir d'accès à Internet.

## Traçage, données personnelles et RGPD

L'estiMATHeur ne stocke aucune donnée personnelle et ne met en place aucun traçage de son utilisation.

Toutes les données des exercices créés restent sur votre ordinateur (utilisation de la fonction de *localStorage* de votre navigateur) ou via les liens (URL) et QRCode que vous générez.

## Comprendre la syntaxe des exercices dans l'URL

Si l'interface de création des exercices ne proposent pas une valeur de paramètre qui vous aurez été utile, vous pouvez directement créer votre exercice en changeant ces paramètres directement dans l'URL de la page.

Le paramètre d'URL qui permet de lancer un exercice est ***m=g*** et celui qui contient le paramètrage de l'exercice se nomme ***e***, et suit la syntaxe ***e=&lt;paramètres de l'exercice&gt;***. Votre URL devra donc ressembler à :
```
https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=<paramètres de l'exercice>
```

Où ***&lt;paramètres de l'exercice&gt;*** contient une suite de clé/valeur séparée pour des ***:***.

Voici les clés/valeurs disponibles :
- m : borne basse du nombre à trouver
- M : borne haute du nombre à trouver
- e : permet de définir la marge d'erreur acceptée pour considérer que le clic a été fait à la bonne position. Si la valeur ***X*** est un simple nombre, ce dernier indique la taille de la marge en unités entières. Si le nombre ***X*** est suivi d'un ***p***, cela correspondera à X% de la largeur totale de la ligne numérique. La marge d'erreur est répartie équitablement autour de la valeur cherchée, ainsi si le nombre à trouver est '3' et que la marge d'erreur vaut '1', les clics entre '2.5' et '3.5' seront acceptés.
- n : permet de définir les numérotations à afficher. Les bornes basse et haute sont toujours affichées mais vous pouvez préciser combien d'autres numérorations ajouter. Si la valeur est un nombre ***X***, le logiciel coupera au mieux la ligne numérique en ***X*** intervalles. Par exemple sur une ligne numérique allant de 0 à 10, si vous choississez une seule numérotation (***X=1***) cette dernière sera le nombre '5', pour deux numérotations (***X=2***) les nombres affichés seront '3' et '6'. Il existe des valeurs particulière : ***eu*** pour mettre une numérotation sur toutes les unités et ***esu*** pour mettre des numérotations une unité sur deux.
- g : permet de définir les graduations à afficher. Ce paramètre fonctionne de la même manière que le paramètre pour les numérotations.
- t : permet de préciser le nombre de questions à poser durant l'exercice.
- d : permet de choisir sous quelle forme afficher le nombre à positionner :
  - n : sous forme de chiffres arabes
  - d : sous forme de dés
  - h : sous forme de mains
  - b : sous forme de petites boites de 5 cases (demi boite de Picbille)
  - B : sous forme de grandes boites de 10 cases (boite de Picbille)
  - r : sous forme de chiffres romains
  - H : sous forme de chiffres héxadécimaux
- T : permet de définir la tolérance d'erreur pour valider l'exercice. La valeur peut être exprimée sous forme de nombre d'erreurs tolérées ou de pourcentage d'erreurs par rapport au nombre total de questions.

Exemple : ***m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n*** peut se traduire en !
- Positionner 5 fois (***t:5***) un nombre en chiffres arabes (***d:n***) situé entre 0 (***m:0***) et 10 (***M:10***).
- Dans cet exercice il n'y aura pas de numérotation (***n:***) mais une graduation à chaque unité (***g:eu***) sera affiché.
- L'exercice sera validé le nombre d'erreurs est inférieur ou égal à 2 (***T:2***)".
- La marge d'erreur acceptée est d'une unité (***e:1***)

Vous pouvez enchainer plusieurs exercices en les séparants par le caractère ***_*** comme dans l'exemple suivant
[https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n_m:0,M:10,e:1,n:,g:esu,t:5,T:2,d:d_m:0,M:10,e:1,n:,g:1,t:5,T:2,d:h_m:0,M:10,e:1,n:,g:,t:5,T:2,d:B](https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n_m:0,M:10,e:1,n:,g:esu,t:5,T:2,d:d_m:0,M:10,e:1,n:,g:1,t:5,T:2,d:h_m:0,M:10,e:1,n:,g:,t:5,T:2,d:B)

## Mode de développement

L'idée a été de créer le plus rapidement possible un prototype pour l'estiMATHeur. Le code a donc été réalisé à *la va-vite* et mérite un bon coup de *refactoring*. Merci de ne pas contribuer sur ce code.

## Licences et remerciements

Le code est sous GPL2.

Merci à [lakanal.net](https://lakanal.net/aide/pictchou.htm) d'avoir permis d'intégrer sa police de caractères Picthchou (pour afficher les mains et les boites de Picbille) sur ce projet.

Merci à l'équipe [ACE](http://blog.espe-bretagne.fr/ace/) pour la création de l'estimateur et les justifications scientifiques et pédagogiques de son usage.
