# Prov 3a: listor och index

Detta prov testar dina kunskaper i att skapa listor, blanda olika typer av information och använda index för att skriva ut specifika delar (bland annat med hjälp av inmatning från användaren).

### Uppgift 1: blandad lista (film)

**Uppgift:** Skapa en lista som innehåller exakt tre saker om en film: Titel (text), Utgivningsår (heltal) och Betyg 1-5 (heltal). Skriv sedan ut hela listan.

**Exempel på körning:**

```text
=== Filmkväll ===
Filminfo: ['Lejonkungen', 1994, 5]
```

**Facit:**

```python
print("=== Filmkväll ===")
# Blandad lista: Text, Heltal, Heltal
film = ["Lejonkungen", 1994, 5]
print("Filminfo:", film)
```

### Uppgift 2: skriva ut specifika delar

**Uppgift:** Utgå från listan `lopare = ["Usain Bolt", "Jesse Owens", "Carl Lewis", "Florence Griffith"]`.
Skriv ut hela listan.
Använd sedan index för att skriva ut den **första** löparen och den **sista** löparen på varsin rad.

**Exempel på körning:**

```text
=== Startfältet ===
Alla löpare: ['Usain Bolt', 'Jesse Owens', 'Carl Lewis', 'Florence Griffith']
Första: Usain Bolt
Sista: Florence Griffith
```

**Facit:**

```python
print("=== Startfältet ===")
lopare = ["Usain Bolt", "Jesse Owens", "Carl Lewis", "Florence Griffith"]
print("Alla löpare:", lopare)
print("Första:", lopare[0])
print("Sista:", lopare[3])
```

### Uppgift 3: välj snacks (input och index)

**Uppgift:** Skapa en lista med tre sorters snacks: `["Chips", "Popcorn", "Choklad"]`.

1. Skriv ut listan så användaren ser alternativen.
2. Be användaren välja vad de vill ha (index 0, 1 eller 2).
3. Skriv ut valet.

**Exempel på körning:**

```text
=== Fredagsmys ===
Meny: ['Chips', 'Popcorn', 'Choklad']
Vad vill du ha (0-2): 1
Du valde: Popcorn
```

**Facit:**

```python
print("=== Fredagsmys ===")
snacks = ["Chips", "Popcorn", "Choklad"]
print("Meny:", snacks)
val = int(input("Vad vill du ha (0-2): "))
print("Du valde:", snacks[val])
```

### Uppgift 4: välj hastighet (tal och input)

**Uppgift:** Skapa en lista med tre hastighetsbegränsningar (heltal): `[30, 50, 70]`.

1. Fråga användaren vilket index de vill se (0-2).
2. Skriv ut hastigheten på det indexet tillsammans med texten "km/h".

**Exempel på körning:**

```text
=== Trafikskyltar ===
Vilken skylt (0-2)? 2
Maxfart: 70 km/h
```

**Facit:**

```python
print("=== Trafikskyltar ===")
skyltar = [30, 50, 70]
val = int(input("Vilken skylt (0-2)? "))
print("Maxfart:", skyltar[val], "km/h")
```

### Uppgift 5: mobilinfo (blandat val)

**Uppgift:** Skapa en lista med info om en mobiltelefon: `["iPhone", 2024, "Guld", 256]`.
(Listan innehåller Modell, År, Färg, Minne).
Låt användaren skriva in ett index (0-3) för att se den specifika informationen.

**Exempel på körning:**

```text
=== Enhetshanterare ===
Data: ['iPhone', 2024, 'Guld', 256]
Välj info (0=Modell, 1=År, 2=Färg, 3=Minne): 3
Info: 256
```

**Facit:**

```python
print("=== Enhetshanterare ===")
mobil = ["iPhone", 2024, "Guld", 256]
print("Data:", mobil)
val = int(input("Välj info (0=Modell, 1=År, 2=Färg, 3=Minne): "))
print("Info:", mobil[val])
```
