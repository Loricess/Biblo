# Déclaration :
En Java la déclaration d'une variable se fait de cette manière :
-  `<modificateur d'accès><Type><Condition><nom> `
Cela donne :
- `String final texte ;`
- < Vide > : modificateur d'accès.
- String : type String.
- Final : Condition.
- Texte : nom.

Pour une méthode :
- `<modificateur d'accès><Type renvoié><nom><paramètre>`
Cela donne :
- `Public String afficher(5)`
- String : type String.
- afficher : nom.
- (5) : paramètre.

Il existent plusieurs modificateur d'accès :

| Modificateur | Accès depuis la même classe | Accès depuis le même package | Accès depuis une sous-classe | Accès depuis une autre classe |
| ------------ | --------------------------- | ---------------------------- | ---------------------------- | ----------------------------- |
| public       | Oui                         | Oui                          | Oui                          | Oui                           |
| protected    | Oui                         | Oui                          | Oui                          | Non                           |
| (par défaut) | Oui                         | Oui                          | Non                          | Non                           |
| private      | Oui                         | Non                          | Non                          | Non                           |

- Le **public** est souvent utilisé pour appelle une fonctions.
- Le protected est utilisé pour une classe mère en cas d'héritage.
- Le vide est utilisé généralement dans une classe main.
- Le private est utilisé pour les variables d'une méthode.

