class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #07 - 21.11.19

Fragen zur Vorlesung

Wiederholung: Arrays

Wiederholung: Mehrdimensionale Arrays

Wiederholung: for und for-each Schleifen

Wiederholung: Sichtbarkeit von Variablen einer Klasse

Wiederholung: Setter und Getter

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
#### Arrays können nur Daten vom angegeben Datentyp enthalten

```java
String[] namen = { "Kimon", "Max" };

System.out.println(namen.length);
// OUTPUT:
// 2
```

---

class: middle, left

### Wiederholung: Mehrdimensionale Arrays

#### Arrays können Arrays enthalten. Dies bezeichnet man als mehrdimensionale Arrays
#### Arrays können beliebig tief vernestet sein, z.B.
#### 2D
```java
int[][] zweidim = new int[3][2];
zweidim[0][1] = 1234;
```
#### 3D
```java
int[][][] dreidim = new int[3][2][2];
dreidim[0][1][1] = 1234;
```

---

class: middle, left

## Wiederholung: for und for-each Schleifen

```java
String[] namen = { "Kimon", "Max" };

// for each loop
for (String name : namen) {
  System.out.println(name);
}

// for loop
for (int i = 0; i < namen.length; i++) {
  System.out.println(namen[i]);
}
```

---

class: middle, left

### Wiederholung: for und for-each Schleifen

#### Mit vernesteten Loops kann man über die vernesteten/mehrdimensionalen Arrays iterieren.
#### for-each Loops können hier bei der Übersichtlichkeit helfen

```java
int[][] tabelle = { {1, 2, 3}, {4, 5, 6} };

for (int[] zeile : tabelle) {
  for (int spalte : zeile) {
    System.out.print(spalte);
  }
}

for (int i = 0; i < tabelle.length; i++) {
  for (int j = 0; j < tabelle[i].length; j++) {
    System.out.print(tabelle[i][j]);
  }
}
```

---

class: middle, left

### Wiederholung: Sichtbarkeit von Variablen einer Klasse

![Sichtbarkeit](sichtbarkeit.png)

#### Hinweis: "Subklassen" sind Teil von Vererbung und kommen erst in der nächsten Sitzung dran

---

class: middle, left

### Wiederholung: Setter und Getter

#### Setter und Getter werden in OOP-Sprachen üblicherweise benutzt um die "unsichtbaren" Variablen einer Klasse zu erreichen

```java
public class Person {
  private String name;

  public void setName(String newName) {
    name = newName;
  }

  public String getName() {
    return name;
  }
}
```

#### Aber warum nicht einfach das Feld "name" public machen?

---

class: middle, left

### Wiederholung: Setter und Getter

#### Wenn ein Feld, z.B. Name noch nicht gesetzt ist, kann man im Getter mit der Situation umgehen

```java
public class Person {
  private String name;

  public void setName(String newName) {
    name = newName;
  }

  public String getName() {
    if (!name || name == "") {
      return "Kein Name";
      // Oder z.B. eine Exception
    }
    return name;
  }
}
```

---

class: middle, left

### Wiederholung: Setter und Getter

#### Ebenso kann im Setter auf valide Werte geprüft werden

```java
public class Person {
  private String name;

  public void setName(String newName) {
    if (newName.length() == 0) {
      // Exception "Name zu kurz"
      return;
    }
    name = newName;
  }

  public String getName() {
    if (!name || name == "") {
      return "Kein Name";
      // Oder z.B. eine Exception
    }
    return name;
  }
}
```

---

class: middle, left

#### Wiederholung: Setter und Getter
#### Innerhalb einer Klasse kann man das Prefix "this" benutzen um explizit auf die Felder der Klasse zuzugreifen
#### Im Getter ist dies bei unserer Person nicht nötig, da es keinen Methoden-Parameter mit derselben Bezeichnung gibt

```java
public class Person {
  private String name;

  public void setName(String name) {
    if (name.length() == 0) {
      // Exception "Name zu kurz"
      return;
    }
    this.name = name;
  }

  public String getName() {
    if (!name || name == "") {
      return "Kein Name";
      // Oder z.B. eine Exception
    }
    return name;
  }
}
```

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit
