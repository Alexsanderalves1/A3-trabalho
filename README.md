# A3-trabalho
Jogo da advinhacao Python

import random

class JogoAdivinhacao:
    def __init__(self):
        self.numero_secreto = random.randint(1, 100)
        self.tentativas = 0

    def jogar(self):
        print("Bem-vindo ao Jogo da Adivinhação! O objetivo é achar o numero randomico de 1 a 100. Boa Sorte!")
        while True:
            tentativa = int(input("Digite um número entre 1 e 100: "))
            self.tentativas += 1

            if tentativa < self.numero_secreto:
                print("Tente um número maior!")
            elif tentativa > self.numero_secreto:
                print("Tente um número menor!")
            else:
                print(f"Parabéns! Você acertou o número secreto em {self.tentativas} tentativas!")
                break
jogo = JogoAdivinhacao()
jogo.jogar()
