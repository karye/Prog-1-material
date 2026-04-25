# Prov 6b: for-loopar och slump

I det här provet testas din förmåga att använda `for`-loopar och modulen `random`. Temat är **städer och resor**.

---

### Uppgift 1: Loopa igenom städer

**Uppgift:** Skapa en lista med tre städer: `["Stockholm", "Göteborg", "Malmö"]`. Använd en `for`-loop för att gå igenom listan och skriva ut varje stad med texten `"Stad:"` framför.

**Exempel på körning:**
```text
Stad: Stockholm
Stad: Göteborg
Stad: Malmö
```

**Facit:**
```python
städer = ["Stockholm", "Göteborg", "Malmö"]
for stad in städer:
    print("Stad:", stad)
```

---

### Uppgift 2: Räkna resdagar

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut siffrorna 1 till 5. Skriv texten `"Dag"` framför varje siffra.

**Exempel på körning:**
```text
Dag 1
Dag 2
Dag 3
Dag 4
Dag 5
```

**Facit:**
```python
for i in range(1, 6):
    print("Dag", i)
```

---

### Uppgift 3: Vill besöka

**Uppgift:** Skapa en lista med tre länder: `["Japan", "Brasilien", "Kanada"]`. Använd en `for`-loop för att skriva ut en mening för varje land.

**Exempel på körning:**
```text
Jag vill besöka Japan
Jag vill besöka Brasilien
Jag vill besöka Kanada
```

**Facit:**
```python
länder = ["Japan", "Brasilien", "Kanada"]
for land in länder:
    print("Jag vill besöka", land)
```

---

### Uppgift 4: Hotellnätter

**Uppgift:** Använd en `for`-loop och `range()` för att skriva ut nätterna 1 till 4. Skriv ut natt-numret och vad det kostar (varje natt kostar 800 kr).

**Exempel på körning:**
```text
Natt 1 kostar 800 kr
Natt 2 kostar 1600 kr
Natt 3 kostar 2400 kr
Natt 4 kostar 3200 kr
```

**Facit:**
```python
for i in range(1, 5):
    print("Natt", i, "kostar", i * 800, "kr")
```

---

### Uppgift 5: Slumpdestination

**Uppgift:** Importera modulen `random`. Skapa en lista med fyra destinationer. Använd `random.choice()` för att slumpa fram en destination. Skriv ut resultatet med en **f-sträng**.

**Exempel på körning (resultatet varierar):**
```text
Vi åker till Tokyo!
```

**Facit:**
```python
import random
destinationer = ["Tokyo", "Paris", "New York", "Sydney"]
val = random.choice(destinationer)
print(f"Vi åker till {val}!")
```
