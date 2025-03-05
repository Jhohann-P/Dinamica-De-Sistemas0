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
$$ [s^{2}X(s) - sx(0) - \dot{x}(0)] + 3[sX(s) - x(0)] + 2X(s) = 0 $$
$$ (s^{2} + 3s + 2)X(s) = a s + b + 3a $$
$$ x(s) = \frac{a s + b + 3a}{s^{2} + 3s + 2} $$
$$ x(s) = \frac{a s + b + 3a}{(s+1)(s+2)} $$
$$ x(s) = \frac{2a + b}{s+1} - \frac{a + b}{s+2} $$
$$ x(t) = \mathcal{L}^{-1} \left[ X(s) \right] $$
$$ x(t) = \mathcal{L}^{-1} \left[ \frac{2a + b}{s+1} \right] - \mathcal{L}^{-1} \left[ \frac{a + b}{s+2} \right] $$
$$ x(t) = (2a + b)e^{-t} - (a + b)e^{-2t}, \quad (t \geq 0) $$








