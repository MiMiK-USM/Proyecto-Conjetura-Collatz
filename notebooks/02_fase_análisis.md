Datos de la Conjetura de Collatz (100k)
Este repositorio contiene los resultados del cálculo de la Conjetura de Collatz para los primeros 100,000 números enteros positivos.

Estructura de los Datos
El archivo datos_collatz_100k.csv contiene las siguientes columnas:

| Número Inicial ($n$) | Número de Pasos (Iteraciones) | Valor Máximo Alcanzado |
| :--- | :--- | :--- |
| 1 | 0 | 1 |
| 2 | 1 | 2 |
| 3 | 7 | 16 |
| 4 | 2 | 4 |
| ... | ... | ... |



## 📈 Estadísticas Descriptivas del Tiempo de Vuelo $T(n)$

Para comprender la distribución del tiempo de vuelo a través de órdenes de magnitud, se extrajeron las métricas estadísticas principales divididas por cotas superiores de muestreo ($10 \le n \le 100,000$):

| Métrica | $T(n) \le 100,000$ | $T(n) \le 10,000$ | $T(n) \le 1,000$ | $T(n) \le 100$ | $T(n) \le 10$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Promedio** | 107.5384 | 84.9666 | 59.5420 | 31.4200 | 6.7000 |
| **Mediana** | 99.0000 | 73.0000 | 43.0000 | 19.0000 | 5.5000 |
| **Desviación Estándar** | 51.3659 | 46.5909 | 40.8729 | 34.4610 | 6.2902 |
| **Desviación Media** | 43.2569 | 40.5042 | 35.8198 | 24.6636 | 4.6400 |
| **Varianza** | 2,638.4312 | 2,170.4915 | 1,668.9242 | 1,175.6836 | 35.6100 |
| **Coef. Correlación** | 0.1708 | 0.2054 | 0.2282 | 0.3378 | 0.5980 |

### 📊 Distribución por Percentiles

La siguiente tabla desglosa la acumulación porcentual de los pasos necesarios para colapsar a 1 en cada uno de los límites evaluados:

| Percentil | $n \le 100,000$ | $n \le 10,000$ | $n \le 1,000$ | $n \le 100$ | $n \le 10$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **100% (Máximo)** | 350 | 261 | 178 | 118 | 19 |
| **90%** | 177 | 150.1 | 121.1 | 106.1 | 16.3 |
| **80%** | 155 | 132 | 109 | 32 | 9.6 |
| **70%** | 138 | 117 | 87 | 25 | 7.3 |
| **60%** | 119 | 95 | 54 | 22 | 6.4 |
| **50% (Mediana)** | 99 | 73 | 43 | 19 | 5.5 |
| **40%** | 84 | 60 | 36 | 16.6 | 4.2 |
| **30%** | 71 | 49 | 29 | 14 | 2.7 |
| **20%** | 59 | 41 | 23 | 9.8 | 1.8 |
| **10%** | 46 | 31 | 17 | 7 | 0.9 |
| **0% (Mínimo)** | 0 | 0 | 0 | 0 | 0 |

---

### 🔍 Conclusiones del Análisis de Escala:
1. **Comportamiento del Máximo Absoluto:** Mientras que para los primeros 10 números el camino más largo es de apenas 19 pasos, al expandir la frontera matemática a 100,000 elementos, aparece un número que requiere un máximo crítico de **350 iteraciones** antes de estabilizarse en el bucle 4-2-1.
2. **Evolución del Promedio:** Se observa un crecimiento sostenido pero desacelerado del promedio ponderado a medida que la muestra incrementa de tamaño, lo cual es característico de las propiedades logarítmicas subyacentes en las tendencias globales de los tiempos de vuelo de Collatz.
