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


## 5. Ejemplos
💡Ejemplo 1: Transformada de inversa de Laplace  
x''+4x=0            x(0) = 5 ; x'(0)=0  
Donde: x'' = S^2X(s)-sX(0)-X'(0)  
       4x  = 4(X)s  
s^2X(s)-sX(0)-X'(0) + 4(X)s=0  
s^2X(s)-5s+ 4(X)s=0  
X(s)[s^2+4] = 5s  
X(s)=(5s)/(S^2+4)  
5L^-1{s/s^2+2^2}  
5Cos(2t)  
MATLAB:  
![MATLAB](images/plantilla/Clase2(1).JPG)



## 7. Ejercicios
📚 Transformada de Laplace:  
### Ejercicio 1: Transformada de Laplace de $$\( f(t) = t^2 e^{3t} \)$$

Calcular la transformada de Laplace de $$\( f(t) = t^2 e^{3t} \)$$.

$$\[\mathcal{L}\{f(t)\} = \int_0^\infty f(t) e^{-st} dt\]$$

Sabemos que:

$$\[\mathcal{L}\{t^n e^{at}\} = \frac{n!}{(s - a)^{n+1}}, \quad \text{para} \quad \Re(s) > a\]$$

Aplicamos con \( n = 2 \) y \( a = 3 \):

$$\[\mathcal{L}\{t^2 e^{3t}\} = \frac{2!}{(s - 3)^3}\]$$

Por lo tanto:

$$\[\mathcal{L}\{t^2 e^{3t}\} = \frac{2}{(s - 3)^3}\]$$

📚 Transformada de laplace:  
### Ejercicio 2: Transformada de Laplace de \( f(t) = \sin(2t) \)

Calcular la transformada de Laplace de $$\( f(t) = \sin(2t) \)$$

Sabemos que:

$$\[\mathcal{L}\{\sin(at)\} = \frac{a}{s^2 + a^2}\]$$

Aplicamos con \( a = 2 \):

$$\[\mathcal{L}\{\sin(2t)\} = \frac{2}{s^2 + 2^2}\]$$

Por lo tanto:

$$\[\mathcal{L}\{\sin(2t)\} = \frac{2}{s^2 + 4}\]$$


## 6. Conclusiones
Se llevaron a cabo las bases matematicas para la resolución de problemas, siendo asi como la solución de ecuaciones diferenciales por el uso de transformada de laplace. Se realizaron ejercicios explicativos y ejercicios de aprendizaje
