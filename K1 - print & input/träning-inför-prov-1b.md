# Träning inför prov 1b: print och input

Här får du träna på samma moment som kommer på Prov 1b. Temat är **skolan**.

---

### Uppgift 1: Välkomstskylt

**Uppgift:** Skriv ett program som använder `print()` två gånger. Skriv ut ett namn på en skola och en välkomstmening på nästa rad.

**Exempel på körning:**
```text
Välkommen till Kodskolan!
Här lär vi oss programmering.
```

**Facit:**
```python
print("Välkommen till Kodskolan!")
print("Här lär vi oss programmering.")
```

---

### Uppgift 2: Schema

**Uppgift:** Skriv ett program som skriver ut ett schema med fyra rader: rubrik och tre lektioner. Det ska se ut exakt som i exemplet nedan, med likhetstecken på översta raden.

**Exempel på körning:**
```text
================
Lektion 1: Matte
Lektion 2: Svenska
Lektion 3: Idrott
```

**Facit:**
```python
print("================")
print("Lektion 1: Matte")
print("Lektion 2: Svenska")
print("Lektion 3: Idrott")
```

---

### Uppgift 3: Fråga efter namn

**Uppgift:** Fråga användaren vad de heter med `input()`. Skriv sedan ut att de är välkomna till klassen.

**Exempel på körning:**
```text
Vad heter du? Leo
Hej Leo välkommen till klassen!
```

**Facit:**
```python
namn = input("Vad heter du? ")
print("Hej", namn, "välkommen till klassen!")
```

---

### Uppgift 4: Favoritämne

**Uppgift:** Fråga användaren om deras namn och favoritämne. Skriv sedan ut en mening med båda med en **f-sträng**.

**Exempel på körning:**
```text
Vad heter du? Nora
Vad är ditt favoritämne? Programmering
Nora gillar Programmering mest.
```

**Facit:**
```python
namn = input("Vad heter du? ")
amne = input("Vad är ditt favoritämne? ")
print(f"{namn} gillar {amne} mest.")
```

---

### Uppgift 5: Elevpresentation

**Uppgift:** Fråga användaren om deras namn, klass och favoritämne. Skriv sedan ut en presentation med tre rader med **f-strängar**.

**Exempel på körning:**
```text
Ditt namn: Sam
Din klass: EE23A
Favoritämne: Programmering
--- Elevpresentation ---
Jag heter Sam och går i klass EE23A.
Mitt favoritämne är Programmering.
Trevligt att träffas!
```

**Facit:**
```python
namn = input("Ditt namn: ")
klass = input("Din klass: ")
amne = input("Favoritämne: ")
print("--- Elevpresentation ---")
print(f"Jag heter {namn} och går i klass {klass}.")
print(f"Mitt favoritämne är {amne}.")
print("Trevligt att träffas!")
```
