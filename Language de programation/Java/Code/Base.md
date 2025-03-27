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

## Les containeurs
**Les listes**
En java il faut importer les listes depuis `import java.util.List;`, une liste est une collection ordonnée qui peut contenir des éléments en double.
#### Implémentations principales
- `ArrayList<E>` → Basé sur un **tableau dynamique** 
- `LinkedList<E>` → Basé sur une **liste chaînée** 

| Opération                            | `ArrayList`                   | `LinkedList`                           |
| ------------------------------------ | ----------------------------- | -------------------------------------- |
| **Accès (`get(i)`)**                 | Très rapide `O(1)`            | Lent `O(n)`                            |
| **Ajout/Suppression (`add/remove`)** | Lent `O(n)` (au début/milieu) | Rapide `O(1)` (début), `O(n)` (milieu) |
| **Utilisation**                      | Pour **accès rapide**         | Pour **modifications fréquentes**      |

**Exemple de liste**

```
public class Main {
    public static void main(String[] args) {
        List<String> arrayList = new ArrayList<>();
        List<String> linkedList = new LinkedList<>();

        arrayList.add("Alice");
        linkedList.add("Bob");

        System.out.println(arrayList.get(0)); // Alice
        System.out.println(linkedList.get(0)); // Bob
    }
}
```
