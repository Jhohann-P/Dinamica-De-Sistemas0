# Ecuaciones Diferenciales
## 1. Ecuaciones diferenciales en dinamica de sistemas
Las ecuaciones diferenciales en dinámica de sistemas describen cómo evolucionan las variables de un sistema a lo largo del tiempo en función de condiciones iniciales y parámetros. Son fundamentales para modelar fenómenos en diversas disciplinas como la física, la biología, la economía y la ingeniería.  

Estas ecuaciones permiten comprender y predecir el comportamiento de un sistema, facilitando su optimización y ajuste mediante métodos analíticos o computacionales como MATLAB y Python.

## 2. Definiciones   
>🔑*Ecuación Diferencial*: Es una ecuación matemática que relaciona una función con sus derivadas, describiendo cómo cambia una variable con respecto al tiempo u otra variable independiente.
  
>🔑*Dinámica de Sistemas*: Es el estudio del comportamiento de sistemas complejos a lo largo del tiempo mediante ecuaciones diferenciales, permitiendo modelar y predecir su evolución.
      
>🔑*Variable de Estado*: Es una magnitud que describe el estado actual de un sistema, como la posición, la velocidad o la temperatura, y cuya evolución está gobernada por ecuaciones diferenciales.
  
>🔑*Solución de una Ecuación Diferencial*: Es la función que satisface la ecuación diferencial para un conjunto de condiciones iniciales, determinando cómo evoluciona el sistema en el tiempo.
  ## 3. Ejemplos con ecuaciones diferenciales

💡Ejemplo Sencillo de ecuaciones diferenciales 
  
$$ \ddot{x} + 3\dot{x} + 2x = 0,  $$ 
$$ x(0) = a,   \dot{x}(0) = b$$
Aplicamos la transformada de LaPlace
$$ \left[ s^2 X(s) - a s - b \right] + 3 \left[ s X(s) - a \right] + 2X(s) = 0 $$
Reemplazamos las condiciones iniciales
$$ [s^{2}X(s) - sx(0) - \dot{x}(0)] + 3[sX(s) - x(0)] + 2X(s) = 0 $$
Despejando X
$$ (s^{2} + 3s + 2)X(s) = a s + b + 3a $$
Solucion dominio S
$$ x(s) = \frac{a s + b + 3a}{s^{2} + 3s + 2} $$
$$ x(s) = \frac{a s + b + 3a}{(s+1)(s+2)} $$
$$ x(s) = \frac{2a + b}{s+1} - \frac{a + b}{s+2} $$
Aplicando transformada inversa desde las tablas para volver al dominio del tiempo
$$ x(t) = \mathcal{L}^{-1} \left[ X(s) \right] $$
$$ x(t) = \mathcal{L}^{-1} \left[ \frac{2a + b}{s+1} \right] - \mathcal{L}^{-1} \left[ \frac{a + b}{s+2} \right] $$
$$ x(t) = (2a + b)e^{-t} - (a + b)e^{-2t}, \quad (t \geq 0)$$

  ## 4. Ejercicios

📚 # Ejemplo 1

$$\ddot{x} + 2\dot{x} - 3x = 0,$$ 
$$x(0) = -1,   \dot{x}(0) = 3$$
$$\left[s^2 X(s) - s X(0) - \dot{x}(0)\right] + 2 \left[s X(s) - X(0)\right] - 3 X(s) = 0$$
$$\left[s^2 X(s) - s \left( -1 \right) - 3 \right] + 2 \left[ s X(s) - \left( -1 \right) \right] - 3 X(s) = 0$$
$$ \left[ s^2 X(s) + s - 3 \right] + 2 \left[ s X(s) + 1\right] - 3X(s) = 0 $$
$$s^2 X(s) + s - 3 + 2 s X(s) + 2 - 3 X(s) = 0$$
$$X(s) \left[ s^2 + 2s - 3 \right] + s - 1 = 0$$
$$X(s) = \frac{-s + 1}{s^2 + 2s - 3}$$
$$X(s) = \frac{-s + 1}{(s + 3)(s - 1)}$$
Realizamos fracciones parciales
$$-s + 1 = \frac{A}{s + 3} + \frac{B}{s - 1}$$
$$-s + 1 = A(s - 1) + B(s + 3)$$
Cuando s = 1
$$-1 + 1 = A(1 - 1) + B(1 + 3)$$
$$0 = B(4)$$
$$B = \frac{0}{4}$$
$$B = 0$$
Cuando s = -3
$$-(-3) + 1 = A(-3 - 1) + B(-3 + 3)$$
$$4 = A(-4)$$
$$A = \frac{4}{-4}$$
$$A = -1$$
Aplicamos la transformada de LaPlace
$$ x(t) =L^{-1}\left[\frac{-1}{s - 3}\right]$$
$$ x(t) =-L^{-1}\left[\frac{1}{s - 3}\right]$$
$$ x(t) =-e^{-3t}$$

📚 # Ejemplo 2

$$\ddot{x} - 8\dot{x} - 9x = 0,$$ 
$$x(0) = 0,   \dot{x}(0) = 4$$
$$\left[s^2 X(s) - s X(0) - \dot{x}(0)\right] -8 \left[s X(s) - X(0)\right] - 9 X(s) = 0$$
$$\left[s^2 X(s) - s \left( 0 \right) - 4 \right] - 8 \left[ s X(s) - \left( 0 \right) \right] - 9 X(s) = 0$$
$$ \left[ s^2 X(s) - 4 \right] - 8 [ s X(s)] - 9X(s) = 0 $$
$$X(s) \left[ s^2 - 8s - 9 \right] - 4 = 0$$
$$X(s) = \frac{4}{s^2 - 8s - 9}$$
$$X(s) = \frac{4}{(s - 9)(s + 1)}$$
Realizamos fracciones parciales
$$4 = \frac{A}{s - 9} + \frac{B}{s + 1}$$
$$4 = A(s + 1) + B(s - 9)$$
Cuando s = -1
$$4 = A(-1 + 1) + B(- 1 - 9)$$
$$4 = B(-10)$$
$$B = \frac{4}{-10}$$
$$B = -\frac{2}{5}$$
Cuando s = 9
$$4 = A(9 + 1) + B(9 - 9)$$
$$4 = A(10)$$
$$A = \frac{4}{10}$$
$$A = \frac{2}{5}$$
Aplicamos la transformada de LaPlace
$$ x(t) =L^{-1}\left[\frac{\frac{2}{5}}{s - 9} + \frac{\frac{2}{-5}}{s + 1}\right]$$
$$ x(t) =\frac{2}{5} L^{-1}\left[\frac{1}{s - 9}\right] - \frac{2}{5} L^{-1}\left[\frac{1}{s + 1}\right]$$
$$ x(t) =\frac{2}{5} e^{9t} - \frac{2}{5} e^{-t}$$





## **Conclusión**
Las ecuaciones diferenciales son esenciales en la dinámica de sistemas, ya que describen cómo evolucionan las variables en el tiempo. La transformada de Laplace facilita su resolución al convertirlas en ecuaciones algebraicas, permitiendo obtener soluciones más fácilmente. Esto es clave en ingeniería y física para analizar sistemas eléctricos, mecánicos y de control. En general, estas ecuaciones son fundamentales para modelar y predecir el comportamiento de sistemas dinámicos. 

