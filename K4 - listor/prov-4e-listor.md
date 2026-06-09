# Prov 4e: Listor – A-nivå

Detta prov testar din förmåga att **självständigt designa och bygga** program med listor. Du får en problembeskrivning – resten är upp till dig.

**Tema:** Datainsamling och presentation.

**Regler:**
* Använd listor, `print()` och `input()`. f-strängar rekommenderas.
* Använd **inte** index, `append()` eller loopar.

**Bedömning:** 2 uppgifter, totalt 20 poäng. Bedömningen väger in både korrekt listhantering och genomtänkt struktur.

---

### Uppgift 1: Festivalprogrammet (10p)

**Uppgift:** Bygg ett program som samlar information om en festival och presenterar den snyggt. Programmet ska:

* Fråga efter festivalens namn och år.
* Fråga efter **tre artister** och vilken **scen** respektive artist spelar på.
* Fråga efter antal besökare och biljettpris.

All information ska organiseras i listor – du bestämmer själv hur de struktureras (en eller flera listor). Därefter ska programmet skriva ut en festivalöversikt med rubrik, alla artister med scener, och besöksinfo. Använd f-strängar och snygg formatering.

**Exempel på körning (ditt program kan se annorlunda ut):**
```text
Festivalens namn: Sommarfest
År: 2026
Artist 1: Håkan
Scen 1: Stora scenen
Artist 2: Veronica Maggio
Scen 2: Tältscenen
Artist 3: Bolaget
Scen 3: Stora scenen
Antal besökare: 5000
Biljettpris: 495
=== SOMMARFEST 2026 ===
Artister: ['Håkan', 'Veronica Maggio', 'Bolaget']
Scener: ['Stora scenen', 'Tältscenen', 'Stora scenen']
Besökare: 5000 | Pris: 495 kr
```

**Facit:**
```python
festival = input("Festivalens namn: ")
ar = input("År: ")

a1 = input("Artist 1: ")
s1 = input("Scen 1: ")
a2 = input("Artist 2: ")
s2 = input("Scen 2: ")
a3 = input("Artist 3: ")
s3 = input("Scen 3: ")

besokare = int(input("Antal besökare: "))
pris = int(input("Biljettpris: "))

artister = [a1, a2, a3]
scener = [s1, s2, s3]

print(f"=== {festival.upper()} {ar} ===")
print(f"Artister: {artister}")
print(f"Scener: {scener}")
print(f"Besökare: {besokare} | Pris: {pris} kr")
```

---

### Uppgift 2: Mitt register (10p)

**Uppgift:** Bygg ett program som fungerar som ett personligt register. Du väljer själv **vad registret ska innehålla** – till exempel böcker du läst, spel du spelat, recept du kan, eller något helt annat.

Programmet ska:

* Samla in information om **fyra objekt** i ditt register. För varje objekt ska du samla in minst **tre egenskaper** (t.ex. titel, betyg, och kategori).
* Organisera all information i listor – du bestämmer själv hur (en lista per objekt, en lista per egenskap, eller någon annan struktur).
* Skriva ut hela registret med en rubrik, tydlig struktur och f-strängar.

Tänk på att utskriften ska vara lätt att läsa – du bestämmer layouten.

**Exempel på körning (bokregister – ditt program kan se helt annorlunda ut):**
```text
Bok 1 titel: Narnia
Bok 1 författare: C.S. Lewis
Bok 1 sidor: 200
Bok 2 titel: Hobbiten
Bok 2 författare: Tolkien
Bok 2 sidor: 310
Bok 3 titel: Bröderna Lejonhjärta
Bok 3 författare: Astrid Lindgren
Bok 3 sidor: 250
Bok 4 titel: Mördarens apa
Bok 4 författare: Wegelius
Bok 4 sidor: 600
=== MITT BOKREGISTER ===
Titlar: ['Narnia', 'Hobbiten', 'Bröderna Lejonhjärta', 'Mördarens apa']
Författare: ['C.S. Lewis', 'Tolkien', 'Astrid Lindgren', 'Wegelius']
Sidor: [200, 310, 250, 600]
```

**Facit:**
```python
t1 = input("Bok 1 titel: ")
f1 = input("Bok 1 författare: ")
s1 = int(input("Bok 1 sidor: "))

t2 = input("Bok 2 titel: ")
f2 = input("Bok 2 författare: ")
s2 = int(input("Bok 2 sidor: "))

t3 = input("Bok 3 titel: ")
f3 = input("Bok 3 författare: ")
s3 = int(input("Bok 3 sidor: "))

t4 = input("Bok 4 titel: ")
f4 = input("Bok 4 författare: ")
s4 = int(input("Bok 4 sidor: "))

titlar = [t1, t2, t3, t4]
forfattare = [f1, f2, f3, f4]
sidor = [s1, s2, s3, s4]

print("=== MITT BOKREGISTER ===")
print(f"Titlar: {titlar}")
print(f"Författare: {forfattare}")
print(f"Sidor: {sidor}")
```
