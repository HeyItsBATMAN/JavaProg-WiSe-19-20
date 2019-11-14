class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #05 - 07.11.19

Fragen zur Vorlesung

Wiederholung: switch-case

Wiederholung: Modulo-Operator

Implementierung: Höher oder Tiefer

Implementierung: FizzBuzz

Wie gehen die Hausaufgaben?

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, left

## Wiederholung: switch-case

#### Mit switch-case kann man eine Variable gegen mehrere Werte prüfen

```java
switch (WERT) {
  case "INHALT1":
    // Selbes wie if (WERT == "INHALT1")
    break;
  case "INHALT2":
    // Selbes wie if (WERT == "INHALT2")
    break;
  default:
    // Selbes wie else am Ende einer if-Kette
    break;
}
```

---

class: middle, left

## Wiederholung: switch-case

#### Mit switch-case lässt sich logisches ODER (||) sehr leicht darstellen

```java
switch (WERT) {
  case "INHALT1":
  case "INHALT2":
    // Selbes wie if (WERT == "INHALT1" || WERT == "INHALT2")
    break;
  default:
    // Selbes wie else am Ende einer if-Kette
    break;
}
```

---

class: middle, left

## Wiederholung: Modulo-Operator

#### Mit dem Modulo-Operator errechnet man den Rest einer Division

```java
int rest = 5 % 3;
System.out.println(rest) // 2
```

---

class: middle, left

## Wiederholung: Modulo-Operator

#### Eine häufige Verwendung für den Modulo-Operator ist zu prüfen, ob eine Zahl gerade oder ungerade ist

```java
int wert = 5;
boolean isEven = wert % 2 == 0;
boolean isOdd = wert % 2 == 1;
```

---

class: middle, left

## Implementierung: Höher oder Tiefer

---

class: middle, left

## Implementierung: FizzBuzz

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit
