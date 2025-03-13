# Ecuaciones Diferenciales

## 1. Ecuaciones diferenciales en dinámica de sistemas
Las ecuaciones diferenciales en dinámica de sistemas describen cómo evolucionan las variables de un sistema a lo largo del tiempo en función de condiciones iniciales y parámetros. Son fundamentales para modelar fenómenos en diversas disciplinas como la física, la biología, la economía y la ingeniería.  

Estas ecuaciones permiten comprender y predecir el comportamiento de un sistema, facilitando su optimización y ajuste mediante métodos analíticos o computacionales como MATLAB y Python.

## 2. Definiciones   
>🔑*Ecuación Diferencial*: Es una ecuación matemática que relaciona una función con sus derivadas, describiendo cómo cambia una variable con respecto al tiempo u otra variable independiente.
  
>🔑*Dinámica de Sistemas*: Es el estudio del comportamiento de sistemas complejos a lo largo del tiempo mediante ecuaciones diferenciales, permitiendo modelar y predecir su evolución.
      
>🔑*Variable de Estado*: Es una magnitud que describe el estado actual de un sistema, como la posición, la velocidad o la temperatura, y cuya evolución está gobernada por ecuaciones diferenciales.
  
>🔑*Solución de una Ecuación Diferencial*: Es la función que satisface la ecuación diferencial para un conjunto de condiciones iniciales, determinando cómo evoluciona el sistema en el tiempo.

## 3. Ejemplos con ecuaciones diferenciales

📚 # Ejemplo 1

$$\ddot{x} + 4\dot{x} + 4x = 0,$$  
$$x(0) = 2,   \dot{x}(0) = -3$$

Aplicamos la transformada de Laplace:
$$ \left[ s^2 X(s) - s x(0) - \dot{x}(0) \right] + 4 \left[ s X(s) - x(0) \right] + 4X(s) = 0 $$

Reemplazamos las condiciones iniciales:
$$ [s^{2}X(s) - 2s + 3] + 4[sX(s) - 2] + 4X(s) = 0 $$

Despejamos X(s):
$$ (s^2 + 4s + 4)X(s) = 2s - 3 + 8 - 4X(s) $$
$$ X(s)(s + 2)^2 = 2s + 5 $$
$$ X(s) = \frac{2s + 5}{(s + 2)^2} $$

Aplicamos transformada inversa:
$$ x(t) = \mathcal{L}^{-1} \left[ X(s) \right] $$
$$ x(t) = (2t + 5)e^{-2t}, \quad (t \geq 0)$$

📚 # Ejemplo 2

$$\ddot{x} - 5\dot{x} + 6x = 0,$$  
$$x(0) = 3,   \dot{x}(0) = -2$$

Aplicamos la transformada de Laplace:
$$ \left[ s^2 X(s) - s x(0) - \dot{x}(0) \right] - 5 \left[ s X(s) - x(0) \right] + 6X(s) = 0 $$

Reemplazamos las condiciones iniciales:
$$ [s^{2}X(s) - 3s + 2] - 5[sX(s) - 3] + 6X(s) = 0 $$

Despejamos X(s):
$$ (s^2 - 5s + 6)X(s) = 3s - 2 + 15 - 6X(s) $$
$$ X(s)(s - 2)(s - 3) = 3s + 13 $$
$$ X(s) = \frac{3s + 13}{(s - 2)(s - 3)} $$

Realizamos fracciones parciales:
$$ 3s + 13 = A(s - 3) + B(s - 2) $$
Cuando s = 3:
$$ 3(3) + 13 = A(3 - 3) + B(3 - 2) $$
$$ 9 + 13 = B(1) $$
$$ B = 22 $$
Cuando s = 2:
$$ 3(2) + 13 = A(2 - 3) + B(2 - 2) $$
$$ 6 + 13 = A(-1) $$
$$ A = -19 $$

Aplicamos la transformada inversa:
$$ x(t) = \mathcal{L}^{-1} \left[ \frac{-19}{s - 3} + \frac{22}{s - 2} \right] $$
$$ x(t) = -19 e^{3t} + 22 e^{2t} $$

## **Conclusión**
Las ecuaciones diferenciales son esenciales en la dinámica de sistemas, ya que describen cómo evolucionan las variables en el tiempo. La transformada de Laplace facilita su resolución al convertirlas en ecuaciones algebraicas, permitiendo obtener soluciones más fácilmente. Esto es clave en ingeniería y física para analizar sistemas eléctricos, mecánicos y de control. En general, estas ecuaciones son fundamentales para modelar y predecir el comportamiento de sistemas dinámicos.

