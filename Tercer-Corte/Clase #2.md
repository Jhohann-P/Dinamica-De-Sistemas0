# Funciones de transferencia
## 1.  Introducción a la Función de Transferencia

En la ingeniería de control, se utiliza una herramienta fundamental llamada **función de transferencia** para analizar sistemas dinámicos. Esta herramienta permite estudiar el comportamiento del sistema sin resolver directamente su ecuación diferencial.

Donde:
- $$G(s)$$: función de transferencia del sistema
- $$Y(s)$$: salida del sistema en el dominio de Laplace
- $$U(s)$$: entrada del sistema en el dominio de Laplace
- $$s$$: variable compleja usada en la transformada de Laplace



## 2. Definiciones   
>🔑*Transformada inversa de Laplace:* Se emplea para convertir funciones en el dominio de la frecuencia (s) al dominio del tiempo (t).  
  
> 🔑 *Función de transferencia:*  Es la relación matemática entre la transformada de Laplace de la salida y la entrada de un sistema, considerando condiciones iniciales nulas. Se utiliza para analizar sistemas dinámicos en el dominio de la frecuencia.

> 🔑 *Polos y ceros:* Los polos son los valores de \( s \) que hacen que la función de transferencia tienda a infinito (raíces del denominador), mientras que los ceros son los valores que anulan la función (raíces del numerador). La ubicación de polos y ceros determina la estabilidad y respuesta del sistema.

> 🔑 *Orden o grado de una función de transferencia:*  Corresponde al grado del polinomio característico (denominador). Indica la complejidad y el número de estados dinámicos del sistema.

> 🔑 *Teorema del valor final:*  Método para encontrar el valor límite de la salida de un sistema cuando el tiempo tiende a infinito, usando transformadas de Laplace, siempre que el sistema sea estable.


### Clasificación de las funciones de transferencia
#### 1. Función **Impropia**

- Condición: $$\( n > m \)$$
- El numerador tiene mayor grado que el denominador.
- Este tipo de función **no es físicamente realizable** directamente, ya que implica un sistema no causal.

**Ejemplo:**

$$G(s) = \frac{s^2 + 1}{s + 1}$$

- Numerador: grado 2  
- Denominador: grado 1  
**Clasificación**: Impropia


####  2. Función **Estrictamente Propia**

- Condición: \( n < m \)
- El denominador tiene mayor grado que el numerador.
- Este es el caso más común y **representa un sistema físicamente realizable y estable**.

**Ejemplo:**

$$G(s) = \frac{1}{s^2 + 1}$$

- Numerador: grado 0  
- Denominador: grado 2  
**Clasificación**: Estrictamente propia



#### 3. Función **Bipropia** (o simplemente Propia)

- Condición: \( n = m \)
- Numerador y denominador tienen el mismo grado.
- El sistema es **realizable**, aunque puede tener un comportamiento especial a altas frecuencias.

**Ejemplo:**

$$G(s) = \frac{s^2 - 1}{s^2 + 1}$$

- Numerador: grado 2  
- Denominador: grado 2  
**Clasificación**: Bipropia (propia)

### Polos y Ceros en Funciones de Transferencia

#### ¿Qué son los polos y ceros?

Dada una función de transferencia en forma racional:

$$G(s) = \frac{N(s)}{D(s)} = \frac{(s - z_1)(s - z_2)\dots(s - z_n)}{(s - p_1)(s - p_2)\dots(s - p_m)}$$

Donde:

- $$\( z_1, z_2, \dots, z_n \)$$ son los **ceros** del sistema.
- $$\( p_1, p_2, \dots, p_m \)$$ son los **polos** del sistema.
- $$\( N(s) \)$$: numerador, determina los ceros.
- $$\( D(s) \)$$: denominador, determina los polos.
- $$\( s \)$$: variable en el dominio de Laplace.


#### Importancia de los polos y ceros

- Los **polos** determinan la **estabilidad** y la **dinámica** del sistema (como su velocidad de respuesta y si oscila o no).
- Los **ceros** afectan la **forma de la respuesta** del sistema, pero no su estabilidad.
- La posición de polos y ceros en el plano complejo \( s \) es esencial para diseñar y analizar sistemas de control.


##  Ejemplos

### Ejemplo 1: Sistema con 2 ceros y 2 polos

$$G(s) = \frac{(s + 2)(s - 1)}{(s + 3)(s + 5)}$$

- **Ceros**: $$\( s = -2 \), \( s = 1 \)  $$
- **Polos**: $$\( s = -3 \), \( s = -5 \)$$

Sistema **estable** (todos los polos tienen parte real negativa).


### Ejemplo 2: Sistema con un polo en el origen

$$G(s) = \frac{5}{s(s + 2)}$$

- **Ceros**: ninguno explícito (numerador es constante)  
- **Polos**: $$\( s = 0 \), \( s = -2 \)$$

El polo en $$\( s = 0 \)$$ implica que el sistema es **tipo 1** y tiene una **respuesta lenta al inicio**.


### Grado de una Función de Transferencia

####  ¿Qué significa el orden de una función de transferencia?

El orden de una función de transferencia está determinado por el grado del polinomio del denominador es decir, el **número más alto de la variable $$\( s \)$$ que aparece en el denominador.


#### Ejemplo

Dada la siguiente función de transferencia:

$$G(s) = \frac{3s - 1}{s^2 + 3s + 2}$$

- El polinomio del denominador es $$\( s^2 + 3s + 2 \)$$
- El grado más alto de $$\( s \) es 2$$

Por lo tanto, se trata de una **función de segundo orden**.


##  ¿Por qué importa el orden?

El orden de un sistema indica:

- El **número de elementos dinámicos** (como integradores o acumuladores)
- La **complejidad** de su respuesta (rápida, lenta, oscilatoria, etc.)
- El número de **variables de estado** necesarias para describirlo



## 4. Ejercicios

## 1. Clasificación de funciones de transferencia
📚 # Ejemplo 1: 

$$G(s) = \frac{s^3 + 2s + 1}{s^2 + 4s + 5}$$

**Solución:**

- Grado del numerador: 3  
- Grado del denominador: 2  
- Como \( n > m \), la función es **impropia**.
  
-----

📚 # Ejemplo 2: 

  $$G(s) = \frac{2s + 3}{s^2 + 5s + 6}$$

**Solución:**

- Grado numerador: 1  
- Grado denominador: 2  
- Como \( n < m \), es **estrictamente propia** (también llamada propia).  

## 2. Polos y ceros
📚 # Ejemplo 1: 

$$G(s) = \frac{s^2 + 4s + 3}{s^2 + 2s + 1}$$

**Solución:**

- Ceros: raíces de $$\( s^2 + 4s + 3 = 0 \)$$
  
  $$s^2 + 4s + 3 = (s + 1)(s + 3) = 0 \implies s = -1, -3$$

- Polos: raíces de $$\( s^2 + 2s + 1 = 0 \)$$  

$$(s + 1)^2 = 0 \implies s = -1 \quad \text{(polo doble)}$$


---

📚 # Ejemplo 2: 

$$G(s) = \frac{5(s + 1)}{s(s + 3)(s + 4)}$$

**Solución:**

- Cero: raíz del numerador $$\( s + 1 = 0 \Rightarrow s = -1 \)$$  
- Polos: raíces del denominador:  

  $$s = 0, \quad s = -3, \quad s = -4$$

---

## 3. Grado de la función de transferencia

📚 # Ejemplo 1: 

$$G(s) = \frac{7s + 2}{s^3 + 6s^2 + 11s + 6}$$

**Solución:**

- Grado del denominador: 3  
- Por lo tanto, la función es de **tercer orden**.


## **Conclusión**
En resumen, la función de transferencia es una herramienta fundamental para analizar y diseñar sistemas de control, ya que simplifica el estudio de sistemas dinámicos en el dominio de la frecuencia. Conocer los polos, ceros y el orden del sistema ayuda a entender su comportamiento y estabilidad.  Además, el teorema del valor final es útil para predecir la respuesta a largo plazo sin resolver la ecuación diferencial completa.  Estas herramientas facilitan la modelación y el control de sistemas en ingeniería.
