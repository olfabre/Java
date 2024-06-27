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





### Sources utilisées pour cet article  
Livre "Programmer en Java : Couvre Java 10 à Java 14 Ed. 11" - Auteur: Delannoy, Claude - Editeur: Eyrolles - Année de Publication: 2020
