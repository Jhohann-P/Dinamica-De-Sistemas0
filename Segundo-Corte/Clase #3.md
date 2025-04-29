# Sistemas Mecanicos II
## 1. Sistemas de control en Dinámica de Sistemas 
En dinámica de sistemas, los **sistemas mecánicos** son aquellos compuestos por componentes físicos que interactúan mediante fuerzas y movimientos. Estos sistemas pueden incluir elementos como masas, resortes, ruedas, palancas, entre otros, y su comportamiento está determinado por las leyes de la física, como las de Newton. En términos de dinámica, se estudian cómo las fuerzas externas o internas afectan el movimiento y las interacciones entre los componentes del sistema.

## 2. Definiciones   
>🔑*Trabajo:* Es la energía transferida cuando una fuerza mueve un objeto a lo largo de una distancia.
  
>🔑*Energía potencial:* Es la energía almacenada en un objeto debido a su posición o estado (como una piedra en lo alto de una colina).
      
>🔑*Energía cinética:* Es la energía que tiene un objeto debido a su movimiento.
  
>🔑*Potencia:* Es la rapidez con la que se realiza un trabajo o se transfiere energía.

## 3. Aplicando a elementos mecánicos
1. Energía potencial en un resorte:
 
   Es el trabajo neto hecho sobre él por las fuerzas que actúan en sus extremos cuando es comprimido o estirado.
   
$U = \int_0^x F \, dx = \int_0^x kx \, dx = \frac{1}{2} k x^2$


   De forma general el cambio de energía sería:

$\Delta U = \int_{x_1}^{x_2} F \, dx = \int_{x_1}^{x_2} kx \, dx = \frac{1}{2} k x_2^2 - \frac{1}{2} k x_1^2$


2. Potencia en un resorte:
 
   Potencia requerida para estirar o comprimir un resorte

$P = \frac{dW}{dt} = \frac{F \, dx}{dt} = F x' = Kx x'$


   sabiendo que $U = \frac{1}{2} K x^2$
(Energia potencial en un resorte)

  $P = Kx x' = U'$

3. Potencia en una masa:

    La potencia requerida para acelerar una masa en línea recta

$P = \frac{dW}{dt} = \frac{F \, dx}{dt} = F x' = m x''x'$

   Sabiendo que $T = \frac{1}{2} m v^2$ (Energia cinetica masa)

  $P = mx''x' = mv'v = T'$

4. Energía disipada:

   La energía disipada en un amortiguador corresponde al trabajo neto realizado sobre este

   ![image](https://github.com/user-attachments/assets/072d40fb-0aa9-4795-ad8f-5869452fde2b)
$\Delta W = \int_{x_1}^{x_2} F \, dx = \int_{x_1}^{x_2} b x' \, dx = b \int_{t_1}^{t_2} x' \cdot \frac{dx}{dt} \, dt = b \int_{t_1}^{t_2} {x'}^2 \, dt$

5. Potencia disipada en amortiguador:

   La potencia disipada en el amortiguador de cilindro es:

$P = \frac{dW}{dt} = \frac{F dx}{dt} = F x'$

Sabiendo que $F = b x'$

$P = b x^2$

### 4. Método de energía para obtener las ecuaciones de movimiento
  
1. Conservación de energía

Es posible obtener el modelo matemático considerando que la energía total de un sistema permanece igual si ninguna energía entra o sale del sistema.

En los sistemas mecánicos la fricción disipa energía en forma de calor.

Los sistemas que ni incluyen fricción se denominan sistemas conservativos.

2. Sistema conservativo:

Toda la energía (cinética y potencial) sale del sistema en forma de trabajo mecánico. No se disipa energía.

$\Delta (T + U) = \Delta W$ (Trabajo neto fuerza externa)

Si no entra energía externa entonces

$\Delta (T + U) = 0$
eso implica que $T + U = constante$




     
 Ejemplo 

$T = \frac{1}{2} m x^2$ , $U = \frac{1}{2} k x^2$

![image](https://github.com/user-attachments/assets/df754bf5-dd90-4543-90c7-a929b33c7aac)


$T + U = \frac{1}{2} m x^2 + \frac{1}{2} k x^2 = \text{constante}$


Al derivar la energía total

$\frac{d}{dt} \left( T + U \right) = m x' x'' + k x x' = \left( m x'' + k x \right) x' = 0$

$m x'' + k x = 0$


## 5. Ejercicios
📚 # Ejemplo 1

![image](https://github.com/user-attachments/assets/1462771c-3c69-4f36-bcfe-542213e2ab17)

$-b x_1' - k(x_1 - x_2) = m_1 x_1''$

$m_1 x_1'' + b x_1' + k(x_1 - x_2) = 0$

$-k(x_2 - x_1) + u = m_2 x_2''$

$m_2 y_2'' + k(x_2 - x_1) = u$

📚 # Ejemplo 2:


## **Conclusión**
En dinámica de sistemas, los sistemas mecánicos se pueden analizar mediante conceptos de trabajo, energía y potencia. Estos principios permiten comprender cómo las fuerzas afectan el movimiento y la energía de los cuerpos. El uso de modelos energéticos, como la conservación de la energía, facilita la obtención de ecuaciones de movimiento, especialmente en sistemas conservativos donde no hay pérdida de energía. Sin embargo, cuando existen elementos como amortiguadores, parte de la energía se disipa en forma de calor, lo que debe considerarse en el análisis. En conjunto, estos enfoques proporcionan una base sólida para entender y predecir el comportamiento dinámico de sistemas mecánicos complejos.
