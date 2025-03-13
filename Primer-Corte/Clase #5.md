# Ecuaciones Diferenciales

## 1. Introducción a las Ecuaciones Diferenciales en Dinámica de Sistemas
Las ecuaciones diferenciales en dinámica de sistemas describen cómo evolucionan las variables de un sistema a lo largo del tiempo en función de condiciones iniciales y parámetros. Son fundamentales para modelar fenómenos en diversas disciplinas como la física, la biología, la economía y la ingeniería.




## 2. Definiciones Claves   

>🔑 *Ecuación Diferencial*: Es una ecuación matemática que relaciona una función con sus derivadas, describiendo cómo cambia una variable con respecto al tiempo u otra variable independiente.
  
>🔑 *Dinámica de Sistemas*: Es el estudio del comportamiento de sistemas complejos a lo largo del tiempo mediante ecuaciones diferenciales, permitiendo modelar y predecir su evolución.
      
>🔑 *Variable de Estado*: Es una magnitud que describe el estado actual de un sistema, como la posición, la velocidad o la temperatura, y cuya evolución está gobernada por ecuaciones diferenciales.
  
>🔑 *Solución de una Ecuación Diferencial*: Es la función que satisface la ecuación diferencial para un conjunto de condiciones iniciales, determinando cómo evoluciona el sistema en el tiempo.


>🔑 *Homogeneidad*: Una ecuación diferencial es homogénea si no tiene términos independientes de la función desconocida y sus derivadas. Si contiene términos adicionales, se dice que es no homogénea.

>🔑 *Linealidad*: Una ecuación diferencial es lineal si la función desconocida y sus derivadas aparecen en forma lineal. De lo contrario, es no lineal.



## 3. Métodos de Resolución

Existen diferentes enfoques para resolver ecuaciones diferenciales:

### 3.1. Métodos Analíticos
- **Separación de Variables**: Se usa en ecuaciones diferenciales de primer orden que pueden reescribirse como la multiplicación de dos funciones separadas.
- **Factor Integrante**: Método utilizado para ecuaciones diferenciales lineales de primer orden.
- **Transformada de Laplace**: Convierte la ecuación diferencial en una ecuación algebraica en el dominio de Laplace, facilitando su resolución.

### 3.2. Métodos Numéricos
Cuando no es posible obtener una solución exacta, se pueden emplear métodos numéricos como:
- **Método de Euler**
- **Método de Diferencias Finitas**


## 4. Fracciones Parciales en Transformadas de Laplace

El método de fracciones parciales se utiliza para descomponer funciones racionales en términos más simples, permitiendo calcular la transformada inversa de Laplace.

### 4.1. Forma General
Si tenemos una función racional:
$$F(s) = \frac{P(s)}{Q(s)} $$
donde \( Q(s) \) es un polinomio factorizable, podemos descomponerla en fracciones parciales:
$$\frac{A}{s - a} + \frac{B}{s - b} $$

Esto permite encontrar la solución en el dominio del tiempo utilizando la transformada inversa de Laplace.

### 4.2. Ejemplo de Fracciones Parciales
Dada la función en el dominio de Laplace:
$$X(s) = \frac{5s + 7}{(s + 2)(s + 3)} $$
Queremos expresarla como:
$$X(s) = \frac{A}{s + 2} + \frac{B}{s + 3} $$
Multiplicamos ambos lados por \((s + 2)(s + 3)\):
$$5s + 7 = A(s + 3) + B(s + 2) $$
Evaluando en \( s = -2 \) y \( s = -3 \), encontramos \( A \) y \( B \).

---

## 5. Ejemplos de Ecuaciones Diferenciales

📚 **Ejemplo 1**

$$\ddot{x} + 4\dot{x} + 4x = 0,$$
$$x(0) = 1, \quad \dot{x}(0) = -2 $$

Aplicamos la transformada de Laplace:
$$(s^2 X(s) - s x(0) - \dot{x}(0)) + 4(s X(s) - x(0)) + 4X(s) = 0 $$
Reemplazamos valores:
$$(s^2 X(s) - s(1) - (-2)) + 4(s X(s) - 1) + 4X(s) = 0 $$
Despejamos \( X(s) \):
$$X(s) = \frac{s + 2}{(s + 2)^2} $$
Aplicamos fracciones parciales y transformada inversa de Laplace para obtener:
$$x(t) = (1 + 2t)e^{-2t} $$

📚 **Ejemplo 2**

$$\ddot{x} - 6\dot{x} + 9x = 0,$$
$$x(0) = 3, \quad \dot{x}(0) = -5 $$

Aplicamos la transformada de Laplace:
$$(s^2 X(s) - s x(0) - \dot{x}(0)) - 6(s X(s) - x(0)) + 9X(s) = 0 $$
Reemplazamos valores:
$$(s^2 X(s) - 3s + 5) - 6(s X(s) - 3) + 9X(s) = 0 $$
Despejamos \( X(s) \):
$$X(s) = \frac{3s - 5}{(s - 3)^2} $$
Aplicamos fracciones parciales y transformada inversa de Laplace para obtener:
$$x(t) = (3 + 5t)e^{3t} $$

---

## 6. Conclusión

Las ecuaciones diferenciales son herramientas fundamentales para modelar el comportamiento de sistemas dinámicos. La transformada de Laplace facilita su resolución al convertirlas en ecuaciones algebraicas, simplificando el análisis. Además, el uso de fracciones parciales permite descomponer funciones en términos más manejables para la transformada inversa. Estas técnicas son esenciales en ingeniería y física para el análisis de sistemas mecánicos, eléctricos y de control.



