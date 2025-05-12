# DIS_CRUCIGRAMA
Las expresiones conformes a la gramática deben cumplir las siguientes condiciones: 
- Un crucigrama se especifica con el número que lo identifica, un título, y el número de filas y de columnas 
(en el ejemplo 13x13). El orden entre ellos puede ser cualquiera.

```
java
Se usó operador & para concatenar cadenas pero sin
importar el orden de los elementos.
```

- Se  describen  las  palabras  que  van  en  horizontal  y  en  vertical,  y  las  casillas  en  negro  que  los  separan.  Se
comienza definiendo todas las horizontales (across) y luego las verticales (down), pero también podría comenzar por las verticales.
```
java
elementos Across y Down una sola vez, elementos Black que separan. 
Para el orden, se usó el operador &
```

- La palabra reservada ‘at’ acompaña al número de fila (o de columna, dependiendo del bloque en el que se encuentre). La definición de la fila (o columna) termina con ‘.’.
```
java
Elemento Row que empieza por at, y está compuesta de elementos tipo Word o Black.
```
- Tras el número (de fila o columna) se enumeran los componentes de dicha fila o columna, separando con ‘;’.
Son casillas negras o palabras.  Las palabras se deben separar con una casilla negra como mínimo (black).
Las casillas negras pueden aparecer tanto antes como después de una palabra.
```
java
```
- Cuando hay casillas negras consecutivas hay dos maneras de definirlas: bien usando repetidamente la palabra
reservada black o bien indicando el número de casillas seguidas (por ejemplo, black 2 times).
```
java
La definición de elemento Black puede ser una palabra reservada o un número seguido de times.
```
- Al especificar las palabras, primero se indica la palabra solución y luego (tras la palabra reservada definition)
su definición correspondiente (la que se utiliza como pista para resolver el crucigrama).
```
java
La definición de elemento Word es una palabra ID seguida de definition y la definición STR.
```
- Los crucigramas pueden definirse para diferentes idiomas (inglés, alemán, español, o euskara) indicándolo
inicialmente. Los crucigramas serían monolingües, todas las palabras y definiciones en el idioma indicado.
```
java
El idioma se define al principio del crucigrama, y se usa un enum para definir los idiomas.
```
Podría pensarse en una mejora, en la que los crucigramas fueran multilingües, es decir, que palabras en
diferentes idiomas pudieran ir mezcladas (p.e. que en un crucigrama en inglés la segunda palabra de la línea
4 fuera en español) (ver segundo ejemplo mostrado).

El lenguaje a utilizar para describir las figuras que representan los crucigramas se deja en manos de la decisión de
cada grupo, siempre y cuando el lenguaje sea textual. No se pretende que las figuras sean perfectas.


