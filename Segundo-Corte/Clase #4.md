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

## 5. Ejercicios
📚 # Ejemplo 1

![image](https://github.com/user-attachments/assets/57cac3c2-e697-400c-9d18-064e91c4e033)

![image](https://github.com/user-attachments/assets/601a9c37-42e0-45e7-93c3-c47b856b7caa)

Aplicando ley de kirchoff de corrientes LKC

$i_u - i_1 - i_c = 0$

$i_u(t) - \frac{V_{AB}}{0.5} - 2 \frac{d y(t)}{dt} = 0$

$V_{AB} = i_c \cdot (1 + y(t))$

$V_{AB} = 2 \frac{d y(t)}{dt} + y(t)$

$u(t) - \frac{2}{0.5} \frac{d y(t)}{dt} - \frac{1}{0.5} y(t) - 2 \frac{d y(t)}{dt} = 0$

$u(t) - 6 \frac{d y(t)}{dt} - 2 y(t) = 0$


---

📚 # Ejemplo 2:

![image](https://github.com/user-attachments/assets/739781b7-ddfe-414c-805b-aab2eae417c4)

$I_1 + I_2 + I_3 = 0$

$\frac{e_1 + e_x}{R_1} + c_1 \frac{d(0 - e_x)}{dt} + \frac{e_0 - e_x}{R_2} = 0$

$- e_x = V_{R2} + e_0$

$- e_x = R_2 \left(I_3\right) + e_0$

$I_3 = C_2 \frac{d e_0}{dt}$

$- e_x = R_2 \cdot C_2 \frac{d e_0}{dt} + e_0$

$- \frac{d e_x}{dt} = R_2 \cdot C_2 \frac{d^2 e_0}{dt^2} + \frac{d e_0}{dt}$

$\frac{e_i}{R_1} + \frac{R_2 C_2}{R_1} \frac{d e_0}{dt} + \frac{1}{2} e_0 + R_2 C_2 C_1 \frac{d^2 e_0}{dt^2} + \frac{d e_0}{dt} + \frac{e_0}{R_2} + C_2 \frac{d e_0}{dt} + \frac{e_0}{R_2}$

## 6. Ejercicios
📚 # Ejercicio #1

![image](https://github.com/user-attachments/assets/d6d55236-79f0-4c3a-a8ac-1898a8ea6836)

$x(t) = R\,i(t) + L \frac{di}{dt} + \frac{1}{C} \int i(t)\,dt$

$x(s) = R\,I(s) + sL\,I(s) + \frac{1}{Cs} I(s)$

$y(s) = \frac{I(s)}{Cs}$

$\frac{y(s)}{x(s)} = \frac{\frac{I(s)}{Cs}}{R I(s) + sL I(s) + \frac{I(s)}{Cs}}$

$H(s) = \frac{\frac{1}{Cs}}{R + sL + \frac{1}{Cs}}$

---

📚 # Ejercicio #2

![image](https://github.com/user-attachments/assets/3fb41b9d-64a8-472b-b54b-7e7488bb35a2)


$X_C = \frac{1}{C s}$

$V_0 = \frac{1}{C s R_1}$

$e_0 = \frac{Z_2}{Z_1} = \frac{R_2}{R_1 + \frac{1}{C s}}= -\frac{R_2}{\frac{1 + R_1 C s}{C s}}= \frac{R_2}{C s + R_1 C s^2}$



## **Conclusión**
Los circuitos RLC y los circuitos con amplificadores operacionales son importantes en el análisis y modelado de sistemas dinámicos eléctricos. Los circuitos RLC permiten representar sistemas de segundo orden donde se estudian fenómenos como la oscilación, el amortiguamiento y la resonancia, características clave en el comportamiento dinámico de muchos sistemas físicos. Por otro lado, los amplificadores operacionales, combinados con resistencias y capacitores, permiten construir integradores, derivadores y filtros, lo cual facilita la implementación de modelos diferenciales y el diseño de sistemas de control analógico. En conjunto, estos circuitos son herramientas importantes para comprender, simular y controlar la dinámica de sistemas tanto eléctricos como mecánicos, térmicos o hidráulicos mediante analogías.




