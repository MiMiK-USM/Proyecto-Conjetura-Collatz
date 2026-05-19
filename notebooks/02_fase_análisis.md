# 🌌 Análisis Numérico y Visual de la Conjetura de Collatz

Este repositorio está dedicado al estudio y visualización matemática de la **Conjetura de Collatz** (comúnmente conocida como el problema $3n + 1$ o la secuencia del granizo). A través de simulaciones computacionales, analizamos el comportamiento, las trayectorias individuales y los tiempos de vuelo para los primeros **10,000 números enteros positivos**.

---

## 📊 Visualizaciones del Proyecto

A continuación, se exponen los resultados analíticos y estadísticos generados a partir de nuestro conjunto de datos:

### 1. Comportamiento de una Trayectoria Crítica ($n = 27$)
El número 27 es célebre dentro del estudio de esta conjetura debido a su sorprendente volatilidad antes de colapsar. Aunque es una semilla pequeña, experimenta un "tiempo de vuelo" sumamente largo y picos numéricos muy elevados.

<p align="center">
  <img src="output.png" alt="Trayectoria de Collatz para n=27" width="70%">
</p>

* **Análisis:** Como se observa en la gráfica, la secuencia asciende a través de picos sucesivos, superando un valor máximo de **9,000** en la iteración ~77, antes de caer en picada hacia el bucle atractor $4 \rightarrow 2 \rightarrow 1$ en el paso 111.

### 2. Dispersión: Semilla Inicial vs. Tiempo de Vuelo
Al mapear cada número inicial contra la cantidad de pasos totales que requiere para llegar a 1, emergen patrones geométricos sorprendentes.

<p align="center">
  <img src="output1.png" alt="Dispersión Número Inicial vs Tiempo de Vuelo" width="85%">
</p>

* **Análisis:** La distribución no es aleatoria; los puntos se agrupan en **bandas o filamentos horizontales nítidos**. Esto demuestra visualmente que números extremadamente distantes entre sí comparten de forma matemática la misma longitud exacta de órbita.

### 3. Distribución Estadística de los Tiempos de Vuelo
Este histograma agrupa las frecuencias de los pasos requeridos para el colapso en el rango evaluado ($n = 1$ hasta $10,000$).

<p align="center">
  <img src="output2.png" alt="Histograma de Tiempos de Vuelo" width="85%">
</p>

* **Análisis:** Se evidencia una distribución bimodal marcada con picos de alta concentración de muestras alrededor de los **10-20 pasos** y un segundo bloque relevante cerca de los **40-50 pasos**, disminuyendo drásticamente la cantidad de números que requieren más de 80 iteraciones.

---

## 📂 Estructura Recomendada del Repositorio

Para el correcto funcionamiento de este formato visual, organiza tus archivos en GitHub de la siguiente manera:

```text
├── datos_collatz_100k.csv   # Tu archivo de datos original extraído de SharePoint
├── output.png               # Gráfica de la trayectoria n=27
├── output1.png              # Gráfica de dispersión
├── output2.png              # Histograma de tiempos de vuelo
└── README.md                # Este archivo de documentación
