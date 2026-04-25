# Prov 6c: for-loopar och slump

I det här provet testas din förmåga att använda `for`-loopar och modulen `random`. Temat är **djur och natur**.

---

### Uppgift 1: Loopa igenom djur

**Uppgift:** Skapa en lista med tre djur: `["lejon", "elefant", "giraff"]`. Använd en `for`-loop för att gå igenom listan och skriva ut varje djur med texten `"Djur:"` framför.

**Exempel på körning:**
```text
Djur: lejon
Djur: elefant
Djur: giraff
```

**Facit:**
```python
djur = ["lejon", "elefant", "giraff"]
for d in djur:
    print("Djur:", d)
```

---

### Uppgift 2: Räkna burar

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut burarna 1 till 4. Skriv texten `"Bur"` framför varje siffra.

**Exempel på körning:**
```text
Bur 1
Bur 2
Bur 3
Bur 4
```

**Facit:**
```python
for i in range(1, 5):
    print("Bur", i)
```

---

### Uppgift 3: Matningstid

**Uppgift:** Skapa en lista med tre djur: `["björn", "varg", "räv"]`. Använd en `for`-loop och skriv ut en mening för varje djur.

**Exempel på körning:**
```text
Dags att mata björn
Dags att mata varg
Dags att mata räv
```

**Facit:**
```python
djur = ["björn", "varg", "räv"]
for d in djur:
    print("Dags att mata", d)
```

---

### Uppgift 4: Djurens vikt

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut djur 1 till 5. Varje djur väger 10 kg mer än det förra (djur 1 väger 10 kg, djur 2 väger 20 kg och så vidare).

**Exempel på körning:**
```text
Djur 1 väger 10 kg
Djur 2 väger 20 kg
Djur 3 väger 30 kg
Djur 4 väger 40 kg
Djur 5 väger 50 kg
```

**Facit:**
```python
for i in range(1, 6):
    print("Djur", i, "väger", i * 10, "kg")
```

---

### Uppgift 5: Dagens djur

**Uppgift:** Importera modulen `random`. Skapa en lista med fyra djur. Använd `random.choice()` för att slumpa fram ett djur. Skriv ut resultatet med en **f-sträng**.

**Exempel på körning (resultatet varierar):**
```text
Idag sköter du om pingvinen!
```

**Facit:**
```python
import random
djur = ["pingvinen", "flamingon", "koalan", "pandaen"]
val = random.choice(djur)
print(f"Idag sköter du om {val}!")
```
