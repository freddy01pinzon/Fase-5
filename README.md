#fecha: 26/05/2026
#proyecto: Fase-5 POA
#Nombre: Freddy Leonardo Pinzon Estupiñan 
#Codigo: 213022
#Problema N° 3

# Matriz de artículos:
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    [101, "Cuadernos", 5, 10],
    [102, "Lápices", 20, 15],
    [103, "Borradores", 3, 8],
    [104, "Marcadores", 12, 12],
    [105, "Reglas", 1, 5]
]

# Función para calcular la cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0

# Mostrar lista de pedidos
print("LISTA DE PEDIDOS\n")

for articulo in inventario:
    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    cantidad_pedir = calcular_pedido(stock_actual, stock_minimo)

    print("Artículo:", nombre)
    print("Cantidad a pedir:", cantidad_pedir)
    print("----------------------")
