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
#### **Les listes (`List`)**
En java il faut importer les listes depuis `import java.util.List;`, une liste est une collection ordonnée qui peut contenir des éléments en double.
##### Implémentations principales
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

##### **Les Ensembles (`Set`)**
Un **ensemble** (Set) est une collection **non ordonnée** où **chaque élément est unique**.
##### Implémentations principales :

- `HashSet<E>` → **Pas d’ordre**, rapide grâce au hachage
- `LinkedHashSet<E>` → **Ordre d’insertion conservé**
- `TreeSet<E>` → **Trié naturellement**
  
| Opération                               | `HashSet`                              | `LinkedHashSet`               | `TreeSet`                  |
| --------------------------------------- | -------------------------------------- | ----------------------------- | -------------------------- |
| **Ordre**                               | Non                                    | Oui (ordre d'insertion)       | Oui (trié)                 |
| **Performance (`add/remove/contains`)** | Rapide                                 | Rapide                        | Lent mais efficace         |
| **Utilisation**                         | Stocker des valeurs uniques sans ordre | Conserver l’ordre d’insertion | Stocker des valeurs triées |
**Exemple d'ensemble**

```
public class Main {
    public static void main(String[] args) {
        Set<String> hashSet = new HashSet<>();
        Set<String> treeSet = new TreeSet<>();

        hashSet.add("Banane");
        hashSet.add("Pomme");
        hashSet.add("Orange");

        treeSet.addAll(hashSet);

        System.out.println(hashSet); // Ordre aléatoire
        System.out.println(treeSet); // [Banane, Orange, Pomme] (trié)
    }
}
```

#### **Les Maps (`Map<K, V>`)**
Une **map** est une structure qui associe **des clés (`K`) à des valeurs (`V`)**.
##### **Implémentations principales :**

- `HashMap<K, V>` → Rapide mais **pas d’ordre**
- `LinkedHashMap<K, V>` → **Conserve l’ordre d’insertion**
- `TreeMap<K, V>` → **Trié**  grâce à un **arbre rouge-noir**
  
| Opération                   | `HashMap`    | `LinkedHashMap`             | `TreeMap`          |
| --------------------------- | ------------ | --------------------------- | ------------------ |
| **Ordre**                   | Non          | Oui (ordre d'insertion)     | Oui (trié par clé) |
| **Performance (`get/put`)** | Rapide       | Rapide                      | Lent mais efficace |
| **Utilisation**             | Accès rapide | Conserver ordre d'insertion | Clés triées        |
**Exemple de map**

```
public class Main {
    public static void main(String[] args) {
        Map<String, Integer> hashMap = new HashMap<>();
        Map<String, Integer> treeMap = new TreeMap<>();

        hashMap.put("Alice", 25);
        hashMap.put("Bob", 30);
        hashMap.put("Charlie", 28);

        treeMap.putAll(hashMap);

        System.out.println(hashMap); // Ordre aléatoire
        System.out.println(treeMap); // Clés triées par ordre alphabétique
    }
}
```

#### Conclusion : Quel conteneur choisir ?
| Besoin                                       | Structure                           |
| -------------------------------------------- | ----------------------------------- |
| Stocker une **liste ordonnée** avec doublons | `List` (`ArrayList` / `LinkedList`) |
| Stocker des **valeurs uniques**              | `Set` (`HashSet`, `TreeSet`)        |
| Associer des **clés → valeurs**              | `Map` (`HashMap`, `TreeMap`)        |
