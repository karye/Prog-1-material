# Prov 4b: listor

I det här provet testas din förmåga att skapa listor med text och tal samt skriva ut dem. Temat är **sport**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Favoritssporter

**Uppgift:** Skapa en lista med tre sporter och skriv ut listan.

**Exempel på körning:**
```text
=== Mina favoritssporter ===
Sporter: ['fotboll', 'simning', 'tennis']
```

**Facit:**
```python
print("=== Mina favoritssporter ===")
sporter = ["fotboll", "simning", "tennis"]
print("Sporter:", sporter)
```

---

### Uppgift 2: Poänglista

**Uppgift:** Skapa en lista med fyra poäng (heltal) och skriv ut listan.

**Exempel på körning:**
```text
=== Poänglista ===
Poäng: [3, 1, 2, 3]
```

**Facit:**
```python
print("=== Poänglista ===")
poang = [3, 1, 2, 3]
print("Poäng:", poang)
```

---

### Uppgift 3: Laginfo

**Uppgift:** Skapa en lista med tre saker om ett lag: lagnamn (text), antal spelare (tal) och antal vinster (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Laginfo ===
Lag: ['Hammarby', 11, 8]
```

**Facit:**
```python
print("=== Laginfo ===")
lag = ["Hammarby", 11, 8]
print("Lag:", lag)
```

---

### Uppgift 4: Två spelare

**Uppgift:** Fråga användaren om två spelarnamn med `input()`. Skapa en lista med de två namnen och skriv ut listan.

**Exempel på körning:**
```text
=== Laguppställning ===
Spelare 1: Zlatan
Spelare 2: Ronaldo
Ditt lag: ['Zlatan', 'Ronaldo']
```

**Facit:**
```python
print("=== Laguppställning ===")
spelare1 = input("Spelare 1: ")
spelare2 = input("Spelare 2: ")
lag = [spelare1, spelare2]
print("Ditt lag:", lag)
```

---

### Uppgift 5: Matchresultat

**Uppgift:** Fråga användaren om ett lagnamn med `input()` och antal mål med `int(input())`. Skapa en lista med lagnamn (text) och mål (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Matchresultat ===
Lag: AIK
Antal mål: 3
Resultat: ['AIK', 3]
```

**Facit:**
```python
print("=== Matchresultat ===")
lag = input("Lag: ")
mal = int(input("Antal mål: "))
resultat = [lag, mal]
print(f"Resultat: {resultat}")
```
