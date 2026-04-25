# **Python lathund**

## **Inmatning & utskrift** 

Läsa in text (sträng) och skriv ut text:

```py
namn = input("Vad heter du? ") 
print("Hej", namn) # Alternativ 1 
print(f"Hej {namn}") # Alternativ 2
```

Läsa in tal för beräkningar:

```py
ålder = int(input("Ålder: ")) # heltal
längd = float(input("Längd i meter: ")) 
print("Nästa år är du", ålder + 1)
```

## **Villkor** 

Jämföra med text:

```py
färg = input("Färg: ")
if färg == "röd":
    print("Du valde röd")
elif färg == "blå":
    print("Du valde blå")
else:
    print("Okänd färg")
```

Kombinera villkor med **and** \= och, **or** \= eller, **not** \= inte:

```py
if ålder >= 18 and land == "Sverige":
    print("Du får rösta i svenska val.")
```

## **Loopar** 

Upprepa kod flera gånger.   
While-loop (så länge villkoret är sant):

```py
while True:
    print("Hej igen!!!")
    break # Avslutar loopen
```

For-loop (över lista):

```py
frukter = ["äpple", "banan", "kiwi"]
for frukt in frukter:
    print("Jag gillar", frukt)
```

For-loop (med range):

```py
for i in range(1, 4): # 1, 2, 3
    print("Tal", i)
for i in range(2, 10, 2): # 2, 4, 6, 8
    print("Tal", i)
```

## **Listor** 

Samling av värden i ordning:

```py
frukter = ["äpple", "banan", "kiwi"] 
print("Första är", frukter[0]) # index 0 
frukter.append("päron") # lägg till
print("Antal", len(frukter)) # längd

import random
print("Slump:", random.choice(frukter))
```

## **Funktioner** 

Skapa egna återanvändbara bitar kod med def .   
Enkel funktion:

```py
def hälsa():
    print("Hej!")

hälsa() # Hej!
```

Med parameter:

```py
def hälsa_namn(namn):
    print("Hej", namn)

hälsa_namn("Sara") # Hej Sara
```

Returnera ett värde:

```py
def dubbla(tal):
    return tal * 2

print("Resultat:", dubbla(5)) # Resultat: 10
```

