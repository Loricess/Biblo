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

Tips pour avoir un code plus expressif 

- Ne mettre des mots évident dans les noms de variables ou autres .
- Eviter la notation hongroise `int nIndex ; char cChar`.
- Ne pas rendre un nom inutilement compliqué.
- Ne pas mettre de mot qui sont déjà connue via le context .
- Eviter les mots qui n'apporte aucune information concrète `data ; state ; value`.

**Les commentaires**
En premier lieu il faut transformer les commentaires simples dans le code c-à-d :

```
// Eviter
String nom; nom et prénom

// Faire;
String nomComplet;
```

En suite il faut éviter les commentaires inutiles du styles :

```
public String nager(){
	// Fonction qui renvoient un string 
	// TODO
}
```

Et finalement il faut éviter les commentaires qui ne servent qu'à expliquer **comment** marche le code est à la place mettre un commentaires qui expliquent **pourquoi** le code existe.

**Comment remarquer un mauvais code ?***
- **Un mauvais code à ** :
	- Des commentaires inutiles
	- Des longues méthodes qui sont désagréable à lire .
	- Des **magic number** c-à-d des des nombres dont la signification n'est pas évidente et qui ne devraient être utilisés qu'une seule fois dans le code*
	- De la duplications.
	- Une mauvaises terminologie.
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
