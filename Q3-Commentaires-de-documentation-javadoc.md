### Commentaires de documentation Javadoc

Les commentaires en Java sont des annotations dans le code qui ne sont pas exécutées par le compilateur. Ils servent à documenter le code pour que les développeurs puissent comprendre ce que fait le code, comment il fonctionne, et pourquoi certaines décisions ont été prises. En Java, il existe trois types principaux de commentaires:  

- Commentaires sur une seule ligne: ils commencent par // et continuent jusqu'à la fin de la ligne.
- Commentaires sur plusieurs lignes: ils commencent par /* et se terminent par */.
- Commentaires de documentation (Javadoc): ils commencent par /** et se terminent par */.

Nous allons nous intéresser dans cet article, aux commentaires de documentation Javadoc. Ils sont spécialement conçus pour être extraits automatiquement par des outils comme Javadoc pour générer de la documentation HTML.  


```java
/**
 * La classe Example représente un exemple de classe Java.
 * Elle contient une méthode principale qui affiche un message.
 *
 * @author John Doe
 * @version 1.0
 */
public class Example {
    /**
     * Méthode principale de l'application.
     * @param args Les arguments de la ligne de commande
     */
    public static void main(String[] args) {
        System.out.println("Bonjour, le monde!");
    }
}
```

#### Javadoc

Javadoc est un outil de documentation qui fait partie du JDK (Java Development Kit). Il analyse les commentaires de documentation dans le code source Java et génère une documentation HTML qui décrit les classes, les interfaces, les constructeurs, les méthodes et les champs du code. Voici un exemple de code Java qui utilise toutes les balises Javadoc courantes:  

`@author`

Utilisée pour indiquer l'auteur du code.  


```java
/**
 * La classe Calculator effectue des opérations arithmétiques simples.
 * ...
 * @author Olivier Fabre
 * ...
 */
public class Calculator {

````



`@version`

Utilisée pour indiquer la version actuelle du code.

```java
/**
 * La classe Calculator effectue des opérations arithmétiques simples.
 * ...
 * @version 1.0
 * ...
 */
public class Calculator {

````


`@since`

Indique la version depuis laquelle l'élément (classe, méthode, etc.) est disponible.

```java
/**
 * La classe Calculator effectue des opérations arithmétiques simples.
 * ...
 * @since 28-06-2024
 * ...
 */
public class Calculator {

````



`@param`

Décrit un paramètre d'une méthode, indiquant son nom et une brève description.


```java
/**
 * Additionne deux nombres entiers.
 * @param a Le premier nombre
 * @param b Le deuxième nombre
 * @return La somme de a et b
 */
public int add(int a, int b) {
    return a + b;
}

````




`@return`

Décrit la valeur de retour d'une méthode.


```java
/**
 * Additionne deux nombres entiers.
 * ...
 * @return La somme de a et b
 */
public int add(int a, int b) {
    return a + b;
}

````




`@throws` ou `@exception`

Indique les exceptions que la méthode peut lancer.


```java
/**
 * Divise le premier nombre par le deuxième.
 * ...
 * @throws ArithmeticException si b est égal à zéro
 */
public double divide(int a, int b) throws ArithmeticException {
    if (b == 0) {
        throw new ArithmeticException("Division par zéro");
    }
    return (double) a / b;
}

````




`@see`

Fournit une référence vers une autre partie de la documentation, souvent une autre méthode ou classe.


```java
/**
 * Méthode principale pour tester la classe Calculator.
 * ...
 * @see #add(int, int)
 * @see #subtract(int, int)
 * @see #multiply(int, int)
 * @see #divide(int, int)
 */
public static void main(String[] args) {
    Calculator calculator = new Calculator();
    System.out.println("Addition: " + calculator.add(5, 3));
    System.out.println("Soustraction: " + calculator.subtract(5, 3));
    System.out.println("Multiplication: " + calculator.multiply(5, 3));
    try {
        System.out.println("Division: " + calculator.divide(5, 3));
    } catch (ArithmeticException e) {
        System.out.println("Erreur: " + e.getMessage());
    }
}

````

Voici un exemple de code complet en Java qui utilise toutes les balises Javadoc courantes:



```java

/**
 * La classe Calculator effectue des opérations arithmétiques simples.
 * <p>
 * Elle fournit des méthodes pour additionner, soustraire, multiplier et diviser des nombres.
 * </p>
 * 
 * @author JOlivier Fabre
 * @version 1.0
 * @since 2024-06-28
 */
public class Calculator {

    /**
     * Additionne deux nombres entiers.
     *
     * @param a Le premier nombre
     * @param b Le deuxième nombre
     * @return La somme de a et b
     */
    public int add(int a, int b) {
        return a + b;
    }

    /**
     * Soustrait le deuxième nombre du premier.
     *
     * @param a Le nombre duquel on soustrait
     * @param b Le nombre à soustraire
     * @return La différence entre a et b
     */
    public int subtract(int a, int b) {
        return a - b;
    }

    /**
     * Multiplie deux nombres entiers.
     *
     * @param a Le premier nombre
     * @param b Le deuxième nombre
     * @return Le produit de a et b
     */
    public int multiply(int a, int b) {
        return a * b;
    }

    /**
     * Divise le premier nombre par le deuxième.
     * <p>
     * Cette méthode lance une {@link ArithmeticException} si le diviseur est zéro.
     * </p>
     *
     * @param a Le dividende
     * @param b Le diviseur
     * @return Le quotient de a divisé par b
     * @throws ArithmeticException si b est égal à zéro
     */
    public double divide(int a, int b) throws ArithmeticException {
        if (b == 0) {
            throw new ArithmeticException("Division par zéro");
        }
        return (double) a / b;
    }

    /**
     * Méthode principale pour tester la classe Calculator.
     *
     * @param args Les arguments de la ligne de commande
     * @see #add(int, int)
     * @see #subtract(int, int)
     * @see #multiply(int, int)
     * @see #divide(int, int)
     */
    public static void main(String[] args) {
        Calculator calculator = new Calculator();
        System.out.println("Addition: " + calculator.add(5, 3));
        System.out.println("Soustraction: " + calculator.subtract(5, 3));
        System.out.println("Multiplication: " + calculator.multiply(5, 3));
        try {
            System.out.println("Division: " + calculator.divide(5, 3));
        } catch (ArithmeticException e) {
            System.out.println("Erreur: " + e.getMessage());
        }
    }
}

```


#### Génération de la documentation Javadoc

Pour générer la documentation à l'aide de Javadoc, vous utilisez la commande javadoc suivie du nom des fichiers source ou des options de paquet. 

```bash
javadoc -d doc src/*.java
```

Cette commande génère la documentation dans le répertoire doc pour tous les fichiers Java situés dans le répertoire src. Javadoc génère ainsi des fichiers HTML qui peuvent être consultés dans un navigateur web. La documentation générée inclut une description des classes et des méthodes, ainsi que les commentaires Javadoc associés.  







