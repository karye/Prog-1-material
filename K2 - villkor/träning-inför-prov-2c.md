# Träning inför prov 2c: villkor

Här får du träna på samma moment som kommer på Prov 2c. Temat är **teknik och mobiler**.

---

### Uppgift 1: Android eller inte?

**Uppgift:** Fråga användaren vilket operativsystem deras mobil har. Om svaret är `"android"` ska programmet skriva `"En Android-användare!"`. Annars ska det skriva `"Inte Android."`.

**Exempel på körning 1:**
```text
Operativsystem: android
En Android-användare!
```

**Exempel på körning 2:**
```text
Operativsystem: ios
Inte Android.
```

**Facit:**
```python
os = input("Operativsystem: ")
if os == "android":
    print("En Android-användare!")
else:
    print("Inte Android.")
```

---

### Uppgift 2: Laddat eller urladdat?

**Uppgift:** Fråga användaren hur många procent batteri mobilen har. Om det är 50 eller mer ska programmet skriva `"Batteriet räcker ett tag till."`. Annars ska det skriva `"Dags att ladda!"`.

**Exempel på körning 1:**
```text
Batteri (%): 80
Batteriet räcker ett tag till.
```

**Exempel på körning 2:**
```text
Batteri (%): 20
Dags att ladda!
```

**Facit:**
```python
batteri = int(input("Batteri (%): "))
if batteri >= 50:
    print("Batteriet räcker ett tag till.")
else:
    print("Dags att ladda!")
```

---

### Uppgift 3: Vilket märke?

**Uppgift:** Fråga användaren vilket märke deras mobil är. Om det är `"samsung"` skriv `"Galaxy-användare!"`. Om det är `"apple"` skriv `"iPhone-användare!"`. Annars skriv `"Spännande val!"`.

**Exempel på körning 1:**
```text
Märke: samsung
Galaxy-användare!
```

**Exempel på körning 2:**
```text
Märke: apple
iPhone-användare!
```

**Exempel på körning 3:**
```text
Märke: sony
Spännande val!
```

**Facit:**
```python
marke = input("Märke: ")
if marke == "samsung":
    print("Galaxy-användare!")
elif marke == "apple":
    print("iPhone-användare!")
else:
    print("Spännande val!")
```

---

### Uppgift 4: Prisklass

**Uppgift:** Fråga användaren hur mycket mobilen kostar. Skriv ut vilken prisklass det är:
- Under 2000 kr: `"Budgetmobil"`
- 2000–4999 kr: `"Mellanklass"`
- 5000–9999 kr: `"Premiumklass"`
- 10000 kr eller mer: `"Flaggskepp"`

**Exempel på körning 1:**
```text
Pris (kr): 1500
Budgetmobil
```

**Exempel på körning 2:**
```text
Pris (kr): 3500
Mellanklass
```

**Exempel på körning 3:**
```text
Pris (kr): 7000
Premiumklass
```

**Exempel på körning 4:**
```text
Pris (kr): 12000
Flaggskepp
```

**Facit:**
```python
pris = int(input("Pris (kr): "))
if pris < 2000:
    print("Budgetmobil")
elif pris < 5000:
    print("Mellanklass")
elif pris < 10000:
    print("Premiumklass")
else:
    print("Flaggskepp")
```

---

### Uppgift 5: Mobilkollen

**Uppgift:** Fråga användaren om märket och lagringsutrymme i GB. Om märket är `"apple"`: kontrollera lagringen — om 128 GB eller mer skriv `"Gott om plats för dina appar!"`, annars skriv `"Kan bli fullt snart."`. Om märket inte är `"apple"` ska programmet med en **f-sträng** skriva ut en kommentar om det märket.

**Exempel på körning 1:**
```text
Märke: apple
Lagring (GB): 256
Gott om plats för dina appar!
```

**Exempel på körning 2:**
```text
Märke: apple
Lagring (GB): 64
Kan bli fullt snart.
```

**Exempel på körning 3:**
```text
Märke: samsung
Lagring (GB): 128
Kul med en samsung!
```

**Facit:**
```python
marke = input("Märke: ")
lagring = int(input("Lagring (GB): "))
if marke == "apple":
    if lagring >= 128:
        print("Gott om plats för dina appar!")
    else:
        print("Kan bli fullt snart.")
else:
    print(f"Kul med en {marke}!")
```
