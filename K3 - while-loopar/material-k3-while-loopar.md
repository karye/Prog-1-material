# Prov: while-loopen – 10 uppgifter

**Regel:** Använd `while` (gärna `while True`), `print()`, `input()` och vid behov `if`/`elif`/`else`. **Undvik variabler i uppgift 1–5.** Från och med **uppgift 6** får variabler användas. Använd `break` först från **uppgift 4**. Varje uppgift har **exempelkörning** och **facit**.

---

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

**Facit:**

```python
print("God morgon")
print("Hej")
while input("Tryck Enter för en gång till (q=sluta): ") != "q":
    print("Hej")
print("Hejdå")
```

**Facit:**

```python
print("Hej! (utan loop)")

i = 0
while i < 1:
    print("Hej! (i loop)")
    i = i + 1
```

---

## Uppgift 2 – Status upprepas (utan input)

**Uppgift:** Skriv först en rad **utanför** loopen: `Status: igång`. Starta sedan en `while`‑loop som **upprepar två rader** varje varv: `Status: igång` och `Arbetar...`. **Ingen** inmatning ska användas här.

**Exempel på körning:**

```
Status: igång
Status: igång
Arbetar...
Status: igång
Arbetar...
Status: igång
Arbetar...
(... fortsätter ...)
```

**Facit:**

```python
print("Status: igång")
while True:
    print("Status: igång")
    print("Arbetar...")
```

**Facit:**

```python
input("Tryck Enter för att starta: ")
print("Status: igång")
while input("Fortsätta? (Enter/q): ") != "q":
    print("Status: igång")
print("Avslutar.")
```

**Facit:**

```python
val = ""
while val != "q":
    print("Status: igång")
    val = input("Fortsätta? (Enter/q): ")
print("Avslutar.")
```

---

## Uppgift 3 – Hälsning på begäran (utan variabler)

**Uppgift:** I en `while`‑loop: först en fråga som avgör om eleven vill ha en hälsning (`ja`), sedan själva hälsningen. Avsluta om första frågan besvaras med `q`. **Ingen** lagring av värden.

**Exempel på körning:**

```
Startar hälsningar...
Fortsätta? (Enter/q): 
Vill du ha en hälsning? (ja/Enter): ja
Hej!
Fortsätta? (Enter/q): 
Vill du ha en hälsning? (ja/Enter): 
(ingen hälsning)
Fortsätta? (Enter/q): q
Hejdå!
```

**Facit:**

```python
print("Startar hälsningar...")
while input("Fortsätta? (Enter/q): ") != "q":
    if input("Vill du ha en hälsning? (ja/Enter): ") == "ja":
        print("Hej!")
print("Hejdå!")
```

**Facit:**

```python
namn = ""
while namn != "q":
    namn = input("Skriv förnamn (q för att sluta): ")
    if namn != "q":
        print("Hej", namn + "!")
print("Hejdå!")
```

---

## Uppgift 4 – Första break

**Uppgift:** Använd `while True` och **break**. Fortsätt skriva `Loopar...` tills användaren skriver `stop`. Då skrivs `Avslutar.` och loopen bryts.

**Exempel på körning:**

```
Loopar...
Skriv "stop" för att avsluta (Enter annars): 
Loopar...
Skriv "stop" för att avsluta (Enter annars): stop
Avslutar.
```

**Facit:**

```python
while True:
    print("Loopar...")
    if input('Skriv "stop" för att avsluta (Enter annars): ') == "stop":
        print("Avslutar.")
        break
```

**Facit:**

```python
varv = 0
while True:
    varv = varv + 1
    print("Varv:", varv)
    svar = input("Fortsätta? (j/n): ")
    if svar == "n":
        print("Klar.")
        break
```

---

## Uppgift 5 – Små val i loopen (utan variabler)

**Uppgift:** I varje varv får eleven tre chanser i följd: visa IP, visa wifi, eller avsluta. Varje val frågas separat och kan lämnas tomt med Enter. Avsluta på `q`. **Inga variabler.**

**Exempel på körning:**

```
Skriv "ip" för att visa IP (Enter annars): ip
IP: 10.0.0.5
Skriv "wifi" för att visa wifi (Enter annars): 
Skriv "q" för att sluta (Enter annars): 
Skriv "ip" för att visa IP (Enter annars): 
Skriv "wifi" för att visa wifi (Enter annars): wifi
Wifi: SkolWifi
Skriv "q" för att sluta (Enter annars): q
Hej då!
```

**Facit:**

```python
while True:
    if input('Skriv "ip" för att visa IP (Enter annars): ') == "ip":
        print("IP: 10.0.0.5")
    if input('Skriv "wifi" för att visa wifi (Enter annars): ') == "wifi":
        print("Wifi: SkolWifi")
    if input('Skriv "q" för att sluta (Enter annars): ') == "q":
        print("Hej då!")
        break
```

**Facit:**

```python
redo = 0
while True:
    svar = input("Är du redo? (ja/nej/q): ")
    if svar == "q":
        print("Antal redo:", redo)
        break
    if svar == "ja":
        redo = redo + 1
```

---

## Uppgift 6 – Första variabeln (räkna varv)

**Uppgift:** Nu får du använda **variabler**. Räkna hur många varv som körts. Fortsätt på Enter, avsluta med `q`, och skriv totalen.

**Exempel på körning:**

```
Kör igen? (Enter/q): 
Kör igen? (Enter/q): 
Kör igen? (Enter/q): q
Antal varv: 2
```

**Facit:**

```python
varv = 0
while True:
    val = input("Kör igen? (Enter/q): ")
    if val == "q":
        print("Antal varv:", varv)
        break
    varv = varv + 1
```

**Facit:**

```python
while True:
    los = input("Skriv lösenord: ")
    if los == "hemlis":
        print("Välkommen!")
        break
    print("Fel, försök igen.")
```

---

## Uppgift 7 – Enkel meny (1/2/3)

**Uppgift:** Visa en meny i en loop. På `1` skriv `IP: 10.0.0.5`. På `2` skriv `Wifi: SkolWifi`. På `3` skriv `Hej då!` och avsluta. Annars skriv `Fel val`.

**Exempel på körning:**

```
1. Visa IP
2. Visa wifi
3. Avsluta
Val: 2
Wifi: SkolWifi
1. Visa IP
2. Visa wifi
3. Avsluta
Val: 1
IP: 10.0.0.5
1. Visa IP
2. Visa wifi
3. Avsluta
Val: 3
Hej då!
```

**Facit:**

```python
while True:
    print("1. Visa IP")
    print("2. Visa wifi")
    print("3. Avsluta")
    val = input("Val: ")
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

## Uppgift 8 – Räkna ner

**Uppgift:** Programmet frågar efter ett heltal `n` och räknar ner i en loop: `n, n-1, ... 1` och skriver `Klart!` när nedräkningen är slut.

**Exempel på körning:**

```
Skriv heltal: 3
3
2
1
Klart!
```

**Facit:**

```python
n = int(input("Skriv heltal: "))
while True:
    print(n)
    n = n - 1
    if n == 0:
        print("Klart!")
        break
```

---

## Uppgift 9 – Summera tal tills q

**Uppgift:** Fråga efter tal i en loop och lägg till i en summa. Avsluta när användaren skriver `q`. Skriv totalsumman.

**Exempel på körning:**

```
Skriv tal (q för att sluta): 10
Skriv tal (q för att sluta): 4
Skriv tal (q för att sluta): q
Summa: 14
```

**Facit:**

```python
summa = 0
while True:
    text = input("Skriv tal (q för att sluta): ")
    if text == "q":
        print("Summa:", summa)
        break
    tal = int(text)
    summa = summa + tal
```

---

## Uppgift 10 – Enkel inlogg med max 3 försök

**Uppgift:** Begär användarnamn och kod i en loop. Korrekt är `lisa` och `hemlis`. Efter varje fel ska ett försök räknas. Avsluta med `Välkommen Lisa!` vid rätt uppgifter eller `Kontot låst` efter 3 fel.

**Exempel på körning (rätt på andra):**

```
Användarnamn: lisa
Kod: 1234
Fel uppgifter.
Användarnamn: lisa
Kod: hemlis
Välkommen Lisa!
```

**Exempel på körning (låst):**

```
Användarnamn: liisa
Kod: 2222
Fel uppgifter.
Användarnamn: liisa
Kod: 2222
Fel uppgifter.
Användarnamn: liisa
Kod: 2222
Kontot låst
```

**Facit:**

```python
forsok = 0
while True:
    anv = input("Användarnamn: ")
    kod = input("Kod: ")
    if anv == "lisa" and kod == "hemlis":
        print("Välkommen Lisa!")
        break
    print("Fel uppgifter.")
    forsok = forsok + 1
    if forsok == 3:
        print("Kontot låst")
        break
```
