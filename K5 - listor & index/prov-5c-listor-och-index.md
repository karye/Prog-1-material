# Prov 5c: listor och index

I det här provet testas din förmåga att skapa listor med blandade datatyper och plocka ut enskilda element med index. Temat är **resor**.

---

### Uppgift 1: Reseinfo

**Uppgift:** Skapa en lista med tre saker om en resa: destination (text), år (tal) och pris i kr (tal). Skriv ut hela listan.

**Exempel på körning:**
```text
=== Reseinfo ===
Resa: ['Tokyo', 2024, 12000]
```

**Facit:**
```python
print("=== Reseinfo ===")
resa = ["Tokyo", 2024, 12000]
print("Resa:", resa)
```

---

### Uppgift 2: Resmål

**Uppgift:** Utgå från listan `resmål = ["Paris", "New York", "Bangkok", "Sydney"]`. Skriv ut hela listan, sedan det **första** resmålet och det **sista** resmålet på varsin rad.

**Exempel på körning:**
```text
=== Resmål ===
Alla resmål: ['Paris', 'New York', 'Bangkok', 'Sydney']
Första: Paris
Sista: Sydney
```

**Facit:**
```python
print("=== Resmål ===")
resmal = ["Paris", "New York", "Bangkok", "Sydney"]
print("Alla resmål:", resmal)
print("Första:", resmal[0])
print("Sista:", resmal[3])
```

---

### Uppgift 3: Välj destination

**Uppgift:** Skapa en lista med tre destinationer: `["Rom", "Lissabon", "Dublin"]`. Skriv ut listan och be sedan användaren välja en destination med ett index (0, 1 eller 2). Skriv ut det valda resmålet.

**Exempel på körning:**
```text
=== Välj din resa ===
Destinationer: ['Rom', 'Lissabon', 'Dublin']
Välj destination (0-2): 1
Du valde: Lissabon
```

**Facit:**
```python
print("=== Välj din resa ===")
destinationer = ["Rom", "Lissabon", "Dublin"]
print("Destinationer:", destinationer)
val = int(input("Välj destination (0-2): "))
print("Du valde:", destinationer[val])
```

---

### Uppgift 4: Prisjämförelse

**Uppgift:** Skapa en lista med tre respaket-priser (heltal): `[4500, 7800, 12000]`. Be användaren välja ett paket med ett index (0-2) och skriv ut priset för det valda paketet tillsammans med texten `"kr"`.

**Exempel på körning:**
```text
=== Respaket ===
Välj paket (0-2): 2
Pris: 12000 kr
```

**Facit:**
```python
print("=== Respaket ===")
priser = [4500, 7800, 12000]
val = int(input("Välj paket (0-2): "))
print("Pris:", priser[val], "kr")
```

---

### Uppgift 5: Resedetaljer

**Uppgift:** Skapa en lista med fyra saker om en resa: `["Spanien", "Barcelona", 7, 6500]` (land, stad, dagar, pris). Be användaren välja en detalj med ett index (0–3). Skriv ut den valda informationen med en **f-sträng**.

**Exempel på körning:**
```text
=== Resedetaljer ===
Data: ['Spanien', 'Barcelona', 7, 6500]
Välj info (0=Land, 1=Stad, 2=Dagar, 3=Pris): 2
Du valde: 7
```

**Facit:**
```python
print("=== Resedetaljer ===")
resa = ["Spanien", "Barcelona", 7, 6500]
print("Data:", resa)
val = int(input("Välj info (0=Land, 1=Stad, 2=Dagar, 3=Pris): "))
print(f"Du valde: {resa[val]}")
```
