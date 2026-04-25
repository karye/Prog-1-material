# Prov 3a: while-loopar

Detta prov testar dina kunskaper i att använda `while`-loopar. Du ska kunna skriva program som upprepar sig, tar emot inmatning och kan avslutas på rätt sätt.

**Regler:**
* Använd alltid en `while True:`-loop.
* Var noga med indentering (indrag).
* I uppgift 3–5 används också `input()`.
* I uppgift 4–5 används `if` och `break`.

---

### Uppgift 1: träna loopar (while och print)

**Uppgift:** Skriv ett program som använder en `while`-loop för att skriva ut meningen `Jag tränar while-loopar` om och om igen. Skriv rubriken `Loopar` utanför loopen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
----- Loopar -----
Jag tränar while-loopar
Jag tränar while-loopar
Jag tränar while-loopar
(... fortsätter ...)
```

**Facit:**
```python
print("----- Loopar -----")
while True:
    print("Jag tränar while-loopar")
```

---

### Uppgift 2: upprepa ett meddelande (input och while)

**Uppgift:** Be användaren skriva ett meddelande **en gång, utanför loopen**. Starta sedan en `while`-loop som skriver ut samma meddelande om och om igen. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Skriv ett meddelande: Hej från loopen!
Startar loopen...
Hej från loopen!
Hej från loopen!
Hej från loopen!
(... fortsätter ...)
```

**Facit:**
```python
text = input("Skriv ett meddelande: ")
print("Startar loopen...")
while True:
    print(text)
```

---

### Uppgift 3: hälsa på besökare (while, input och print)

**Uppgift:** Skriv ett program med en `while`-loop som i **varje varv** frågar efter ett namn och direkt skriver ut en hälsning med namnet. Du behöver inte avsluta loopen.

**Exempel på körning:**
```text
Välkommen!
Skriv ett namn: Lisa
Hej Lisa
Skriv ett namn: Ali
Hej Ali
Skriv ett namn: Sara
Hej Sara
(... fortsätter ...)
```

**Facit:**
```python
print("Välkommen!")
while True:
    namn = input("Skriv ett namn: ")
    print("Hej", namn)
```

---

### Uppgift 4: avsluta med q (while, input, if och break)

**Uppgift:** Skriv ett program med en `while`-loop som i varje varv frågar efter ett namn och skriver `Hej` plus namnet. Om användaren skriver `q` ska programmet skriva `Programmet avslutas` och sedan avsluta loopen med `break`.

**Exempel på körning:**
```text
Namnlista:
Skriv ett namn (q för att sluta): Lisa
Hej Lisa
Skriv ett namn (q för att sluta): Ali
Hej Ali
Skriv ett namn (q för att sluta): q
Programmet avslutas
```

**Facit:**
```python
print("Namnlista:")
while True:
    namn = input("Skriv ett namn (q för att sluta): ")
    if namn == "q":
        print("Programmet avslutas")
        break
    print("Hej", namn)
```

---

### Uppgift 5: skolmatsmeny (while, input, if-elif-else och break)

**Uppgift:** Skriv ett program med en `while`-loop som visar en meny och väntar på ett val. På `1` skriv ut `Dagens lunch: Pasta med tomatsås`. På `2` skriv ut `Matsedel: Mån-pasta, Tis-soppa, Ons-pannkakor`. På `3` skriv ut `Avslutar meny` och avsluta loopen. För andra val skriv `Fel val`.

**Exempel på körning:**
```text
Skolmatsmeny
============

1. Visa dagens lunch
2. Visa matsedel för veckan
3. Avsluta
Val: 1
Dagens lunch: Pasta med tomatsås

1. Visa dagens lunch
2. Visa matsedel för veckan
3. Avsluta
Val: 3
Avslutar meny
```

**Facit:**
```python
print("Skolmatsmeny")
print("============")
while True:
    print()
    print("1. Visa dagens lunch")
    print("2. Visa matsedel för veckan")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Dagens lunch: Pasta med tomatsås")
    elif val == "2":
        print("Matsedel: Mån-pasta, Tis-soppa, Ons-pannkakor")
    elif val == "3":
        print("Avslutar meny")
        break
    else:
        print("Fel val")
```
