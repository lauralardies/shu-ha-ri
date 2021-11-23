# shu-ha-ri
Codigo recibido:
---Hemos encontrado los siguientes fallos:
>No tienen "from ramdon import choice, sample" bien codificado


El diagrama de flujo es el siguiente:

![WhatsApp Image 2021-11-23 at 11 56 22](https://user-images.githubusercontent.com/91721888/143012212-56f42be1-50fd-4823-8236-1a4a189f61bd.jpeg)

El codigo del juego es el siguiente:
```#vamos a crear un juego de black jack

cartas= {chr(0x1f0a): 11, 
        chr(0x1fa2):2,
        chr(0x1f03):3, 
        chr(0x1f0a4):4,
        chr(0x1f0a5):5,
        chr(0x1f0a6):6, 
        chr(0x1f0a7):7, 
        chr(0x1f0a8):8, 
        chr(0x1f0a9):9, 
        chr(0x1f0aa):10, 
        chr(0x1f0ab):10, 
        chr(0x1f0ad):10, 
        chr(0x1f0ae):10}
print("cartas{}".format("".join(cartas.keys)))
print ("puntos{}".format(list(cartas.values())))

print("1\ Interacción estándar sobre un dirección")
for carta, valor in cartas.items():
        print ("la carta {} vale {}".format(carta,valor))
print("2\ Interaccion ordenada sobre un diccionario")
for carta in sorted(cartas.keys()):
        print("La carta {} vale {}".format(carta , cartas [carta] ))
import random
print("3\Black Jack")
lista_cartas = list(cartas)

print("Has seleccionado: " , end= " ")
carta= random.choice (lista_cartas)
score = cartas[carta]
print(carta, end = " ")
carta = random.choice(lista_cartas)
score += cartas[carta]
print(carta, end = " ")
print(">>> su puntación es de ", score)

main_banca = random.sample(lista_cartas, 2)
score_banc = random.sum (cartas[carta] for carta in main_banca)
print("La banca tiene: {} {} >> su score es {}".format(main_banca[0] , main_banca[1] , score_banc))
