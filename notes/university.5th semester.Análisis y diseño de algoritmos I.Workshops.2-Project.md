---
id: thpzzff6kb81s06vls2cv03
title: 2-Project
desc: ''
updated: 1687479473099
created: 1686427286181
---

## Enunciado

El Zoológico de Cali está planeando un gran espectáculo a ser realizado próximamente.

El espectáculo consistirá en tener como protagonistas algunos animales del zoológico. Exactamente, todo el espectáculo tendrá como protagonistas a $n$ animales de todos los que habitan el zoológico. Cada uno de estos animales tiene un valor que corresponde a su **grandeza** en el espectáculo. La grandeza causa más asombro a las personas que asisten al espectáculo. El rango de valores que toman las grandezas de los animales va de 1 hasta $n$ (sin repetirse).

El evento consistirá en $m$ partes:

1. Una gran apertura del evento, que consiste en $(m − 1) ∗ k$ escenas, donde en cada escena participan 3 animales **distintos**.

2. $m - 1$ partes de $k$ escenas cada una, donde, al igual que en la apertura, en cada escena participan 3 animales distintos.

	> Las escenas de la gran apertura participarán en estas escenas.

> Una escena es un conjunto de 3 elementos (animales) cuyo orden esta por definir.

> $n$, $m$ y $k$ son enteros positivos.

Es decir que en total hay $(m − 1) ∗ 2k$ escenas, sin hacer la distinción entre las de la apretura y las de las demás partes del espectáculo.

## Problema

Los parámetros de entrada del algoritmo a desarrollar son $n$ (animales con su respectiva grandeza), $m$ (número de partes del espectáculo) y $k$.

### Restricciones

- Localmente en cada escena se presentan los animales en orden ascendente según la grandeza de cada animal.

- Cada una de las $m$ partes del gran espectáculo, las escenas se presenten en orden ascendente según la grandeza total de cada escena (la suma de las grandezas de los animales que participan en la escena).

	> El criterio de desempate de dos escenas con la misma grandeza total, será la grandeza individual, es decir, la escena que tenga el animal con la mayor grandeza entre ellas, será la que se presente primero.

- Las $m -1$ partes posteriores a la gran apertura se deben presentar en orden ascendente según la grandeza total (la suma de las grandezas totales de cada escena).

### Información adicional

- El animal que más participo en escenas dentro del espectáculo y en cuantas participo.

	> Si hay empate(s) se deben mostrar todos los animales.

- El animal que menos participo en escenas dentro del espectáculo y en cuantas participo.

	> Si hay empate(s) se deben mostrar todos los animales.

- La escena de menor grandeza total.

- La escena de mayor grandeza total.

- El promedio de grandeza de todo el espectáculo (en las escenas).

### Características

- En las grandezas están todos los números de 1 hasta $n$.

- En la apertura están todas las escenas que estarán en las partes después de la apertura.

	> Es decir, las escenas que están en las $m − 1$ partes seguidas a la apertura sucedieron en la apertura.

## Entrega

Plantear soluciones para el problema en las siguientes complejidades:

- $O(n^2)$.

- $O(n\log n)$.

- $O(n)$.

## Solucion

> La implementacion de la solucion se hizo en el lenguaje de programacion Python.

### Representacion

Antes de solucionar el problema, primero se debe establece se recibiran los datos de una instancia del problema:

- `n`: sera una lista de objetos de clase `Animal` que tiene como atribuso `name` y `greatness`.

- `m`: un entero.

- `k`: un entero.

