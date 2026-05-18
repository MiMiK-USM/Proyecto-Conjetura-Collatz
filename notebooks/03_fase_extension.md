# Stopping Time

Para entender cómo se comporta la conjetura de Collatz a gran escala, no basta con ver cómo los números bajan a uno, sino que es necesario analizar el **Stopping Time** (en español, *tiempo de parada*).

El stopping time, que se escribe comúnmente como $S(n)$, se fija en cuántos pasos le toma a una secuencia llegar a un número menor que el valor con el que empezamos.

Esto se entiende mejor si se analiza la paridad del número inicial. Por ejemplo, con los números pares es inmediato: como el primer paso es dividirlos por dos,

$$
\frac{n}{2},
$$

el resultado es menor que el inicial. Esto significa que para la mitad de todos los números naturales, el tiempo de parada es exactamente $1$.

Con los impares la situación se complica, porque la regla abreviada

$$
\frac{3n+1}{2}
$$

siempre entrega un número más grande, obligando a la secuencia a iterar varias veces antes de empezar a descender.

Si tomamos como ejemplo el número $11$, su camino sería:

$$
11 \rightarrow 34 \rightarrow 17 \rightarrow 52 \rightarrow 26 \rightarrow 13 \rightarrow 40 \rightarrow 20 \rightarrow 10
$$

Aquí vemos que el $10$ es el primer número menor que $11$, y como tomó $8$ pasos llegar hasta ahí, podemos decir que:

$$
S(11)=8
$$

A nivel estadístico, si se observan estas secuencias como caminos aleatorios donde se sube y se baja al azar, se puede notar que para “casi todos” los números el valor de $S(n)$ es relativamente bajo. De hecho, se estima que el comportamiento promedio sigue una tendencia logarítmica aproximada por:

$$
S(n)\approx \frac{2}{\ln(4/3)}\ln n
$$

Esto fue clave para que el matemático Terence Tao lograra en 2019 el avance más importante sobre la conjetura de Collatz en décadas.

Tao no demostró la conjetura por completo, pero utilizó el stopping time para probar que casi el cien por ciento de los números terminan descendiendo a valores mucho menores que el inicial.

Lo interesante de su trabajo es que demostró que, para casi todo $n$, el tiempo de parada es menor que cualquier función que crezca al infinito, incluso si lo hace extremadamente lento, como:

$$
\ln \ln \ln \ln n
$$

Para lograr esto, Tao combinó herramientas avanzadas de análisis armónico y ecuaciones en derivadas parciales, tratando el problema no como casos aislados, sino como una gran distribución estadística.

De este modo, aunque la conjetura de Collatz sigue sin resolverse completamente, este enfoque probabilístico redefine la búsqueda de contraejemplos, mostrando que cualquier excepción tendría que ser una anomalía extremadamente rara dentro de los números naturales.
