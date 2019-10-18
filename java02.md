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

# Jetbrains IntelliJ als IDE

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
void
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
```

---

class: middle, left

# Loops/Iterationen am Beispiel von Listen

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

```

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

---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

namen.forEach(name -> System.out.println(name));
```

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

namen[0] // -> Kimon?
```
---

class: middle, left

```java
List<String> namen = new ArrayList<String>();

namen.add("Kimon");
namen.add("Max");

namen[0] // -> Kimon? Error :(
```
---

class: middle, left

```java
String[] namen = new String[]{"Kimon", "Max"};

System.out.println(namen[0]);
// Kimon

System.out.println(namen.length);
// 2
```
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
