# Prov 1a: input och print

Detta prov testar dina kunskaper i att skriva ut text med `print()` och att ta emot information från användaren med `input()`.

---

### Uppgift 1: skriv ut ett meddelande

**Uppgift:** Skriv ett program som skriver ut två rader: först en rubrik och sedan en mening. Du ska bara använda `print()`.

**Exempel på körning:**

```text
=== Rymdbasen ===
Välkommen till kontrollrummet!
```

**Facit:**

```python
print("=== Rymdbasen ===")
print("Välkommen till kontrollrummet!")
```

---

### Uppgift 2: skriv ut flera rader information

**Uppgift:** Skriv ett program som skriver ut en liten rapport med fyra rader: en rubrik, uppdragsnamn, destination och status. Använd bara `print()`.

**Exempel på körning:**

```text
=== Uppdragsrapport ===
Uppdrag: Apollo 99
Destination: Mars
Status: Redo för start
```

**Facit:**

```python
print("=== Uppdragsrapport ===")
print("Uppdrag: Apollo 99")
print("Destination: Mars")
print("Status: Redo för start")
```

---

### Uppgift 3: fråga efter namn och hälsa

**Uppgift:** Fråga användaren vad de heter med `input()`. Spara svaret i en variabel och skriv sedan ut en personlig hälsning.

**Exempel på körning:**

```text
Vad heter du? Laila
Hej Laila, välkommen ombord!
```

**Facit:**

```python
namn = input("Vad heter du? ")
print("Hej", namn, "välkommen ombord!")
```

---

### Uppgift 4: fråga efter namn och hemplanet

**Uppgift:** Fråga användaren efter deras namn och vilket planet de kommer ifrån. Skriv sedan ut en mening som använder båda svaren. Använd en f-sträng.

**Exempel på körning:**

```text
Vad heter du? Yusuf
Vilket planet kommer du från? Jupiter
Hej Yusuf! Det är långt från Jupiter hit.
```

**Facit:**

```python
namn = input("Vad heter du? ")
planet = input("Vilket planet kommer du från? ")
print(f"Hej {namn}! Det är långt från {planet} hit.")
```

---

### Uppgift 5: skapa ett rymdbrev

**Uppgift:** Fråga användaren efter tre saker: namn, ålder och favoritplanet. Skriv sedan ut en fullständig presentation i tre rader med hjälp av f-strängar.

**Exempel på körning:**

```text
Namn: Fatima
Ålder: 16
Favoritplanet: Saturnus
--- Rymdbrev ---
Jag heter Fatima och är 16 år gammal.
Mitt favoritplanet är Saturnus.
En dag ska jag åka dit!
```

**Facit:**

```python
namn = input("Namn: ")
alder = input("Ålder: ")
favoritplanet = input("Favoritplanet: ")
print("--- Rymdbrev ---")
print(f"Jag heter {namn} och är {alder} år gammal.")
print(f"Mitt favoritplanet är {favoritplanet}.")
print("En dag ska jag åka dit!")
```
