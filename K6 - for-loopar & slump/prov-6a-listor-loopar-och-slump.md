# Prov 6a: for-loopar och slump

I det här provet testas din förmåga att använda for-loopar med listor, bygga listor dynamiskt, samt använda modulen `random` för att slumpa värden. Temat för provet är **mat och inköpslistor**.

---

### Uppgift 1: Skriva ut matvaror

**Uppgift:** Skapa en lista som heter `matvaror` och fyll den med tre saker du gillar att äta. Använd sedan en `for`-loop för att gå igenom listan och skriva ut varje matvara tillsammans med ordet "Gott: " framför.

**Exempel på körning:**
```text
Gott: Pizza
Gott: Tacos
Gott: Hamburgare
```

**Facit:**
```python
matvaror = ["Pizza", "Tacos", "Hamburgare"]

for mat in matvaror:
    print("Gott:", mat)
```

---

### Uppgift 2: Räkna måltider

**Uppgift:** Använd en `for`-loop och funktionen `range()` för att skriva ut siffrorna 1 till 5. Framför varje siffra ska texten "Måltid" skrivas ut.

**Exempel på körning:**
```text
Måltid 1
Måltid 2
Måltid 3
Måltid 4
Måltid 5
```

**Facit:**
```python
for i in range(1, 6):
    print("Måltid", i)
```

---

### Uppgift 3: Lägga till i kundvagnen

**Uppgift:** Skapa en tom lista som heter `kundvagn`. Använd `input()` för att fråga användaren efter en vara, och lägg till den i listan med `.append()`. Upprepa detta så att totalt två varor läggs till. Använd sedan `len()` och en **f-sträng** för att skriva ut hur många varor som finns i listan.

**Exempel på körning:**
```text
Vad vill du lägga i vagnen? Mjölk
Vad mer vill du lägga till? Bröd
Du har nu 2 varor i kundvagnen.
```

**Facit:**
```python
kundvagn = []

vara1 = input("Vad vill du lägga i vagnen? ")
kundvagn.append(vara1)

vara2 = input("Vad mer vill du lägga till? ")
kundvagn.append(vara2)

print(f"Du har nu {len(kundvagn)} varor i kundvagnen.")
```

---

### Uppgift 4: Dagens middag

**Uppgift:** Importera modulen `random`. Skapa en lista med tre olika middagsrätter. Använd funktionen `random.choice()` för att låta datorn slumpa fram en av rätterna. Skriv sedan ut resultatet.

**Exempel på körning (resultatet varierar):**
```text
Idag blir det: Korv med bröd
```

**Facit:**
```python
import random

middagar = ["Pannkakor", "Spaghetti", "Korv med bröd"]
vald_middag = random.choice(middagar)

print("Idag blir det:", vald_middag)
```

---

### Uppgift 5: Obegränsad inköpslista

**Uppgift:** Skapa en tom lista. Använd en `while True`-loop för att fråga användaren efter varor att köpa. Om användaren skriver "klar", avbryts loopen med `break`. Annars läggs varan till i listan med `.append()`. När loopen är klar ska hela listan skrivas ut.

**Exempel på körning:**
```text
Lägg till vara (eller 'klar'): Äpple
Lägg till vara (eller 'klar'): Banan
Lägg till vara (eller 'klar'): klar
Din inköpslista: ['Äpple', 'Banan']
```

**Facit:**
```python
inkopslista = []

while True:
    svar = input("Lägg till vara (eller 'klar'): ")
    if svar == "klar":
        break
    inkopslista.append(svar)

print("Din inköpslista:", inkopslista)
```
