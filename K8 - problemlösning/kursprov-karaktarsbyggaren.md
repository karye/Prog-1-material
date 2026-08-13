# Kursprov: Karaktärsbyggaren

Kursprov som täcker alla moment från K1–K7. Varje uppgift beskriver **vad programmet ska göra** — du som elev ska själv komma på hur du löser det med kod.

**Tema:** Du bygger ett spel där spelaren väljer en karaktär och möter en slumpmässig boss i strid.

**Bedömning:** 5 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Välj din hjälte (4p)

**Uppgift:** Programmet ska innehålla fyra karaktärer: Krigaren, Magikern, Tjuven och Bothågen. Varje karaktär har en styrka och en hälsa. När programmet körs ska det skriva ut en rubrik och visa alla karaktärer. Därefter ska programmet fråga spelaren vilken karaktär hen vill veta mer om (ange en siffra 0–3). Beroende på vilken karaktär spelaren väljer ska programmet skriva ut karaktärens namn, styrka och hälsa. Varje karaktär ska ha unika värden.

**Exempel på körning:**
```text
=== KARAKTÄRSBYGGAREN ===
Hjältar: ['Krigaren', 'Magikern', 'Tjuven', 'Bothågen']
Välj karaktär (0-3): 1
Magikern | Styrka: 8 | Hälsa: 60
```

---

### Uppgift 2: Karaktärsmeny (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 1. När programmet körs ska det upprepade gånger visa en meny med tre val:

1. Inspektera en karaktär (samma visning som i uppgift 1)
2. Visa alla karaktärer
3. Avsluta

Efter varje menyval ska programmet utföra rätt åtgärd och sedan visa menyn igen — utom vid val 3 då programmet ska skriva en avslutningsfras och stanna.

**Exempel på körning:**
```text
=== KARAKTÄRSBYGGAREN ===
Hjältar: ['Krigaren', 'Magikern', 'Tjuven', 'Bothågen']

1. Inspektera karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 2
['Krigaren', 'Magikern', 'Tjuven', 'Bothågen']

1. Inspektera karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 3
Bothågen | Styrka: 12 | Hälsa: 50

1. Inspektera karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 3
Spelet avslutas.
```

---

### Uppgift 3: Bossen uppenbarar sig (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 2, men med två förändringar:

1. **En boss dyker upp.** Varje gång programmet startar ska en boss slumpas fram bland fyra möjliga: Draken, Jätten, Demonen och Skuggan. Bossens styrka ska också slumpas fram — ett tal mellan 5 och 15. Programmet ska meddela att en boss har uppenbarat sig, men **inte** avslöja bossens namn eller styrka.

2. **Karaktärsgalleri.** När spelaren väljer att visa alla karaktärer ska det inte längre se ut som en lista. Istället ska varje karaktär skrivas ut på en egen rad med sitt nummer framför.

3. **Inspektionen förenklas.** Programmet ska inte längre skriva ut karaktärernas stats i förväg. Istället: när spelaren väljer en karaktär skrivs bara karaktärens namn ut. Spelaren får veta stats först i uppgift 4.

**Exempel på körning:**
```text
=== KARAKTÄRSBYGGAREN ===
En boss har uppenbarat sig!

1. Inspektera karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 2
Hjälte 0: Krigaren
Hjälte 1: Magikern
Hjälte 2: Tjuven
Hjälte 3: Bothågen

1. Inspektera karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 0
Du valde Krigaren.
```

---

### Uppgift 4: Strid! (4p)

**Uppgift:** Bygg vidare på programmet från uppgift 3. Nu ska spelaren kunna strida mot bossen.

- När spelaren väljer en karaktär (val 1) ska en strid avgöras direkt. Karaktärerna har fast styrka: Krigaren 10, Magikern 8, Tjuven 6 och Bothågen 12.
- **Stridsregler:** Om karaktärens styrka är **högre än eller lika med** bossens styrka vinner spelaren. Annars förlorar spelaren och förlorar 20 i hälsa.
- Spelaren börjar med 100 i hälsa. Efter varje förlust ska programmet visa hur mycket hälsa som är kvar.
- När hälsan når 0 eller lägre ska programmet meddela att spelaren är besegrad och stanna.
- Om spelaren vinner en strid ska programmet avslöja bossens namn och styrka, gratulera spelaren och stanna.

**Exempel på körning:**
```text
=== KARAKTÄRSBYGGAREN ===
En boss har uppenbarat sig!
Din hälsa: 100

1. Strid med karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 2
Du valde Tjuven (styrka 6).
Du förlorade! Hälsa kvar: 80

1. Strid med karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 0
Du valde Krigaren (styrka 10).
Du besegrade bossen! Det var Draken med styrka 9.
```

---

### Uppgift 5: Paketera spelet (4p)

**Uppgift:** Nu ska hela spelet paketeras så att det enkelt kan startas med olika spelare och olika antal stridsförsök.

- Spelet ska kunna startas genom att ange ett spelarnamn och ett maxantal strider.
- När spelet startar ska det hälsa spelaren välkommen och skriva ut hur många stridsförsök hen har.
- Därefter ska spelet fungera precis som i uppgift 4, men istället för att ha obegränsat med försök ska spelaren bara få det antal strider som angavs vid start. En strid förbrukas oavsett om spelaren vinner eller förlorar.
- När antalet strider tar slut ska programmet meddela detta och stanna — oavsett om bossen är besegrad eller inte.

Utanför spelet ska du starta det med ett valfritt namn och valfritt antal strider.

**Exempel på körning:**
```text
Välkommen Zäta! Du får 3 stridsförsök.
En boss har uppenbarat sig!

1. Strid med karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 2
Du valde Tjuven (styrka 6).
Du förlorade! Strid 1 av 3.

1. Strid med karaktär
2. Visa alla karaktärer
3. Avsluta
Val: 1
Välj karaktär (0-3): 0
Du valde Krigaren (styrka 10).
Du besegrade bossen! Det var Skuggan med styrka 8.
```


