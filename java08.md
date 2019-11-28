class: middle, center

# Programmierpraktikum Java I im WiSe 2019/20

---

class: middle, center

# Sitzung #08 - 27.11.19

Fragen zur Vorlesung

Wiederholung: Packages

Wiederholung: Klassen

Wiederholung: Vererbung

Wiederholung: abstrakte Klassen

Wiederholung: @Override von Methoden

Wiederholung: final

Wie gehen die Hausaufgaben?

---

class: middle, center

# Fragen zur Vorlesung

## Falls ihr Fragen habt
## kai.niebes@uni-koeln.de

---

class: middle, left

### Wiederholung: Packages

#### Was sind Packages?

#### Warum benutzen Packages?

---

class: middle, left

### Wiederholung: Packages

#### Was sind Packages?

#### Im Prinzip einfach nur Ordner. Wenn wir uns den Projektordner auf unseren PCs anschauen sehen wir, dass Packages die Unterordner sind

---

class: middle, left

### Wiederholung: Packages

#### Warum benutzen Packages?

#### Für eine klare Unterteilung unserer Klassen. In Java erstellen wir viele Klassen (und Interfaces)

---

class: middle, left

### Wiederholung: Klassen

#### Klassen sind in OOP unser Werkzeug, mit dem wir Zusammenhänge, die wir aus der echten Welt kennen, modellieren
#### Wenn wir mittels Klassen z.B. einen Hund modelliert haben, können wir einzelne Hunde erzeugen. Diese nennen wir dann "Instanzen" oder "Objekte" in OOP

---

class: middle, left

### Wiederholung: Klassen

#### Eine valide Klasse benötigt nicht viel

```java
public class Hund {
  // Klassenvariablen sind typischerweise am Anfang

  // Constructor folgt typischerweise den Klassenvariablen

  // Klassenmethoden sind typischerweise am Ende
}
```

---

class: middle, left

### Wiederholung: Klassen

```java
public class Hund {
  // Klassenvariablen sind typischerweise am Anfang
  private String name;
  private int alter;

  // Constructor folgt typischerweise den Klassenvariablen
  public Hund(String name, int alter) {
    this.name = name;
    this.alter = alter;
  }

  // Klassenmethoden sind typischerweise am Ende
  public String getName() {
    return this.name;
  }
}
```

---

class: middle, left

### Wiederholung: Vererbung

#### Wenn wir nun eine Katze mit einer Klasse modellieren wollen, fällt uns auf, dass sich die meisten Felder (Variablen & Methoden) überschneiden werden.

#### Deshalb können wir die Felder, welche sich überschneiden, in eine übergeordnete Klasse packen

---

class: middle, left

### Wiederholung: Vererbung

```java
public class Tier {
  private String name;
  private int alter;

  public Tier(String name, int alter) {
    this.name = name;
    this.alter = alter;
  }

  // ...
}
```

---

class: middle, left

### Wiederholung: Vererbung

#### Jetzt können wir Hund und Katze als Erweiterung von Tier modellieren

#### Dies nennt man Vererbung. Erbende Klassen, auch Subklassen genannt, erben alle Felder (Variablen & Methoden) der Elternklasse, auch Superklasse genannt


---

class: middle, left

### Wiederholung: Vererbung

#### Wir müssen unsere Subklassen 'extenden':

```java
public class Hund extends Tier {

}
```

```java
public class Katze extends Tier {

}
```

---

class: middle, left

### Wiederholung: Vererbung

#### Jetzt können wir unsere Subklassen erweitern, ohne dass es unübersichtlich wird

```java
public class Hund extends Tier {
  public void stockHolen() {}
}
```

```java
public class Katze extends Tier {
  public void miauen() {}
  public void kratzen() {}
  public void schnurren() {}
}
```

---

class: middle, left

### Wiederholung: abstrakte Klassen

#### Nicht alle Klassen die wir als übergeordnete Zusammenfassung modellieren (wie z.B. die Tier Klasse) wären als Objekte nützlich. Wir benutzen sie nur, um von ihnen zu erben.

#### Die Tierklasse ist für uns als Objekt/Instanz nicht zu gebrauchen.

#### Deshalb können wir abstrakte Klassen erzeugen.

#### Abstrakte Klassen sind nur für die Vererbung gedacht.

---

class: middle, left

### Wiederholung: abstrakte Klassen

#### Eine abstrakte Klasse erzeugen wir mit "abstract"

```java
public abstract class Tier {
  private String name;
  private int alter;

  public Tier(String name, int alter) {
    this.name = name;
    this.alter = alter;
  }

  // ...
}
```

---

class: middle, left

### Wiederholung: abstrakte Klassen

#### Wir können die Kinder/Subklassen von abstrakten Klassen dazu zwingen, bestimmte Methoden zu implementieren. Dies ist dafür gedacht, wenn alle Subklassen etwas gemeinsam haben, aber sich diese Gemeinsamkeit inhaltlich unterscheidet

```java
public abstract class Tier {
  // ...

  // nicht alle Tiere essen dasselbe, aber alle Tiere essen etwas
  public abstract void wasEsseIch();
}
```

---

class: middle, left

### Wiederholung: @Override von Methoden

#### Falls Methoden in Superklassen schon implementiert sind, aber diese nicht zur Subklasse passen, können wir diese mit einem @Override in der Subklasse überschreiben

#### Jede Klasse ist Subklasse von Javas Object, welches die Methoden toString() und equals(Object obj) implementiert. Diese überschreiben wir typischerweise mit eigenen, sinnvolleren Implementierungen.

```java
public abstract class Tier {
  // ...

  @Override
  public String toString() {
    return "Mein Name ist " + this.name;
  }
}
```

---

class: middle, left

### Wiederholung: final

#### Mit final können wir festlegen, dass:

#### Primitive Variablen für _immer_ unveränderbar sind

#### Komplexe Variablen in ihrer Referenz nicht änderbar sind

---

class: middle, left

### Wiederholung: final

```java
import de.example.Spielzeug;
import de.example.Ball;

public class Hund extends Tier {
  // Hunde sind immer supersüß, also geben wir dem boolean das final-Keyword
  private final boolean supercute = true;

  // Das hier erstellte Ballobjekt wird für immer der Lieblingsball sein
  private final Spielzeug ball = new Ball();

  // Die Felder vom komplexen Typ Ball sind aber noch veränderbar
  public void mitBallSpielen() {
    this.ball.setZustand(this.ball.getZustand() - 1);
  }
}
```

---

class: middle, center

# Wie gehen die Hausaufgaben?

---

class: center, middle

# Danke für eure Aufmerksamkeit
