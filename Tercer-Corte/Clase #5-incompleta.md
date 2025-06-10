# Diagrama de flujo de señales 
El diagrama de flujo de señales es una representación gráfica utilizada para analizar sistemas complejos. Permite visualizar las relaciones entre las diferentes variables del sistema mediante nodos y ramas. Su principal ventaja es que facilita la obtención de la función de transferencia total del sistema, haciendo el análisis más sencillo y ordenado.

## 1. Fundamentos del Algebra de Bloques
El diagrama de flujo de señales es una herramienta gráfica que se utiliza principalmente en el análisis de sistemas lineales e invariantes en el tiempo (LTI). Su propósito es representar el flujo de señales dentro de un sistema, mostrando de forma ordenada la relación entre variables y operaciones matemáticas.

## 2. Definiciones
> 🔑 *Nodos:* Representan las variables del sistema (entradas, salidas o internas).

> 🔑 *Ramas:* Líneas con una ganancia asociada (función de transferencia) que indican cómo una variable influye sobre otra.

> 🔑 *Dirección del flujo:* Las flechas muestran el sentido en que fluye la señal.


## 3.  Elementos de los diagramas de flujo de señal

### Flecha
Representa la relación entre las variables del sistema

• Se representa por medio de flechas que indicando el sentido de la relación

• La fleche sale de la señal (Nodo) de entrada y llega a la señal de salida (Nodo)

• Se agrega una etiqueta a la flecha para indicar la función de transferencia que relaciona la entrada y la salida

![image](https://github.com/user-attachments/assets/e3edfe30-020d-473b-8fea-de27cebce4d6)

### Nodo
Representan las señales de entrada o salida delSistema

• Se representa por medio de un círculo con una etiqueta que
indique el nombre de la señal

![image](https://github.com/user-attachments/assets/9ef656a4-ac7f-4578-9161-0f729dd7c5f7)



## 4. Interpretación de los diagramas de flujo de señales
![image](https://github.com/user-attachments/assets/1b8327d7-d990-440f-83a2-28d3f48cc68a)


## 5. Comparación diagramas de bloques y flujo de señales
![image](https://github.com/user-attachments/assets/03701750-94fd-4f51-ac69-7f8e822f20df)

## 6. Definiciones  

• Camino o trayectoria: Camino o trayecto es un recorrido de ramas conectadas en el sentido de las flechas de las ramas.

• Si no se cruza ningún nodo más de una vez, el camino o trayecto es abierto.

• Si el camino o trayecto finaliza en el mismo nodo del cual partió, y no cruza ningún otro más de una vez, es un camino o trayecto cerrado

• Ganancia de lazo: La ganancia de lazo es el producto de las ganancias de ramas de un lazo.

• Trayecto o camino directo: Trayecto directo es el camino o trayecto de un nodo de entrada a un nodo de salida, sin cruzar ningún nodo más de una vez.

• Ganancia de trayecto directo: La ganancia de trayecto directo es el producto de las ganancias de rama de un camino o trayecto directo.

• Lazo: Un lazo es un camino o trayecto cerrado.

• Ganancia de lazo: La ganancia de lazo es el producto de las ganancias de ramas de un lazo.

## 7. Fórmula de Mason
![image](https://github.com/user-attachments/assets/c11157fc-a942-4b54-902d-5806ea27c35d)

• 𝑃𝑘 Ganancia de los caminos directos

• Δ = 1 − (suma ganancias de los lazos) + (suma producto de 2 lazos que no se tocan) – (suma producto de 3 lazos que no se tocan)+…

• Δ𝑘 = 1 −(suma ganancias lazos que no toquen la trayectoria 𝑃𝑘)+(suma ganancias 2 lazos que no toquen la trayectoria 𝑃𝑘 y no se toquen entre sí)-(suma ganancias 3 lazos que no toquen la trayectoria 𝑃𝑘 y no se toquen entre sí)+…

## 7. Ejemplos

### Ejemplo 1: 

![image](https://github.com/user-attachments/assets/2aa7e635-8fbb-42f3-9314-7ca223699f29)

Trayectoria directos

$P_1 = 1 \cdot 1 \cdot G_1 \cdot G_2 \cdot G_3 \cdot 1 = G_1 G_2 G_3$

Lazos cerrados

$L_1 = G_1 G_2 H_1$

$L_2 = - G_2 G_3 H_2$

$L_3 = - G_1 G_2 G_3$

Determinante

$\Delta = 1 - (L_1 + L_2 + L_3)$     

Cofactores

$\Delta_1 = 1$     

$\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1}{\Delta} = \frac{G_1 G_2 G_3}{1 - G_1 G_2 H_1 + G_2 G_3 H_2 + G_1 G_2 G_3}$



### Ejemplo 2: 

![image](https://github.com/user-attachments/assets/9ee6286a-cf5f-4f52-b7d4-4a1d022c6409)


Trayectoria directos

$P_1 = G_1 G_2 G_3 G_4 G_5$

$P_2 = G_1 G_6 G_4 G_5$

$P_3 = G_1 G_2 G_7$

Lazos cerrados

$L_1 = - G_4 H_1$

$L_2 = - G_2 G_7 H_2$

$L_3 = - G_6 G_4 G_5 H_2$

$L_4 = - G_2 G_3 G_4 G_5 H_2$

Determinante

$\Delta = 1 - (L_1 + L_2 + L_3 + L_4) + + L_1 + L_2$ 

Cofactores

$\Delta_1 = 1$   

$\Delta_2 = 1$   

$\Delta_3 = 1 - L_1$   

$\frac{C(s)}{R(s)} = \frac{1}{\Delta} (P_1 \Delta_1 + P_2 \Delta_2 + P_3 \Delta_3) = \frac{G_1 G_2 G_3 G_4 G_5 + G_1 G_6 G_4 G_5 + G_1 G_2 G_7 (1 + G_4 H_1)}{1 + G_4 H_1 + G_2 G_7 H_2 + G_6 G_4 G_5 H_2 + G_2 G_3 G_4 G_5 H_2 + G_4 H_1 G_2 G_7 H_2}$





## 8. Ejercicios

📚 # Ejemplo 1: 

![image](https://github.com/user-attachments/assets/b2820717-8728-4e4f-81b2-3bb4b94a76fb)

Trayectoria directos

$P_1 = G_1 G_2$

$P_2 = G_4$

$P_3 = G_3$

Lazos cerrados

$L_1 = - G_1 H_2$

$L_2 = - G_2 H_1$

$L_3 = - G_3 H_1 H_2$

Cofactores

$\Delta_1 = 1$   

$\Delta_2 = 1 - L_1$   

$\frac{C(s)}{R(s)} = \frac{P_1 \Delta_1 + P_2 \Delta_2 + P_3 \Delta_3}{\Delta} = \frac{G_1 G_2 \cdot 1 + G_4 (1 + G_1 H_2) + G_3 \cdot 1}{1 + G_1 H_2 + G_2 H_1 - G_3 H_1 H_2}$
  


## **Conclusión**
Los diagramas de flujo de señal son herramientas gráficas fundamentales en el análisis y diseño de sistemas dinámicos, especialmente en control automático y procesamiento de señales. Permiten visualizar de forma estructurada la relación entre las variables y operaciones de un sistema, facilitando la comprensión de su comportamiento. Además, su uso optimiza la resolución de ecuaciones mediante la aplicación de reglas específicas como la de Mason. Gracias a su capacidad para simplificar sistemas complejos, los diagramas de flujo de señal son esenciales para ingenieros, técnicos y diseñadores en el desarrollo de soluciones eficientes y precisas en automatización, electrónica y telecomunicaciones.
