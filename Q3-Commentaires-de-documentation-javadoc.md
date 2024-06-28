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
 * @author John Doe
 * ...
 */
public class Calculator {

````



