class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #03 - 24.10.19

Fragen zur Vorlesung

Wiederholung: Vergleichsoperatoren

Wiederholung: Konditionaloperatoren

Sicherheitshinweis zu den Operatoren

Anwendungsbeispiel

Wiederholung: Nutzereingabe

Umwandlung von Strings zu Zahlen

Einstieg ins Error-Handling

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, left

# Wiederholung: Vergleichsoperatoren

|Operator|Function|
|-|-|
|==|Equal to|
|!=|Not equal to|
|>|Greater than|
|>=|Greater than or equal to|
|<|Less than|
|<=|Less than or equal to|

---

class: middle, left

### Wiederholung: Vergleichsoperatoren

```java
int a = 1;
int b = 2;

if (a == b) {
  System.out.println("a ist gleich b");
} else {
  System.out.println("a ist ungleich b");
}
```

#### a und b werden verglichen. Nur wenn die Werte exakt gleich sind, evaluiert der Vergleich zum Booleschen true


---

class: middle, left

### Wiederholung: Vergleichsoperatoren

```java
int a = 1;
int b = 2;

b = 3;

// ganz viel code

b = 1;

if (a == b) {
  System.out.println("a ist gleich b");
} else {
  System.out.println("a ist ungleich b");
}
```

#### An welcher Stelle sich die Werte ändern ist irrelevant. Es zählt der Wert zum Zeitpunkt des Aufrufs

---

class: middle, left

### Wiederholung: Vergleichsoperatoren

```java
int a = 1;
int b = 2;
boolean istGleich = a == b;

b = 3;

if (istGleich) {
  System.out.println("a ist gleich b");
} else {
  System.out.println("a ist ungleich b");
}
```
---

class: middle, left

### Wiederholung: Vergleichsoperatoren

```java
int a = 1;
int b = 2;
boolean istKleiner = a < b;
boolean istGrößer = a > b;

if (istKleiner) {
  System.out.println("a ist kleiner als b");
} else if (istGrößer) {
  System.out.println("a ist größer als b");
} else {
  System.out.println("a ist gleich b");
}
```

---

class: middle, left

### Wiederholung: Konditionaloperatoren

|Operator|Logic|
|-|-|
|&&|Conditional-AND|
|&#124;&#124;|Conditional-OR|
|?:|Ternary (shorthand for if-then-else statement)|

##### Der Ternär-Operator (oder auch bedingter Operator) dient zur Kurzschreibweise, aber es ist nicht notwendig diesen auswendig zu können

```java
int a = 1;
int b = 2;
int biggerNumber = (a >= b) ? a : b;
```
---

class: middle, left

### Wiederholung: Konditionaloperatoren
#### Wahrheitstabelle

##### && ist ein logisches UND
##### || ist ein logisches ODER

|a|b|Operator|Result|
|-|-|-|-|
|false|false|&&|false|
|true|false|&&|false|
|false|true|&&|false|
|true|true|&&|true|
|-|-|-|-|
|false|false|&#124;&#124;|false|
|true|false|&#124;&#124;|true|
|false|true|&#124;&#124;|true|
|true|true|&#124;&#124;|true|

---

class: middle, center

### Sicherheitshinweis zu den Operatoren

### Links ist richtig, rechts ist falsch

#### < ist nicht gleich <<
#### > ist nicht gleich >>
#### && ist nicht gleich &
#### || ist nicht gleich |

##### Die rechten Operatoren sind "Bitwise" und "Bit Shift" Operatoren und funktionieren ganz anders

---

class: middle, left

### Anwendungsbeispiel

```java
boolean führerschein = true;
boolean inProbezeit = false;
int alter = 17;

if (führerschein) {
  if (alter < 18) {
    System.out.println("Finger weg vom Alkohol!");
  } else {
    if (inProbezeit || alter < 21) {
      System.out.println("Finger weg vom Alkohol!");
    } else {
      System.out.println("1 Fahrerbier hehe");
    }
  }
} else {
  System.out.println("Finger weg vom Auto & vom Alkohol!");
}
```

---

class: middle, left

## Anwendungsbeispiel

### Codebeispiel in Eclipse

### Voriges Beispiel als Methode

---

class: middle, left

# Wiederholung: User Input

```java
// Anfang der Datei
import java.util.Scanner;

// Später im Programm
Scanner input = new Scanner(System.in);
```
#### Scanner ist Teil des java.util Pakets und muss importiert werden
#### Der Parameter System.in greift (einfach gesagt) auf die Texteingabe des Betriebssystems zu

---

class: middle, left

# Wiederholung: User Input

#### Scanner hat Methoden um die Texteingabe des Nutzers einzulesen und als Datentyp zurückzugeben

```java
Scanner input = new Scanner(System.in);

String text = input.nextLine();
int zahl = input.nextInt();
boolean zustand = input.nextBoolean();
```

---

class: middle, left

# Umwandlung von Strings zu Zahlen

```java
int zahl = (int)"2";
// Error: Cannot cast from String to int
```

#### Die Klasse Integer bietet mehrere Methoden hierfür an, z.B:

```java
int zahl = Integer.valueOf("2");
int zahl2 = Integer.parseInt("2");
```

---

class: middle, left

## Einstieg ins Error-Handling

### Kommt in der Vorlesung irgendwann noch im Detail
```java
try {
  // Probiere einen Codeblock auszuführen
} catch (Exception e) {
  // Falls der Code einen Fehler wirft, führe stattdessen diesen Code aus
}
```
#### Ist jetzt noch nicht super wichtig, wird aber in den Hausaufgaben angedeutet

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit

---

class: center, middle

# Bierle?
