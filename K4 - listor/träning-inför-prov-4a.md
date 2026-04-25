# Träning inför prov 4a: listor

Här får du träna på samma moment som kommer på Prov 4a. Temat är **musik**.

**Regler:**
* Använd bara listor, `print()` och `input()`.
* Använd **inte** index, `append()` eller loopar.
* Skriv alltid en tydlig text framför när du skriver ut en lista.

---

### Uppgift 1: Favoritlåtar

**Uppgift:** Skapa en lista med tre låttitlar och skriv ut listan.

**Exempel på körning:**
```text
=== Mina favoritlåtar ===
Låtar: ['Blinding Lights', 'Shape of You', 'Levitating']
```

**Facit:**
```python
print("=== Mina favoritlåtar ===")
latar = ["Blinding Lights", "Shape of You", "Levitating"]
print("Låtar:", latar)
```

---

### Uppgift 2: Tempo

**Uppgift:** Skapa en lista med fyra tempon i BPM (heltal) och skriv ut listan.

**Exempel på körning:**
```text
=== Tempo i BPM ===
Tempo: [90, 120, 140, 100]
```

**Facit:**
```python
print("=== Tempo i BPM ===")
tempo = [90, 120, 140, 100]
print("Tempo:", tempo)
```

---

### Uppgift 3: Albuminfo

**Uppgift:** Skapa en lista med tre saker om ett album: titel (text), år (tal) och antal låtar (tal). Skriv ut listan.

**Exempel på körning:**
```text
=== Albuminfo ===
Album: ['Thriller', 1982, 9]
```

**Facit:**
```python
print("=== Albuminfo ===")
album = ["Thriller", 1982, 9]
print("Album:", album)
```

---

### Uppgift 4: Två favoritartister

**Uppgift:** Fråga användaren om två artistnamn med `input()`. Skapa en lista med de två namnen och skriv ut listan.

**Exempel på körning:**
```text
=== Mina favoritartister ===
Artist 1: Beyoncé
Artist 2: Drake
Din lista: ['Beyoncé', 'Drake']
```

**Facit:**
```python
print("=== Mina favoritartister ===")
artist1 = input("Artist 1: ")
artist2 = input("Artist 2: ")
artister = [artist1, artist2]
print("Din lista:", artister)
```

---

### Uppgift 5: Spellista

**Uppgift:** Fråga användaren om en låttitel med `input()` och ett betyg med `int(input())`. Skapa en lista med titel (text) och betyg (tal). Skriv ut listan med en **f-sträng**.

**Exempel på körning:**
```text
=== Lägg till låt ===
Låttitel: Watermelon Sugar
Betyg (1-5): 5
Din spellista: ['Watermelon Sugar', 5]
```

**Facit:**
```python
print("=== Lägg till låt ===")
titel = input("Låttitel: ")
betyg = int(input("Betyg (1-5): "))
spellista = [titel, betyg]
print(f"Din spellista: {spellista}")
```
