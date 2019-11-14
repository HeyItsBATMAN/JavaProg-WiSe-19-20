class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #06 - 14.11.19

Fragen zur Vorlesung

Wiederholung: Arrays

Mehrdimensionale Arrays

Implementierung: Doppelte Zahl in unsortiertem Array finden

Implementierung: Doppelte Zahlen in Arrays zählen

Implementierung: Bubblesort

Wie gehen die Hausaufgaben?

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, left

## Wiederholung: Arrays

#### Arrays beschreiben (An-)Sammlungen an Elementen
#### Die Größe von Arrays ist nicht änderbar

```java
String[] namen = { "Kimon", "Max" };

System.out.println(namen.length);

// OUTPUT:
// 2
```

---

class: middle, left

## Wiederholung: Arrays

#### Arrays können nur Daten vom angegeben Datentyp enthalten

```java
String[] namen = { "Kimon", 2 };
```

#### ^ ERROR: Type mismatch

---

class: middle, left

## Wiederholung: Arrays

```java
String[] namen = { "Kimon", "Max" };

System.out.println(namen.length);

// for each loop
for (String name : namen) {
  System.out.println(name);
}

// for loop
for (int i = 0; i < namen.length; i++) {
  System.out.println(namen[i]);
}

// OUTPUT:
// 2
// Kimon
// Max
// Kimon
// Max
```

---

class: middle, left

## Implementierung: Doppelte Zahl in unsortiertem Array finden

#### Gegeben sein ein int-Array in dem Zahlen zwischen 0 und 9 vorkommen, z.B. {9,1,2,5,4,3,2,8,7} wobei eine Zahl doppelt vorkommt. Jede andere Zahl kommt nur 1mal vor

#### Finde die doppelte Zahl

---

class: middle, left

## Implementierung: Doppelte Zahlen in Arrays zählen

#### Gegeben sein ein int-Array in dem Zahlen zwischen 0 und 9 vorkommen, z.B. {9,1,2,5,4,3,2,8,7,1,5,9,9}. Zahlen können mehrfach vorkommen

#### Zähle und gebe aus, wie oft die Zahlen vorkommen

---

class: middle, left

## Implementierung: Bubblesort

#### Gegeben sei ein int-Array in dem Zahlen vorkommen, z.B. {9,3,4,2,9,9,8,6,4,8,1,5,3,5,10,3,5,9,6,3}. Zahlen können mehrfach vorkommen

#### Sortiere die Zahlen aufsteigend, also die kleinste Zahl an erster Stelle und die höchste Zahl an letzter Stelle im ursprünglichen Array

---

class: middle, left

## Implementierung: Bubblesort

![Bubblesort](bubblesort.gif)

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit
