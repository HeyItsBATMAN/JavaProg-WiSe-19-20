class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# 2. Sitzung - 17.10.19

Fragen zur Vorlesung

Jetbrains IntelliJ als IDE

Primitive Datentypen

Loops/Iterationen am Beispiel von Listen

Wie gehen die Hausaufgaben?

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, center

# Jetbrains IntelliJ als alternatives IDE

---

class: middle, center

# Primitive Datentypen

```java

// Ganzzahlen
byte
short
int
long

// Gleitkommazahlen
float
double

// Andere
boolean
char

```

---

class: middle, left

# Primitive Datentypen - Ganzzahlen

```java
byte forTinyNumbers = 127;
// -128 bis 127
short forSmallNumbers = 32 000;
// -32,768 bis 32,767
int forMostNumbers = 2 000 000 000;
// -2,147,483,648 bis 2,147,483,647
long forLargeNumbers = 9 000 000 000 000 000 000;
// -9,223,372,036,854,775,808 bis 9,223,372,036,854,775,807

System.out.println(Integer.MAX_VALUE);
// 2147483647
System.out.println(Integer.MAX_VALUE + 1);
// -2147483648

```


---

class: middle, left

# Primitive Datentypen - Gleitkommazahlen

```java
float precise = 0.1234567f;
// ~7 stellige Dezimalpräzision
double evenMorePrecise = 0.1234567890123456;
// ~16 stellige Dezimalpräzision
```

---

class: middle, left

# Primitive Datentypen - Andere

```java
boolean trueOrFalse = true;
// Kann nur true und false enthalten
boolean oneEqualsOne = 1 == 1;
// -> true
boolean oneDoesNotEqualTwo = 1 == 2;
// -> false

char singleCharacter = 'A';
// char wird mit einfachen Anführungsstrichen initialisiert
char doubleQuote = "A";
// ERROR

String foo = "Bar";
// String (kein primitiver Datentyp) wird mit doppelten Anführungsstrichen initialisiert
```

---

class: middle, left

# Loops/Iterationen am Beispiel von Listen

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

```

### Erstellen einer Liste
### Die Typen List und ArrayList werden aus java.util importiert
### Mit der Methode .add() fügen wir neue Elemente hinzu

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

System.out.println(namen.size());
// -> 2
System.out.println(namen.get(0));
// Kimon
System.out.println(namen.get(2));
// Error IndexOutOfBounds

```

### Das erste Element liegt in der Liste an der Stelle 0, also
### Kimon liegt auf Stelle 0
### Max liegt auf Stelle 1

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

for (int i = 0; i < namen.size(); i++) {
  System.out.println(namen.get(i));
}
```

### Klassische Schreibweise

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

for (String name : namen) {
  System.out.println(name);
}
```

### for-each Schreibweise

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

namen.remove(1);
```

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

namen[0] // -> Kimon? Error :(
```

### Ein Zugriff auf Elemente wie bei Arrays geht bei Listen nicht

---

class: middle, left

```java
String[] namen = new String[]{"Kimon", "Max"};

System.out.println(namen[0]);
// Kimon

System.out.println(namen.length);
// 2
```
### Java hat auch Arrays ähnlich den Arrays in JavaScript (BSI)
### allerdings bietet der Arrays-Typ weniger Methoden an, um damit zu arbeiten

---

class: middle, left

```java
boolean trueOrFalse = true;

if (trueOrFalse == true) {
  // Code zwischen { und } wird ausgeführt
  // wenn die Bedingung in der Klammer gültig ist
  System.out.println("https://www.youtube.com/watch?v=MCT80HJWQ2A");
} else {
  // Ansonsten, also nur, wenn ein if vorm else nicht ausgeführt wurde
  // wird dieser Code ausgeführt
  System.out.println("https://www.youtube.com/watch?v=GM-e46xdcUo");
}

```

---

class: middle, left

```java
boolean printFirstName = true;
boolean printSecondName = true;

if (printFirstName == true) {
  System.out.println("Max");
} else if (printSecondName == true) {
  System.out.println("Kimon");
} else {
  System.out.println("Keine Namen :(");
}

```

### Obwohl beide Bedingungen der ifs gültig sind wird nur "Max" ausgegeben

---

class: middle, left

```java
boolean printFirstName = true;
boolean printSecondName = true;

if (printFirstName == true) {
  System.out.println("Max");
}

if (printSecondName == true) {
  System.out.println("Kimon");
}

if (printFirstName == false && printSecondName == false) {
  System.out.println("Keine Namen :(");
}

```

### Jetzt werden beide Namen ausgegeben

---

class: middle, left

```java
boolean trueOrFalse = true;

if (trueOrFalse) {
  // ...
} else {
  // ...
}

```

### Das "== true" kann ausgelassen werden
### Das Programm vergleicht dann immer noch die Bedingung mit "== true",
### aber es muss nicht explizit geschrieben werden

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit

---

class: center, middle

# Bierle?

---
