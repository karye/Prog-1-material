# Prov 4a: listor

I det här provet testas din förmåga att skapa listor med text och tal samt skriva ut dem. Temat är **film**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Favoritfilmer

**Uppgift:** Skapa en lista med tre filmtitlar och skriv ut listan.

**Exempel på körning:**
```text
=== Mina favoritfilmer ===
Filmer: ['Titanic', 'Inception', 'Interstellar']
```

**Facit:**
```python
print("=== Mina favoritfilmer ===")
filmer = ["Titanic", "Inception", "Interstellar"]
print("Filmer:", filmer)
```

---

### Uppgift 2: Filmbetyg

**Uppgift:** Skapa en lista med fyra betyg (tal mellan 1 och 5) och skriv ut listan.

**Exempel på körning:**
```text
=== Mina filmbetyg ===
Betyg: [5, 3, 4, 5]
```

**Facit:**
```python
print("=== Mina filmbetyg ===")
betyg = [5, 3, 4, 5]
print("Betyg:", betyg)
```

---

### Uppgift 3: Filminfo

**Uppgift:** Skapa en lista med tre saker om en film: titel (text), år (tal) och betyg (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Filminfo ===
Info: ['The Matrix', 1999, 5]
```

**Facit:**
```python
print("=== Filminfo ===")
film = ["The Matrix", 1999, 5]
print("Info:", film)
```

---

### Uppgift 4: Två favoritfilmer

**Uppgift:** Fråga användaren om två filmtitlar med `input()`. Skapa en lista med de två titlarna och skriv ut listan.

**Exempel på körning:**
```text
=== Mina två favoritfilmer ===
Film 1: Shrek
Film 2: Frost
Din lista: ['Shrek', 'Frost']
```

**Facit:**
```python
print("=== Mina två favoritfilmer ===")
film1 = input("Film 1: ")
film2 = input("Film 2: ")
filmer = [film1, film2]
print("Din lista:", filmer)
```

---

### Uppgift 5: Filmrecension

**Uppgift:** Fråga användaren om en filmtitel med `input()` och ett betyg med `int(input())`. Skapa en lista med titel (text) och betyg (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Skriv din recension ===
Filmtitel: Avatar
Betyg (1-5): 4
Din recension: ['Avatar', 4]
```

**Facit:**
```python
print("=== Skriv din recension ===")
titel = input("Filmtitel: ")
betyg = int(input("Betyg (1-5): "))
recension = [titel, betyg]
print(f"Din recension: {recension}")
```
