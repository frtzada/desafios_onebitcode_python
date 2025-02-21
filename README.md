# Desafios OneBitCode Python 🚀

**Explore o universo da programação com desafios práticos!** Este repositório reúne soluções para os desafios da OneBitCode em Python, começando com o "Desafio Missão Espacial".

![Python Badge](https://img.shields.io/badge/Python-3.9-blue) ![Status](https://img.shields.io/badge/Status-Em%20Progresso-green)

---

## O que é isso?

Este repositório é um espaço para aprimorar suas habilidades em Python por meio de desafios divertidos e educativos. O primeiro deles, **Missão Espacial**, simula a distribuição de suprimentos entre astronautas em uma viagem intergaláctica. Perfeito para praticar lógica de programação e manipulação de dicionários em Python!

---

## Desafio Missão Espacial 🌌

### Objetivo
Dividir suprimentos igualmente entre astronautas. Se algum item não puder ser distribuído sem sobras, a missão é abortada!

---

## Como Funciona? 🛠️

O código segue uma lógica simples e eficiente:
- **Entrada**: Recebe um dicionário `supplies` (com tipos de suprimentos e suas quantidades) e o número de astronautas (`number_of_astronauts`).
- **Verificação**: Checa se cada quantidade é divisível igualmente pelo número de astronautas usando o operador `%`.
- **Saída**: 
  - Se todas as quantidades forem divisíveis, retorna um dicionário com a quantidade por astronauta (usando divisão inteira `//`).
  - Caso contrário, retorna `None`, indicando que a distribuição falhou.

**Exemplo prático**: Com 50 unidades de comida e 5 astronautas, cada um recebe 10. Se fosse 51, a missão falharia!

---

## Como Rodar

1. **Pré-requisitos**: Tenha Python 3.9+ instalado.
2. Clone o repositório:
   ```bash
   git clone https://github.com/frtzada/desafios_onebitcode_python.git

### Código
```python
def distribute_supplies(supplies, number_of_astronauts):
    distribution = {}
    
    for type, quantity in supplies.items():
        if quantity % number_of_astronauts != 0:
            return None  # Missão falha se não for divisível
        distribution[type] = quantity // number_of_astronauts
    
    return distribution

# Exemplo de uso
supplies = {'food': 50, 'water': 80, 'kits': 60}
number_of_astronauts = 5

result = distribute_supplies(supplies, number_of_astronauts)
print(result)  # Saída: {'food': 10, 'water': 16, 'kits': 12}




