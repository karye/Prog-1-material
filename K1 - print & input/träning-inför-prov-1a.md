# Träningsuppgifter inför prov 1a: input och print

Här får du träna på att skriva ut text med `print()` och att ta emot svar från användaren med `input()`. Det är grundstenarna i Python — allt annat bygger på dessa!

### Uppgift 1ab: skriv ut ett meddelande

**Uppgift:** Skriv ett program som skriver ut två rader: först en rubrik och sedan en mening. Du ska bara använda `print()`.

**Exempel på körning:**

```text
=== Caféet ===
Välkommen, vad får det lov att vara?
```

**Facit:**

```python
print("=== Caféet ===")
print("Välkommen, vad får det lov att vara?")
```

---

### Uppgift 1bb: skriv ut flera rader information

**Uppgift:** Skriv ett program som skriver ut en liten meny med fyra rader: en rubrik, och tre maträtter. Använd bara `print()`.

**Exempel på körning:**

```text
=== Dagens meny ===
1. Köttbullar med mos
2. Laxpasta
3. Vegetarisk curry
```

**Facit:**

```python
print("=== Dagens meny ===")
print("1. Köttbullar med mos")
print("2. Laxpasta")
print("3. Vegetarisk curry")
```

---

### Uppgift 1cb: fråga efter namn och hälsa

**Uppgift:** Fråga användaren vad de heter med `input()`. Spara svaret i en variabel och skriv sedan ut en personlig hälsning.

**Exempel på körning:**

```text
Vad heter du? Marcus
Hej Marcus, kul att du är här!
```

**Facit:**

```python
namn = input("Vad heter du? ")
print("Hej", namn, "kul att du är här!")
```

---

### Uppgift 1db: fråga efter namn och favoritfärg

**Uppgift:** Fråga användaren efter deras namn och vad deras favoritfärg är. Skriv sedan ut en mening som använder båda svaren. Använd en f-sträng.

**Exempel på körning:**

```text
Vad heter du? Elin
Vad är din favoritfärg? lila
Hej Elin! Kul att din favoritfärg är lila.
```

**Facit:**

```python
namn = input("Vad heter du? ")
farg = input("Vad är din favoritfärg? ")
print(f"Hej {namn}! Kul att din favoritfärg är {farg}.")
```

---

### Uppgift 1eb: skapa ett presentationskort

**Uppgift:** Fråga användaren efter tre saker: namn, ålder och favorithobbyn. Skriv sedan ut ett presentationskort i tre rader med hjälp av f-strängar.

**Exempel på körning:**

```text
Namn: Sofia
Ålder: 17
Favorithobbyn: fotboll
--- Presentationskort ---
Jag heter Sofia och är 17 år gammal.
Min favorithobbyn är fotboll.
Trevligt att träffas!
```

**Facit:**

```python
namn = input("Namn: ")
alder = input("Ålder: ")
hobby = input("Favorithobbyn: ")
print("--- Presentationskort ---")
print(f"Jag heter {namn} och är {alder} år gammal.")
print(f"Min favorithobbyn är {hobby}.")
print("Trevligt att träffas!")
```
