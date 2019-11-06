class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #04 - 31.10.19

Fragen zur Vorlesung

Wiederholung: if - else if - else

Wiederholung: Schleifen

Arrays in Java

Zufällige Zahlen generieren

Implementierung: Hangman

Wie gehen die Hausaufgaben?

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, left

## Wiederholung: if - else if - else

```java
boolean shouldPrint = true;

if (!shouldPrint) {
  System.out.println("sorry dave i'm afraid i can't do that");
} else {
  System.out.println("victory royale");
}

```

### Was wird ausgegeben?

---

class: middle, left

## Wiederholung: if - else if - else

```java
boolean shouldPrint = false;
boolean detour = true;

if (shouldPrint) {
  System.out.println("sorry dave i'm afraid i can't do that");
} else if (detour) {
  System.out.println("well");
} else {
  System.out.println("victory royale");
}

System.out.println("done!");

```

### Was wird ausgegeben?

---

class: middle, left

## Wiederholung: if - else if - else

```java
boolean shouldPrint = true;
boolean detour = true;

if (shouldPrint) {
  System.out.println("sorry dave i'm afraid i can't do that");
} else if (detour) {
  System.out.println("well");
} else {
  System.out.println("victory royale");
}

System.out.println("done!");
```

### Was wird ausgegeben?

---

class: middle, left

## Wiederholung: if - else if - else

```java
boolean shouldPrint = true;
boolean detour = true;

if (shouldPrint) {
  System.out.println("sorry dave i'm afraid i can't do that");
} else if (detour) {
  System.out.println("well");
} else {
  System.out.println("victory royale");
}

System.out.println("done!");
```

#### Nur einer der Codepfade wird ausgeführt

---

class: middle, left

## Wiederholung: if - else if - else

```java
boolean shouldPrint = true;
boolean detour = false;

if (shouldPrint) {
  System.out.println("sorry dave i'm afraid i can't do that");
}

if (detour) {
  System.out.println("well");
} else {
  System.out.println("victory royale");
}
```
---

class: middle, left

## Wiederholung: Schleifen

```java
boolean repeat = true;
while (repeat) {
  // wird für immer ausgeführt
}
```

#### while (BEDINGUNG) { CODE }

---

class: middle, left

## Wiederholung: Schleifen

```java
boolean repeat = true;
int counter = 0;
while (repeat) {
  counter++;
  System.out.println(counter);
  if (counter >= 10) {
    break;
  }
}
```

#### break; kann Schleifen unterbrechen

---

class: middle, left

## Wiederholung: Schleifen

```java
boolean repeat = true;
int counter = 0;
while (repeat) {
  counter++;
  if (counter < 5) {
    continue;
  }

  System.out.println(counter);
  if (counter >= 10) {
    break;
  }
}
```

#### continue; überspringt eine Iteration

---

class: middle, left

## Wiederholung: Schleifen

```java
boolean repeat = false;

while (repeat) {
  // ...
}
```

#### Wenn die Bedingung nicht stimmt, wird der Inhalt nie ausgeführt

---

class: middle, left

## Wiederholung: Schleifen

```java
boolean repeat = false;

do {
  // ...
} while (repeat)
```

#### do {} while() hingegen führt den Code mindestens 1mal aus und überprüft danach die Bedingung

---

class: middle, left

## Wiederholung: Schleifen

```java
for (int counter = 0; counter < 10; counter++) {
  System.out.println(counter);
}
```

#### for-Schleifen bestehen aus 3 Teilen
#### for (ZUWEISUNG; BEDINGUNG; AUSDRUCK) { CODE }

---

class: middle, left

## Wiederholung: Schleifen

```java
for (int counter = 0; counter <= 10; counter++) {
  System.out.println(counter);
}
// als while
int counter = 0;
while (counter <= 10) {
  System.out.println(counter);
  counter++;
}
```

#### Platzsparend!

---

class: middle, left

## Arrays in Java

#### Arrays beschreiben (An-)Sammlungen an Elementen
#### Die Größe von Arrays ist nicht änderbar

```java
String[] namen = { "Kimon", "Max" };

System.out.println(namen.length); // 2

for (String name : namen) {
  System.out.println(name);
}
// 1. Iteration -> Kimon
// 2. Iteration -> Max
```

---

class: middle, left

## Arrays in Java

#### Arrays können nur Daten vom angegeben Datentyp enthalten

```java
String[] namen = { "Kimon", 2 };
```

#### ^ ERROR: Type mismatch

---

class: middle, left

## Zufällige Zahlen generieren

#### Wir benötigen die Random-Klasse in Java

```java
import java.util.Random;
```

#### Die Methoden einer Random-Instanz geben uns zufällige Werte. Je nach Methode kann man auch einen Limit setzen

```java
Random rand = new Random();
System.out.println(rand.nextInt());
System.out.println(rand.nextInt(10));
```

---

class: middle, left

## Implementierung: Hangman

#### Wie könnte man das Spiel Hangman mit den besprochenen Elementen umsetzen?

#### [Aufgabe + Lösung hier](https://github.com/HeyItsBATMAN/JavaProg-WiSe-19-20/blob/master/Hangman.zip)

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit
