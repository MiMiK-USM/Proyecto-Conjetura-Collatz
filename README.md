# Proyecto 1: Conjetura de Collatz

**Integrantes del Equipo:**
* Nicolas Mira
* Yamna Bruna
* Diego Escobar
* Paula Valdivia

Requisitos de instalacion 

Para poder ejecutar los análisis y códigos de este proyecto, asegúrate de tener Python 3 instalado en tu equipo y sigue estos pasos:

1. Clona este repositorio en tu máquina local.
2. Abre la terminal en la carpeta raíz del proyecto e instala todas las dependencias obligatorias ejecutando:
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Orden de Ejecución de los Notebooks

Para que los datos y los gráficos se generen correctamente en la carpeta `/figs`, los códigos deben ejecutarse de forma secuencial dentro de la carpeta `notebooks/`:

1. **`01_fase_base.ipynb`**: Implementación de las funciones base de Collatz y generación de gráficos principales para los primeros 10,000 números (Fase 1).
2. **`02_fase_analisis.ipynb`**: Escalado del algoritmo a 100,000 números y análisis estadístico avanzado junto con los récords sucesivos (Fase 2).
3. **`03_fase_extension.ipynb`**: Implementación de la extensión B3 (*Stopping Time*) y discusión analítica orientada al teorema de Terence Tao (Fase 3).
