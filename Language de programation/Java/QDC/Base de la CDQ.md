# Base
## Type d'écriture :
Tous en Java est écris en camel case c-à-d `commeCeuxCi` :
- Les classes commencent par une majuscule `Main` ou `EtreUnFermier`.
- Les méthodes commencent par une minuscule `dancer()` ou `planterDesPatate()`.
	- La seul exceptions étant le constructeur qui à un nom identique à sa classe.	  
Il est important lors de l'écriture du code de montrer correctement sont intention en nommant correctement les variables ou autres c-à-d :
- Eviter les variables `a1` ou fonction `f1` 
- A la place donner des noms qui explique leur fonctions `a1 -> numResultat` et `f1 -> suiteDeFibonnacci`
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
