# Prov 2d: Villkor – C-nivå

Detta prov testar din förmåga att självständigt använda `if`, `elif` och `else` för att styra programmets flöde. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Vardagsbeslut.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Frukosttips (7p)

**Uppgift:** Programmet ska fråga användaren efter två saker: en tid på dygnet och en allergi. Baserat på svaren ska programmet ge ett frukostförslag.

- Tiden ska läsas in som en siffra (0–23). **Före klockan 10** är det frukostdags – då ska programmet föreslå en frukost. **Klockan 10 eller senare** ska programmet säga att frukosten är stängd.
- Om det är frukostdags: programmet ska också fråga om allergi. Om svaret är `"laktos"` föreslås havregrynsgröt, om svaret är `"gluten"` föreslås yoghurt, annars föreslås pannkakor.
- Använd f-sträng i minst en av utskrifterna.

**Exempel på körning:**
```text
Vad är klockan? 7
Allergi: gluten
Frukosttips: yoghurt
```

```text
Vad är klockan? 12
Frukosten är stängd – testa lunchen istället!
```

**Facit:**
```python
tid = int(input("Vad är klockan? "))
if tid < 10:
    allergi = input("Allergi: ")
    if allergi == "laktos":
        print("Frukosttips: havregrynsgröt")
    elif allergi == "gluten":
        print("Frukosttips: yoghurt")
    else:
        print("Frukosttips: pannkakor")
else:
    print("Frukosten är stängd – testa lunchen istället!")
```

---

### Uppgift 2: Träningsprogram (7p)

**Uppgift:** Programmet ska fråga användaren efter deras träningsnivå och mål. Baserat på svaren ska programmet skriva ut ett personligt träningsprogram.

* Fråga först efter träningsnivå: `"nybörjare"`, `"van"` eller `"elit"`.
* Fråga sedan efter mål: `"styrka"` eller `"kondition"`.
* Baserat på kombinationen ska programmet skriva ut ett träningsupplägg. Du hittar själv på vad de olika uppläggen innehåller – använd f-strängar för att väva in nivå och mål i utskriften.
* Om användaren skriver något annat än de giltiga alternativen ska programmet skriva ut ett felmeddelande.

**Exempel på körning:**
```text
Träningsnivå (nybörjare/van/elit): nybörjare
Mål (styrka/kondition): styrka
Program: 3 x 10 armhävningar, 3 x 10 knäböj. Vila 60s mellan set.
```

```text
Träningsnivå (nybörjare/van/elit): van
Mål (styrka/kondition): kondition
Program: 30 min löpning i medeltempo, avsluta med 5 min stretch.
```

**Facit:**
```python
niva = input("Träningsnivå (nybörjare/van/elit): ")
mal = input("Mål (styrka/kondition): ")

if niva == "nybörjare" and mal == "styrka":
    print("Program: 3 x 10 armhävningar, 3 x 10 knäböj. Vila 60s mellan set.")
elif niva == "nybörjare" and mal == "kondition":
    print("Program: 20 min rask promenad, avsluta med lätt stretch.")
elif niva == "van" and mal == "styrka":
    print("Program: 4 x 12 marklyft, 4 x 12 bänkpress. Vila 45s mellan set.")
elif niva == "van" and mal == "kondition":
    print("Program: 30 min löpning i medeltempo, avsluta med 5 min stretch.")
elif niva == "elit" and mal == "styrka":
    print("Program: 5 x 5 tunga marklyft, 5 x 5 knäböj. Fokus på explosivitet.")
elif niva == "elit" and mal == "kondition":
    print("Program: 10 km löpning i högt tempo, intervallavslut 4 x 400 m.")
else:
    print("Ogiltigt val. Ange nybörjare/van/elit och styrka/kondition.")
```

---

### Uppgift 3: Biobiljett (6p)

**Uppgift:** Programmet ska beräkna priset på en biobiljett baserat på ålder och tidpunkt.

* Fråga efter ålder och vilken typ av visning (`"matiné"` eller `"kväll"`).
* Regler:
  - **Under 12 år:** alltid 80 kr.
  - **12–17 år:** 100 kr på matiné, 120 kr på kväll.
  - **18–64 år:** 120 kr på matiné, 140 kr på kväll.
  - **65 år eller äldre:** alltid 90 kr.
* Skriv ut priset med en f-sträng. Om visningstypen inte är `"matiné"` eller `"kväll"` ska programmet skriva `"Ogiltig visningstyp"`.

**Exempel på körning:**
```text
Ålder: 15
Visning (matiné/kväll): kväll
Pris: 120 kr
```

```text
Ålder: 70
Visning (matiné/kväll): matiné
Pris: 90 kr
```

**Facit:**
```python
alder = int(input("Ålder: "))
visning = input("Visning (matiné/kväll): ")

if visning not in ("matiné", "kväll"):
    print("Ogiltig visningstyp")
elif alder < 12:
    print("Pris: 80 kr")
elif alder < 18:
    if visning == "matiné":
        print("Pris: 100 kr")
    else:
        print("Pris: 120 kr")
elif alder < 65:
    if visning == "matiné":
        print("Pris: 120 kr")
    else:
        print("Pris: 140 kr")
else:
    print("Pris: 90 kr")
```
