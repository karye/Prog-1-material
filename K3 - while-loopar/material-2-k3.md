# Prov: while-loopen – uppgifter

Regel: Använd alltid en while-loop, `print()`, `input()` och vid behov `if` / `elif` / `else`. I flera uppgifter används också `break`, variabler och heltal med `int()`. Varje uppgift har exempelkörning och facit.

---

## Uppgift 1 – god morgon och hej (endast utskrift)

**Uppgift:**

Skriv först en rad utanför loopen: `God morgon`. Starta sedan en while-loop som skriver ordet `Hej` flera gånger. Ingen inmatning ska användas här.

**Exempel på körning:**

```text
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

## Uppgift 2 – bara skriva ut utan input (endast utskrift)

**Uppgift:**

Skriv ett program som använder en while-loop och bara `print` för att skriva samma mening om och om igen, till exempel `Jag tränar while-loopar`. Du behöver inte avsluta loopen.

Tillåtna kommandon: `print`.

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

## Uppgift 3 – skriva ut ett mönster (endast utskrift)

**Uppgift:**

Skriv ett program som med en while-loop och bara `print` skriver ut ett enkelt mönster flera gånger, till exempel:

```
***
***
***
```

Du behöver inte avsluta loopen.

Tillåtna kommandon: `print`.

**Exempel på körning:**

```text
Mönster:
***
***
***
***
***
***
(... fortsätter ...)
```

**Facit:**

```python
print("Mönster:")
while True:
    print("***")
    print("***")
    print("***")
```

---

## Uppgift 4 – status upprepas (endast utskrift)

**Uppgift:**

Skriv först en rad utanför loopen: `Status: igång`. Starta sedan en while-loop som upprepar två rader varje varv: `Status: igång` och `Arbetar...`. Ingen inmatning ska användas här.

**Exempel på körning:**

```text
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

---

## Uppgift 5 – input före loopen (input sedan loop med utskrift)

**Uppgift:**

Be användaren skriva ett meddelande **en gång före loopen**. Använd sedan loopen för att skriva ut samma meddelande om och om igen. Programmet fortsätter tills du stoppar det.

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

## Uppgift 6 – namn i början av loopen (loop med input och utskrift)

**Uppgift:**

Skriv ett program som i varje varv frågar efter ett namn och direkt skriver ut en hälsning med namnet.

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

## Uppgift 7 – frukt och färg (loop med input och utskrift)

**Uppgift:**

Skriv ett program med en while-loop som i **varje varv** frågar efter en frukt och en färg, och sedan skriver ut en mening med båda.

**Exempel på körning:**

```text
Frukt- och färgloop
Skriv en frukt: äpple
Skriv en färg: röd
Du valde äpple med färgen röd
Skriv en frukt: banan
Skriv en färg: gul
Du valde banan med färgen gul
(... fortsätter ...)
```

**Facit:**

```python
print("Frukt- och färgloop")
while True:
    frukt = input("Skriv en frukt: ")
    färg = input("Skriv en färg: ")
    print("Du valde", frukt, "med färgen", färg)
```

---

## Uppgift 8 – paus i slutet (loop med input och utskrift)

**Uppgift:**

Skriv ett program med en while-loop som först skriver ut en text, och **i slutet av varje varv** frågar användaren att trycka Enter för att fortsätta. Programmet kör vidare tills du stoppar det.

**Exempel på körning:**

```text
Startar programmet...
Programmet kör ett varv.
Tryck Enter för att köra ett varv till: 
Programmet kör ett varv.
Tryck Enter för att köra ett varv till: 
Programmet kör ett varv.
Tryck Enter för att köra ett varv till: 
(... fortsätter ...)
```

**Facit:**

```python
print("Startar programmet...")
while True:
    print("Programmet kör ett varv.")
    input("Tryck Enter för att köra ett varv till: ")
```

---

## Uppgift 9 – eko med q för att sluta (loop med input, if och break)

**Uppgift:**

Skriv ett program som i en loop frågar efter text och direkt skriver ut samma text. Om användaren skriver `q` ska loopen avslutas.

**Exempel på körning:**

```text
Ekoprogram startar...
Skriv något (q för att sluta): hej
Du skrev: hej
Skriv något (q för att sluta): python är kul
Du skrev: python är kul
Skriv något (q för att sluta): q
Hejdå!
```

**Facit:**

```python
print("Ekoprogram startar...")
while True:
    text = input("Skriv något (q för att sluta): ")
    if text == "q":
        print("Hejdå!")
        break
    print("Du skrev:", text)
```

---

## Uppgift 10 – eko av text (variant, loop med input, if och break)

**Uppgift:**

Skriv ett program som i en loop frågar efter text och sedan skriver ut samma text. Programmet ska sluta när användaren skriver `q`.

**Exempel på körning:**

```text
Ekoprogram startar...
Skriv text (q för att sluta): hej
Du skrev: hej
Skriv text (q för att sluta): python är kul
Du skrev: python är kul
Skriv text (q för att sluta): q
Hejdå!
```

**Facit:**

```python
print("Ekoprogram startar...")
while True:
    text = input("Skriv text (q för att sluta): ")
    if text == "q":
        print("Hejdå!")
        break
    print("Du skrev:", text)
```

---

## Uppgift 11 – hälsa på namn (loop med input, if och break)

**Uppgift:**

Skriv ett program som i en loop frågar efter ett namn och skriver `Hej` plus namnet. Programmet ska sluta när användaren skriver `q` som namn.

Tillåtna kommandon: `print`, `input`, `break`.

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

## Uppgift 12 – eko av namn (variant, loop med input, if och break)

**Uppgift:**

Skriv ett program som i en loop frågar efter ett namn och skriver `Hej` plus namnet. Programmet ska sluta när användaren skriver `q` som namn.

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

## Uppgift 13 – hälsning på begäran (if och break)

**Uppgift:**

Programmet ska i en while-loop först fråga om du vill fortsätta, och sedan om du vill ha en hälsning. Avsluta om den första frågan besvaras med `q`. Inga variabler behövs.

**Exempel på körning:**

```text
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
while True:
    if input("Fortsätta? (Enter/q): ") == "q":
        break
    if input("Vill du ha en hälsning? (ja/Enter): ") == "ja":
        print("Hej!")
print("Hejdå!")
```

---

## Uppgift 14 – första break (if och break)

**Uppgift:**

Använd en while-loop och `break`. Fortsätt skriva `Loopar...` tills användaren skriver `stop`. Då skrivs `Avslutar.` och loopen bryts.

**Exempel på körning:**

```text
Startar loop...
Loopar...
Skriv "stop" för att avsluta (Enter annars): 
Loopar...
Skriv "stop" för att avsluta (Enter annars): stop
Avslutar.
```

**Facit:**

```python
print("Startar loop...")
while True:
    print("Loopar...")
    if input('Skriv "stop" för att avsluta (Enter annars): ') == "stop":
        print("Avslutar.")
        break
```

---

## Uppgift 15 – små val i loopen (if och break)

**Uppgift:**

I varje varv får användaren tre chanser i följd: visa IP, visa wifi eller avsluta. Varje val frågas separat och kan lämnas tomt med Enter. Avsluta på `q`. Inga variabler behövs.

**Exempel på körning:**

```text
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

---

## Uppgift 16 – första variabeln (räkna varv)

**Uppgift:**

Nu ska du använda en variabel för att räkna hur många varv som körts. Fortsätt på Enter, avsluta med `q`, och skriv totalen.

**Exempel på körning:**

```text
Startar räknare...
Kör igen? (Enter/q): 
Kör igen? (Enter/q): 
Kör igen? (Enter/q): q
Antal varv: 2
```

**Facit:**

```python
print("Startar räknare...")
varv = 0
while True:
    val = input("Kör igen? (Enter/q): ")
    if val == "q":
        print("Antal varv:", varv)
        break
    varv = varv + 1
```

---

## Uppgift 17 – enkel meny (if-elif-else)

**Uppgift:**

Visa en meny i en loop. På `1` skriv `IP: 10.0.0.5`. På `2` skriv `Wifi: SkolWifi`. På `3` skriv `Hej då!` och avsluta. Annars skriv `Fel val`.

**Exempel på körning:**

```text
Menyprogram
============

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
print("Menyprogram")
print("============")
while True:
    print()
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

## Uppgift 18 – skolmatsmeny (if-elif-else)

**Uppgift:**

Visa en meny i en loop för skolmaten. På `1` skriv `Visa dagens lunch`. På `2` skriv `Visa matsedel för veckan`. På `3` skriv `Avslutar meny` och avsluta programmet. Annars skriv `Fel val`.

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
Val: 2
Matsedel: Mån-pasta, Tis-soppa, Ons-pannkakor, ...

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
        print("Matsedel: Mån-pasta, Tis-soppa, Ons-pannkakor, ...")
    elif val == "3":
        print("Avslutar meny")
        break
    else:
        print("Fel val")
```

---

## Uppgift 19 – musikmeny (if-elif-else)

**Uppgift:**

Visa en meny i en loop för en musikspelare. På `1` skriv `Spela favoritlåt`. På `2` skriv `Visa spellista`. På `3` skriv `Stänger musikspelare` och avsluta programmet. Annars skriv `Fel val`.

**Exempel på körning:**

```text
Musikspelare
============

1. Spela favoritlåt
2. Visa spellista
3. Avsluta
Val: 1
Spelar: Thunderstruck

1. Spela favoritlåt
2. Visa spellista
3. Avsluta
Val: 2
Spellista: Thunderstruck, Believer, Shape of You

1. Spela favoritlåt
2. Visa spellista
3. Avsluta
Val: 3
Stänger musikspelare
```

**Facit:**

```python
print("Musikspelare")
print("============")
while True:
    print()
    print("1. Spela favoritlåt")
    print("2. Visa spellista")
    print("3. Avsluta")
    val = input("Val: ")
    if val == "1":
        print("Spelar: Thunderstruck")
    elif val == "2":
        print("Spellista: Thunderstruck, Believer, Shape of You")
    elif val == "3":
        print("Stänger musikspelare")
        break
    else:
        print("Fel val")
```

---

## Uppgift 20 – räkna ner (if och break)

**Uppgift:**

Programmet ska fråga efter ett heltal `n` och räkna ner i en loop: `n, n-1, ... 1` och skriva `Klart!` när nedräkningen är slut.

**Exempel på körning:**

```text
Skriv heltal: 3
Startar nedräkning...
3
2
1
Klart!
```

**Facit:**

```python
n = int(input("Skriv heltal: "))
print("Startar nedräkning...")
while True:
    print(n)
    n = n - 1
    if n == 0:
        print("Klart!")
        break
```

---

## Uppgift 21 – summera tal tills q (if, break och variabel)

**Uppgift:**

Fråga efter tal i en loop och lägg till i en summa. Avsluta när användaren skriver `q`. Skriv totalsumman.

**Exempel på körning:**

```text
Startar summering...
Skriv tal (q för att sluta): 10
Skriv tal (q för att sluta): 4
Skriv tal (q för att sluta): q
Summa: 14
```

**Facit:**

```python
print("Startar summering...")
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

## Uppgift 22 – enkel inlogg med max 3 försök (if, elif, else och break)

**Uppgift:**

Begär användarnamn och kod i en loop. Korrekt är `lisa` och `hemlis`. Efter varje fel ska ett försök räknas. Avsluta med `Välkommen Lisa!` vid rätt uppgifter eller `Kontot låst` efter 3 fel.

**Exempel på körning (rätt på andra):**

```text
Startar inloggning...
Användarnamn: lisa
Kod: 1234
Fel uppgifter.
Användarnamn: lisa
Kod: hemlis
Välkommen Lisa!
```

**Exempel på körning (låst):**

```text
Startar inloggning...
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
print("Startar inloggning...")
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

---

## Uppgift 23 – Statusloop med stopp (superenkel)

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

## Uppgift 24 – IP-eko tills q (eko och break)

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

## Uppgift 25 – Logg med enter/q (paus eller stoppa)

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

## Uppgift 26 – Enkel meny i loop (1/2/3)

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

## Uppgift 27 – Startsekvens med avbrott

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
