# Chiffren

# ADFG(V)X
**Beschreibung:**
**1. Phase: Substitution:**
Zu Beginn muss eine Matrix mit sechst Zeilen und Spalten gebildet werden. Jeder Buchstabe (A-Z) und die Ziffern 0-9 müsssen genau einmal eingetragen werden.
|  | A | D | F | G | V | X |
|---|---|---|---|---|---|---|
| **A** | J | E | 5 | C | L | 1 |
| **D** | D | 3 | 4 | 7 | A | 2 |
| **F** | X | N | S | 0 | U | P |
| **G** | M | F | K | Z | 8 | 9 |
| **V** | I | 6 | Q | V | W | B |
| **X** | T | G | Y | O | R | H |

Der Buchstabe G wird mit dieser Matrix mit XD ersetzt (Zeile X und Spalte D). Ein E wird mit AD ersetzt (Zeile A und Spalte D).
Klartext: Geheimnachricht
Substitution: XD AD XX AD VA GA FD DV AG XX XV VA AG XX XA

**2. Phase: Transposition:**
 Im 2. Schritt wird zuerst ein beliebiges Schlüsselwort gewählt (Hier: Mykey). Die Übersetzung nach der Substitution wird nun von links nach rechts unter das Schlüsselwort geschrieben. Meistens braucht es dafür mehrere Zeilen.
| M | Y | K | E | Y |
|---|---|---|---|---|
| X | D | A | D | X |
| X | A | D | V | A |
| G | A | F | D | D |
| V | A | G | X | X |
| X | V | V | A | A |
| G | X | X | X | A |

Die Spalten werden nun nach dem Alphabet sortiert. 
| E | K | M | Y | Y |
|---|---|---|---|---|
| D | A | X | D | X |
| V | D | X | A | A |
| D | F | G | A | D |
| X | G | V | A | X |
| A | V | X | V | A |
| X | X | G | X | A |

Um den Geheimtext zu erhalten, muss zum Schluss die Matrix wieder spaltenweise, von oben nach unten auslesen. 
Der endgültige Geheimtext lautet: „DV DX AX AD FG VX XX GV XG DA AA VX XA DX AA“.

# Caesar
Im 1. Schritt wird das Alphabet 2 Mal untereinander aufgeschrieben. Das untere Alphabet wird dabei um eine beliebige Anzahl verschoben. In diesem Beispiel wird es 3 nach links verschoben, also hat es den Schlüssel 3.

A  B  C  D  E  F  G  H  I  J  K  L  M  N  O  P  Q  R  S  T  U  V  W  X  Y  Z

D  E  F  G  H  I  J  K  L  M  N  O  P  Q  R  S  T  U  V  W  X  Y  Z  A  B  C

Ein A wird somit mit einem B ersetzt, ein B mit einem E und so weiter.

Klartext: Geheimnachricht
Schlüssel: 3
Verschlüsselter Text: Jhkhlpqdfkulfkw

Klartext: Geheimnachricht
Schlüssel: 5
Verschlüsselter Text: Ljmjnrsfhmwnhmy

# Atbash
Die Atbash-Chiffre kehrt die Buchstaben des Alphabets um: A wird Z, B wird Y, ..., Y wird B, Z wird A.

| A | B | C | D | E | F | G | H | I | J | K | L | M |
| - | - | - | - | - | - | - | - | - | - | - | - | - |
| Z | Y | X | W | V | U | T | S | R | Q | P | O | N |

Klartext: Geheimnachricht
Verschlüsselter Text: Tvsvrnmzxsirxsg

Nachteil: Es ist eine ziemlich einfache und berühmte Chiffre. Deshalb kann sie einfach geknackt werden.
