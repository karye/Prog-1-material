# Träning inför prov 1c: print och input

Här får du träna på samma moment som kommer på Prov 1c. Temat är **musik**.

---

### Uppgift 1: Konsertaffisch

**Uppgift:** Skriv ett program som använder `print()` två gånger. Skriv ut ett namn på en konsert och en slogan på nästa rad.

**Exempel på körning:**
```text
Välkommen till KodKonserten!
En kväll du sent kommer glömma.
```

**Facit:**
```python
print("Välkommen till KodKonserten!")
print("En kväll du sent kommer glömma.")
```

---

### Uppgift 2: Bandinfo

**Uppgift:** Skriv ett program som skriver ut information om ett band med fyra rader: rubrik, bandnamn, genre och antal medlemmar.

**Exempel på körning:**
```text
=== Bandinformation ===
Band: The Coders
Genre: Rock
Medlemmar: 4
```

**Facit:**
```python
print("=== Bandinformation ===")
print("Band: The Coders")
print("Genre: Rock")
print("Medlemmar: 4")
```

---

### Uppgift 3: Fråga efter namn

**Uppgift:** Fråga användaren vad de heter med `input()`. Skriv sedan ut en hälsning.

**Exempel på körning:**
```text
Vad heter du? Karin
Hej Karin välkommen till konserten!
```

**Facit:**
```python
namn = input("Vad heter du? ")
print("Hej", namn, "välkommen till konserten!")
```

---

### Uppgift 4: Favoritlåt

**Uppgift:** Fråga användaren om deras namn och favoritlåt. Skriv sedan ut en mening med båda. Använd **inte** en f-sträng.

**Exempel på körning:**
```text
Vad heter du? Erik
Vad är din favoritlåt? Bohemian Rhapsody
Erik lyssnar helst på Bohemian Rhapsody.
```

**Facit:**
```python
namn = input("Vad heter du? ")
lat = input("Vad är din favoritlåt? ")
print(namn, "lyssnar helst på", lat + ".")
```

---

### Uppgift 5: Musikdagbok

**Uppgift:** Fråga användaren om deras namn, vilket band de lyssnade på och hur länge. Skriv sedan ut en musikdagbok med tre rader med **f-strängar**.

**Exempel på körning:**
```text
Ditt namn: Mia
Vilket band lyssnade du på? Coldplay
Hur länge (minuter)? 45
--- Musikdagbok ---
Mia lyssnade på musik idag.
Band: Coldplay
Tid: 45 minuter
```

**Facit:**
```python
namn = input("Ditt namn: ")
band = input("Vilket band lyssnade du på? ")
tid = input("Hur länge (minuter)? ")
print("--- Musikdagbok ---")
print(f"{namn} lyssnade på musik idag.")
print(f"Band: {band}")
print(f"Tid: {tid} minuter")
```
