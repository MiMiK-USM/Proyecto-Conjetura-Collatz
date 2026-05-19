import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

def calcular_collatz(n):
    pasos, max_v = 0, n
    while n > 1:
        n = n // 2 if n % 2 == 0 else 3 * n + 1
        if n > max_v: max_v = n
        pasos += 1
    return pasos, max_v

# Generar rango de 100k
limite = 100000
datos = [calcular_collatz(i) for i in range(1, limite + 1)]

# Crear DataFrame y guardar como CSV
df = pd.DataFrame(datos, columns=['iteraciones', 'valor_maximo'])
df.index.name = 'numero_inicial'
df.index += 1
df.to_csv('datos_collatz_100k.csv')

# Generar gráficos
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(14, 5))
ax1.scatter(df.index, df['iteraciones'], s=0.1, alpha=0.5, color='blue')
ax1.set_title('Pasos Totales')
ax2.scatter(df.index, df['valor_maximo'], s=0.1, alpha=0.5, color='magenta')
ax2.set_yscale('log')
ax2.set_title('Valor Máximo (Escala Log)')
plt.savefig('graficos_collatz_100k.png', dpi=150)
