# Prov: If-Else Och If-Elif-Else (Med Exempel Och Facit)

**Instruktion:** Använd bara `print()`, `input()`, `if`, `elif`, `else`. Inga loopar eller egna funktioner. Varje uppgift har en kort uppgiftstext, två exempel på körning (ett där villkoren stämmer och ett där de inte gör det) samt facit.

---

# Sorterad Provbank – Enklast → Svårast

## Uppgift 1 – God morgon och Hej (superenkel)

**Uppgift:** Skriv först en rad **utanför** loopen: `God morgon`. Starta sedan en `while`‑loop som skriver ordet **Hej** flera gånger. **Ingen** inmatning ska användas här.

**Exempel på körning:**

```
God morgon
Hej
Hej
Hej
Hej
(... fortsätter ...)
```

**Facit:**

```python
print("God morgon")
print("Hej")
while True:
    print("Hej")
```

---

## Uppgift 2 – Entrékod (1 Input Text, If-Else)

**Uppgift:** Programmet frågar efter en entrékod och ger besked om tillträde.

**Exempel på körning (rätt):**

```
Skriv entrékod: silver
Tillträde beviljat.
```

**Exempel på körning (fel):**

```
Skriv entrékod: guld
Fel kod.
```

**Facit:**

```python
kod = input("Skriv entrékod: ")
if kod == "silver":
    print("Tillträde beviljat.")
else:
    print("Fel kod.")
```

---

## Uppgift 3 – Aviseringar (1 Input Text, If-Else)

**Uppgift:** Programmet frågar om användaren vill slå på aviseringar (ja/nej) och skriver ett tydligt besked.

**Exempel på körning (ja):**

```
Slå på aviseringar? (ja/nej): ja
Aviseringar påslagna.
```

**Exempel på körning (nej):**

```
Slå på aviseringar? (ja/nej): nej
Aviseringar avstängda.
```

**Facit:**

```python
svar = input("Slå på aviseringar? (ja/nej): ")
if svar == "ja":
    print("Aviseringar påslagna.")
else:
    print("Aviseringar avstängda.")
```

---

## Uppgift 4 – Gästlista (Text, If-Else)

**Uppgift:**
Programmet frågar efter **namn**.
Om namnet är `Alex` ska programmet skriva **"Välkommen tillbaka!"**.
Annars ska det skriva **"Hej namn!"**

**Exempel på körning (stämmer):**

```
Skriv ditt namn: Alex
Välkommen tillbaka!
```

**Exempel på körning (stämmer inte):**

```
Skriv ditt namn: Mira
Hej Mira!
```

**Facit:**

```python
namn = input("Skriv ditt namn: ")
if namn == "Alex":
    print("Välkommen tillbaka!")
else:
    print("Hej " + namn + "!")
```

---

## Uppgift 5 – Nyhetsbrev (1 Input Text, If-Else)

**Uppgift:** Programmet frågar om användaren vill prenumerera (ja/nej) och skriver därefter ett tydligt besked om prenumerationen.

**Exempel på körning (ja):**

```
Vill du prenumerera? (ja/nej): ja
Prenumeration aktiverad.
```

**Exempel på körning (nej):**

```
Vill du prenumerera? (ja/nej): nej
Prenumeration avböjd.
```

**Facit:**

```python
svar = input("Vill du prenumerera? (ja/nej): ")
if svar == "ja":
    print("Prenumeration aktiverad.")
else:
    print("Prenumeration avböjd.")
```

---

## Uppgift 6 – Stad Och Väder (Text, Flera If)

**Uppgift:** Fråga efter **stad** och **väder** (t.ex. "sol", "regn").

* Om staden är `Uppsala` **och** vädret är `sol`: skriv **"Perfekt dag i Uppsala!"**
* Om staden är `Uppsala` (oavsett väder): skriv dessutom **"Hälsa Uppsala!"**

**Exempel på körning (båda villkor uppfyllda):**

```
Skriv stad: Uppsala
Skriv väder: sol
Perfekt dag i Uppsala!
Hälsa Uppsala!
```

**Exempel på körning (delvis uppfyllda villkor):**

```
Skriv stad: Uppsala
Skriv väder: regn
Hälsa Uppsala!
```

**Facit:**

```python
stad = input("Skriv stad: ")
vader = input("Skriv väder: ")
if stad == "Uppsala" and vader == "sol":
    print("Perfekt dag i Uppsala!")
if stad == "Uppsala":
    print("Hälsa Uppsala!")
```

---

## Uppgift 7 – Lösenordscheck L1 (1 Input Text, 2 If-Else)

**Uppgift:** Programmet granskar ett lösenord med två separata kontroller utan specialfunktioner:

1. Om lösenordet **exakt** är `hemlis` ska ett godkännande skrivas.
2. Om lösenordet **exakt** är `HEMLIS` ska ett tips om caps lock skrivas.
   I båda fallen ska det också finnas ett alternativt besked när villkoret inte stämmer.

**Exempel på körning 1 (hemlis):**

```
Skriv lösenord: hemlis
Lösenord godkänt.
Ok.
```

**Exempel på körning 2 (HEMLIS):**

```
Skriv lösenord: HELMIS
Fel lösenord.
Tips: stäng av caps lock.
```

**Exempel på körning 3 (annat):**

```
Skriv lösenord: abc
Fel lösenord.
Ok.
```

**Facit:**

```python
los = input("Skriv lösenord: ")
if los == "hemlis":
    print("Lösenord godkänt.")
else:
    print("Fel lösenord.")
if los == "HELMIS":
    print("Tips: stäng av caps lock.")
else:
    print("Ok.")
```

---

## Uppgift 8 – Lösenordscheck L2 (1 Input Text, 2 If-Else)

**Uppgift:** Programmet kontrollerar ett lösenord med två separata, enkla kontroller (exakta jämförelser):

1. Om lösenordet är `pass123` → skriv godkännande, annars fel.
2. Om lösenordet är `PASS123` → skriv caps lock‑tips, annars OK.

**Exempel på körning 1 (pass123):**

```
Skriv lösenord: pass123
Lösenord godkänt.
Ok.
```

**Exempel på körning 2 (PASS123):**

```
Skriv lösenord: PASS123
Fel lösenord.
Tips: stäng av caps lock.
```

**Exempel på körning 3 (annat):**

```
Skriv lösenord: hejsan
Fel lösenord.
Ok.
```

**Facit:**

```python
los = input("Skriv lösenord: ")
if los == "pass123":
    print("Lösenord godkänt.")
else:
    print("Fel lösenord.")
if los == "PASS123":
    print("Tips: stäng av caps lock.")
else:
    print("Ok.")
```

---

## Uppgift 9 – Domänkoll L1 (1 Input Text, 2 If-Else)

**Uppgift:** Programmet tar emot en **domän** (t.ex. `gmail.com`, `skola.se`) och ger två besked:

1. Om domänen är `gmail.com` ska ett Google-besked skrivas, annars ett annat besked.
2. Om domänen är `skola.se` ska ett skol-besked skrivas, annars ett annat besked.

**Exempel på körning 1 (gmail.com):**

```
Skriv domän: gmail.com
Google-adress.
Ej skoladress.
```

**Exempel på körning 2 (skola.se):**

```
Skriv domän: skola.se
Inte Google.
Skoladress.
```

**Exempel på körning 3 (annan domän):**

```
Skriv domän: example.org
Inte Google.
Ej skoladress.
```

**Facit:**

```python
doman = input("Skriv domän: ")
if doman == "gmail.com":
    print("Google-adress.")
else:
    print("Inte Google.")
if doman == "skola.se":
    print("Skoladress.")
else:
    print("Ej skoladress.")
```

---

## Uppgift 10 – Domänkoll L2 (1 Input Text, 2 If-Else)

**Uppgift:** Programmet tar emot en domän och ger två enkla besked med exakta jämförelser:

1. `outlook.com` → Microsoft‑adress, annars inte.
2. `student.se` → Studeradress, annars inte.

**Exempel på körning 1 (outlook.com):**

```
Skriv domän: outlook.com
Microsoft-adress.
Ej studeradress.
```

**Exempel på körning 2 (student.se):**

```
Skriv domän: student.se
Inte Microsoft.
Studeradress.
```

**Exempel på körning 3 (annan domän):**

```
Skriv domän: mysite.net
Inte Microsoft.
Ej studeradress.
```

**Facit:**

```python
doman = input("Skriv domän: ")
if doman == "outlook.com":
    print("Microsoft-adress.")
else:
    print("Inte Microsoft.")
if doman == "student.se":
    print("Studeradress.")
else:
    print("Ej studeradress.")
```

---

## Uppgift 11 – Supportkategori (Text, If-Elif-Else)

**Uppgift:**
Programmet frågar efter **problemtyp** som text: skriv `nät`, `dator` eller `skrivare`.

* Vid `nät`: skriv **"Kolla kabel och router."**
* Vid `dator`: skriv **"Starta om och testa igen."**
* Vid `skrivare`: skriv **"Kontrollera papper och toner."**
* Annars: skriv **"Okänd kategori."**

**Exempel på körning (nät):**

```
Vilken problemtyp? (nät/dator/skrivare): nät
Kolla kabel och router.
```

**Exempel på körning (dator):**

```
Vilken problemtyp? (nät/dator/skrivare): dator
Starta om och testa igen.
```

**Exempel på körning (skrivare):**

```
Vilken problemtyp? (nät/dator/skrivare): skrivare
Kontrollera papper och toner.
```

**Exempel på körning (annat):**

```
Vilken problemtyp? (nät/dator/skrivare): batteri
Okänd kategori.
```

**Facit:**

```python
typ = input("Vilken problemtyp? (nät/dator/skrivare): ")
if typ == "nät":
    print("Kolla kabel och router.")
elif typ == "dator":
    print("Starta om och testa igen.")
elif typ == "skrivare":
    print("Kontrollera papper och toner.")
else:
    print("Okänd kategori.")
```

---

## Uppgift 12 – Prioritet (Text, If-Elif-Else)

**Uppgift:** Fråga efter **prioritet**: `hög`, `medel` eller `låg`. Programmet ska skriva **endast en** rad beroende på vad användaren skrev:

* `hög` → "Åtgärda omedelbart."
* `medel` → "Planera åtgärd."
* `låg` → "Observera tills vidare."

**Exempel på körning (hög):**

```
Skriv prioritet (hög/medel/låg): hög
Åtgärda omedelbart.
```

**Exempel på körning (medel):**

```
Skriv prioritet (hög/medel/låg): medel
Planera åtgärd.
```

**Exempel på körning (låg):**

```
Skriv prioritet (hög/medel/låg): låg
Observera tills vidare.
```

**Facit:**

```python
prio = input("Skriv prioritet (hög/medel/låg): ")
if prio == "hög":
    print("Åtgärda omedelbart.")
elif prio == "medel":
    print("Planera åtgärd.")
elif prio == "låg":
    print("Observera tills vidare.")
```

---

## Uppgift 13 – Biogräns 11 (1 Input Tal, If-Else)

**Uppgift:** Programmet avgör om en person får se en film med 11-årsgräns utifrån angiven ålder och skriver ett tydligt besked.

**Exempel på körning:**

```
Skriv ålder: 12
Tillåten
```

```
Skriv ålder: 9
Inte tillåten
```

**Facit:**

```python
alder = int(input("Skriv ålder: "))
if alder >= 11:
    print("Tillåten")
else:
    print("Inte tillåten")
```

---

## Uppgift 14 – Åldersgräns För Konto (Tal, If-Else)

**Uppgift:**
Programmet frågar efter **ålder** (heltal).

* Om åldern är **13 eller mer**: skriv **"Du får skapa konto."**
* Annars: skriv **"Tyvärr, för ung."**

**Exempel på körning (stämmer):**

```
Skriv din ålder: 14
Du får skapa konto.
```

**Exempel på körning (stämmer inte):**

```
Skriv din ålder: 11
Tyvärr, för ung.
```

**Facit:**

```python
alder_text = input("Skriv din ålder: ")
alder = int(alder_text)
if alder >= 13:
    print("Du får skapa konto.")
else:
    print("Tyvärr, för ung.")
```

---

## Uppgift 15 – Talgräns 100 (1 Input Tal, If-Else)

**Uppgift:** Programmet avgör om ett angivet heltal är **större än eller lika med 100** eller **mindre än 100** och skriver ett tydligt besked.

**Exempel på körning:**

```
Skriv tal: 140
Minst 100
```

```
Skriv tal: 73
Mindre än 100
```

**Facit:**

```python
tal = int(input("Skriv tal: "))
if tal >= 100:
    print("Minst 100")
else:
    print("Mindre än 100")
```

---

## Uppgift 16 – Poäng Till Betygsbokstav (Tal, If-Elif-Else)

**Uppgift:**
Programmet frågar efter **poäng** (0–100, heltal). Skriv ut betyg enligt:

* **90–100** → `A`
* **75–89** → `B`
* **60–74** → `C`
* **0–59** → `D`

**Exempel på körning (A):**

```
Skriv poäng (0-100): 92
Betyg: A
```

**Exempel på körning (B):**

```
Skriv poäng (0-100): 80
Betyg: B
```

**Exempel på körning (C):**

```
Skriv poäng (0-100): 61
Betyg: C
```

**Exempel på körning (D):**

```
Skriv poäng (0-100): 35
Betyg: D
```

**Facit:**

```python
poang_text = input("Skriv poäng (0-100): ")
poang = int(poang_text)
if poang >= 90:
    print("Betyg: A")
elif poang >= 75:
    print("Betyg: B")
elif poang >= 60:
    print("Betyg: C")
else:
    print("Betyg: D")
```

---

## Uppgift 17 – Studentrabatt (2 Input Text, 2 If-Else, AND)

**Uppgift:** Programmet avgör om en person har rätt till studentrabatt utifrån två svar (student ja/nej och student-ID ja/nej) och ger därefter en tydlig uppföljning.

**Exempel på körning:**

```
Är du student? (ja/nej): ja
Har du student-ID? (ja/nej): nej
Rabatt nekad.
Visa upp giltigt student-ID.
```

```
Är du student? (ja/nej): ja
Har du student-ID? (ja/nej): ja
Rabatt beviljad.
Ingen ytterligare åtgärd.
```

**Facit:**

```python
stud = input("Är du student? (ja/nej): ")
idk = input("Har du student-ID? (ja/nej): ")
if stud == "ja" and idk == "ja":
    print("Rabatt beviljad.")
else:
    print("Rabatt nekad.")
if stud == "ja" and idk == "nej":
    print("Visa upp giltigt student-ID.")
else:
    print("Ingen ytterligare åtgärd.")
```

---

## Uppgift 18 – Salbehörighet (2 Input Text, 2 If-Else, AND)

**Uppgift:** Programmet bedömer tillträde till en sal utifrån om bokning finns och om en lärare är med, och återkopplar med tydliga besked.

**Exempel på körning:**

```
Har du bokning? (ja/nej): ja
Är en lärare med? (ja/nej): nej
Tillträde nekas.
```

```
Har du bokning? (ja/nej): ja
Är en lärare med? (ja/nej): ja
Tillträde beviljas.
```

**Facit:**

```python
bok = input("Har du bokning? (ja/nej): ")
lar = input("Är en lärare med? (ja/nej): ")
if bok == "ja" and lar == "ja":
    print("Tillträde beviljas.")

if bok == "nej" and lar == "nej":
    print("Kräver bokning och lärare.")

```

---

## Uppgift 19 – Inlogg Grund (Text, Nästade If)

**Uppgift:** Fråga efter **användarnamn** och **kod**. Om användarnamnet är `lisa` ska programmet **därefter** kontrollera koden (`hemlis`).

* Rätt båda → skriv: `Välkommen Lisa!`
* Rätt namn men fel kod → skriv: `Fel kod.`
* Fel namn → skriv: `Fel användarnamn.` (kontrollera inte koden då)

**Exempel på körning (båda rätt):**

```
Skriv användarnamn: lisa
Skriv kod: hemlis
Välkommen Lisa!
```

**Exempel på körning (fel kod):**

```
Skriv användarnamn: lisa
Skriv kod: 1234
Fel kod.
```

**Exempel på körning (fel namn):**

```
Skriv användarnamn: liisa
Skriv kod: 1234
Fel användarnamn.
```

**Facit:**

```python
anv = input("Skriv användarnamn: ")
kod = input("Skriv kod: ")
if anv == "lisa":
    if kod == "hemlis":
        print("Välkommen Lisa!")
    else:
        print("Fel kod.")
else:
    print("Fel användarnamn.")
```

---

## Uppgift 20 – Stad Och Väder Plus (Text, Nästade If)

**Uppgift:** Fråga efter **stad** och **väder**. Om staden är `Uppsala`, skriv först `Hälsa Uppsala!` och kontrollera **därefter** vädret:

* Om vädret är `sol` → skriv även `Perfekt dag i Uppsala!`
* Om staden inte är `Uppsala` → skriv `Hej från <stad>.`

**Exempel på körning (Uppsala + sol):**

```
Skriv stad: Uppsala
Skriv väder: sol
Hälsa Uppsala!
Perfekt dag i Uppsala!
```

**Exempel på körning (annan stad):**

```
Skriv stad: Malmö
Skriv väder: regn
Hej från Malmö.
```

**Facit:**

```python
stad = input("Skriv stad: ")
vader = input("Skriv väder: ")
if stad == "Uppsala":
    print("Hälsa Uppsala!")
    if vader == "sol":
        print("Perfekt dag i Uppsala!")
else:
    print("Hej från " + stad + ".")
```

---

## Uppgift 21 – Poäng Med Bonus (Tal + Text, Nästade If)

**Uppgift:** Fråga efter **poäng** (heltal) och om **bonus** används (`ja`/`nej`).

* Om poäng ≥ 60 → skriv `Godkänt`. Inuti samma gren: om bonus = `ja` → skriv även `Bonus registrerad.`
* Om poäng < 60 → skriv `Underkänt` (ignorera bonus i denna gren).

**Exempel på körning (godkänt + bonus):**

```
Skriv poäng: 60
Använd bonus? (ja/nej): ja
Godkänt
Bonus registrerad.
```

**Exempel på körning (underkänt):**

```
Skriv poäng: 45
Använd bonus? (ja/nej): ja
Underkänt
```

**Facit:**

```python
p_text = input("Skriv poäng: ")
bonus = input("Använd bonus? (ja/nej): ")
poang = int(p_text)
if poang >= 60:
    print("Godkänt")
    if bonus == "ja":
        print("Bonus registrerad.")
else:
    print("Underkänt")
```

---

## Uppgift 22 – Nätverk: VLAN-Typ (Text, Nästade If)

**Uppgift:** Fråga efter **VLAN-ID** (som text) och **trafiktyp** (`voice` eller `data`).

* Om trafiktypen är `voice` → skriv `Röst-VLAN: <ID>` och kontrollera **därefter** om ID är `10`. Om ja → skriv `Standard röst-VLAN.`
* Om trafiktypen är `data` → skriv `Data-VLAN: <ID>`.
* Annars → skriv `Okänd trafiktyp.`

**Exempel på körning (voice + standard):**

```
Skriv VLAN-ID: 10
Skriv trafiktyp (voice/data): voice
Röst-VLAN: 10
Standard röst-VLAN.
```

**Exempel på körning (data):**

```
Skriv VLAN-ID: 20
Skriv trafiktyp (voice/data): data
Data-VLAN: 20
```

**Exempel på körning (okänd):**

```
Skriv VLAN-ID: 99
Skriv trafiktyp (voice/data): video
Okänd trafiktyp.
```

**Facit:**

```python
vid = input("Skriv VLAN-ID: ")
typ = input("Skriv trafiktyp (voice/data): ")
if typ == "voice":
    print("Röst-VLAN: " + vid)
    if vid == "10":
        print("Standard röst-VLAN.")
elif typ == "data":
    print("Data-VLAN: " + vid)
else:
    print("Okänd trafiktyp.")
```

---

---

## Uppgift 23 – Biljettkategori (If-Elif-Else)

**Uppgift:** Programmet frågar efter en biljettkategori: `barn`, `ungdom` eller `vuxen`. Skriv ett tydligt besked.

**Exempel på körning (barn):**

```
Skriv biljettkategori (barn/ungdom/vuxen): barn
Prisnivå: reducerad
```

**Exempel på körning (ungdom):**

```
Skriv biljettkategori (barn/ungdom/vuxen): ungdom
Prisnivå: mellan
```

**Exempel på körning (vuxen):**

```
Skriv biljettkategori (barn/ungdom/vuxen): vuxen
Prisnivå: ordinarie
```

**Facit:**

```python
kat = input("Skriv biljettkategori (barn/ungdom/vuxen): ")
if kat == "barn":
    print("Prisnivå: reducerad")
elif kat == "ungdom":
    print("Prisnivå: mellan")
else:
    print("Prisnivå: ordinarie")
```

---

## Uppgift 24 – Temperaturkoll (Tal, If-Elif-Else)

**Uppgift:** Programmet frågar efter temperatur (heltal). Skriv ett besked:

* 25 eller mer → "Varm dag"
* 10 till 24 → "Lagom"
* Mindre än 10 → "Kallt"

**Exempel på körning (varmt):**

```
Skriv temperatur (°C): 27
Varm dag
```

**Exempel på körning (lagom):**

```
Skriv temperatur (°C): 18
Lagom
```

**Exempel på körning (kallt):**

```
Skriv temperatur (°C): 4
Kallt
```

**Facit:**

```python
t_text = input("Skriv temperatur (°C): ")
t = int(t_text)
if t >= 25:
    print("Varm dag")
elif t >= 10:
    print("Lagom")
else:
    print("Kallt")
```

---

## Uppgift 25 – Skollunch Val (If-Elif-Elif-Else)

**Uppgift:** Programmet frågar efter kostval: `vegetarisk`, `vegansk`, `kott` eller något annat. Skriv ett besked.

**Exempel på körning (vegetarisk):**

```
Skriv kostval (vegetarisk/vegansk/kott): vegetarisk
Kök: grön meny
```

**Exempel på körning (vegansk):**

```
Skriv kostval (vegetarisk/vegansk/kott): vegansk
Kök: växtbaserad
```

**Exempel på körning (kott):**

```
Skriv kostval (vegetarisk/vegansk/kott): kott
Kök: klassisk meny
```

**Exempel på körning (annat):**

```
Skriv kostval (vegetarisk/vegansk/kott): halal
Kök: specialkost
```

**Facit:**

```python
val = input("Skriv kostval (vegetarisk/vegansk/kott): ")
if val == "vegetarisk":
    print("Kök: grön meny")
elif val == "vegansk":
    print("Kök: växtbaserad")
elif val == "kott":
    print("Kök: klassisk meny")
else:
    print("Kök: specialkost")
```

---

## Uppgift 26 – Klädråd Efter Temperatur (Tal, If-Elif-Elif-Else)

**Uppgift:** Programmet frågar efter temperatur (heltal) och ger klädråd:

* 30 eller mer → "T‑shirt"
* 20–29 → "Lätt jacka"
* 10–19 → "Tröja"
* Mindre än 10 → "Vinterjacka"

**Exempel på körning (≥30°C):**

```
Skriv temperatur (°C): 33
T-shirt
```

**Exempel på körning (20–29°C):**

```
Skriv temperatur (°C): 25
Lätt jacka
```

**Exempel på körning (10–19°C):**

```
Skriv temperatur (°C): 12
Tröja
```

**Exempel på körning (<10°C):**

```
Skriv temperatur (°C): 5
Vinterjacka
```

**Facit:**

```python
t_text = input("Skriv temperatur (°C): ")
t = int(t_text)
if t >= 30:
    print("T-shirt")
elif t >= 20:
    print("Lätt jacka")
elif t >= 10:
    print("Tröja")
else:
    print("Vinterjacka")
```

---

## Uppgift 27 – Transportval (If-Elif-Else)

**Uppgift:** Programmet frågar efter färdsätt: `buss`, `tåg` eller `cykel`. Skriv ett besked som inte innehåller ordet från inmatningen.

**Exempel på körning (buss):**

```
Skriv färdsätt (buss/tåg/cykel): buss
Resplan: kollektivtrafik
```

**Exempel på körning (tåg):**

```
Skriv färdsätt (buss/tåg/cykel): tåg
Resplan: fjärr eller pendel
```

**Exempel på körning (annat):**

```
Skriv färdsätt (buss/tåg/cykel): bil
Resplan: egen lösning
```

**Facit:**

```python
satt = input("Skriv färdsätt (buss/tåg/cykel): ")
if satt == "buss":
    print("Resplan: kollektivtrafik")
elif satt == "tåg":
    print("Resplan: fjärr eller pendel")
else:
    print("Resplan: egen lösning")
```

---

## Uppgift 28 – Supportkanal (If-Elif-Elif-Else)

**Uppgift:** Programmet frågar efter supportkanal: `telefon`, `chatt`, `e-post` eller annat. Skriv ett besked utan att upprepa kanalen ordagrant.

**Exempel på körning (telefon):**

```
Välj supportkanal (telefon/chatt/e-post): telefon
Spårning: samtal öppnat
```

**Exempel på körning (chatt):**

```
Välj supportkanal (telefon/chatt/e-post): chatt
Spårning: liveärende
```

**Exempel på körning (e-post):**

```
Välj supportkanal (telefon/chatt/e-post): e-post
Spårning: inkorgsärende
```

**Exempel på körning (annat):**

```
Välj supportkanal (telefon/chatt/e-post): forum
Spårning: övrig kanal
```

**Facit:**

```python
kanal = input("Välj supportkanal (telefon/chatt/e-post): ")
if kanal == "telefon":
    print("Spårning: samtal öppnat")
elif kanal == "chatt":
    print("Spårning: liveärende")
elif kanal == "e-post":
    print("Spårning: inkorgsärende")
else:
    print("Spårning: övrig kanal")
```

---

## Uppgift 29 – Lektionstyp (If-Elif-Else)

**Uppgift:** Programmet frågar efter lektionstyp: `teori`, `labb` eller `idrott`. Skriv ett besked utan att upprepa inmatad lektionstyp.

**Exempel på körning (teori):**

```
Skriv lektionstyp (teori/labb/idrott): teori
Upplägg: genomgång
```

**Exempel på körning (labb):**

```
Skriv lektionstyp (teori/labb/idrott): labb
Upplägg: praktiskt arbete
```

**Exempel på körning (idrott):**

```
Skriv lektionstyp (teori/labb/idrott): idrott
Upplägg: aktivitet
```

**Facit:**

```python
typ = input("Skriv lektionstyp (teori/labb/idrott): ")
if typ == "teori":
    print("Upplägg: genomgång")
elif typ == "labb":
    print("Upplägg: praktiskt arbete")
else:
    print("Upplägg: aktivitet")
```

---

## Uppgift 30 – Matallergi (If-Elif-Elif-Else)

**Uppgift:** Programmet frågar efter allergi: `gluten`, `laktos`, `nötter` eller annat. Skriv en anpassning utan att upprepa inmatat ord.

**Exempel på körning (gluten):**

```
Ange allergi (gluten/laktos/nötter): gluten
Serveras utan spannmål
```

**Exempel på körning (laktos):**

```
Ange allergi (gluten/laktos/nötter): laktos
Serveras med laktosfritt alternativ
```

**Exempel på körning (nötter):**

```
Ange allergi (gluten/laktos/nötter): nötter
Serveras utan spår av nötter
```

**Exempel på körning (annat):**

```
Ange allergi (gluten/laktos/nötter): fisk
Serveras enligt överenskommelse
```

**Facit:**

```python
allergi = input("Ange allergi (gluten/laktos/nötter): ")
if allergi == "gluten":
    print("Serveras utan spannmål")
elif allergi == "laktos":
    print("Serveras med laktosfritt alternativ")
elif allergi == "nötter":
    print("Serveras utan spår av nötter")
else:
    print("Serveras enligt överenskommelse")
```

---

# Nytt prov – While-loopen (5 uppgifter)

## Uppgift 31 – Statusloop med stopp (superenkel)

**Uppgift:** Skriv ut en statusrad i en loop. Fråga varje varv om programmet ska fortsätta. Om svaret är `n` ska programmet avsluta loopen.

**Exempel på körning:**

```
Status: wifi anslutet
Fortsätta? (j/n): j
Fortsätter...
Status: wifi anslutet
Fortsätta? (j/n): n
Avslutar.
```

---

## Uppgift 32 – IP-eko tills q (eko och break)

**Uppgift:** Fråga om en IP‑adress i en loop och skriv ut vald IP. Avsluta när användaren skriver `q`.

**Exempel på körning:**

```
Skriv IP (q för att sluta): 192.168.0.10
Vald IP: 192.168.0.10
Skriv IP (q för att sluta): 10.0.0.5
Vald IP: 10.0.0.5
Skriv IP (q för att sluta): q
Stänger IP-eko.
```

**Facit:**

```python
while True:
    ip = input("Skriv IP (q för att sluta): ")
    if ip == "q":
        print("Stänger IP-eko.")
        break
    else:
        print("Vald IP:", ip)
```

---

## Uppgift 33 – Logg med enter/q (paus eller stoppa)

**Uppgift:** Skriv en loggrad. Fråga direkt efter varje rad: `Enter för ny logg, q för att sluta:`. Fortsätt på enter, avsluta på `q`.

**Exempel på körning (fortsätta, sedan stoppa):**

```
Logg: nätverk OK
Enter för ny logg, q för att sluta:
Fortsätter loggning...
Logg: nätverk OK
Enter för ny logg, q för att sluta: q
Logg stoppad.
```

---

## Uppgift 34 – Enkel meny i loop (1/2/3)

**Uppgift:** Visa en liten meny i en loop. På 1, skriv en IP‑rad. På 2, skriv ett wifi‑namn. På 3, skriv "Hej då!" och avsluta. Annars skriv "Fel val" och visa menyn igen.

**Exempel på körning:**

```
1. Visa IP
2. Visa wifi
3. Avsluta
Välj: 2
Wifi: SkolWifi
1. Visa IP
2. Visa wifi
3. Avsluta
Välj: 1
IP: 10.0.0.5
1. Visa IP
2. Visa wifi
3. Avsluta
Välj: 3
Hej då!
```

**Facit:**

```python
while True:
    print("1. Visa IP")
    print("2. Visa wifi")
    print("3. Avsluta")
    val = input("Välj: ")
    if val == "1":
        print("IP: 10.0.0.5")
    elif val == "2":
        print("Wifi: SkolWifi")
    elif val == "3":
        print("Hej då!")
        break
    else:
        print("Fel val")
```

---

## Uppgift 35 – Startsekvens med avbrott

**Uppgift:** Kör en startsekvens i flera steg inuti en loop. Efter varje steg (eller efter två steg) fråga om start ska avbrytas. Avbryt på `j`. Om alla steg körts utan avbrott: skriv "Start klar" och avsluta.

**Exempel på körning 1 (ingen avbrytning):**

```
Start: init router
Avbryta start? (j/n): n
Start: init wifi
Avbryta start? (j/n): n
Start: init brandvägg
Start klar
```

**Exempel på körning 2 (avbryts):**

```
Start: init router
Avbryta start? (j/n): j
Start avbruten
```
