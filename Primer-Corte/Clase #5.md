# Ecuaciones Diferenciales

## 1. Ecuaciones diferenciales en dinámica de sistemas
Las ecuaciones diferenciales en dinámica de sistemas describen cómo evolucionan las variables de un sistema a lo largo del tiempo en función de condiciones iniciales y parámetros. Son fundamentales para modelar fenómenos en diversas disciplinas como la física, la biología, la economía y la ingeniería.

Estas ecuaciones permiten comprender y predecir el comportamiento de un sistema, facilitando su optimización y ajuste mediante métodos analíticos o computacionales como MATLAB y Python.

## 2. Definiciones
>🔑*Ecuación Diferencial*: Es una ecuación matemática que relaciona una función con sus derivadas, describiendo cómo cambia una variable con respecto al tiempo u otra variable independiente.

>🔑*Dinámica de Sistemas*: Es el estudio del comportamiento de sistemas complejos a lo largo del tiempo mediante ecuaciones diferenciales, permitiendo modelar y predecir su evolución.

>🔑*Variable de Estado*: Es una magnitud que describe el estado actual de un sistema, como la posición, la velocidad o la temperatura, y cuya evolución está gobernada por ecuaciones diferenciales.

>🔑*Solución de una Ecuación Diferencial*: Es la función que satisface la ecuación diferencial para un conjunto de condiciones iniciales, determinando cómo evoluciona el sistema en el tiempo.

## 3. Métodos de solución
Existen diferentes enfoques para resolver ecuaciones diferenciales:  
### 3.1. Transformada de Laplace  
La transformada de Laplace es una herramienta matemática que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia, facilitando su resolución.

### 3.2. Método de separación de variables
Se utiliza cuando la ecuación diferencial puede reescribirse como el producto de una función de la variable dependiente y otra de la variable independiente.

### 3.3. Método de coeficientes indeterminados
Se usa para resolver ecuaciones diferenciales lineales con coeficientes constantes cuando la función forzante es de un tipo específico, como polinomios, senos y cosenos.

### 3.4. Método de variación de parámetros
Este método permite encontrar soluciones particulares para ecuaciones diferenciales no homogéneas utilizando soluciones de la ecuación homogénea asociada.

## 4. Ejemplos con ecuaciones diferenciales

### 📚 Ejemplo 1
Resolver la ecuación diferencial:
$$\ddot{x} + 2\dot{x} - 3x = 0$$   
Con condiciones iniciales:
$$x(0) = -1, \quad \dot{x}(0) = 3$$   

Aplicamos la transformada de Laplace:
$$\left[s^2 X(s) - s X(0) - \dot{x}(0)\right] + 2 \left[s X(s) - X(0)\right] - 3 X(s) = 0$$   

Sustituyendo valores iniciales:
$$\left[s^2 X(s) - s (-1) - 3\right] + 2 \left[s X(s) + 1\right] - 3 X(s) = 0$$   

$$s^2 X(s) + s - 3 + 2s X(s) + 2 - 3X(s) = 0$$   
$$X(s) [s^2 + 2s - 3] = -s + 1$$   
$$X(s) = \frac{-s + 1}{(s + 3)(s - 1)}$$   

Usamos fracciones parciales:
$$\frac{-s + 1}{(s + 3)(s - 1)} = \frac{A}{s + 3} + \frac{B}{s - 1}$$   
Resolvemos para A y B:
$$-s + 1 = A(s - 1) + B(s + 3)$$   
Sustituyendo valores específicos, obtenemos:
$$A = -1, \quad B = 0$$   

Aplicamos la transformada inversa:
$$x(t) = -e^{-3t}$$   

### 📚 Ejemplo 2
Resolver la ecuación diferencial:
$$\ddot{x} - 8\dot{x} - 9x = 0$$   
Con condiciones iniciales:
$$x(0) = 0, \quad \dot{x}(0) = 4$$   

Aplicamos la transformada de Laplace:
$$\left[s^2 X(s) - s X(0) - \dot{x}(0)\right] -8 \left[s X(s) - X(0)\right] - 9 X(s) = 0$$   

Sustituyendo valores iniciales:
$$\left[s^2 X(s) - 4\right] - 8 [ s X(s)] - 9X(s) = 0$$   
$$X(s) [s^2 - 8s - 9] = 4$$   
$$X(s) = \frac{4}{(s - 9)(s + 1)}$$   

Usamos fracciones parciales:
$$\frac{4}{(s - 9)(s + 1)} = \frac{A}{s - 9} + \frac{B}{s + 1}$$   
Resolvemos para A y B:
$$A = \frac{2}{5}, \quad B = -\frac{2}{5}$$   

Aplicamos la transformada inversa:
$$x(t) = \frac{2}{5} e^{9t} - \frac{2}{5} e^{-t}$$   

## **Conclusión**
Las ecuaciones diferenciales son herramientas fundamentales para modelar el comportamiento de sistemas dinámicos. La transformada de Laplace facilita su resolución al convertirlas en ecuaciones algebraicas, simplificando el análisis. Además, el uso de fracciones parciales permite descomponer funciones en términos más manejables para la transformada inversa. Estas técnicas son esenciales en ingeniería y física para el análisis de sistemas mecánicos, eléctricos y de control.

