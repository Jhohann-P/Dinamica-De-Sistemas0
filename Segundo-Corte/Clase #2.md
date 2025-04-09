# Sistemas Dinámicos

Un **sistema dinámico** es un modelo matemático que describe cómo evoluciona un sistema físico, biológico, económico, etc., a lo largo del tiempo. Este comportamiento se expresa generalmente mediante ecuaciones diferenciales.  

Un sistema dinámico es aquel cuyo estado cambia con el tiempo, influenciado por condiciones iniciales y posibles entradas externas.  

## 2. Definiciones   
> 🔑 *Resorte:* Elemento mecánico que almacena energía elástica.

> 🔑 *Amortiguador:* Dispositivo que disipa energía mediante fricción viscosa, oponiéndose al movimiento.

> 🔑 *Sistema masa-resorte-amortiguador:* Sistema mecánico clásico formado por una masa, un resorte y un amortiguador. 

> 🔑 *Fricción en seco:* Fuerza que se opone al movimiento relativo entre dos superficies sin lubricación.

> 🔑 *Fricción estática:* Tipo de fricción en seco que impide el inicio del movimiento.

> 🔑 *Fricción cinética:* También llamada fricción de deslizamiento, actúa cuando ya hay movimiento.

## 3 Clasificación de los Sistemas Dinámicos

### Según la linealidad
- **Lineales**: Su comportamiento puede analizarse mediante superposición. Ejemplo: sistemas eléctricos con resistencias, inductancias y capacitores lineales.  
- **No lineales**: No cumplen el principio de superposición. Su análisis suele ser más complejo. Ejemplo: péndulo con grandes desplazamientos.  

### Según la variación de parámetros
- **Estacionarios (o invariantes en el tiempo)**: Sus parámetros no cambian con el tiempo.  
- **No estacionarios (o variantes en el tiempo)**: Sus parámetros cambian con el tiempo.  

### Según la respuesta
- **Estables**: Retornan a su estado de equilibrio ante perturbaciones.  
- **Inestables**: Se alejan de su estado de equilibrio ante perturbaciones.  

## 4. Ejemplos de Sistemas Dinámicos

## Resorte

Un **resorte** ideal se modela como un sistema lineal donde la fuerza aplicada es directamente proporcional al desplazamiento desde una posición de equilibrio. Este comportamiento se basa en la **Ley de Hooke**.  

### Ecuación del resorte:

$$F = kx = k(x_1 - x_2)$$  

F: Fuerza ejercida por el resorte.  

k: Constante del resorte (rigidez).  

$$x_1, x_2$$: Posiciones de los extremos del resorte.  

Siempre se debe mantener el mismo marco de referencia.  

#### Tipos de resortes según rigidez:  
Resorte duro: Tiene una pendiente más pronunciada en la curva fuerza-desplazamiento.  

Resorte lineal: Tiene una relación lineal ideal entre fuerza y desplazamiento.  

Resorte suave: Tiene una pendiente menor, ofreciendo menos resistencia.  

Nota: Se asumen resortes lineales, donde la fuerza externa aplicada y el desplazamiento están relacionados por una constante de proporcionalidad.  

## Amortiguador

Un amortiguador es un dispositivo que disipa energía en un sistema mecánico. Modela fuerzas resistivas proporcionales a la velocidad relativa entre sus extremos.  

### Ecuación del amortiguador
$$F = b \dot{x} = b \left( \dot{x}_1 - \dot{x}_2 \right)$$  

F: Fuerza de amortiguamiento.  

b: Constante de fricción viscosa o coeficiente de amortiguamiento.  

$$\dot{x}_1, \dot{x}_2$$: Velocidades de los extremos del amortiguador.  

Características del amortiguador:  
Comportamiento lineal, proporcional a la velocidad de desplazamiento.  
Este principio también se utiliza para representar la fricción entre una masa y una superficie.  

## Sistema Masa-Resorte-Amortiguador (combinado)
Al combinar un resorte y un amortiguador con una masa, se obtiene un sistema clásico utilizado para modelar vibraciones mecánicas.  

### Ecuación del sistema masa-resorte-amortiguador:

$$m \ddot{x} + b \dot{x} + kx = 0$$  

m: Masa del cuerpo.  

$$\ddot{x}$$: Aceleración.  

$$\dot{x}$$: Velocidad.  

x: Desplazamiento.  

b: Coeficiente de amortiguamiento.  

k: Constante del resorte.  


## 5 Fricción en Seco

La fricción en seco es una fuerza que se opone al movimiento relativo entre dos superficies en contacto sin lubricación. Esta fricción es causada por la interacción de las asperezas microscópicas entre las superficies, y depende del tipo de materiales, la rugosidad, y la fuerza normal que las mantiene unidas.

Existen tres tipos principales de fricción en seco:

### 1. Fricción Estática

La fricción estática es la fuerza que evita que un objeto comience a moverse cuando se aplica una fuerza externa.

#### Características:

- Ocurre antes de que comience el movimiento.
- Si la fuerza aplicada excede este valor, el cuerpo comienza a moverse.
  
### 2. Fricción Cinética 

Una vez que el objeto comienza a moverse, entra la fricción cinética, también conocida como fricción de deslizamiento.

#### Características:

- Actúa durante el movimiento relativo entre superficies.
- Tiene un valor constante en movimiento a velocidad constante.

### 3. Fricción por Rodamiento

La fricción por rodamiento aparece cuando un objeto rueda sobre una superficie, como una rueda o una bola.

#### Características:

- Es mucho menor que la fricción de deslizamiento.
- Muy importante en el diseño de mecanismos con ruedas y rodamientos.

  


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
