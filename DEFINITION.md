# **HypnoScript** – Eine esoterische, TypeScript-inspirierte Sprache mit hypnotischem Flair

---

## **Inhaltsverzeichnis**

- [**HypnoScript** – Eine esoterische, TypeScript-inspirierte Sprache mit hypnotischem Flair](#hypnoscript--eine-esoterische-typescript-inspirierte-sprache-mit-hypnotischem-flair)
  - [**Inhaltsverzeichnis**](#inhaltsverzeichnis)
  - [**1. Einleitung**](#1-einleitung)
  - [**2. Grundaufbau**](#2-grundaufbau)
    - [2.1 Lexikalische Struktur](#21-lexikalische-struktur)
    - [2.2 Schlüsselwörter](#22-schlüsselwörter)
    - [2.3 Operatoren und Sonderzeichen](#23-operatoren-und-sonderzeichen)
    - [2.4 Bezeichner (Identifier)](#24-bezeichner-identifier)
    - [2.5 Literale](#25-literale)
  - [**3. Syntax**](#3-syntax)
    - [3.1 Programmstruktur](#31-programmstruktur)
    - [3.2 Deklarationen](#32-deklarationen)
      - [3.2.1 Variablen – `induce`](#321-variablen--induce)
      - [3.2.2 Funktionen – `suggestion`](#322-funktionen--suggestion)
    - [3.3 Kontrollstrukturen](#33-kontrollstrukturen)
      - [3.3.1 Bedingung – `if` / `else`](#331-bedingung--if--else)
      - [3.3.2 Schleifen – `while`, `loop`](#332-schleifen--while-loop)
    - [3.4 Blöcke](#34-blöcke)
    - [3.5 **Erweiterte Konzepte**](#35-erweiterte-konzepte)
      - [3.5.1 Objektorientierung: `session`](#351-objektorientierung-session)
      - [3.5.2 Warte-Mechanismus: `drift(ms)`](#352-warte-mechanismus-driftms)
      - [3.5.3 Hypnotische Operator-Synonyme](#353-hypnotische-operator-synonyme)
      - [3.5.4 Benutzerdefinierte Strukturen/Typen: `tranceify`](#354-benutzerdefinierte-strukturentypen-tranceify)
      - [3.5.5 Weitere Gimmicks (optional)](#355-weitere-gimmicks-optional)
  - [**4. Grammatik (EBNF)**](#4-grammatik-ebnf)
  - [**5. Semantik**](#5-semantik)
    - [5.1 Variablen und Scope](#51-variablen-und-scope)
    - [5.2 Ein- / Ausgabe](#52-ein---ausgabe)
    - [5.3 Turing-Vollständigkeit](#53-turing-vollständigkeit)
  - [**6. Beispielprogramme**](#6-beispielprogramme)
    - [6.1 Einfaches „Hello Trance!“](#61-einfaches-hello-trance)
    - [6.2 Summierung mit Input](#62-summierung-mit-input)
    - [6.3 Verwendung erweiterter Konzepte](#63-verwendung-erweiterter-konzepte)
      - [6.3.1 `session`, `drift`, Operator-Synonyme](#631-session-drift-operator-synonyme)

---

## **1. Einleitung**

**HypnoScript** ist eine minimalistische, esoterische Sprache, die sich an die Syntax von TypeScript/JavaScript anlehnt und dabei alle möglichen Klischees rund um Hypnose, Trance und hypnotische Induktion verwendet.  
Trotz des humorvollen Charakters ist sie auf Turing-Vollständigkeit ausgelegt und unterstützt Variablen, Schleifen, bedingte Anweisungen, Funktionen, Objektorientierung (als _Session-Konzept_) und diverse Sprach-Gimmicks im hypnotischen Stil.

---

## **2. Grundaufbau**

### 2.1 Lexikalische Struktur

- **Groß- und Kleinschreibung**: In dieser Definition gehen wir davon aus, dass Schlüsselwörter case-sensitive sind und stets in **Kleinschreibung** geschrieben werden.  
- **Kommentare**:  
  - Einzeilig: `// Kommentar`  
  - Mehrzeilig: `/* ... */`

### 2.2 Schlüsselwörter

```plaintext
Focus, Relax,
if, else,
while, loop,
snap, sink,
suggestion, awaken, call,
entrance,
deepFocus,
induce,
observe,
trance,
from, external,
number, string, boolean,
true, false,
session, constructor,
expose, conceal, dominant,
drift,
youAreFeelingVerySleepy, lookAtTheWatch, fallUnderMySpell, 
tranceify,
mindLink, sharedTrance,
imperative
```

_(Die zusätzlichen hypnotischen Begriffe siehe Kapitel „Erweiterte Konzepte“.)_

### 2.3 Operatoren und Sonderzeichen

- **Zuweisung**: `=`  
- **Arithmetisch**: `+`, `-`, `*`, `/`, `%`  
- **Vergleich**: `==`, `!=`, `>`, `>=`, `<`, `<=` (ergänzt durch hypnotische Synonyme, siehe [3.5.3](#hypnotische-operator-synonyme))  
- **Logisch**: `&&`, `||`, `!`  
- **Trennzeichen/Klammern**: `;`, `,`, `(`, `)`, `{`, `}`, `[` , `]`

### 2.4 Bezeichner (Identifier)

- **Syntax**:  
  - Beginnend mit einem Buchstaben `a-z`/`A-Z` oder `_`  
  - Gefolgt von beliebigen Buchstaben, Ziffern `0-9` oder `_`  

Beispiele: `counter`, `myVar2`, `_hiddenField`.  
Schlüsselwörter dürfen nicht als Bezeichner verwendet werden.

### 2.5 Literale

- **Numerisch**: `42`, `3.14`  
- **String**: `"Hello Trance!"` (Escapes optional, z. B. `\"`)  
- **Boolean**: `true`, `false`  
- _(Optionaler Fantasietyp `trance` hat keine separaten Literale, kann aber als Typannotation dienen.)_

---

## **3. Syntax**

### 3.1 Programmstruktur

Ein einfaches HypnoScript-Programm wird von `Focus { ... } Relax` umschlossen. Innerhalb dieses Blocks stehen Deklarationen, Funktionen und Anweisungen.

Beispiel:

```plaintext
Focus {
    // Programmcode
} Relax
```

Optionale Besonderheit:  

- **`entrance { ... }`** kann als „Startblock“ dienen.  
  - Wenn vorhanden, wird der Code im `entrance`-Block zuerst ausgeführt.  
  - Ist kein `entrance`-Block definiert, wird das Programm z. B. von oben nach unten abgearbeitet oder folgt anderen Implementierungsdetails.

### 3.2 Deklarationen

#### 3.2.1 Variablen – `induce`

```plaintext
induce x: number = 5;
induce y: string = "Hallo";
```

- Mit oder ohne Initialisierung.  
- **Input**: `induce name: string from external;` – kann (fiktiv) einen Wert von außen einlesen.

#### 3.2.2 Funktionen – `suggestion`

```plaintext
suggestion add(a: number, b: number): number {
    awaken a + b;
}
```

- **Aufruf**:  

  ```plaintext
  add(2, 3);
  // oder
  call add(2, 3);
  ```

- **Rückgabe**: `awaken <Ausdruck>;` (analog zu `return`).  

_(Für Funktionen ohne Rückgabewert kann man wahlweise `imperative suggestion` verwenden, siehe [3.5](#erweiterte-konzepte).)_

### 3.3 Kontrollstrukturen

#### 3.3.1 Bedingung – `if` / `else`

```plaintext
if (x > 0) {
    observe "x ist positiv";
} else {
    observe "x ist nicht positiv";
}
```

- **`deepFocus`** als optionaler Ersatz für `{ }`-Blöcke:  

  ```plaintext
  if (counter > 5) deepFocus {
      observe "Counter > 5";
  } else deepFocus {
      observe "Counter <= 5";
  }
  ```

#### 3.3.2 Schleifen – `while`, `loop`

**while**:

```plaintext
while (counter < 10) {
    observe counter;
    counter = counter + 1;
}
```

**loop** (ähnlich `for` in C/JavaScript):

```plaintext
loop (induce i: number = 0; i < 5; i = i + 1) {
    observe i;
}
```

- **`snap;`**: bricht Schleife ab (analog `break`).  
- **`sink;`**: springt zum nächsten Durchlauf (analog `continue`).

### 3.4 Blöcke

- Geschweifte Klammern `{ ... }` oder optional `deepFocus { ... }` als Block.  
- Mehrere Anweisungen können in einem Block stehen.

### 3.5 **Erweiterte Konzepte**

#### 3.5.1 Objektorientierung: `session`

Ermöglicht „Klassen“ in HypnoScript:

```plaintext
session Person {
    expose name: string;
    conceal secretId: number;

    suggestion constructor(newName: string, id: number) {
        this.name = newName;
        this.secretId = id;
    }

    suggestion greet() {
        observe "Hello from " + this.name;
    }
}
```

- **Instanziierung**:

  ```plaintext
  induce p = Person("Alice", 123);
  p.greet();
  ```

- `expose`: Feld/Methoden sind öffentlich (zugreifbar von außen).  
- `conceal`: Feld/Methoden sind privat (nur innerhalb der Session).  
- **`constructor`**: Spezialmethode, die bei Instanzierung aufgerufen wird.  
- **`dominant suggestion`**: (optional) für statische Methoden (z. B. `MathWizard.power(a,b)`).  

#### 3.5.2 Warte-Mechanismus: `drift(ms)`

Fügt eine Verzögerung oder Blockade für `ms` Millisekunden ein:

```plaintext
observe "Starte Hypnose...";
drift(3000);
observe "...Nach 3 Sekunden geht's weiter.";
```

_(Implementierung abhängig von Interpreter/Runtime.)_

#### 3.5.3 Hypnotische Operator-Synonyme

Neben den üblichen `==`, `>`, `<` usw. können folgende Synonyme verwendet werden:

- **`youAreFeelingVerySleepy`** statt `==`  

  ```plaintext
  if (x youAreFeelingVerySleepy y) { ... }
  ```

- **`lookAtTheWatch`** statt `>`  
- **`fallUnderMySpell`** statt `<`  

_(Beliebige weitere Wortspiele für `!=`, `>=`, `<=` etc. sind denkbar.)_

#### 3.5.4 Benutzerdefinierte Strukturen/Typen: `tranceify`

Erlaubt das Definieren eigener Datensammlungen (Records oder einfache Objekte):

```plaintext
tranceify HypnoRecord {
    name: string;
    age: number;
    isInTrance: boolean;
}

induce r = HypnoRecord {
    name: "Alice",
    age: 30,
    isInTrance: true
};
observe r.name;
```

- Weist Felder per `{ feldname: wert, ... }` zu.  
- Intern kann dies wie eine _struct_ oder ein _Record_ behandelt werden.

#### 3.5.5 Weitere Gimmicks (optional)

- **`imperative suggestion`**: Eine Funktion ohne Rückgabewert (Prozedur).  
- **`mindLink "myLibrary.hyp";`**: Zum Import weiterer Module/Dateien.  
- **`sharedTrance`**: Globale Variablen-Definition.  
- **Sprünge** (Goto-ähnlich):  

  ```plaintext
  myLabel:
  observe "Label erreicht!";
  if (x < 10) sinkTo myLabel; 
  ```

  _(Extremes Feature – kann, muss aber nicht verwendet werden.)_

---

## **4. Grammatik (EBNF)**

Nachfolgend eine beispielhafte EBNF-Skizze, die die Kernsyntax (ohne alle Operator-Synonyme) abbildet. Die Synonyme (`youAreFeelingVerySleepy`, etc.) könnten in der Praxis direkt auf die Standardoperatoren gemappt werden.

```ebnf
Program         ::= "Focus" Block "Relax" ;

Block           ::= { Statement } ;

Statement       ::= VarDeclarationStatement
                  | ExpressionStatement
                  | IfStatement
                  | WhileStatement
                  | LoopStatement
                  | BreakStatement
                  | ContinueStatement
                  | FunctionDeclaration
                  | ReturnStatement
                  | ObserveStatement
                  | EntranceBlock
                  | SessionDeclaration
                  | TranceifyDeclaration
                  | BlockStatement
                  ;

BlockStatement  ::= ("deepFocus" |) "{" { Statement } "}" 
                  ;

EntranceBlock   ::= "entrance" BlockStatement ;

VarDeclarationStatement
                  ::= "induce" Identifier [ ":" Type ] [ "=" Expression ] ";"
                  | "induce" Identifier [ ":" Type ] "from" "external" ";" ;

ObserveStatement
                  ::= "observe" Expression ";" ;

IfStatement     ::= "if" "(" Expression ")" BlockStatement
                    [ "else" BlockStatement ] ;

WhileStatement  ::= "while" "(" Expression ")" BlockStatement ;

LoopStatement   ::= "loop" "(" [ VarDeclarationStatementNoSemicolon ] 
                             ";" Expression ";" Expression ")"
                    BlockStatement ;

BreakStatement  ::= "snap" ";" ;
ContinueStatement
                  ::= "sink" ";" ;

FunctionDeclaration
                  ::= ( "suggestion" | "imperative suggestion" | "dominant suggestion" )
                      Identifier "(" [ ParameterList ] ")" [ ":" Type ]
                      BlockStatement ;

ParameterList   ::= Parameter { "," Parameter } ;
Parameter       ::= Identifier [ ":" Type ] ;

ReturnStatement ::= "awaken" [ Expression ] ";" ;

ExpressionStatement
                  ::= Expression ";" ;

Expression      ::= AssignmentExpression ;

AssignmentExpression
                  ::= LogicalOrExpression [ "=" AssignmentExpression ] ;

LogicalOrExpression
                  ::= LogicalAndExpression
                      { "||" LogicalAndExpression } ;

LogicalAndExpression
                  ::= EqualityExpression
                      { "&&" EqualityExpression } ;

EqualityExpression
                  ::= RelationalExpression
                      { ( "==" | "!=" | "youAreFeelingVerySleepy" ) 
                          RelationalExpression } ; // Bsp. für Synonym

RelationalExpression
                  ::= AdditiveExpression
                      { ( ">" | ">=" | "<" | "<=" 
                          | "lookAtTheWatch" | "fallUnderMySpell" ) 
                          AdditiveExpression } ;

AdditiveExpression
                  ::= MultiplicativeExpression
                      { ( "+" | "-" ) MultiplicativeExpression } ;

MultiplicativeExpression
                  ::= UnaryExpression
                      { ( "*" | "/" | "%" ) UnaryExpression } ;

UnaryExpression ::= [ ("+" | "-" | "!") ] PrimaryExpression ;

PrimaryExpression
                  ::= Identifier
                  | Literal
                  | "(" Expression ")"
                  | FunctionCall
                  ;

FunctionCall    ::= [ "call" ] Identifier "(" [ ArgumentList ] ")" ;

ArgumentList    ::= Expression { "," Expression } ;

SessionDeclaration
                  ::= "session" Identifier "{" { SessionMember } "}" ;

SessionMember   ::= ( "expose" | "conceal" )? 
                    ( VarDeclarationStatementNoSemicolon 
                      | FunctionDeclaration 
                      | ConstructorDeclaration ) ;

ConstructorDeclaration
                  ::= "suggestion" "constructor" "(" [ ParameterList ] ")" 
                      BlockStatement ;

TranceifyDeclaration
                  ::= "tranceify" Identifier "{" { VarDefinition } "}" ;

VarDefinition   ::= Identifier ":" Type ";" ;

VarDeclarationStatementNoSemicolon
                  ::= "induce" Identifier [ ":" Type ] [ "=" Expression ]
                  | "induce" Identifier [ ":" Type ] "from" "external" ;

Literal         ::= NumericLiteral
                  | StringLiteral
                  | BooleanLiteral ;

NumericLiteral  ::= Digit { Digit } [ "." Digit { Digit } ] ;
StringLiteral   ::= '"' { <char außer '"' oder Zeilenumbruch> } '"' ;
BooleanLiteral  ::= "true" | "false" ;

Type            ::= "number" | "string" | "boolean" | "trance"
                  | Identifier ; // Für benutzerdefinierte Typen, struct-Namen etc.

Digit           ::= [0-9] ;
```

---

## **5. Semantik**

### 5.1 Variablen und Scope

- **`induce varName: type = expr;`**: Deklariert eine lokale Variable im aktuellen Block.  
- **Gültigkeit**: Variablen sind innerhalb des Blockes und seiner Unterblöcke sichtbar (lexikalischer Scope).  
- **Zuweisung**: `varName = expr;` ändert den Wert einer bereits deklarierten Variable.  
- **Eingabe**: `from external` simuliert Benutzer-/Dateiinput (Implementation abhängig).

### 5.2 Ein- / Ausgabe

- **`observe expr;`**: Gibt den Wert von `expr` (z. B. String, Zahl, boolean) an das „Trance-Log“ aus (Konsole, UI, etc.).  
- **`drift(ms);`**: Unterbricht / pausiert den Programmfluss (themenbedingt „Verzögerung in Trance“).  

### 5.3 Turing-Vollständigkeit

- **Schleifen (while, loop)** bzw. **Rekursion** ermöglichen beliebig lange bzw. wiederholende Prozesse.  
- **Bedingte Verzweigungen (if/else)** erlauben dynamische Pfadwahl.  
- **Variablen** speichern veränderbare Werte.  

Diese Faktoren reichen aus, um Turing-Vollständigkeit zu gewährleisten.

---

## **6. Beispielprogramme**

### 6.1 Einfaches „Hello Trance!“

```plaintext
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

**Erwartete Ausgabe**:

```
Starte jetzt das HypnoScript-Programm...
Hello Trance!
Hello Trance!
Hello Trance!
```

---

### 6.2 Summierung mit Input

```plaintext
Focus {

  // Fragt Benutzer nach einer Zahl, summiert von 1 bis zu dieser Zahl und gibt das Ergebnis aus
  induce n: number from external;
  induce sum: number = 0;

  loop (induce i: number = 1; i <= n; i = i + 1) {
      sum = sum + i;
  }

  observe "Die Summe von 1 bis " + n + " ist " + sum;

} Relax
```

_(Implementierungsspezifisch muss natürlich definiert sein, wie „from external“ den Wert für `n` erhält.)_

---

### 6.3 Verwendung erweiterter Konzepte

#### 6.3.1 `session`, `drift`, Operator-Synonyme

```plaintext
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

      // Hypnotische Verzögerung
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

  // Nutze Synonym: youAreFeelingVerySleepy für ==
  if (x youAreFeelingVerySleepy y) {
      observe "x ist gleich y!";
  }

  alice.slowGreet();
  bob.slowGreet();

} Relax
```
