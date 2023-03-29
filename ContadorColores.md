# Python
Funciones Básicas en Py
lista= ['azul', 'rojo', 'verde', 'verde', 'verde', 'rojo', 'verde', 'verde', 'azul', 'amarillo', 'azul', 'azul', 'verde', 'verde', 'verde', 'amarillo', 'amarillo']
def color_frecuente(lista):
    contador = {}
    for color in lista:
        if color in contador:
            contador[color] += 1 # incrementamos si existe el color
        else:
            contador[color] = 1 # creamos un nuevo item con el key del color y el valor inicial de 1
    m = max(contador.values()) # obtenemos el max de repeticiones
    color_seleccionado = [key for key, value in contador.items() if value == m] # seleccionamos los colores que cumplen con el maximo
    if len(color_seleccionado) > 1: # verificamos si existe mas de un maximo
        color_seleccionado = min(color_seleccionado, key= lambda x: lista.index(x)) # obtenemos el elemento segun la prioridad
    else:
         color_seleccionado = color_seleccionado[0]
    return color_seleccionado, m
    
print(color_frecuente(lista))
