# Prov 1d: Input och print – C-nivå

Detta prov testar din förmåga att självständigt bygga program med `print()`, `input()` och f-strängar. Du får veta **vad** programmet ska göra – men **hur** du löser det är upp till dig.

**Tema:** Kommunikation och presentation.

**Bedömning:** 3 uppgifter, totalt 20 poäng.

---

### Uppgift 1: Visitkort (7p)

**Uppgift:** Programmet ska fråga användaren efter tre saker: namn, yrke och e-postadress. Därefter ska det skriva ut ett snyggt visitkort med fyra rader:

1. En ram av likhetstecken (samma bredd som namnet + yrket)
2. Namnet på en egen rad
3. Yrke och e-post på en gemensam rad, åtskilda med `|`
4. En ram av likhetstecken igen

**Exempel på körning:**
```text
Namn: Maria Andersson
Yrke: Utvecklare
E-post: maria@kod.se
===========
Maria Andersson
Utvecklare | maria@kod.se
===========
```

**Facit:**
```python
namn = input("Namn: ")
yrke = input("Yrke: ")
epost = input("E-post: ")
ram = "=" * len(namn + yrke)
print(ram)
print(namn)
print(f"{yrke} | {epost}")
print(ram)
```

---

### Uppgift 2: Veckoschema (7p)

**Uppgift:** Programmet ska fråga användaren efter fyra aktiviteter – en för varje dag måndag–torsdag. Därefter ska det skriva ut ett schema med rubrik och en rad per dag. Varje rad ska innehålla dagens namn, ett kolon och aktiviteten. Använd f-strängar för utskrifterna. Du avgör själv exakt hur rubrik och layout ser ut, men alla fyra dagar ska synas.

**Exempel på körning:**
```text
Aktivitet måndag: Träning
Aktivitet tisdag: Gitarrlektion
Aktivitet onsdag: Plugga Python
Aktivitet torsdag: Filmkväll
=== VECKOSCHEMA ===
Måndag: Träning
Tisdag: Gitarrlektion
Onsdag: Plugga Python
Torsdag: Filmkväll
```

**Facit:**
```python
man = input("Aktivitet måndag: ")
tis = input("Aktivitet tisdag: ")
ons = input("Aktivitet onsdag: ")
tor = input("Aktivitet torsdag: ")
print("=== VECKOSCHEMA ===")
print(f"Måndag: {man}")
print(f"Tisdag: {tis}")
print(f"Onsdag: {ons}")
print(f"Torsdag: {tor}")
```

---

### Uppgift 3: Evenemangsaffisch (6p)

**Uppgift:** Programmet ska fråga användaren efter tre saker: evenemangets namn, plats och tid. Därefter ska det skriva ut en affisch med tre delar:

1. En rubrik i **versaler** (använd `.upper()`) följt av en skiljelinje
2. Plats och tid på varsin rad
3. En avslutande uppmaning ("Varmt välkomna!" eller liknande – du väljer själv)

**Exempel på körning:**
```text
Evenemangets namn: Vårkonsert
Plats: Aulan
Tid: Fredag 18:00
===== VÅRKONSERT =====
Plats: Aulan
Tid: Fredag 18:00
Varmt välkomna!
```

**Facit:**
```python
namn = input("Evenemangets namn: ")
plats = input("Plats: ")
tid = input("Tid: ")
print(f"===== {namn.upper()} =====")
print(f"Plats: {plats}")
print(f"Tid: {tid}")
print("Varmt välkomna!")
```
