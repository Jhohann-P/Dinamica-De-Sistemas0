# Funcion de transferencia en diagrama de bloques
Los diagramas de bloques son herramientas para comprobar y realizar un análisis de sistemas dinámicos, ya que permiten representar de manera visual las interacciones entre las diferentes partes de un sistema y sus funciones de transferencia. Cada bloque en un diagrama representa un componente del sistema, y las conexiones entre los bloques indican cómo fluye la señal entre ellos.

## 1.  Modelamientos de sistemas


- **Modelado a partir de funciones de transferencia individuales:**  
  Una forma de abordar un sistema complejo es descomponerlo en sus componentes básicos, hallar la función de transferencia de cada uno, y luego integrarlos para representar el comportamiento global del sistema.

- **Diversidad de procesos y dispositivos involucrados:**  
  Incluso utilizando modelos ya conocidos, es bueno considerar que los sistemas complejos pueden integrar una amplia gama de dispositivos, procesos dinámicos y no lineales. Esto incluye, por ejemplo, sistemas térmicos, hidráulicos, eléctricos, mecánicos, etc



## 2. Definiciones   
> 🔑 *Sistema dinámico:* Es aquel cuyo comportamiento cambia con el tiempo, y puede modelarse mediante ecuaciones diferenciales o funciones de transferencia.

> 🔑 *Motor DC:* Dispositivo electromecánico que convierte energía eléctrica en movimiento rotacional.

> 🔑 *Solenoide:* Actuador lineal electromecánico que genera una fuerza proporcional a la corriente en su bobina, provocando un desplazamiento mecánico.

> 🔑 *Tacómetro:* Sensor que convierte la velocidad angular de un eje en una señal de voltaje proporcional

> 🔑 *Engranajes y poleas:* Elementos mecánicos que transmiten potencia y modifican el torque y velocidad angular en sistemas rotacionales. Alteran la inercia reflejada hacia el motor.

> 🔑 *Sensor transmisor:* Dispositivo que mide una variable física y entrega una señal eléctrica proporcional (si es lineal) o relacionada de forma no lineal, según el tipo de sensor.

> 🔑 *Diagrama de bloques:* Representación gráfica de un sistema, donde se muestran las relaciones funcionales entre los componentes mediante bloques interconectados con señales.


## 3. Modelos de sistemas más conocidos
### 1. Modelo de un Selenoide

Un solenoide es un sistema electromecánico compuesto por:

- **Circuito eléctrico:** Embobinado con resistencia $$\( r \)$$ e inductancia $$\( L \)$$.
- **Transductor electromagnético:** Convierte corriente en fuerza mecánica.
- **Sistema mecánico de traslación:** Produce movimiento lineal.


#### 1. Modelo Eléctrico

- **Ecuación en el tiempo:**

  $$\[L \frac{di(t)}{dt} + r \cdot i(t) = v(t)\]$$

- **En Laplace:**

  $$\[I(s) = \frac{V(s)}{Ls + r}\]$$

#### 2. Acoplamiento Electromecánico

La corriente genera una fuerza proporcional:

$$\[F_s(s) = K_s \cdot I(s)\]$$


#### 3. Modelo Mecánico

El sistema responde con movimiento:

$$\[X(s) = \frac{F_s(s)}{ms^2 + bs + k}\]$$

#### Diagrama de Bloques del Solenoide

$$V(s) → [1 / (Ls + r)] → [K_s] → [1 / (ms² + bs + k)] → X(s)$$

---

###  2. Modelo de un Motor de Corriente Directa (Motor DC)

- Un motor DC es un sistema electromecánico compuesto por:

- **Embobinado:** Produce el campo magnético.
- **Imán o campo:** Genera el flujo magnético.
- **Eje y carga:** Parte mecánica que se mueve por el torque del motor.


#### 1. Motor DC con Corriente de Campo

- El **flujo magnético** $$\( \Phi \)$$ es proporcional a la **corriente de campo** $$\( i_f \)$$.
- El **torque desarrollado** $$\( T \)$$ es proporcional al producto $$\( \Phi \cdot i_a \)$$, donde $$\( i_a \)$$ es la corriente de armadura:

  $$\[T = K_T \cdot \Phi \cdot i_a\]$$

- El **torque aplicado a la carga** considera la inercia \( J \) y fricción \( b \):

  $$\[T = J \cdot \frac{d\omega}{dt} + b \cdot \omega\]$$



#### 2. Motor DC con Corriente de Armadura

Si el flujo $$\( \Phi \)$$ se mantiene constante, el torque es directamente proporcional a la corriente de armadura:

$$\[T = K_T \cdot i_a\]$$

- La corriente de armadura se relaciona con el voltaje aplicado $$\( V_a \)$$, la resistencia $$\( R_a \)$$, la inductancia $$\( L_a \)$$, y el voltaje inducido $$\( e_b \)$$:

  $$\[V_a = L_a \cdot \frac{di_a}{dt} + R_a \cdot i_a + e_b\]$$

- El **voltaje inducido** (fuerza contraelectromotriz) es proporcional a la velocidad angular:

  $$\[e_b = K_e \cdot \omega\]$$


#### 3. Parte Mecánica

La parte mecánica del motor se modela como un sistema rotacional clásico:

$$\[T = J \cdot \frac{d\omega}{dt} + b \cdot \omega\]$$

#### 4. Diagrama y Modelo de bloques 
![image](https://github.com/user-attachments/assets/ef660411-3a83-4a2b-a8da-ebfb2706e97a)

 **Entrada:** Voltaje aplicado a la armadura $$\( V_a(s) \)$$.
- **Salida:** Posición angular del eje $$\( \Theta(s) \)$$.

#### Componentes del sistema:

1. **Bloque eléctrico (armadura):**
   $$\[\frac{K_m}{sL_a + R_a}\]$$
   Este bloque representa la dinámica del circuito eléctrico del motor, considerando la inductancia $$\( L_a \)$$, resistencia $$\( R_a \)$$ y constante de torque $$\( K_m \)$$.

2. **Torque mecánico desarrollado:**  
   $$\( T_m(s) \)$$, generado por el motor.

3. **Torque de carga o perturbación:**  
   $$\( T_p(s) \)$$, se resta del torque total aplicado.

4. **Sistema mecánico rotacional:**  
   $$\[ \frac{1}{Js + b}\]$$
   Modela la dinámica del eje del motor, donde:
   - $$\( J \)$$: inercia del rotor,
   - $$\( b \)$$: coeficiente de fricción.

5. **Integrador final:**  
   $$\[\frac{1}{s}\]$$
   Convierte la velocidad angular $$\( \omega(s) \)$$ en posición angular $$\( \Theta(s) \)$$.

6. **Retroalimentación de velocidad:**  
   El voltaje inducido (fuerza contraelectromotriz) está dado por:
   $$\[e_b(s) = K_b \cdot \omega(s)\]$$
   Se retroalimenta y se resta del voltaje de entrada.
   
---

### 3. Elementos transmisores de energía

### Engranajes y Poleas en Sistemas Dinámicos

Los **engranajes** y **poleas** son elementos mecánicos utilizados para transmitir potencia y movimiento entre diferentes partes de un sistema.



#### Función en el Modelado de Sistemas

- Transfieren **energía mecánica** de un componente a otro (por ejemplo, del motor a la carga).
- Afectan los parámetros dinámicos del sistema, como la **inercia equivalente** $$\( J \)$$ y la **constante de torque** $$\( K_m \)$$, cuando se consideran las relaciones de transmisión.


#### Efecto de la Relación de Transmisión

Para un sistema con una relación de transmisión $$\( \frac{N_1}{N_2} \)$$:

- El ángulo de salida $$\( \theta_2 \)$$ y el de entrada $$\( \theta_1 \)$$ se relacionan como:
  
  $$\[\theta_2 = \frac{N_1}{N_2} \cdot \theta_1\]$$

- La velocidad angular y el torque se transforman de forma inversa respecto a la relación de engranajes:
  
  $$\[\omega_2 = \frac{N_1}{N_2} \cdot \omega_1, \quad T_1 = \frac{N_2}{N_1} \cdot T_2\]$$

- La **inercia reflejada** al eje del motor se calcula como:

  $$\[J_{\text{eq}} = J_{\text{carga}} \cdot \left( \frac{N_2}{N_1} \right)^2\]$$


#### Diagramas de Bloques

#### Sistema con Engranajes o Poleas

V → [Motor: θ₁] → (Relación N₁:N₂) → [Carga: θ₂]

Donde:
- $$\( \theta_1 \)$$: posición angular del motor
- $$\( \theta_2 \)$$: posición angular de la carga
- $$\( N_1/N_2 \)$$: relación de transmisión entre poleas o engranajes

---

### Tacómetros

- Son dispositivos que convierten la **velocidad angular** \( \omega(t) \) en una **señal de voltaje** proporcional.
- Modelo en Laplace:
  
  $$\[V_{\text{taco}}(s) = K_t \cdot \omega(s)\]$$


### Sensores Transmisores

#### Lineales:
- La salida es proporcional a la variable medida (PV):
  
  $$\[\frac{TO(s)}{PV(s)} = K\]$$

### No lineales:
- La relación entre entrada y salida depende de la magnitud, no se puede expresar con una ganancia constante.

---

##  Ejemplos 

### Ejemplo 1:  Modelo de un Solenoide

Un solenoide recibe un voltaje de entrada \( V(s) \), y se desea conocer el desplazamiento del émbolo \( X(s) \).

### Datos:
- $$\( L = 0.5 \, H \)$$
- $$\( R = 2 \, \Omega \)$$
- $$\( K_s = 3 \, N/A \)$$
- Sistema mecánico: $$\( m = 0.2 \, kg \)$$, $$\( b = 1 \, N \cdot s/m \)$$, $$\( k = 10 \, N/m \)$$

### Solución:
1. Función de transferencia eléctrica:
   $$\[I(s) = \frac{V(s)}{Ls + R} = \frac{V(s)}{0.5s + 2}\]$$

2. Fuerza generada:
   $$\[F_s(s) = K_s \cdot I(s) = 3 \cdot \frac{V(s)}{0.5s + 2}\]$$

3. Desplazamiento mecánico:
   $$\[X(s) = \frac{F_s(s)}{ms^2 + bs + k} = \frac{3V(s)}{(0.5s + 2)(0.2s^2 + s + 10)}\]$$


### Ejemplo 2: Motor DC

Dado un motor DC con:
- $$\( L_a = 0.1 \, H \)$$, $$\( R_a = 1 \, \Omega \)$$, $$\( K_b = 0.01 \)$$, $$\( J = 0.01 \)$$, $$\( b = 0.1 \)$$, $$\( K_m = 0.01 \)$$
- Entrada: $$\( V_a(s) \)$$

### Pregunta:
Encuentra la función de transferencia $$\( \frac{\omega(s)}{V_a(s)} \)$$

### Solución:

1. Circuito eléctrico:
   $$\[I(s) = \frac{V_a(s) - K_b \cdot \omega(s)}{sL_a + R_a}\]$$

2. Torque:
  $$\[T(s) = K_m \cdot I(s)\]$$

3. Mecánica:
   $$\[\omega(s) = \frac{T(s)}{Js + b}\]$$

4. Sustituyendo y simplificando:
   $$\[\frac{\omega(s)}{V_a(s)} = \frac{K_m}{(Js + b)(sL_a + R_a) + K_b K_m}\]$$

   Reemplazando valores:
   $$\[\frac{\omega(s)}{V_a(s)} = \frac{0.01}{(0.01s + 0.1)(0.1s + 1) + 0.0001}\]$$







## **Conclusión**
El modelado con diagramas de bloques permite y ayuda a representar y analizar sistemas electromecánicos como motores, solenoides y sensores de forma clara con su debida estructura. Estos modelos simplifican el diseño de controles y ayudan a entender cómo interactúan las partes eléctricas y mecánicas en un sistema dinámico.

