# Prog 1 (EE23A) — Kursmaterial Python

Det här repot innehåller prov och träningsuppgifter för kursen **Programmering 1** på gymnasienivå. Alla uppgifter är skrivna i Markdown och innehåller exempelkörning samt facit i Python.

---

## 📚 Kursens avsnitt

| Avsnitt | Moment |
|---|---|
| **K1** | Input & output |
| **K2** | Villkor |
| **K3** | Loopar (while) |
| **K4** | Listor |
| **K5** | Listor, index & random |
| **K6** | Loopar (for) |
| **K7** | Funktioner |

---

## 📁 Filer per avsnitt

### K1 - print & input
| Fil | Typ | Uppgifter |
|---|---|---|
| `prov-1a-input-och-output.md` | Prov | 5 |
| `prov-1b-input-och-output.md` | Prov (alternativversion) | 5 |
| `träning-inför-prov-1a.md` | Träning | 5 |
| `material-k1-input-och-output.md` | Materialbank | 10 |

### K2 - villkor
| Fil | Typ | Uppgifter |
|---|---|---|
| `material-k2-villkor.md` | Materialbank | 35 |

### K3 - while-loopar
| Fil | Typ | Uppgifter |
|---|---|---|
| `prov-3a-while-loopar.md` | Prov | 5 |
| `material-k3-while-loopar.md` | Materialbank | 10 |

### K4 - listor
| Fil | Typ | Uppgifter |
|---|---|---|
| `material-k4-listor.md` | Materialbank | 30 |

### K5 - index & random
| Fil | Typ | Uppgifter |
|---|---|---|
| `prov-5a-listor-och-index.md` | Prov | 5 |
| `prov-5b-listor-och-index.md` | Prov (alternativversion) | 5 |
| `träning-inför-prov-5a.md` | Träning | 5 |
| `träning-inför-prov-5b.md` | Träning (alternativversion) | 5 |

### K6 - for-loopar
| Fil | Typ | Uppgifter |
|---|---|---|
| `prov-blandat-listor-loopar-och-slump.md` | Prov (K5+K6) | 5 |
| `träning-inför-blandat-listor-loopar-a.md` | Träning (K5+K6) | 5 |
| `träning-inför-blandat-listor-loopar-b.md` | Träning (K5+K6, alternativ) | 5 |

### K7 - funktioner
| Fil | Typ | Uppgifter |
|---|---|---|
| `prov-7a-funktioner.md` | Prov | 5 |
| `prov-7b-funktioner.md` | Prov (alternativversion) | 5 |
| `prov-7c-funktioner.md` | Prov (alternativversion) | 5 |

### blandat — Spänner över flera avsnitt
| Fil | Avsnitt | Typ | Uppgifter |
|---|---|---|---|
| `prov-blandat-villkor-och-loopar.md` | K2+K3+K6 | Prov | 5 |
| `träning-inför-blandat-villkor-och-loopar.md` | K2+K3+K6 | Träning | 5 |

---

## ⚠️ Saknade filer

Följande avsnitt saknar ännu prov och/eller träning:

| Avsnitt | Saknas |
|---|---|
| K1 | Träning inför prov 1b |
| K2 | Prov, träning |
| K3 | Träning inför prov 3a |
| K4 | Prov, träning |
| K6 | Eget prov (enbart for-loopar), material, träning |

---

## 🧠 Pedagogik

### Principer

- **Ett moment i taget.** Varje prov fokuserar på ett avgränsat kodningsmoment. Eleverna ska inte behöva kombinera flera nya koncept på samma gång.
- **Igenkänning via teman.** Uppgifterna använder vardagliga och roliga teman (film, fika, spel, mat, djur) för att sänka tröskeln och hålla motivationen uppe.
- **Exempelkörning som kontrakt.** Varje uppgift har ett tydligt exempel på hur programmet ska se ut när det körs. Det ger eleverna ett konkret mål utan att avslöja lösningen.
- **Facit synligt.** Facit ligger direkt under varje uppgift. Tanken är att eleverna ska lära sig genom att jämföra sitt eget svar med facit — inte att facit ska döljas.
- **Gradvis svårighetsökning inom provet.** Uppgift 1 är alltid enklast, uppgift 5 kräver att eleven kombinerar det nya momentet med tidigare kunskaper (t.ex. input, beräkning, f-sträng).
- **Alternativversioner (a/b/c).** Samma prov finns i flera versioner med olika teman men identisk struktur. Det möjliggör omprov eller parallella grupper utan att uppgifterna sprids.

---

## 📐 Recept för framtida prov

Alla prov följer samma mall. Här beskrivs strukturen så att nya prov enkelt kan skapas.

### Allmän mall

```
# Prov K[n][version]: [moment]

[En mening som beskriver vad provet testar.]

**Regler:** (valfritt, används när regler behövs, t.ex. för funktioner)
* Regel 1
* Regel 2

### Uppgift 1: [lättast]
### Uppgift 2: ...
### Uppgift 3: ...
### Uppgift 4: [ett argument / lite svårare]
### Uppgift 5: [kombinerar momentet med något mer, t.ex. beräkning]
```

Varje uppgift har alltid tre delar:

```markdown
### Uppgift N: [kort beskrivande titel]

**Uppgift:** [Instruktion i löptext. Exakt vad som ska göras, steg för steg om det behövs.]

**Exempel på körning:**
\```text
[Exakt terminalutskrift]
\```

**Facit:**
\```python
[Pythonkod]
\```
```

---

### Recept: K1 — Input och output

**Fokus:** Skriva ut text med `print()`, ta emot inmatning med `input()`, lagra i variabler, bygga meningar med f-strängar.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Skriva ut rubrik + mening | `print("...")` × 2 |
| 2 | Skriva ut flera rader (rapport/meny) | `print("...")` × 4 |
| 3 | Fråga efter ett svar, skriv ut hälsning | `x = input("...")` + `print("Hej", x, "...")` |
| 4 | Två inputs, kombinera i f-sträng | `x = input(...)` × 2 + `print(f"... {x} ... {y} ...")` |
| 5 | Tre inputs, presentera i flera rader | `input()` × 3 + `print(f"...")` × 3 |

**Teman att rotera:** rymd, café/restaurang, sport, skola, djur, resor, musik.

---

### Recept: K2 — Villkor

**Fokus:** Styra programflödet med `if`, `elif`, `else`.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Binärt villkor (text) | `if x == "...": ... else: ...` |
| 2 | Binärt villkor (tal) | `if x >= N: ... else: ...` |
| 3 | Tre-vägsval | `if ... elif ... else ...` |
| 4 | Fyra-vägsval med tal | `if x >= A: elif x >= B: elif x >= C: else:` |
| 5 | Nästade villkor eller AND | `if x == "..." and y == "...":` |

**Teman att rotera:** temperatur, trafikljus, ålder, lösenord, biobiljett, klädval, betyg.

---

### Recept: K3 — Loopar (while)

**Fokus:** Repetera kod med `while True`, ta emot inmatning i loopen, avbryta med `break`.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Oändlig loop, ingen input | `while True: print(...)` |
| 2 | Input i loop, ingen break | `while True: x = input(...); print(...)` |
| 3 | Input i loop, hälsa användaren | `while True: namn = input(...); print("Hej", namn)` |
| 4 | Break på nyckelord | `if x == "q": break` |
| 5 | Meny med if/elif/else + break | `while True: val = input(...); if/elif/else + break` |

**Teman att rotera:** namnlista, skolmat, statusloop, IP-eko, lösenord.

---

### Recept: K4 — Listor

**Fokus:** Skapa listor, lägga till element med `.append()`, räkna med `len()`.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Skapa lista, skriva ut | `lista = [...]` + `print(lista)` |
| 2 | Skapa tom lista, append × 2 | `lista = []` + `lista.append(x)` × 2 |
| 3 | Append + len | `lista.append(x)` + `print(len(lista))` |
| 4 | Input → append → print lista | `x = input(...)` + `lista.append(x)` + `print(lista)` |
| 5 | While-loop + append + break | `while True: input → append eller break` + `print(lista)` |

**Teman att rotera:** inköpslista, namnlista, ryggsäck, favoriter, spellista.

---

### Recept: K5 — Listor, index och random

**Fokus:** Skapa listor med blandade datatyper (`str`, `int`), komma åt element med index, kombinera med `input()`, slumpa med `random`.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Skapa blandad lista, skriv ut hela | `lista = ["text", heltal, heltal]` + `print(lista)` |
| 2 | Given lista, skriv ut hela + första + sista | `lista[0]` och `lista[N]` |
| 3 | Lista + input → välj element (text) | `val = int(input(...))` + `lista[val]` |
| 4 | Lista med heltal + input → välj + enhet | `print(lista[val], "enhet")` |
| 5 | Längre blandad lista (4 element), val 0–3 | Kombinerar allt ovan + etikett i prompt |

**Teman att rotera:** film, sport, snacks, trafik, mobil, spelkaraktär, musik, fika, väder, husdjur.

---

### Recept: K6 — Loopar (for)

**Fokus:** Iterera med `for x in lista` och `for i in range()`.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | for-loop igenom lista + print | `for x in lista: print("text:", x)` |
| 2 | for-loop med range | `for i in range(1, N): print("Ord", i)` |
| 3 | for-loop + f-sträng | `for x in lista: print(f"... {x} ...")` |
| 4 | for-loop med range + beräkning | `for i in range(...): print(i * N)` |
| 5 | for-loop kombinerat med input/lista | Kombinerar K5 + K6 |

**Teman att rotera:** mat, städer, sporter, tal, veckor, planeter.

---

### Recept: K7 — Funktioner

**Fokus:** Definiera och anropa egna funktioner, skicka in argument, göra beräkningar inuti funktioner.

| Uppgift | Vad eleven tränar | Mönster |
|---|---|---|
| 1 | Enkel funktion utan argument | `def f(): print(...)` + `f()` |
| 2 | Samma funktion anropad 3 gånger | `f()` × 3 |
| 3 | Tre funktioner i logisk ordning | `def f1/f2/f3()` + anrop i rätt följd |
| 4 | Funktion med ett argument | `def f(x): print(f"... {x} ...")` + `f("värde")` |
| 5 | Funktion med två argument + beräkning | `def f(a, b): tot = a*b; print(f"... {tot} ...")` |

**Teman att rotera:** spel, bakning, morgonrutin, bio, kvitto, monstrar, resor.

---

## ✅ Checklista när du skapar ett nytt prov

- [ ] 5 uppgifter i stigande svårighetsgrad
- [ ] Varje uppgift har: **Uppgift**, **Exempel på körning**, **Facit**
- [ ] Exempelkörningen matchar exakt vad facit producerar
- [ ] Temat är genomgående och roligt (ett enda tema per prov, t.ex. "bakning")
- [ ] Alternativversioner (b/c) har identisk struktur men nytt tema
- [ ] Träningsfilen är strukturellt identisk med provfilen (samma uppgiftstyper, nytt tema)
- [ ] Filnamn följer mönstret: `prov-[K-nummer][a/b/c]-[moment].md` och `träning-inför-prov-[K-nummer][a/b].md`
