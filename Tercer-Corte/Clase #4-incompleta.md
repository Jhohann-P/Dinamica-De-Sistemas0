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

### Ejemplo 1: 

![image](https://github.com/user-attachments/assets/ef61deca-526a-402b-98b6-1b25cd5b79c4)

Para solucionar este ejercicio, realizamos 1/s * 10/s+5

$$\frac{1}{s} \cdot \frac{10}{s + 5} = \frac{10}{s(s + 5)}\$$
$$\frac{10}{s^2 + 5s}\$$

realizando nuevamente el esquema, nos daría:    

![image](https://github.com/user-attachments/assets/16d5afdd-debf-4679-8948-21c5c37c1893)    

realizando nuevamente mediante las reglas de bloques, tendriamos que: 

$$\frac{\frac{10}{s^2 + 5s}}{1 + \frac{10}{s^2 + 5s} \cdot \frac{1}{s + 2}}$$

## Paso 1: Factorizar

Factorizamos el denominador $$\(s^2 + 5s\)$$:

$$
s^2 + 5s = s(s + 5)
$$

Entonces la expresión queda:

$$
\frac{\frac{10}{s(s + 5)}}{1 + \frac{10}{s(s + 5)} \cdot \frac{1}{s + 2}}
$$

Paso 2: Multiplicación en el denominador

Multiplicamos las fracciones del segundo término del denominador:

$$
\frac{10}{s(s + 5)} \cdot \frac{1}{s + 2} = \frac{10}{s(s + 5)(s + 2)}
$$

 Paso 3: Sumar fracciones

Expresamos el 1 como fracción con el mismo denominador:

$$
1 = \frac{s(s + 5)(s + 2)}{s(s + 5)(s + 2)}
$$

Entonces:

$$
1 + \frac{10}{s(s + 5)(s + 2)} = \frac{s(s + 5)(s + 2) + 10}{s(s + 5)(s + 2)}
$$

Paso 4: Reescribir la expresión

Sustituimos todo en la expresión original:

$$
\frac{\frac{10}{s(s + 5)}}{\frac{s(s + 5)(s + 2) + 10}{s(s + 5)(s + 2)}}
$$

Multiplicamos por el recíproco:

$$
= \frac{10}{s(s + 5)} \cdot \frac{s(s + 5)(s + 2)}{s(s + 5)(s + 2) + 10}
$$

Simplificamos \(s(s + 5)\) en numerador y denominador:

$$
= \frac{10(s + 2)}{s(s + 5)(s + 2) + 10}
$$



Paso 5: Expandir el denominador

Primero expandimos:

$$
(s + 5)(s + 2) = s^2 + 7s + 10
$$

Luego:

$$
s(s^2 + 7s + 10) = s^3 + 7s^2 + 10s
$$

Sumamos el 10 final:

$$
s^3 + 7s^2 + 10s + 10
$$


## Resultado final

$$
\frac{10(s + 2)}{s^3 + 7s^2 + 10s + 10} = \frac{10s + 20}{s^3 + 7s^2 + 10s + 10}
$$

![image](https://github.com/user-attachments/assets/7666643c-c501-419a-8393-1eb45dd9928f)

---

### Ejemplo 2: 

![image](https://github.com/user-attachments/assets/af6864d8-e9f2-4e04-a43c-d71ae5191203)  

Buscaremos reducir g3 y g2 dandonos como resultado una suma, y eliminando el producto suma de al lado de g2
dandonos el siguiente resultado:

![image](https://github.com/user-attachments/assets/9549efa4-5f73-44f2-be15-4f89e664ffe0)

ahora g1 lo multiplicador por g2 y g3, uniendo directamente, ademas g5 lo dividiremos en ambas partes como regla o distribucion de bloques  

![image](https://github.com/user-attachments/assets/a2431223-2000-45c5-ac04-d496b570ed28)  

ahora, multiplicaremois g4 * g5 ya que estaria directo y lo uniremos con g3, dandonos una multiplicacion directa, y el g5 de la parte inferior, lo multiplicamos 1/ 1 + g5, dandonos como resultado lo siguiente:  

![image](https://github.com/user-attachments/assets/0c64da24-4118-4e94-866f-90372221900e)  






## 8. Ejercicios

## 1. Clasificación de funciones de transferencia
📚 # Ejemplo 1: 


---  


📚 # Ejemplo 2: 

  


## **Conclusión**
La función de transferenciaaes una herramienta fundamental para analizar y diseñar sistemas de control, ya que simplifica el estudio de sistemas dinámicos en el dominio de la frecuencia. Conocer los polos, ceros y el orden del sistema ayuda a entender su comportamiento y estabilidad.  Además, el teorema del valor final es útil para predecir la respuesta a largo plazosin resolver la ecuación diferencial completa.  Estas herramientas facilitan la modelación y el control de sistemas en ingenier+ia.
