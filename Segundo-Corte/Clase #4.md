# Sistemas Eléctricos
## 1. Redes RLC
Las redes RLC son circuitos compuestos por resistores (R), inductores (L) y condensadores (C). En la dinámica de sistemas, se utilizan para estudiar cómo estos componentes interactúan y afectan la respuesta de un sistema a señales de entrada. Las ecuaciones diferenciales que describen el comportamiento de estos circuitos dependen de la configuración (serie o paralelo) y los valores de R, L y C.


## 2. Definiciones   
  
>🔑*Resistor (R):* Componente que limita el flujo de corriente eléctrica y convierte la energía en calor.
      
>🔑*Inductor (L):* Componente que almacena energía en un campo magnético y resiste cambios en la corriente.
  
>🔑*Condensador (C):* Componente que almacena energía en un campo eléctrico y resiste cambios en el voltaje.
  
## 3. Circuito RLC

![image](https://github.com/user-attachments/assets/3b1fad0f-f089-47ac-8336-9b226b9e0cab)

𝐸𝑙 𝑓𝑒𝑛ó𝑚𝑒𝑛𝑜 𝑓í𝑠𝑖𝑐𝑜 𝑞𝑢𝑒 𝑚𝑜𝑑𝑒𝑙𝑎 𝑒𝑠𝑡𝑒 𝑐𝑜𝑚𝑝𝑜𝑟𝑡𝑎𝑚𝑖𝑒𝑛𝑡𝑜 𝑒𝑠 𝑙𝑎𝑠 𝑙𝑒𝑦𝑒𝑠 𝑑𝑒 𝑘𝑖𝑟𝑐ℎ𝑜𝑓𝑓 para el circuito

$R = \frac{v(t)}{i(t)}$   Ley de ohm

$i(t) = C \left( \frac{dv(t)}{dt} \right)$   𝐶𝑎𝑟𝑔𝑎 𝑑𝑒 𝑢𝑛 𝑐𝑜𝑛𝑑𝑒𝑛𝑠𝑎𝑑𝑜r

$v(t) = L \left( \frac{di(t)}{dt} \right)$   𝐶𝑎𝑟𝑔𝑎 𝑑𝑒 𝑢𝑛 𝑖𝑛𝑑𝑢𝑐𝑡𝑜r

### Ejemplo

![image](https://github.com/user-attachments/assets/580094df-c7ed-464e-a77a-ab8669e87d3f)

Aplicando ley de Kirchoff

$-u + v_R + v_L + v_C = 0$

$-u(t) + i(t) \cdot R + L\left(\frac{di(t)}{dt}\right) + y(t) = 0$

$-u(t) + RC\left(\frac{dy(t)}{dt}\right) + LC\left(\frac{d^2 y(t)}{dt^2}\right) + y(t) = 0$


Aún no está en términos de la variable y

$-u(t) + C\left(\frac{dy(t)}{dt}\right) \cdot R + L\left(\frac{d}{dt}\left[ C\left( \frac{dy(t)}{dt} \right) \right]\right) + y(t) = 0$


## 4. Circuitos con amplificadores operacionales
Se utilizan leyes de Kirchoff y el modelo simplificado del amplificador operacional

![image](https://github.com/user-attachments/assets/c8e92a10-62a5-4d72-8069-7118870a443e)

- La tension en ambas entradas del amplificador son iguales V+ = V-

- La corriente a las entradas del amplificador es 0

- La impedancia de entrada es muy grande

- La impedancia de salida es muy pequeña

### Amplificador no inversor

![image](https://github.com/user-attachments/assets/15290413-be04-4625-a83b-591630241be8)

$i_1 - i_2 = 0$

$\frac{e_o -e_i}{R_2} - \frac{e_i}{R_1} = 0$

$\frac{e_o}{R_2} = e_i \left( \frac{1}{R_2} + \frac{1}{R_1} \right)$

$e_o = e_i \left( 1 + \frac{R_2}{R_1} \right)$




#### Con elementos almacenadores de energía

![image](https://github.com/user-attachments/assets/7b39a7c0-05f7-4720-acfb-13d0fdb68558)

$i_1 - i_2 - i_3 = 0$

$\frac{e_i - e'}{R_1} - \frac{e' - e_o}{R_2} - C\frac{d(e' - e_o)}{dt} = 0$

$e' = 0$

$\frac{e_i}{R_1} - \frac{-e_o}{R_2} - C \frac{d (-e_o)}{dt} = 0$

$\frac{e_i}{R_1} = -\frac{e_o}{R_2} - C \frac{d (e_o)}{dt}$








## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos.




