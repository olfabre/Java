### Erreur classique de conversion de type double à float  

### Comprendre cette erreur classique  


Lorsqu'on débute en Java, il est courant de rencontrer des erreurs de compilation qui peuvent sembler déroutantes. Une de ces erreurs est:  

```csharp
java: incompatible types: possible lossy conversion from double to float
```

Dans cet article, je vais expliquer en détail pourquoi cette erreur se produit, comment l'identifier, et les différentes façons de la corriger. Mon objectif est de démystifier cette erreur et essayer de vous fournir les connaissances nécessaires pour l'éviter à l'avenir.  

#### Comprendre les types Primitifs en Java   

Java propose huit types primitifs: byte, short, int, long, float, double, char, et boolean. Parmi ceux-ci, float et double sont utilisés pour représenter des nombres à virgule flottante. Cependant, ils diffèrent par leur précision:  

- `float`  utilise 32 bits pour stocker une valeur en virgule flottante. Il offre une précision d'environ 6 à 7 chiffres décimaux.  
- `double` Utilise 64 bits pour stocker une valeur en virgule flottante. Il offre une précision d'environ 15 à 16 chiffres décimaux.

  
En Java, les littéraux décimaux comme 1.234 sont par défaut de type double. Cela peut causer des problèmes lorsque vous essayez de les assigner à une variable de type float.  

#### La Source de l'erreur

Prenons un exemple de code pour illustrer cette erreur:  

```java
public class Main {
    public static void main(String[] args) {
        int n;
        float x;
        n = 5;
        x = (2 * n + 1.500000008);

        System.out.println("n = " + n);
        System.out.println("x = " + x);
        double y;
        y = n * x + 12;
        System.out.println("Valeur de y : " + y);
    }
}

```

Lorsqu'on compilez ce code, on obtient l'erreur suivante:


```csharp
java: incompatible types: possible lossy conversion from double to float

```
 
#### Pourquoi cette erreur se produit-elle ?

L'expression 2 * n + 1.500000008 contient un littéral décimal 1.500000008 qui est traité comme un double.   
En Java, les opérations impliquant des int et des double produisent un résultat de type double.   
Ensuite, Java tente d'assigner ce double à x, qui est de type float.   
Cette conversion n'est pas implicite car elle peut entraîner une perte de précision, d'où l'erreur.  

#### Comment corriger cette erreur

Il existe plusieurs méthodes pour résoudre cette erreur en fonction de vos besoins:  

- Solution 1) Utiliser un littéral float: pour indiquer explicitement que 1.500000008 est un float, ajoutez f ou F à la fin du littéral.

```java

x = (2 * n + 1.500000008f);

```
  

- Solution 2) Changer le type de la variable: si vous n'avez pas besoin de restreindre x à un float, déclarez x comme double.  

```java

double x;
x = (2 * n + 1.500000008);

```


#### Comparaison des solutions


Solution avec `float`

```java
public class Main {
    public static void main(String[] args) {
        int n;
        float x;
        n = 5;
        x = (2 * n + 1.500000008f); // Utilisation de 1.500000008f pour indiquer un float

        System.out.println("n = " + n);
        System.out.println("x = " + x);

        double y;
        y = n * x + 12;
        System.out.println("Valeur de y : " + y);
    }
}


```

Solution avec `double`


```java

public class Main {
    public static void main(String[] args) {
        int n;
        double x; // Déclaration de x comme double
        n = 5;
        x = (2 * n + 1.500000008); // Pas de conversion nécessaire

        System.out.println("n = " + n);
        System.out.println("x = " + x);

        double y;
        y = n * x + 12;
        System.out.println("Valeur de y : " + y);
    }
}

```

#### Conclusion

L'erreur "incompatible types: possible lossy conversion from double to float" est courante mais facile à comprendre une fois que l'on maîtrise les bases des types primitifs en Java. En choisissant la bonne méthode pour déclarer et utiliser nos variables, nous pouvons éviter cette erreur et écrire du code plus propre et plus efficace.  







### Sources utilisées pour rédiger cet article  
Livre "Programmer en Java : Couvre Java 10 à Java 14 Ed. 11" - Auteur: Delannoy, Claude - Editeur: Eyrolles - Année de Publication: 2020
