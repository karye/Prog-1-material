# Prov 5b: listor och index

Här får du träna mer på samma moment som kommer på Prov 3. Fokus ligger på att blanda olika typer av information i listor och att använda `input()` tillsammans med index för att plocka fram rätt information från datorns minne.

---

### Uppgift 1: blandad lista (spelkaraktär)

**Uppgift:** Skapa en lista som innehåller exakt tre saker om en spelkaraktär: Namn (text), Level (heltal) och Styrka 1-10 (heltal). Skriv sedan ut hela listan.

**Exempel på körning:**

```text
=== Karaktärsmeny ===
Info: ['Super Mario', 99, 8]
```

**Facit:**

```python
print("=== Karaktärsmeny ===")
# Blandad lista: Text, Heltal, Heltal
karaktar = ["Super Mario", 99, 8]
print("Info:", karaktar)
```

---

### Uppgift 2: skriva ut specifika delar

**Uppgift:** Utgå från listan `artister = ["Taylor Swift", "The Weeknd", "Avicii", "Beyoncé"]`.
Skriv ut hela listan.
Använd sedan index för att skriva ut den **första** artisten och den **sista** artisten på varsin rad.

**Exempel på körning:**

```text
=== Topplistan ===
Alla artister: ['Taylor Swift', 'The Weeknd', 'Avicii', 'Beyoncé']
Första: Taylor Swift
Sista: Beyoncé
```

**Facit:**

```python
print("=== Topplistan ===")
artister = ["Taylor Swift", "The Weeknd", "Avicii", "Beyoncé"]
print("Alla artister:", artister)
print("Första:", artister[0])
print("Sista:", artister[3])
```

---

### Uppgift 3: välj fika (input och index)

**Uppgift:** Skapa en lista med tre sorters fika: `["Kanelbulle", "Kladdkaka", "Dammsugare"]`.

1. Skriv ut listan så användaren ser alternativen.
2. Be användaren välja vad de vill ha (index 0, 1 eller 2).
3. Skriv ut valet.

**Exempel på körning:**

```text
=== Caféet ===
Meny: ['Kanelbulle', 'Kladdkaka', 'Dammsugare']
Vad vill du ha (0-2): 1
Du valde: Kladdkaka
```

**Facit:**

```python
print("=== Caféet ===")
fika = ["Kanelbulle", "Kladdkaka", "Dammsugare"]
print("Meny:", fika)
val = int(input("Vad vill du ha (0-2): "))
print("Du valde:", fika[val])
```

---

### Uppgift 4: välj temperatur (tal och input)

**Uppgift:** Skapa en lista med tre temperaturer (heltal): `[15, 22, 30]`.

1. Fråga användaren vilken dag de vill se temperaturen för, genom att välja ett index (0-2).
2. Skriv ut temperaturen på det indexet tillsammans med texten "grader".

**Exempel på körning:**

```text
=== Väderappen ===
Vilken dag (0-2)? 2
Temperatur: 30 grader
```

**Facit:**

```python
print("=== Väderappen ===")
temperaturer = [15, 22, 30]
val = int(input("Vilken dag (0-2)? "))
print("Temperatur:", temperaturer[val], "grader")
```

---

### Uppgift 5: husdjursinfo (blandat val)

**Uppgift:** Skapa en lista med info om ett husdjur: `["Hund", 5, "Svart", 12]`.
(Listan innehåller Art, Ålder, Färg, Vikt).
Låt användaren skriva in ett index (0-3) för att se den specifika informationen.

**Exempel på körning:**

```text
=== Djurkliniken ===
Data: ['Hund', 5, 'Svart', 12]
Välj info (0=Art, 1=Ålder, 2=Färg, 3=Vikt): 2
Info: Svart
```

**Facit:**

```python
print("=== Djurkliniken ===")
djur = ["Hund", 5, "Svart", 12]
print("Data:", djur)
val = int(input("Välj info (0=Art, 1=Ålder, 2=Färg, 3=Vikt): "))
print("Info:", djur[val])
```
