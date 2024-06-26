### Java dispose de types primitifs pour représenter les entiers, les flottants, les caractères et les booléens. 
### Mais qu'appelle t-on vraiement type primitif ?   

En Java, les types primitifs sont des types de données de base intégrés au langage. Ils sont appelés "primitifs" parce qu'ils ne sont pas des objets et n'ont pas de méthodes associées. Les types primitifs sont gérés directement par le langage et offrent une manière simple et efficace de manipuler des données.  

#### Les types primitifs en Java sont les suivants:

- byte: un entier signé sur 8 bits. Plage de valeurs : -128 à 127.
- short: un entier signé sur 16 bits. Plage de valeurs : -32,768 à 32,767.
- int: un entier signé sur 32 bits. Plage de valeurs : -2^31 à 2^31-1.
- long: un entier signé sur 64 bits. Plage de valeurs : -2^63 à 2^63-1.
- float: un nombre à virgule flottante simple précision sur 32 bits.
- double: un nombre à virgule flottante double précision sur 64 bits.
- char: un caractère Unicode sur 16 bits. Plage de valeurs : '\u0000' (ou 0) à '\uffff' (ou 65,535).
- boolean: représente une valeur booléenne, soit true ou false.
  

Attention 'String' n'est pas un type primitif mais une classe.  

```java

public class PrimitivesExample {
    public static void main(String[] args) {
        // Types entiers
        byte myByte = 100;
        short myShort = 1000;
        int myInt = 100000;
        long myLong = 1000000000L;

        // Types à virgule flottante
        float myFloat = 3.14f;
        double myDouble = 3.141592653589793;

        // Type caractère
        char myChar = 'A';

        // Type booléen
        boolean myBoolean = true;

        // Affichage des valeurs
        System.out.println("byte: " + myByte);
        System.out.println("short: " + myShort);
        System.out.println("int: " + myInt);
        System.out.println("long: " + myLong);
        System.out.println("float: " + myFloat);
        System.out.println("double: " + myDouble);
        System.out.println("char: " + myChar);
        System.out.println("boolean: " + myBoolean);
    }
}

```

