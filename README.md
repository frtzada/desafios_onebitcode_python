# desafios_onebitcode_python

##### Desafio Missao Espacial #####

def distribute_supplies(supplies, number_of_astronauts):
    distribution = {}
    
    for type, quantity in supplies.items():
        if quantity % number_of_astronauts != 0:
            return None  
        distribution[type] = quantity // number_of_astronauts
    
    return distribution

supplies = {'food': 50, 'water': 80, 'kits': 60}
number_of_astronauts = 5

result = distribute_supplies(supplies, number_of_astronauts)
print(result)

####################################################################
