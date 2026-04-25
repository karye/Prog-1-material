# Prov 1c: print och input

I det här provet testas din förmåga att skriva ut text med `print()` och ta emot information från användaren med `input()`. Temat är **träning och sport**.

---

### Uppgift 1: Gymskylten

**Uppgift:** Skriv ett program som använder `print()` två gånger. Skriv ut ett namn på ett gym och sedan en slogan på nästa rad.

**Exempel på körning:**
```text
Välkommen till GymKoden!
Här tränar vi hårt och har kul.
```

**Facit:**
```python
print("Välkommen till GymKoden!")
print("Här tränar vi hårt och har kul.")
```

---

### Uppgift 2: Träningsrapport

**Uppgift:** Skriv ett program som skriver ut en träningsrapport med fyra rader: rubrik, sport, tid och kalorier.

**Exempel på körning:**
```text
=== Träningsrapport ===
Sport: Löpning
Tid: 45 minuter
Kalorier: 400 kcal
```

**Facit:**
```python
print("=== Träningsrapport ===")
print("Sport: Löpning")
print("Tid: 45 minuter")
print("Kalorier: 400 kcal")
```

---

### Uppgift 3: Fråga efter namn

**Uppgift:** Fråga användaren vad de heter med `input()`. Skriv sedan ut en hälsning med namnet.

**Exempel på körning:**
```text
Vad heter du? Sara
Hej Sara dags att träna!
```

**Facit:**
```python
namn = input("Vad heter du? ")
print("Hej", namn, "dags att träna!")
```

---

### Uppgift 4: Favoritsport

**Uppgift:** Fråga användaren om deras namn och favoritort. Skriv sedan ut en mening med båda. Använd **inte** en f-sträng.

**Exempel på körning:**
```text
Vad heter du? Ali
Vad är din favoritspot? Fotboll
Ali tränar helst Fotboll.
```

**Facit:**
```python
namn = input("Vad heter du? ")
sport = input("Vad är din favoritspot? ")
print(namn, "tränar helst", sport + ".")
```

---

### Uppgift 5: Träningsdagbok

**Uppgift:** Fråga användaren om deras namn, vilken sport de tränade och hur länge. Skriv sedan ut en träningsdagbok med tre rader med **f-strängar**.

**Exempel på körning:**
```text
Ditt namn: Fatima
Vilken sport tränade du? Simning
Hur länge (minuter)? 60
--- Träningsdagbok ---
Fatima tränade idag.
Sport: Simning
Tid: 60 minuter
```

**Facit:**
```python
namn = input("Ditt namn: ")
sport = input("Vilken sport tränade du? ")
tid = input("Hur länge (minuter)? ")
print("--- Träningsdagbok ---")
print(f"{namn} tränade idag.")
print(f"Sport: {sport}")
print(f"Tid: {tid} minuter")
```
