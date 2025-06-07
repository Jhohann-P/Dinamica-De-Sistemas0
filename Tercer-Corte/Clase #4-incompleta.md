# Algebra de bloques
Una herramienta fundamental para modelar y analizar la interacción entre sistemas dinámicos son los diagramas de bloques. Estas representaciones gráficas permiten visualizar de manera clara las relaciones entre diferentes componentes de un sistema y son especialmente útiles en el ámbito del Álgebra de Bloques.

## Fundamentos del Algebra de Bloques
Los diagramas de bloques permiten:
- Representar sistemas complejos mediante bloques interconectados
- Simplificar sistemas mediante reglas algebraicas específicas
- Analizar señales y sus transformaciones a través del sistema

## 2. Definiciones
> 🔑 *Diagrama de bloques:* Representación gráfica de un sistema dinámico donde los componentes se muestran como bloques interconectados por flechas que indican el flujo de señales. Permite visualizar y analizar la estructura del sistema.  

> 🔑 *Función de transferencia de un bloque:* Relación matemática entre la transformada de Laplace de la señal de salida y la de entrada de un bloque individual

> 🔑 *Punto de suma (comparador):* Elemento que realiza operaciones algebraicas (suma/resta) entre señales. Se representa con un círculo y símbolos +/- en sus entradas. Las señales deben tener mismas unidades.  

> 🔑 *Punto de ramificación:* Nodo donde una señal se divide para dirigirse a múltiples bloques o puntos de suma simultáneamente. 

> 🔑 *Álgebra de bloques:* Conjunto de reglas para simplificar diagramas complejos mediante operaciones como combinación de bloques en serie/paralelo o reducción de lazos de realimentación.  

> 🔑 *Realimentación unitaria:* Configuración donde la señal de salida se retroalimenta directamente (sin bloques adicionales) al punto de suma.


## 3.  Elementos de un diagrama de bloques

### 1. Flechas (Señales)
**Representación:**  
→ *Direccionalidad:*  
- Indican el flujo unidireccional de señales entre componentes  
- La punta que apunta al bloque = Entrada* 
- La punta que sale del bloque = Salida   

**Características clave:**  
- Modelan la propiedad unilateral de los sistemas de control  
- Transportan información de variables físicas (tensión, presión, temperatura, etc.)

![image](https://github.com/user-attachments/assets/e1837bcf-a14f-4eda-b65e-daa5010e0a8d)

### 2. Punto de Suma (Comparador)

Símbolo estándar:*
○ (Círculo con cruce interior)  

Funcionalidad:
- Opera algebraicamente señales mediante:  
  - Suma (+) 
  - Resta (−)  
- Configuración de signos:  
  + → Señal a sumar
  - → Señal a restar

  ![image](https://github.com/user-attachments/assets/a4c36c98-7c17-4c29-a2cf-b16822586988)
  
---

## 4. Interpretación Matemática de Bloques
*Relación entrada-salida:**  
Para un bloque con función de transferencia $$\( G(s) \)$$:

$$\[Y(s) = U(s) \cdot G(s)\]$$

Donde:  
- $$\( U(s) \)$$: Señal de entrada en dominio de Laplace  
- $$\( G(s) \)$$: Función de transferencia del bloque  
- $$\( Y(s) \)$$: Señal de resultado  

**Ejemplo:**  
Si $$\( G(s) = \frac{1}{s+2} \) y \( U(s) = \frac{1}{s} \)$$:  

$$\[Y(s) = \frac{1}{s} \cdot \frac{1}{s+2} = \frac{1}{s(s+2)}\]$$

### 1. Conexión de Bloques en Cascada

[U₁(s)] → [G₁(s)] →  [G₂(s)] → [Y₂(s)]

**Configuración:**  
Salida del primer bloque → Entrada del segundo bloque  

**Teorema:**  
La función de transferencia equivalente $$\( G_{eq}(s) \)$$ es el **producto** de las funciones individuales:

$$\[G_{eq}(s) = G_1(s) \cdot G_2(s)\]$$

[U₁(s)] → [G₁(s)] →  [G₂(s)] → [Y₂(s)]    
[U₁(s)] → [G₁(s)G₂(s)] → [Y₂(s)]



## 5. Solución Sistemática con Álgebra de Bloques
Las reglas de conexión en cascada permiten resolver problemas complejos paso a paso  

1. **Identificar bloques consecutivos** en la trayectoria de señal.  
2. **Multiplicar sus funciones de transferencia** (conservando el orden).  
3. **Simplificar el diagrama** reemplazando por un solo bloque equivalente.  
4. **Repetir** hasta obtener una función de transferencia total.  

*Ejemplo práctico:*  
Si un sistema tiene `[G₁(s)] → [G₂(s)] → [G₃(s)]`, su reducción es inmediata: 

$$\[G_{total}(s) = G_1(s) \cdot G_2(s) \cdot G_3(s)\]$$    

## 6.Imagenes o archivos necesarios
![image](https://github.com/user-attachments/assets/b177ec62-bc48-45ca-a542-935f694ad9f2)
![image](https://github.com/user-attachments/assets/e1eb0411-7f38-4e23-b714-a2dc8cae7ed0)


## 7. Ejemplos

### Ejemplo 1: Sistema con 2ceros y 2 polos



---

### Ejemplo 2: Sistema con un polo en el origen



## 8. Ejercicios

## 1. Clasificación de funciones de transferencia
📚 # Ejemplo 1: 


---  


📚 # Ejemplo 2: 

  


## **Conclusión**
La función de transferenciaaes una herramienta fundamental para analizar y diseñar sistemas de control, ya que simplifica el estudio de sistemas dinámicos en el dominio de la frecuencia. Conocer los polos, ceros y el orden del sistema ayuda a entender su comportamiento y estabilidad.  Además, el teorema del valor final es útil para predecir la respuesta a largo plazosin resolver la ecuación diferencial completa.  Estas herramientas facilitan la modelación y el control de sistemas en ingenier+ia.
