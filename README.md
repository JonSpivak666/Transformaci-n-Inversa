# Método de la Transformación Inversa

Este repositorio contiene código y explicaciones sobre el método de la transformación inversa, una técnica utilizada para generar variables aleatorias a partir de una distribución uniforme.

## Descripción

El método de la transformación inversa es una técnica utilizada en simulación para generar muestras aleatorias de una distribución específica a partir de una distribución uniforme \( U(0,1) \). Este método es especialmente útil cuando la función de distribución acumulativa (CDF) de la variable aleatoria objetivo es invertible.

### Matemática del Método

Dada una variable aleatoria uniforme \( U \sim U(0,1) \) y una variable aleatoria \( X \) con función de distribución \( F_X \), el método consiste en:

1. Generar una muestra \( U \) de la distribución uniforme \( U(0,1) \).
2. Aplicar la función inversa de la CDF de \( X \): \( X = F_X^{-1}(U) \).

### Ejemplo

Si la función de distribución acumulativa (CDF) de \( X \) es \( F_X(x) = 1 - e^{-x} \) para \( x \geq 0 \), entonces su inversa es:

$$
F_X^{-1}(u) = -\log(1-u)
$$

Por lo tanto, \( X = -\log(1-U) \) tendrá la distribución deseada.

## Requisitos

- Python 3.x
- numpy
- pandas
- matplotlib
- plotnine
- scipy

Puedes instalar los paquetes necesarios usando:

```bash
pip install numpy pandas matplotlib plotnine scipy
