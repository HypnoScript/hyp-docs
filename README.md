# HypnoScript

**HypnoScript** ist eine esoterische, TypeScript-inspirierte Sprache mit hypnotischem Flair.

## Inhaltsverzeichnis

- [HypnoScript](#hypnoscript)
	- [Inhaltsverzeichnis](#inhaltsverzeichnis)
	- [Einleitung](#einleitung)
	- [Grundaufbau](#grundaufbau)
		- [Lexikalische Struktur](#lexikalische-struktur)
		- [Schlüsselwörter](#schlüsselwörter)
		- [Operatoren und Sonderzeichen](#operatoren-und-sonderzeichen)
		- [Bezeichner (Identifier)](#bezeichner-identifier)
		- [Literale](#literale)
	- [Syntax](#syntax)
		- [Programmstruktur](#programmstruktur)
		- [Deklarationen](#deklarationen)
		- [Kontrollstrukturen](#kontrollstrukturen)
		- [Blöcke](#blöcke)
		- [Erweiterte Konzepte](#erweiterte-konzepte)
	- [Grammatik (EBNF)](#grammatik-ebnf)
	- [Semantik](#semantik)
	- [Beispielprogramme](#beispielprogramme)
		- [Einfaches „Hello Trance!“](#einfaches-hello-trance)
	- [Summierung mit Input](#summierung-mit-input)
	- [Verwendung erweiterter Konzepte](#verwendung-erweiterter-konzepte)

## Einleitung

**HypnoScript** ist eine minimalistische, esoterische Sprache, die sich an die Syntax von TypeScript/JavaScript anlehnt und dabei alle möglichen Klischees rund um Hypnose, Trance und hypnotische Induktion verwendet. Trotz des humorvollen Charakters ist sie auf Turing-Vollständigkeit ausgelegt und unterstützt Variablen, Schleifen, bedingte Anweisungen, Funktionen, Objektorientierung (als _Session-Konzept_) und diverse Sprach-Gimmicks im hypnotischen Stil.

## Grundaufbau

### Lexikalische Struktur

- **Groß- und Kleinschreibung**: Schlüsselwörter sind case-sensitive und stets in Kleinschreibung.
- **Kommentare**: Einzeilig (`// Kommentar`) und mehrzeilig (`/* ... */`).

### Schlüsselwörter

Beispiele für Schlüsselwörter sind `Focus`, `Relax`, `if`, `else`, `while`, `loop`, `suggestion`, `awaken`, `induce`, `observe`, `trance`, `session`, `constructor`, `drift`, `tranceify`, etc.

### Operatoren und Sonderzeichen

- **Zuweisung**: `=`
- **Arithmetisch**: `+`, `-`, `*`, `/`, `%`
- **Vergleich**: `==`, `!=`, `>`, `>=`, `<`, `<=`
- **Logisch**: `&&`, `||`, `!`
- **Trennzeichen/Klammern**: `;`, `,`, `(`, `)`, `{`, `}`, `[`, `]`

### Bezeichner (Identifier)

Bezeichner beginnen mit einem Buchstaben `a-z`/`A-Z` oder `_` und können beliebige Buchstaben, Ziffern `0-9` oder `_` enthalten.

### Literale

- **Numerisch**: `42`, `3.14`
- **String**: `"Hello Trance!"`
- **Boolean**: `true`, `false`

## Syntax

### Programmstruktur

Ein einfaches HypnoScript-Programm wird von `Focus { ... } Relax` umschlossen. Innerhalb dieses Blocks stehen Deklarationen, Funktionen und Anweisungen.

### Deklarationen

- **Variablen**: `induce x: number = 5;`
- **Funktionen**: `suggestion add(a: number, b: number): number { awaken a + b; }`

### Kontrollstrukturen

- **Bedingung**: `if (x > 0) { observe "x ist positiv"; } else { observe "x ist nicht positiv"; }`
- **Schleifen**: `while (counter < 10) { observe counter; counter = counter + 1; }`

### Blöcke

Blöcke werden mit `{ ... }` oder optional `deepFocus { ... }` umschlossen.

### Erweiterte Konzepte

- **Objektorientierung**: `session Person { ... }`
- **Warte-Mechanismus**: `drift(ms)`
- **Hypnotische Operator-Synonyme**: `youAreFeelingVerySleepy` statt `==`
- **Benutzerdefinierte Strukturen/Typen**: `tranceify HypnoRecord { ... }`

## Grammatik (EBNF)

Eine beispielhafte EBNF-Skizze, die die Kernsyntax abbildet, ist in der `DEFINITION.md` enthalten.

## Semantik

- **Variablen und Scope**: Variablen sind innerhalb des Blockes und seiner Unterblöcke sichtbar.
- **Ein- / Ausgabe**: `observe expr;` gibt den Wert von `expr` aus.
- **Turing-Vollständigkeit**: Schleifen, Rekursion und bedingte Verzweigungen ermöglichen Turing-Vollständigkeit.

## Beispielprogramme

### Einfaches „Hello Trance!“

```hypnoscript
Focus {
  entrance {
      observe "Starte jetzt das HypnoScript-Programm...";
  }
  induce greeting: string = "Hello Trance!";
  induce counter: number = 0;
  suggestion repeatGreet(times: number) {
      while (times > 0) {
          observe greeting;
          times = times - 1;
      }
  }
  repeatGreet(3);
} Relax
```

## Summierung mit Input

```hypnoscript
Focus {
  induce n: number from external;
  induce sum: number = 0;
  loop (induce i: number = 1; i <= n; i = i + 1) {
      sum = sum + i;
  }
  observe "Die Summe von 1 bis " + n + " ist " + sum;
} Relax
```

## Verwendung erweiterter Konzepte

```hypnoscript
Focus {
  entrance {
      observe "Willkommen in der tiefen Hypno-Welt...";
      drift(2000);
      observe "Wir werden nun zwei Personen hypnotisieren!";
  }
  session Person {
      expose name: string;
      suggestion constructor(newName: string) {
          this.name = newName;
      }
      suggestion greet() {
          observe "Du fühlst dich sehr entspannt, " + this.name;
      }
      suggestion slowGreet() {
          greet();
          observe "... Warte kurz ...";
          drift(1500);
      }
  }
  induce alice = Person("Alice");
  induce bob   = Person("Bob");
  induce x: number = 5;
  induce y: number = 5;
  if (x youAreFeelingVerySleepy y) {
      observe "x ist gleich y!";
  }
  alice.slowGreet();
  bob.slowGreet();
} Relax
```
