# Transformada de Laplace
## 1. Transformada de Laplace en Dinámica de Sistemas 
La dinámica de sistemas estudia la evolución de los sistemas en el tiempo, modelando su comportamiento mediante ecuaciones diferenciales. Un sistema se define como un conjunto de componentes interconectados que trabajan para alcanzar un objetivo. Si la salida depende de entradas pasadas, se dice que es un sistema dinámico; de lo contrario, es estático.

En este contexto, se utilizan modelos dinámicos basados en ecuaciones diferenciales para describir la evolución de las variables del sistema en función del tiempo. Existen sistemas lineales, que cumplen con el principio de superposición, y sistemas no lineales, que requieren técnicas de aproximación para su análisis.


## 2. Definiciones   
>🔑*Modelos Dinamico:* Son aquellos sistemas que varian conforme al tiempo, que son analizables desde la perspectiva matemática
  
>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
>🔑*Sistema lineal:* Cumple con el principio de superposición, es decir, la respuesta a una combinación de entradas es la suma de las respuestas individuales.
  
>🔑*Transformada de Laplace:* Método matemático que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia compleja.
  
## 3. Modelos dinámicos.
Un modelo dinámico es una representación matemática o conceptual de un sistema que describe cómo sus variables cambian con el tiempo. A diferencia de los modelos estáticos, que representan relaciones en un estado fijo.
  
Estos modelos son principales en diversas áreas como la ingeniería, la física, la biología, la economía y el control de sistemas, ya que permiten predecir y optimizar el desempeño de sistemas complejos.  
  
### 4. Derivada de una función  
  
La derivada de una función $$\( f(x) \)$$ mide la razón de cambio instantánea de la función con respecto a la variable independiente $$( x \)$$. Matemáticamente, se define como:  
  
$$f'(x) = \lim_{{h \to 0}} \frac{f(x + h) - f(x)}{h}\$$

Esto representa la pendiente de la recta tangente a la función en un punto dado.    
    
     
 **Ejemplo 1: Derivada de una función cuadrática**
Dada la función:
  
$$f(x) = x^2\$$  
  
Su derivada es:  
  
$$f'(x) = \frac{d}{dx} x^2 = 2x\$$

**Cálculo en puntos específicos:**
- $$\ f'(2) = 2(2) = 4 \$$
- $$\ f'(3) = 2(3) = 6 \$$
- $$\ f'(0) = 2(0) = 0 \$$


### 4.1. Modelos de ecuaciones Diferenciales.  
**Modelos de Ecuaciones Diferenciales**  
  
Las ecuaciones diferenciales describen el comportamiento de sistemas dinámicos mediante la relación entre una función y sus derivadas. Son fundamentales en el estudio de sistemas físicos, control de procesos y modelado matemático.  
      
Una ecuación diferencial ordinaria (EDO) tiene la forma:  
  
$$a_n \frac{d^n F}{dt^n} + a_{n-1} \frac{d^{n-1} F}{dt^{n-1}} + \dots + a_1 \frac{dF}{dt} + a_0 F = u(t)$$  

Donde:
- $$\ F(t) \$$ es la salida del sistema.  
- $$\ u(t) \$$ es la entrada del sistema.  
- $$\ a_n, a_{n-1}, \dots, a_0 \$$ son coeficientes constantes o funciones de $$\( t \)$$.  
  
  
### 4.2 Influencia de parámetros
Los parámetros de un sistema determinan su respuesta ante cambios en las condiciones iniciales o entradas externas. Estos comportamientos pueden ser:

Comportamiento Sinusoidal: El sistema oscila de manera regular sin pérdida de energía, común en circuitos eléctricos sin pérdidas y sistemas mecánicos ideales.  
Decaimiento Exponencial: La respuesta disminuye gradualmente debido al amortiguamiento, hasta que el sistema alcanza el equilibrio, típico en circuitos con resistencias altas y sistemas con amortiguadores.  
Combinación de Oscilación y Decaimiento: Se observa cuando el sistema oscila inicialmente, pero la amplitud de las oscilaciones disminuye progresivamente hasta estabilizarse, común en sistemas con amortiguamiento moderado.  



### 4.3. Transformada de laplace
Es un cambio de función de variable real a una función de variable compleja. La transformada de laplace muestra las señales 
senosiudales y exponenciales  
$$x(t) - X(s)$$  
- Transformada inversa  
$$X(s) - x(t)$$  
- Transformada de una función   
$$l{f(t)} = F(s)$$  
- Transformada de la derivada  
$$L{f′(t)}=sL{f(t)}−f(0)$$  
L denota la Transformada de Laplace.  
𝑠 es la variable compleja de la transformada de Laplace.  
𝑓(0) es el valor de la función en 𝑡=0.  

#### 4.2. Descomposición en fracciones parciales.
# **Descomposición en Fracciones Parciales**

Dada la siguiente fracción:  

$$\[\frac{2s^2 - 4}{(s+1)(s-2)(s-3)} = \frac{A}{s+1} + \frac{B}{s-2} + \frac{C}{s-3}\]$$  

Multiplicamos por el denominador común para cancelar fracciones:  

$$\[2s^2 - 4 = A(s-2)(s-3) + B(s+1)(s-3) + C(s+1)(s-2)\]$$

Paso 2: Sustituimos valores para encontrar \( A, B, C \)**

Para $$\( s = 2 \)$$:  

$$\[2(4) - 4 = B(2+1)(2-3)\]$$  

$$\[8 - 4 = B(3)(-1)\]$$

$$\[4 = -3B\]$$

$$\[B = -\frac{4}{3}\]$$

Para $$\( s = 3 \)$$:


$$\[2(9) - 4 = C(4)(1)\]$$

$$\[18 - 4 = 4C\]$$

$$\[14 = 4C\]$$

$$\[C = \frac{7}{2}\]$$



Para $$\( s = -1 \)$$:

$$\[2(-1)^2 - 4 = A(-1-2)(-1-3)\]$$

$$\[2 - 4 = A(-3)(-4)\]$$

$$\[-2 = 12A\]$$

$$\[A = -\frac{1}{6}\]$$


Sustituyendo los valores de \( A, B, C \):

$$\[\frac{2s^2 - 4}{(s+1)(s-2)(s-3)} = \frac{-1/6}{s+1} + \frac{-4/3}{s-2} + \frac{7/2}{s-3}\]$$



## 5. Ejemplos
💡Ejemplo Sencillo de la Transformada de Laplace  

Dada la función:  

$$\[f(t) = e^{-3t}, \quad t \geq 0\]$$  

Aplicamos la definición de la Transformada de Laplace:  

$$\[F(s) = \int_0^{\infty} e^{-3t} e^{-st} dt\]$$  

Reescribimos la ecuación:  

$$\[F(s) = \int_0^{\infty} e^{-(s+3)t} dt\]$$  

Usamos la propiedad de la integral:  

$$\[\int_0^{\infty} e^{-at} dt = \frac{1}{a}, \quad \text{para } a > 0\]$$  

Donde $$\( a = s + 3 \)$$, entonces:  

$$\[F(s) = \frac{1}{s + 3}, \quad \text{para } s > -3\]$$  

Resultado:  

$$\[\mathcal{L} \{ e^{-3t} \} = \frac{1}{s + 3}\]$$  



## 6. Ejercicios
📚 # Ejemplo 1

Dada la siguiente fracción racional:  

$$\frac{3s^2 + 5s - 2}{(s+2)(s-1)(s-4)} = \frac{A}{s+2} + \frac{B}{s-1} + \frac{C}{s-4}$$  

    


Multiplicamos ambos lados por el denominador común para cancelar las fracciones:  

$$3s^2 + 5s - 2 = A(s-1)(s-4) + B(s+2)(s-4) + C(s+2)(s-1)$$  



Paso 2: Sustitución de valores para encontrar \( A, B, C \)  

Para $$\( s = -2 \)$$:  

$$3(-2)^2 + 5(-2) - 2 = A(-2-1)(-2-4)$$  

$$3(4) + (-10) - 2 = A(-3)(-6)$$  

$$12 - 10 - 2 = A(18)$$  

$$0 = 18A$$  

$$A = 0$$  



Para $$\( s = 1 \)$$:  

$$3(1)^2 + 5(1) - 2 = B(1+2)(1-4)$$  

$$3(1) + 5(1) - 2 = B(3)(-3)$$  

$$3 + 5 - 2 = -9B$$  

$$6 = -9B$$  

$$B = -\frac{2}{3}$$  



Para $$\( s = 4 \)$$:  

$$3(4)^2 + 5(4) - 2 = C(4+2)(4-1)$$  

$$3(16) + 20 - 2 = C(6)(3)$$  

$$48 + 20 - 2 = 18C$$  

$$66 = 18C$$  

$$C = \frac{11}{3}$$  



Sustituyendo los valores de $$\( A, B, C \)$$:  

$$\frac{3s^2 + 5s - 2}{(s+2)(s-1)(s-4)} = \frac{0}{s+2} + \frac{-2/3}{s-1} + \frac{11/3}{s-4}$$  

Simplificando:  

$$\frac{3s^2 + 5s - 2}{(s+2)(s-1)(s-4)} = -\frac{2}{3(s-1)} + \frac{11}{3(s-4)}$$  

---

📚 # Ejemplo 2:

Dada la siguiente fracción racional:

$$\frac{4s^2 + 7s + 5}{(s+3)(s-2)(s-5)} = \frac{A}{s+3} + \frac{B}{s-2} + \frac{C}{s-5}$$  


Multiplicamos ambos lados por el denominador común para cancelar las fracciones:  
  
$$4s^2 + 7s + 5 = A(s-2)(s-5) + B(s+3)(s-5) + C(s+3)(s-2)$$  


Paso 2: Sustitución de valores para encontrar \( A, B, C \)**  

Para $$\( s = -3 \)$$:  
  
$$4(-3)^2 + 7(-3) + 5 = A(-3-2)(-3-5)$$  

$$4(9) - 21 + 5 = A(-5)(-8)$$  

$$36 - 21 + 5 = A(40)$$  

$$20 = 40A$$  

$$A = \frac{1}{2}$$  

Para $$\( s = 2 \)$$:  
  
$$4(2)^2 + 7(2) + 5 = B(2+3)(2-5)$$  

$$4(4) + 14 + 5 = B(5)(-3)$$  

$$16 + 14 + 5 = -15B$$  

$$35 = -15B$$  

$$B = -\frac{7}{3}$$  


Para $$\( s = 5 \)$$:

$$4(5)^2 + 7(5) + 5 = C(5+3)(5-2)$$  

$$4(25) + 35 + 5 = C(8)(3)$$  

$$100 + 35 + 5 = 24C$$  

$$140 = 24C$$  

$$C = \frac{35}{6}$$  



Resultado Final
Sustituyendo los valores de \( A, B, C \):  

$$\frac{4s^2 + 7s + 5}{(s+3)(s-2)(s-5)} = \frac{1/2}{s+3} + \frac{-7/3}{s-2} + \frac{35/6}{s-5}$$  

Simplificando:

$$\frac{4s^2 + 7s + 5}{(s+3)(s-2)(s-5)} = \frac{1}{2(s+3)} - \frac{7}{3(s-2)} + \frac{35}{6(s-5)}$$  




## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos. En el contexto de la Transformada de Laplace, permite encontrar la transformada inversa de manera más sencilla, dividiendo expresiones complejas en términos más simples.  



