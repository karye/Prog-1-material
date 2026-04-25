## Prov: listor i Python

Du har fått i uppdrag att hjälpa en spelstudio. De behöver små listor för saker som karaktärsnamn, poäng, föremål och menyer.

I det här provet tränar du bara på två saker:

1. **Skapa listor** med text, tal eller blandat
2. **Skriva ut listor** med `print()`

**Regler**

* Använd bara **listor**, `print()` och ibland `input()`.
* Använd **inte** `sort()`, `append()`, index eller `len()`.
* Koden ska börja med en `print()`-rad som ser ut ungefär så här: `=== ... ===`.
* När du skriver ut en lista ska du ha **tydlig text framför**, till exempel: `print("Här är min lista med färger:", lista)`.

---

### Uppgift 1 – färger

**Uppgift:** Skapa en lista med tre färger och skriv ut listan.

**Exempel på körning:**

```text
=== Mina tre favoritfärger ===
Här är min lista med färger: ['röd', 'blå', 'grön']
```

**Facit:**

```python
print("=== Mina tre favoritfärger ===")
farger = ["röd", "blå", "grön"]
print("Här är min lista med färger:", farger)
```

---

### Uppgift 2 – djur

**Uppgift:** Skapa en lista med fyra djur och skriv ut listan.

**Exempel på körning:**

```text
=== Fyra djur i min lista ===
Här är min lista med djur: ['hund', 'katt', 'kanin', 'fisk']
```

**Facit:**

```python
print("=== Fyra djur i min lista ===")
djur = ["hund", "katt", "kanin", "fisk"]
print("Här är min lista med djur:", djur)
```

---

### Uppgift 3 – frukter

**Uppgift:** Skapa en lista med tre frukter och skriv ut listan.

**Exempel på körning:**

```text
=== Tre frukter jag valde ===
Här är min lista med frukter: ['äpple', 'banan', 'päron']
```

**Facit:**

```python
print("=== Tre frukter jag valde ===")
frukter = ["äpple", "banan", "päron"]
print("Här är min lista med frukter:", frukter)
```

---

### Uppgift 4 – skolämnen

**Uppgift:** Skapa en lista med tre skolämnen och skriv ut listan.

**Exempel på körning:**

```text
=== Tre skolämnen ===
Här är min lista med skolämnen: ['matte', 'svenska', 'idrott']
```

**Facit:**

```python
print("=== Tre skolämnen ===")
amnen = ["matte", "svenska", "idrott"]
print("Här är min lista med skolämnen:", amnen)
```

---

### Uppgift 5 – spel

**Uppgift:** Skapa en lista med tre spel och skriv ut listan.

**Exempel på körning:**

```text
=== Tre spel jag gillar ===
Här är min lista med spel: ['minecraft', 'roblox', 'mario kart']
```

**Facit:**

```python
print("=== Tre spel jag gillar ===")
spel = ["minecraft", "roblox", "mario kart"]
print("Här är min lista med spel:", spel)
```

---

### Uppgift 6 – tre tal

**Uppgift:** Skapa en lista med tre tal och skriv ut listan.

**Exempel på körning:**

```text
=== Tre tal i en lista ===
Här är min lista med tal: [3, 8, 1]
```

**Facit:**

```python
print("=== Tre tal i en lista ===")
tal = [3, 8, 1]
print("Här är min lista med tal:", tal)
```

---

### Uppgift 7 – fyra tal

**Uppgift:** Skapa en lista med fyra tal och skriv ut listan.

**Exempel på körning:**

```text
=== Fyra tal i en lista ===
Här är min lista med tal: [10, 20, 30, 40]
```

**Facit:**

```python
print("=== Fyra tal i en lista ===")
tal = [10, 20, 30, 40]
print("Här är min lista med tal:", tal)
```

---

### Uppgift 8 – poäng

**Uppgift:** Skapa en lista med fem poäng och skriv ut listan.

**Exempel på körning:**

```text
=== Mina poäng i spelet ===
Här är min lista med poäng: [0, 1, 2, 3, 4]
```

**Facit:**

```python
print("=== Mina poäng i spelet ===")
poang = [0, 1, 2, 3, 4]
print("Här är min lista med poäng:", poang)
```

---

### Uppgift 9 – blandat

**Uppgift:** Skapa en lista med text, tal och text. Skriv ut listan.

**Exempel på körning:**

```text
=== En blandad lista ===
Här är min blandade lista: ['ada', 12, 'katt']
```

**Facit:**

```python
print("=== En blandad lista ===")
lista = ["ada", 12, "katt"]
print("Här är min blandade lista:", lista)
```

---

### Uppgift 10 – tom lista

**Uppgift:** Skapa en tom lista och skriv ut listan.

**Exempel på körning:**

```text
=== Min tomma lista ===
Här är min lista just nu: []
```

**Facit:**

```python
print("=== Min tomma lista ===")
lista = []
print("Här är min lista just nu:", lista)
```

---

### Uppgift 11 – två färger med input

**Uppgift:** Fråga efter två färger med `input()`. Lägg dem i en lista och skriv ut listan.

**Exempel på körning:**

```text
=== Jag väljer två färger ===
Färg 1: röd
Färg 2: grön
Här är min lista med färger: ['röd', 'grön']
```

**Facit:**

```python
print("=== Jag väljer två färger ===")
f1 = input("Färg 1: ")
f2 = input("Färg 2: ")
farger = [f1, f2]
print("Här är min lista med färger:", farger)
```

---

### Uppgift 12 – tre djur med input

**Uppgift:** Fråga efter tre djur med `input()`. Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in tre djur ===
Djur 1: hund
Djur 2: katt
Djur 3: hamster
Här är min lista med djur: ['hund', 'katt', 'hamster']
```

**Facit:**

```python
print("=== Jag skriver in tre djur ===")
d1 = input("Djur 1: ")
d2 = input("Djur 2: ")
d3 = input("Djur 3: ")
djur = [d1, d2, d3]
print("Här är min lista med djur:", djur)
```

---

### Uppgift 13 – två tal med input

**Uppgift:** Fråga efter två tal med `input()`. Gör om till `int`, skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in två tal ===
Tal 1: 7
Tal 2: 12
Här är min lista med tal: [7, 12]
```

**Facit:**

```python
print("=== Jag skriver in två tal ===")
t1 = int(input("Tal 1: "))
t2 = int(input("Tal 2: "))
tal = [t1, t2]
print("Här är min lista med tal:", tal)
```

---

### Uppgift 14 – tre tal med input

**Uppgift:** Fråga efter tre tal med `input()`. Gör om till `int`, skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in tre tal ===
Tal 1: 3
Tal 2: 9
Tal 3: 1
Här är min lista med tal: [3, 9, 1]
```

**Facit:**

```python
print("=== Jag skriver in tre tal ===")
t1 = int(input("Tal 1: "))
t2 = int(input("Tal 2: "))
t3 = int(input("Tal 3: "))
tal = [t1, t2, t3]
print("Här är min lista med tal:", tal)
```

---

### Uppgift 15 – namn med input

**Uppgift:** Fråga efter två namn. Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in två namn ===
Namn 1: Lin
Namn 2: Omar
Här är min lista med namn: ['Lin', 'Omar']
```

**Facit:**

```python
print("=== Jag skriver in två namn ===")
n1 = input("Namn 1: ")
n2 = input("Namn 2: ")
namn = [n1, n2]
print("Här är min lista med namn:", namn)
```

---

### Uppgift 16 – blandat med input

**Uppgift:** Fråga efter ett namn och en ålder. Skapa en lista som innehåller namn (text) och ålder (tal).

**Exempel på körning:**

```text
=== Jag skriver in namn och ålder ===
Namn: Ada
Ålder: 12
Här är min blandade lista: ['Ada', 12]
```

**Facit:**

```python
print("=== Jag skriver in namn och ålder ===")
namn = input("Namn: ")
alder = int(input("Ålder: "))
lista = [namn, alder]
print("Här är min blandade lista:", lista)
```

---

### Uppgift 17 – tre saker med input

**Uppgift:** Fråga efter tre saker. Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in tre saker ===
Sak 1: bok
Sak 2: mobil
Sak 3: nyckel
Här är min lista med saker: ['bok', 'mobil', 'nyckel']
```

**Facit:**

```python
print("=== Jag skriver in tre saker ===")
s1 = input("Sak 1: ")
s2 = input("Sak 2: ")
s3 = input("Sak 3: ")
saker = [s1, s2, s3]
print("Här är min lista med saker:", saker)
```

---

### Uppgift 18 – städer

**Uppgift:** Skapa en lista med tre städer och skriv ut listan.

**Exempel på körning:**

```text
=== Tre städer ===
Här är min lista med städer: ['stockholm', 'göteborg', 'malmö']
```

**Facit:**

```python
print("=== Tre städer ===")
stader = ["stockholm", "göteborg", "malmö"]
print("Här är min lista med städer:", stader)
```

---

### Uppgift 19 – veckodagar

**Uppgift:** Skapa en lista med tre veckodagar och skriv ut listan.

**Exempel på körning:**

```text
=== Tre veckodagar ===
Här är min lista med dagar: ['måndag', 'tisdag', 'onsdag']
```

**Facit:**

```python
print("=== Tre veckodagar ===")
dagar = ["måndag", "tisdag", "onsdag"]
print("Här är min lista med dagar:", dagar)
```

---

### Uppgift 20 – månader

**Uppgift:** Skapa en lista med tre månader och skriv ut listan.

**Exempel på körning:**

```text
=== Tre månader ===
Här är min lista med månader: ['januari', 'februari', 'mars']
```

**Facit:**

```python
print("=== Tre månader ===")
manader = ["januari", "februari", "mars"]
print("Här är min lista med månader:", manader)
```

---

### Uppgift 21 – två filmer med input

**Uppgift:** Fråga efter två filmnamn. Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in två filmer ===
Film 1: Toy Story
Film 2: Frost
Här är min lista med filmer: ['Toy Story', 'Frost']
```

**Facit:**

```python
print("=== Jag skriver in två filmer ===")
f1 = input("Film 1: ")
f2 = input("Film 2: ")
filmer = [f1, f2]
print("Här är min lista med filmer:", filmer)
```

---

### Uppgift 22 – tre ord med input

**Uppgift:** Fråga efter tre ord. Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in tre ord ===
Ord 1: sol
Ord 2: regn
Ord 3: snö
Här är min lista med ord: ['sol', 'regn', 'snö']
```

**Facit:**

```python
print("=== Jag skriver in tre ord ===")
o1 = input("Ord 1: ")
o2 = input("Ord 2: ")
o3 = input("Ord 3: ")
ordlista = [o1, o2, o3]
print("Här är min lista med ord:", ordlista)
```

---

### Uppgift 23 – två listor med text

**Uppgift:** Skapa två listor med text och skriv ut båda.

**Exempel på körning:**

```text
=== Jag har två listor ===
Här är min första lista: ['sol', 'regn']
Här är min andra lista: ['snö', 'vind']
```

**Facit:**

```python
print("=== Jag har två listor ===")
lista1 = ["sol", "regn"]
lista2 = ["snö", "vind"]
print("Här är min första lista:", lista1)
print("Här är min andra lista:", lista2)
```

---

### Uppgift 24 – två listor med tal

**Uppgift:** Skapa två listor med tal och skriv ut båda.

**Exempel på körning:**

```text
=== Jag har två tallistor ===
Här är min första tallista: [1, 2, 3]
Här är min andra tallista: [100, 200]
```

**Facit:**

```python
print("=== Jag har två tallistor ===")
tal1 = [1, 2, 3]
tal2 = [100, 200]
print("Här är min första tallista:", tal1)
print("Här är min andra tallista:", tal2)
```

---

### Uppgift 25 – blandad lista

**Uppgift:** Skapa en lista med fem saker där både text och tal finns med. Skriv ut listan.

**Exempel på körning:**

```text
=== En blandad lista med text och tal ===
Här är min blandade lista: ['hp', 10, 'mp', 5, 'level']
```

**Facit:**

```python
print("=== En blandad lista med text och tal ===")
lista = ["hp", 10, "mp", 5, "level"]
print("Här är min blandade lista:", lista)
```

---

### Uppgift 26 – receptlista

**Uppgift:** Skapa en lista med fyra saker som kan vara i ett recept och skriv ut listan.

**Exempel på körning:**

```text
=== Ingredienser till ett recept ===
Här är min lista med ingredienser: ['mjöl', 'ägg', 'mjölk', 'smör']
```

**Facit:**

```python
print("=== Ingredienser till ett recept ===")
ingredienser = ["mjöl", "ägg", "mjölk", "smör"]
print("Här är min lista med ingredienser:", ingredienser)
```

---

### Uppgift 27 – saker till skolan

**Uppgift:** Skapa en lista med fyra saker man kan ta med till skolan och skriv ut listan.

**Exempel på körning:**

```text
=== Saker jag kan ta med till skolan ===
Här är min lista med skolsaker: ['bok', 'penna', 'sudd', 'linjal']
```

**Facit:**

```python
print("=== Saker jag kan ta med till skolan ===")
skolsaker = ["bok", "penna", "sudd", "linjal"]
print("Här är min lista med skolsaker:", skolsaker)
```

---

### Uppgift 28 – temperaturer med input

**Uppgift:** Fråga efter tre temperaturer (tal). Skapa en lista med talen och skriv ut listan.

**Exempel på körning:**

```text
=== Jag skriver in tre temperaturer ===
Temp 1: 18
Temp 2: 20
Temp 3: 16
Här är min lista med temperaturer: [18, 20, 16]
```

**Facit:**

```python
print("=== Jag skriver in tre temperaturer ===")
t1 = int(input("Temp 1: "))
t2 = int(input("Temp 2: "))
t3 = int(input("Temp 3: "))
temperaturer = [t1, t2, t3]
print("Här är min lista med temperaturer:", temperaturer)
```

---

### Uppgift 29 – meny med input

**Uppgift:** Fråga efter tre maträtter. Skapa en lista och skriv ut den som en meny.

**Exempel på körning:**

```text
=== Jag skapar en meny ===
Maträtt 1: pizza
Maträtt 2: pasta
Maträtt 3: tacos
Här är min menylista: ['pizza', 'pasta', 'tacos']
```

**Facit:**

```python
print("=== Jag skapar en meny ===")
m1 = input("Maträtt 1: ")
m2 = input("Maträtt 2: ")
m3 = input("Maträtt 3: ")
meny = [m1, m2, m3]
print("Här är min menylista:", meny)
```

---

### Uppgift 30 – blandat med input

**Uppgift:** Fråga efter en sak (text) och ett antal (tal). Skapa en lista och skriv ut den.

**Exempel på körning:**

```text
=== Jag skriver in en sak och ett antal ===
Sak: pennor
Antal: 3
Här är min blandade lista: ['pennor', 3]
```

**Facit:**

```python
print("=== Jag skriver in en sak och ett antal ===")
sak = input("Sak: ")
antal = int(input("Antal: "))
lista = [sak, antal]
print("Här är min blandade lista:", lista)
```
