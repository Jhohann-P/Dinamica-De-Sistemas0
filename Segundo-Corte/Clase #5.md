# Introducción a Amplificadores en Dinámica de Sistemas
## 1. Tipos de Amplificadores
### Amplificador Inversor

- **Descripción**: Toma una señal de entrada, **la amplifica** y **la invierte** (cambia su signo).
- **Comportamiento**: Si la entrada es positiva, la salida será negativa, y viceversa.
- **Ganancia**: 
  $$A_v = -\frac{R_f}{R_{in}}$$
  Donde:
  - $$\( R_f \)$$ = Resistencia de realimentación.
  - $$\( R_{in} \)$$ = Resistencia de entrada.

### Amplificador No Inversor

- **Descripción**: Amplifica la señal **sin invertirla**.
- **Comportamiento**: Si la entrada es positiva, la salida también será positiva, solo que amplificada.
- **Ganancia**:
$$A_v = 1 + \frac{R_f}{R_{in}}$$


## 2. Definiciones   
>🔑*Amplificador:* Dispositivo que aumenta la magnitud de una señal de entrada sin alterar significativamente su forma.

>🔑*Amplificador Inversor:* Tipo de amplificador que invierte la fase de la señal de entrada mientras la amplifica.

>🔑*Amplificador No Inversor:* Amplificador que incrementa la magnitud de la señal de entrada manteniendo su misma fase.

>🔑*Ganancia:* Relación entre la señal de salida y la señal de entrada de un sistema, que indica cuánto se ha amplificado o atenuado la señal.

>🔑Amplificador Operacional (Op-Amp): Componente electrónico altamente versátil utilizado para amplificar señales, realizar operaciones matemáticas y construir sistemas de control.

>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
  
## 3. Ejercicio 1.
### Amplificador no inversor

![image](https://github.com/user-attachments/assets/2266b393-86ff-40e0-bc79-ff18525992cc)

$$i_1 - i_2 = 0$$

$$\frac{e_o - e_i}{R_2} - \frac{e_i}{R_1} = 0$$

$$\frac{e_o}{R_2} = e_i \left( \frac{1}{R_2} + \frac{1}{R_1} \right)$$

$$e_o = e_i \left( 1 + \frac{R_2}{R_1} \right)$$

### Con elementos almacenadores de energía

![image](https://github.com/user-attachments/assets/3a1f64a1-f2e4-48e3-a404-01ca1168a69f)


$$i_1 - i_2 - i_3 = 0$$

$$\frac{e_i - e'}{R_1} - \frac{e' - e_o}{R_2} - C \frac{d(e' - e_o)}{dt} = 0$$

$$e' = 0$$

$$\frac{e_i}{R_1} - \frac{e_o}{R_2} - C \frac{d(-e_o)}{dt} = 0$$

$$\frac{e_i}{R_1} = -\frac{e_o}{R_2} - C \frac{d(e_o)}{dt}$$



## 4. Propiedades Ideales del Amplificador Operacional

- Ganancia de voltaje infinita.
- Impedancia de entrada infinita.
- Impedancia de salida cero.
- Ancho de banda infinito.
- Respuesta instantánea (sin retardo).

### Realimentación en Amplificadores

- **Realimentación negativa:** 
  - Se toma parte de la salida y se regresa a la entrada inversora.
  - Estabiliza el circuito y define la ganancia de manera precisa.
- **Realimentación positiva:** 
  - Se toma parte de la salida y se regresa a la entrada no inversora.
  - Se utiliza para crear osciladores y comparadores.

### **Idealidad en los Amplificadores Operacionales**

**Ganancia de Lazo Abierto Infinita** $$(\(A_{OL} \to \infty\))$$:
 - En la práctica, se asume que una diferencia de voltaje infinitesimal entre las entradas (+ y −) produce un voltaje de salida finito.

**Impedancia de Entrada Infinita**:
  - No consume corriente desde la fuente de entrada $$(\(i_+ = i_- = 0\))$$.

**Impedancia de Salida Cero**:
 - Puede entregar corriente ilimitada a la carga sin afectar el voltaje de salida.

**Ancho de Banda Infinito**:
 - Respuesta plana para todas las frecuencias (sin retrasos ni atenuación).

**Cero Ruido y Deriva**:
  - No introduce errores por temperatura o variaciones de fabricación.

## 5. Ejercicios

📚 # Ejemplo 1


![image](https://github.com/user-attachments/assets/42b3b0f6-9e36-405b-8ee3-23c9672b3909)

**Datos**

- $$\( E_1 = 2.5V \)$$
- $$\( R_1 = 470k\Omega \)$$
- $$\( R_2 = 180k\Omega \)$$
- $$\( R_L = 1k\Omega \)$$

**Fórmulas Utilizadas:**

- Amplificación del amplificador no inversor:
  $$V_o = V_i \left( 1 + \frac{R_f}{R_i} \right)$$

- Corriente:
  $$I = \frac{V}{R}$$

- Potencia:
  $$P = V \times I$$


$$V_{RL} = 2.5 \left( 1 + \frac{470k\Omega}{180k\Omega} \right)$$

$$V_{RL} = 2.5 \left( 1 + 2.6 \right)$$

$$V_{RL} = 2.5 \times 3.6$$

$$V_{RL} = 9V$$


$$I = \frac{V}{R}$$

$$I = \frac{9V}{1k\Omega} = 9mA$$

$$P_{RL} = V_{RL} \times I_{RL}$$

$$P_{RL} = 9V \times 9mA$$

$$P_{RL} = 0.081W = 81mW$$

---

📚 # Ejemplo 2

![image](https://github.com/user-attachments/assets/1641d882-0897-4a0a-a4b9-e60f39b40a31)

$$\ i_1 = i_2 \$$

$$\frac{v_i-0}{R_1}=\frac{v_0-v_1}{R_2}$$

$$\frac{v_0}{v_1} = \frac{R_1 + R_2}{R_1} = 1 + \frac{R_2}{R_1}$$

$$v_0 = \left( 1 + \frac{R_2}{R_1} \right) v_1$$


## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos.





