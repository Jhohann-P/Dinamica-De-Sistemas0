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

- **Lineales**: Su comportamiento puede analizarse mediante superposición. Ejemplo: sistemas eléctricos con resistencias, inductancias y capacitores lineales.  
- **No lineales**: No cumplen el principio de superposición. Su análisis suele ser más complejo. Ejemplo: péndulo con grandes desplazamientos.  

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
**Comportamiento lineal**, proporcional a la velocidad de desplazamiento.  
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
![image](https://github.com/user-attachments/assets/37ce6630-56b2-4009-ba83-f0f72627126e)



- $$\( F(t) \)$$: Fuerza externa aplicada hacia la derecha.
- $$\( F_r = -k x \)$$: Fuerza del resorte, que se opone al desplazamiento.
- $$\( F_c = -b \dot{x} \)$$: Fuerza del amortiguador (resistencia viscosa), que se opone a la velocidad.


Entonces, aplicando la Segunda Ley de Newton en la dirección del movimiento:

$$
\sum F = m \ddot{x}(t)
$$

$$
F(t) - b \dot{x}(t) - k x(t) = m \ddot{x}(t)
$$


Reorganizando términos:

$$
m \ddot{x}(t) + b \dot{x}(t) + k x(t) = F(t)
$$

Esta es la ecuación del sistema masa-resorte-amortiguador clásico, donde:

- $$\( \ddot{x} \)$$: Aceleración
- $$\( \dot{x} \)$$: Velocidad
- $$\( x \)$$: Desplazamiento
- $$\( m \)$$: Masa
- $$\( b \)$$: Coeficiente de amortiguamiento
- $$\( k \)$$: Constante del resorte


- $$\( x_1 = x(t) \)$$: Posición
- $$\( x_2 = \dot{x}(t) \)$$: Velocidad

Entonces el sistema se puede representar como:

$$
\dot{x}_1 = x_2
$$
$$
\dot{x}_2 = \frac{1}{m} \left( F(t) - b x_2 - k x_1 \right)
$$



## 6. Ejercicios
📚 # Ejemplo 1
![image](https://github.com/user-attachments/assets/bf960432-9c6c-4ed3-a562-194761de6ea9)

Para una masa \( m \) desplazándose horizontalmente, se tienen tres fuerzas actuando sobre ella:

### Fuerzas que actúan:
- $$\( F(t) \)$$: Fuerza externa aplicada hacia la derecha.  
- $$\( F_r = -kx \)$$: Fuerza del resorte, que se opone al desplazamiento.  
- $$\( F_c = -c\dot{x} \)$$: Fuerza del amortiguador (resistencia viscosa), que se opone a la velocidad.



$$
\sum F = m \ddot{x}(t)
$$

$$
F(t) - c \dot{x}(t) - k x(t) = m \ddot{x}(t)
$$



Reorganizando términos:

$$
m \ddot{x}(t) + c \dot{x}(t) + k x(t) = F(t)
$$

Esta es la ecuación del sistema masa-resorte-amortiguador clásico, donde:

- $$\( \ddot{x} \)$$: Aceleración  
- $$\( \dot{x} \)$$: Velocidad  
- $$\( x \)$$: Desplazamiento  
- $$\( m \)$$: Masa  
- $$\( c \)$$: Coeficiente de amortiguamiento  
- $$\( k \)$$: Constante del resorte  



### Variables de estado:

$$
x_1 = x(t) \quad \text{(posición)}, \quad x_2 = \dot{x}(t) \quad \text{(velocidad)}
$$

Entonces:

$$
\dot{x}_1 = x_2
$$

$$
\dot{x}_2 = \frac{1}{m} \left( F(t) - c x_2 - k x_1 \right)
$$


📚 # Ejemplo 2:

-![image](https://github.com/user-attachments/assets/59874cab-91d8-4d49-8f99-9ed23d5d9cd7)


Tenemos un sistema con dos masas $$\( m_1 \), \( m_2 \)$$ y tres resortes $$\( k_1 \), \( k_2 \), \( k_3 \)$$

- $$\( x_1(t) \): desplazamiento de la masa \( m_1 \)$$
- $$\( x_2(t) \): desplazamiento de la masa \( m_2 \)$$



### Para $$\( m_1 \)$$:
- $$\( -k_1 x_1 \)$$: resorte conectado a la pared izquierda
- $$\( -k_2(x_1 - x_2) \)$$: resorte entre $$\( m_1 \)$$ y $$\( m_2 \)$$

### Para \( m_2 \):
- $$\( -k_2(x_2 - x_1) \)$$: resorte entre $$\( m_2 \)$$ y $$\( m_1 \)$$
- $$\( -k_3 x_2 \)$$: resorte conectado a la pared derecha


### Para la masa \( m_1 \):

$$
m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0
$$

### Para la masa $$\( m_2 \)$$:

$$
m_2 \ddot{x}_2 - k_2 x_1 + (k_2 + k_3)x_2 = 0
$$




## **Conclusión**
El estudio de los sistemas dinámicos mecánicos, como el resorte, el amortiguador y las distintas formas de fricción, constituye una base fundamental para el análisis y modelado de sistemas físicos en ingeniería. Comprender cómo estas fuerzas interactúan permite establecer modelos precisos que describen el comportamiento real de estructuras, mecanismos y dispositivos sometidos a diversas condiciones de operación.


Asimismo, el uso de herramientas como la Transformada de Laplace permite llevar estos modelos al dominio de la frecuencia, facilitando su análisis y solución mediante técnicas algebraicas, lo cual es especialmente útil en la formulación de sistemas de control y en la resolución de problemas complejos de ingeniería.
