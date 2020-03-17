# EstiMATHeur

## Comment ça marche ?

L'estiMATHeur permet de créer un ou plusieurs exercices de placement de nombre.

## Liste d'exercies

Si vous voulez récupérer un des ces exercices pour le modifier ou récupérer son QRCode, copier l'URL de ce dernier et modifier la partie ***m=g*** par ***m=m***.

## Une version tablette est-elle prévue ?

Oui c'est en cours, mais si vous avez besoin d'une version "hors-ligne" rapidement vous pouvez directement télécharger le contenu de ce dépôt au format Zip (appuyer sur le bouton "Clone or download" puis "Donwload ZIP"). Vous aurez ensuite à dézipper ce fichier sur votre tablette/téléphone/PC. Il suffira ensuite de cliquer sur le fichier "index.html" pour lancer l'estiMATHeur dans votre navigateur web préféré. 

## Comprendre la syntaxe des exercices dans l'URL

Si l'interface de création des exercices ne proposent pas une valeur de paramètre que vous aurez été utile, vous pouvez directement créer votre exercice en changeant l'URL de la page.

Le paramètre d'URL qui permet de lancer un exercice est ***m=g*** et celui qui contient la description d'un exercice se nomme ***e=&lt;paramètres de l'exercice&gt;***. Votre URL devra donc ressembler à :
```
https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=<paramètres de l'exercice>
```

Où &lt;paramètres de l'exercice&gt; contient une suite de clé/valeur séparé pour des ***:***. Voici les clés/valeurs disponibles :
- m : borne basse du nombre à trouver
- M : borne haute du nombre à trouver
- e : permet de définir la marge d'erreur acceptée pour considérer que le clic a été fait à la bonne position. Si valeur est un simple nombre, ce dernier indique la taille de la marge de façon entière. Si le nombre est suivi d'un ***p***, cela correspondera à X% de la largeur totale de la barre. La marge d'erreur est bien répartie équitablement autour de la valeur cherchée, ainsi si le nombre à trouver est '3' que la marge vaut '1', les clic entre '2.5' et '3.5' seront compté comme bon.
- n : permet de définir les numérotations à afficher. Les bornes basse et haute sont toujours affichées mais vous pouvez préciser combien d'autres numéroration ajouter. Si la valeur est un chiffre, le logiciel coupera au mieux l'intervalle à cette valeur. Par exemple sur un intervalle de 0 à 10, si vous choississez une numérotation cette dernière sera le nombre '5', pour deux numérotations les nombres affichés seront '3' et '6'. Il existe des valeurs particulière : ***eu*** pour mettre une numérotation sur toutes les unités et ***esu*** pour mettre des numérotations une unité sur deux.
- g : permet de définir les graduations  à afficher. Ce paramètre fonctionne le même manière que le paramètre pour les numérotations.
- t : permet de préciser le nombre de questions à poser sur l'exercice
- d : permet de choisir sous quelle forme afficher le nombre à trouver :
  - n : sous forme de chiffres arabes
  - d : sous forme de dés
  - h : sous forme de mains
  - r : sous forme de chiffres romains
  - b : sous forme de petites boites de 5 cases
  - B : sous forme de grandes boites de 10 cases
- T : permet de définir la tolérance d'erreur pour valider l'exercice. La valeur peut être exprimé sous forme de nombre d'erreurs tolérées ou par pourcentage d'erreurs par rapport au nombre de question.

Exemple : ***m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n*** peut se traduire en "chercher 5 nombres (t:5) entre 0 (m:0) et 10 (M:10) affichés sous forme de chiffres arabes (d:n) avec une marge d'erreur d'une unité (e:1) sans afficher de numérotation (n:) et avec une graduation à chaque unité (g:eu). L'exercice sera validé si l'élève ne fait pas plus de 2 erreurs (T:2)".

Vous pouvez enchainer plusieurs exercices en les séparants par le caractère ***|*** comme dans l'exemple suivant
[https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n|m:0,M:10,e:1,n:,g:esu,t:5,T:2,d:d|m:0,M:10,e:1,n:,g:1,t:5,T:2,d:h|m:0,M:10,e:1,n:,g:,t:5,T:2,d:B](https://matthieusalvat.github.io/estiMATHeur/index.html?m=g&e=m:0,M:10,e:1,n:,g:eu,t:5,T:2,d:n|m:0,M:10,e:1,n:,g:esu,t:5,T:2,d:d|m:0,M:10,e:1,n:,g:1,t:5,T:2,d:h|m:0,M:10,e:1,n:,g:,t:5,T:2,d:B)

## Mode de développement

L'idée a été de créer le plus rapidement possible un prototype pour l'estiMATHeur. Le code est donc été réalisé à la va-vite et mérite un bon coup de 'refactoring'. Merci de ne pas contribuer sur ce code.

## Licences et remerciements

Le code est sous GPL2.

Merci à [lakanal.net](https://lakanal.net/aide/pictchou.htm) d'avoir permis d'intégrer leur police de caractères Picthchou (pour afficher les mains et les boites) sur ce projet.

