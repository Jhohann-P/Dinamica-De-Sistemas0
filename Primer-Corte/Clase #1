# Transformada de Laplace
## 1. Conceptos Fundamentales  
La Transformada de Laplace es una herramienta matemática que convierte una función de una variable real, generalmente el tiempo 
t, en una función de una variable compleja  
s. Es ampliamente utilizada en la resolución de ecuaciones diferenciales lineales, sistemas de control, circuitos eléctricos y análisis de señales  

## 2. Definiciones   
>🔑*Modelos Dinamico:* Son aquellos sistemas que varian conforme al tiempo, que son analizables desde la perspectiva matemática  
>🔑*Sistemas lineas y no lineales:* Se considera un sistema lineal siempre y cuando cumpla con las reglas de un circuito de superposición,.  

## 3. Modelos dinámicos.
Encontrar funciones que determinan el tiempo de una variable o su cambio.
### Derivada de una función

La derivada de una función $f(t)$ con respecto a $t$ se denota como:  
$$\frac{df(t)}{dt}$$  
Recordando que la derivada es la pendiente de una curva, tomamos un ejemplo:  
F(x) = x^2  
La derivada de esta función es:  
F'(x) = 2x  
F'(2) = 4  
F'(3) = 6  
### 3.1. Modelos de ecuaciones Diferenciales.  
$$a1 d^2F/dt`2 + a2 df/dt + a3f= u(t)$$  
Donde la solución se convierte en un función, en este caso función de (t)  
### 3.2. Transformada de laplace
Es un cambio de función de variable real a una función de variable compleja. La transformada de laplace muestra las señales 
senosiudales y exponenciales  
x(t) - X(s)  
- Transformada inversa  
X(s) - x(t)  
- Transformada de una función   
$$l{f(t)} = F(s)$$  
- Transformada de la derivada  
$$L{f′(t)}=sL{f(t)}−f(0)$$  
L denota la Transformada de Laplace.  
𝑠 es la variable compleja de la transformada de Laplace.  
𝑓(0) es el valor de la función en 𝑡=0.  
### 3.2. Evaluación del curso
Autoevaluación y coevaluación : 20%  
Parcial: 40%  
Tareas: 30%  
Apuntes: 10%  
  -Plantilla.  
  -2 Ejercicios.  
  -Github.  
### 3.3. Matlab
Es un computo de programación númerico, el cual ofrece distintas tareas conforme a la programación matematica, su nombre se deriva de MATrix LABoratory o Laboratorio de matrices).  
Su sistema se maneja mediante lenguaje de programación unico o propio "Lenguaje M",
Figura 1.
## 4. Ejemplos
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



## 5. Código
>> A = [7 8 2; 3 2 6; 5 9 4];  
>> determinant_A = det(A);  
>> disp(determinant_A);  
  -144  

>> B = [1 5 2; 6 7 9; 4 7 3];  
>> inverse_B = inv(B);  
>> disp(inverse_B);  
   -0.5526   -0.0132    0.4079  
    0.2368   -0.0658    0.0395  
    0.1842    0.1711   -0.3026  

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
