---
title: Binario
date: 2023-09-24 20:30:00 +0100
categories: [Sistemas Microinformáticos y Redes, Redes Locales]
tags: [redes locales, binario, decimal, hexadecimal, smr]
---

# 1. ¿Qué es el sistema binario?

El sistema binario es un sistema numérico que utiliza solo dos dígitos para representar números y realizar operaciones matemáticas: 0 y 1. Este sistema es fundamental en la informática y la electrónica, ya que se adapta perfectamente a la forma en que los ordenadores almacenan y procesan la información en forma de corriente eléctrica (encendido/apagado) y se utiliza como base para todos los cálculos y operaciones que realizan.

A diferencia del sistema decimal, que utiliza diez dígitos (0 al 9) para representar números, el sistema binario se limita a dos dígitos, lo que lo hace muy eficiente y fácil de implementar en circuitos electrónicos. Cada dígito binario se llama un "bit" (abreviatura de "binary digit"). Los bits se agrupan en conjuntos más grandes llamados "bytes" para representar información más compleja.

El sistema binario se basa en los mismos principios que otros sistemas numéricos, como el decimal. Por ejemplo, en el sistema decimal, el valor de cada posición en un número se multiplica por diez a la potencia de la posición. En el sistema binario, el valor de cada posición se multiplica por dos a la potencia de la posición. Por lo tanto, un número binario se puede expresar como una suma de potencias de dos.

Por ejemplo, consideremos el número binario "1011", que consta de cuatro bits. Podemos calcular su valor en base 10 de la siguiente manera:

- El bit más a la derecha tiene un valor de 2^0 = 1.
- El siguiente bit tiene un valor de 2^1 = 2.
- El siguiente bit tiene un valor de 2^2 = 4.
- El bit más a la izquierda tiene un valor de 2^3 = 8.
- Entonces, el número binario "1011" en base 10 es igual a 8 + 0 + 2 + 1 = 11.

El sistema binario es esencial en la programación de computadoras porque todas las operaciones de la CPU se realizan en binario. Los programas y datos se almacenan en memoria en formato binario, y los circuitos electrónicos dentro de las computadoras utilizan señales binarias para representar y procesar información. Además, el sistema binario se utiliza para representar información en forma de texto, gráficos, audio y video en las computadoras.

En resumen, el sistema binario es un sistema numérico que utiliza solo dos dígitos, 0 y 1, para representar números y es fundamental en la informática y la electrónica debido a su eficiencia y capacidad para representar y procesar información en el mundo de las computadoras y la tecnología digital.

# 2. Pasar de binario a decimal

Para convertir un número binario a decimal, simplemente debes entender cómo funcionan las posiciones en el sistema binario y cómo calcular el valor decimal correspondiente. Aquí tienes un paso a paso para realizar esta conversión:

1. Escribe el número binario que deseas convertir. Por ejemplo, tomemos el número binario "101101".

2. Enumera las posiciones de derecha a izquierda, comenzando desde 0 y aumentando en 1 para cada posición hacia la izquierda. Esto se llama "posición de bits" y se usa para asignar poderes de 2 a cada dígito binario. Por ejemplo:

| 5 | 4 | 3 | 2 | 1 | 0 |
| 1 | 0 | 1 | 1 | 0 | 1 |

3. Ahora, para convertir el número binario a decimal, realiza los siguientes pasos para cada dígito binario:
- Multiplica el dígito binario (0 o 1) por 2 elevado a la potencia de su posición de bits.
- Suma estos valores para obtener el equivalente decimal.
- Siguiendo nuestro ejemplo:

- Para el bit en la posición 0: 1 * 2^0 = 1.
- Para el bit en la posición 1: 0 * 2^1 = 0.
- Para el bit en la posición 2: 1 * 2^2 = 4.
- Para el bit en la posición 3: 1 * 2^3 = 8.
- Para el bit en la posición 4: 0 * 2^4 = 0.
- Para el bit en la posición 5: 1 * 2^5 = 32.

4. Ahora, suma todos estos valores juntos:

1 + 4 + 8 + 0 + 32 = 45

Entonces, el número binario "101101" es igual a 45 en decimal.

En resumen, para convertir un número binario a decimal, debes multiplicar cada dígito binario por 2 elevado a la potencia de su posición de bits correspondiente y luego sumar estos valores. Esto te dará el valor decimal equivalente.

# 2.1 Consejos para el paso de binario a decimal
- Si el bit de menor peso vale 1 nos encontraremos ante un número impar.
- Si añadimos ceros por la izquierda a un número binario, el número no cambia.
- Si añadimos ceros por la derecha a un número binario lo estamos multiplicando por dos.
- Si el número que es todo unos, una forma rápida de calcular su valor es calcular el siguiente número y restarle uno a posteriori. Es decir, si tengo que obtener el valor de 111111, puedo calcular el valor de 1000000 que es 64 y restarle uno obteniendo que (111111)2 = (63)10.

# 2.2 Binario a hexadecimal
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/IQpDcrMrlsE?si=i8YMvAW32Mn1d1nz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>