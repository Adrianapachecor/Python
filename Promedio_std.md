# Python
Funciones Básicas en Py
def promedio_std(lista):

   x = 0

   y = 0

   suma = 0

   media = sum(lista) / len(lista)

   total = 0.0

   for i in lista:

       suma = suma + i

       total = total + (i - media) ** 2

   y = (total / len(lista)) ** 0.5

   x = suma / len(lista)

   return (x, y)


lista = [3, 5, 10, 12]
media, desviacion_tipica = promedio_std(lista)
print(f"Media: {media}")
print(f"Desviación estandar: {desviacion_tipica}")
