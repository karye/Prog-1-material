# Träning inför prov 5c: listor och index

Här får du träna på samma moment som kommer på Prov 5c. Temat är **musik**.

---

### Uppgift 1: Albuminfo

**Uppgift:** Skapa en lista med tre saker om ett album: artist (text), år (tal) och antal låtar (tal). Skriv ut hela listan.

**Exempel på körning:**
```text
=== Albuminfo ===
Album: ['ABBA', 1976, 10]
```

**Facit:**
```python
print("=== Albuminfo ===")
album = ["ABBA", 1976, 10]
print("Album:", album)
```

---

### Uppgift 2: Topplistans artister

**Uppgift:** Utgå från listan `artister = ["Beyoncé", "Drake", "Taylor Swift", "Ed Sheeran"]`. Skriv ut hela listan, sedan den **första** artisten och den **sista** artisten på varsin rad.

**Exempel på körning:**
```text
=== Topplistan ===
Alla artister: ['Beyoncé', 'Drake', 'Taylor Swift', 'Ed Sheeran']
Första: Beyoncé
Sista: Ed Sheeran
```

**Facit:**
```python
print("=== Topplistan ===")
artister = ["Beyoncé", "Drake", "Taylor Swift", "Ed Sheeran"]
print("Alla artister:", artister)
print("Första:", artister[0])
print("Sista:", artister[3])
```

---

### Uppgift 3: Välj genre

**Uppgift:** Skapa en lista med tre musikgenrer: `["pop", "rock", "jazz"]`. Skriv ut listan och be sedan användaren välja en genre med ett index (0, 1 eller 2). Skriv ut den valda genren.

**Exempel på körning:**
```text
=== Välj genre ===
Genrer: ['pop', 'rock', 'jazz']
Välj genre (0-2): 2
Du valde: jazz
```

**Facit:**
```python
print("=== Välj genre ===")
genrer = ["pop", "rock", "jazz"]
print("Genrer:", genrer)
val = int(input("Välj genre (0-2): "))
print("Du valde:", genrer[val])
```

---

### Uppgift 4: Biljettpris

**Uppgift:** Skapa en lista med tre konsertpriser (heltal): `[299, 499, 799]`. Be användaren välja ett pris med ett index (0-2) och skriv ut priset tillsammans med texten `"kr"`.

**Exempel på körning:**
```text
=== Konsertbiljetter ===
Välj kategori (0-2): 1
Pris: 499 kr
```

**Facit:**
```python
print("=== Konsertbiljetter ===")
priser = [299, 499, 799]
val = int(input("Välj kategori (0-2): "))
print("Pris:", priser[val], "kr")
```

---

### Uppgift 5: Låtinfo

**Uppgift:** Skapa en lista med fyra saker om en låt: `["Adele", "Hello", 4, 2015]` (artist, titel, minuter, år). Be användaren välja en detalj med ett index (0–3). Skriv ut den valda informationen med en **f-sträng**.

**Exempel på körning:**
```text
=== Låtinfo ===
Data: ['Adele', 'Hello', 4, 2015]
Välj info (0=Artist, 1=Titel, 2=Minuter, 3=År): 1
Du valde: Hello
```

**Facit:**
```python
print("=== Låtinfo ===")
lat = ["Adele", "Hello", 4, 2015]
print("Data:", lat)
val = int(input("Välj info (0=Artist, 1=Titel, 2=Minuter, 3=År): "))
print(f"Du valde: {lat[val]}")
```
