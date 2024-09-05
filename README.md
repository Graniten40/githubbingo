# githubbingo
Pythone code to play bingo

import random

# Slumpa fram 10 tal mellan 1 och 100
slumpade_tal = [random.randint(1, 100) for _ in range(10)]

# Fördefinierade tal från 5 till 50
fordefinierade_tal = [5, 10, 15, 20, 25, 30, 35, 40, 45, 50]

# Låt användaren ange 10 tal och lägg till dem i listan
for i in range(10):
    tal = int(input(f"Ange tal #{i+1}: "))
    fordefinierade_tal.append(tal)

# Jämför de slumpade talen med de fördefinierade talen och skriv ut "Bingo" vid matchning
poang = 0
for tal in slumpade_tal:
    if tal in fordefinierade_tal:
        print("Bingo:", tal)
        poang += 1

# Skriv ut totala poängen
print("Totala poäng:", poang)
