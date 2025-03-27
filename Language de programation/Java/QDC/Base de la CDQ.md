# Base
## Type d'écriture :
Tous en Java est écris en camel case c-à-d `commeCeuxCi` :
- Les classes commencent par une majuscule `Main` ou `EtreUnFermier`.
- Les méthodes commencent par une minuscule `dancer()` ou `planterDesPatate()`.
	- La seul exceptions étant le constructeur qui à un nom identique à sa classe.	  
Il est important lors de l'écriture du code de montrer correctement sont intention en nommant correctement les variables ou autres c-à-d :
- Eviter les variables `a1` ou fonction `f1` 
- A la place donner des noms qui explique leur fonctions `a1 -> numResultat` et `f1 -> suiteDeFibonnacci`
  
> <span style="color: red; font-weight: bold;">Un nommage explicite permet de contextualiser le code et son intention</span>

<span style="color: red; font-weight: bold;">Tips pour avoir un code plus expressif </span>
- Ne mettre des mots évident dans les noms de variables ou autres .
- Eviter la notation hongroise `int nIndex ; char cChar`.
- Ne pas rendre un nom inutilement compliqué.
- Ne pas mettre de mot qui sont déjà connue via le context .
- Eviter les mots qui n'apporte aucune information concrète `data ; state ; value`.

**Les commentaires

## Eviter les répétitions
Il est important d'éviter les répétitions dans le code donc par exemple :

```
System.out.println("------");
System.out.println("Je suis un fermier et je plante des patates");
System.out.println("------");
```

A la place de répéter  `"------"` il est plus judicieux de faire cela :

```
String LIGNE = "------" ;

System.out.println(LIGNE);
System.out.println("Je suis un fermier et je plante des patates");
System.out.println("LIGNE");
```
