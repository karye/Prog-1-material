# Träning inför prov 6c: for-loopar och slump

Här får du träna på samma moment som kommer på Prov 6c. Temat är **sport**.

---

### Uppgift 1: Loopa igenom sporter

**Uppgift:** Skapa en lista med tre sporter: `["tennis", "basket", "simning"]`. Använd en `for`-loop för att gå igenom listan och skriva ut varje sport med texten `"Sport:"` framför.

**Exempel på körning:**
```text
Sport: tennis
Sport: basket
Sport: simning
```

**Facit:**
```python
sporter = ["tennis", "basket", "simning"]
for sport in sporter:
    print("Sport:", sport)
```

---

### Uppgift 2: Räkna halvlekar

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut halvlekarna 1 till 4. Skriv texten `"Halvlek"` framför varje siffra.

**Exempel på körning:**
```text
Halvlek 1
Halvlek 2
Halvlek 3
Halvlek 4
```

**Facit:**
```python
for i in range(1, 5):
    print("Halvlek", i)
```

---

### Uppgift 3: Tränar idag

**Uppgift:** Skapa en lista med tre sporter: `["löpning", "cykling", "yoga"]`. Använd en `for`-loop och skriv ut en mening för varje sport.

**Exempel på körning:**
```text
Idag tränar vi löpning
Idag tränar vi cykling
Idag tränar vi yoga
```

**Facit:**
```python
sporter = ["löpning", "cykling", "yoga"]
for sport in sporter:
    print("Idag tränar vi", sport)
```

---

### Uppgift 4: Poäng per omgång

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut omgångarna 1 till 5. Varje omgång ger 3 poäng mer än den förra (omgång 1 ger 3 poäng, omgång 2 ger 6 poäng och så vidare).

**Exempel på körning:**
```text
Omgång 1 ger 3 poäng
Omgång 2 ger 6 poäng
Omgång 3 ger 9 poäng
Omgång 4 ger 12 poäng
Omgång 5 ger 15 poäng
```

**Facit:**
```python
for i in range(1, 6):
    print("Omgång", i, "ger", i * 3, "poäng")
```

---

### Uppgift 5: Dagens sport

**Uppgift:** Importera modulen `random`. Skapa en lista med fyra sporter. Använd `random.choice()` för att slumpa fram en sport. Skriv ut resultatet med en **f-sträng**.

**Exempel på körning (resultatet varierar):**
```text
Idag spelar vi badminton!
```

**Facit:**
```python
import random
sporter = ["badminton", "fotboll", "hockey", "handboll"]
val = random.choice(sporter)
print(f"Idag spelar vi {val}!")
```
