# Prov 2c: villkor

I det här provet testas din förmåga att styra programflödet med `if`, `elif` och `else`. Temat är **bio och film**.

---

### Uppgift 1: Medlem eller inte?

**Uppgift:** Fråga användaren om de är medlem. Om svaret är `"ja"` ska programmet skriva `"Välkommen, du får 20% rabatt!"`. Annars ska det skriva `"Ingen rabatt idag."`.

**Exempel på körning 1:**
```text
Är du medlem? (ja/nej): ja
Välkommen, du får 20% rabatt!
```

**Exempel på körning 2:**
```text
Är du medlem? (ja/nej): nej
Ingen rabatt idag.
```

**Facit:**
```python
svar = input("Är du medlem? (ja/nej): ")
if svar == "ja":
    print("Välkommen, du får 20% rabatt!")
else:
    print("Ingen rabatt idag.")
```

---

### Uppgift 2: Får du se filmen?

**Uppgift:** Fråga användaren hur gammal de är. Om åldern är 15 eller mer ska programmet skriva `"Du får se filmen."`. Annars ska det skriva `"Tyvärr, du är för ung."`.

**Exempel på körning 1:**
```text
Hur gammal är du? 17
Du får se filmen.
```

**Exempel på körning 2:**
```text
Hur gammal är du? 12
Tyvärr, du är för ung.
```

**Facit:**
```python
alder = int(input("Hur gammal är du? "))
if alder >= 15:
    print("Du får se filmen.")
else:
    print("Tyvärr, du är för ung.")
```

---

### Uppgift 3: Filmgenre

**Uppgift:** Fråga användaren vilken filmgenre de vill se. Om det är `"action"` skriv `"Häng i bältet!"`. Om det är `"komedi"` skriv `"Dags att skratta!"`. Annars skriv `"En fin filmkväll!"`.

**Exempel på körning 1:**
```text
Vilken genre? action
Häng i bältet!
```

**Exempel på körning 2:**
```text
Vilken genre? komedi
Dags att skratta!
```

**Exempel på körning 3:**
```text
Vilken genre? drama
En fin filmkväll!
```

**Facit:**
```python
genre = input("Vilken genre? ")
if genre == "action":
    print("Häng i bältet!")
elif genre == "komedi":
    print("Dags att skratta!")
else:
    print("En fin filmkväll!")
```

---

### Uppgift 4: Åldersgräns

**Uppgift:** Fråga användaren hur gammal de är. Skriv ut vilken åldersgräns de klarar:
- Under 7: `"Ingen film idag."`
- 7–10: `"Du klarar 7-årsgränsen."`
- 11–14: `"Du klarar 11-årsgränsen."`
- 15 eller mer: `"Du klarar alla filmer."`

**Exempel på körning 1:**
```text
Ålder: 5
Ingen film idag.
```

**Exempel på körning 2:**
```text
Ålder: 9
Du klarar 7-årsgränsen.
```

**Exempel på körning 3:**
```text
Ålder: 13
Du klarar 11-årsgränsen.
```

**Exempel på körning 4:**
```text
Ålder: 16
Du klarar alla filmer.
```

**Facit:**
```python
alder = int(input("Ålder: "))
if alder < 7:
    print("Ingen film idag.")
elif alder < 11:
    print("Du klarar 7-årsgränsen.")
elif alder < 15:
    print("Du klarar 11-årsgränsen.")
else:
    print("Du klarar alla filmer.")
```

---

### Uppgift 5: Biobiljett

**Uppgift:** Fråga användaren om filmens genre och användarens ålder. Om genren är `"skräck"`: kontrollera åldern — om 15 eller mer skriv `"Välkommen in, om du vågar!"`, annars skriv `"Den här filmen är inte för dig."`. Om genren inte är `"skräck"` ska programmet med en **f-sträng** skriva ut att det är dags att se filmen.

**Exempel på körning 1:**
```text
Genre: skräck
Ålder: 17
Välkommen in, om du vågar!
```

**Exempel på körning 2:**
```text
Genre: skräck
Ålder: 12
Den här filmen är inte för dig.
```

**Exempel på körning 3:**
```text
Genre: komedi
Ålder: 10
Dags att se komedi!
```

**Facit:**
```python
genre = input("Genre: ")
alder = int(input("Ålder: "))
if genre == "skräck":
    if alder >= 15:
        print("Välkommen in, om du vågar!")
    else:
        print("Den här filmen är inte för dig.")
else:
    print(f"Dags att se {genre}!")
```
