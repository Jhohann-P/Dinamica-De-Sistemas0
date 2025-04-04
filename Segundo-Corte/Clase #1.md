# Correcion del parcial
## 1. Transformada de Laplace y Fracciones parciales en Dinámica de Sistemas 
La dinámica de sistemas estudia la evolución de los sistemas en el tiempo, modelando su comportamiento mediante ecuaciones diferenciales. Un sistema se define como un conjunto de componentes interconectados que trabajan para alcanzar un objetivo. Si la salida depende de entradas pasadas, se dice que es un sistema dinámico; de lo contrario, es estático.

En este contexto, se utilizan modelos dinámicos basados en ecuaciones diferenciales para describir la evolución de las variables del sistema en función del tiempo. Existen sistemas lineales, que cumplen con el principio de superposición, y sistemas no lineales, que requieren técnicas de aproximación para su análisis.


## 2. Definiciones   
>🔑*Modelos Dinamico:* Son aquellos sistemas que varian conforme al tiempo, que son analizables desde la perspectiva matemática
  
>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
>🔑*Sistema lineal:* Cumple con el principio de superposición, es decir, la respuesta a una combinación de entradas es la suma de las respuestas individuales.
  
>🔑*Transformada de Laplace:* Método matemático que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia compleja.
  
## 3. Ejercicio de parcial #1.
$$
x'' + 4x = 5 \quad\quad x(0) = 5 \quad;\quad x'(0) = 0
$$

Aplicamos transformada de Laplace:

$$
s^2X(s) - sX(0) - X'(0) + 4X(s) = \frac{5}{s}
$$

Reescribiendo y cancelando términos:

$$
s^2X(s) - 5s + 4X(s) = \frac{5}{s}
$$

$$
X(s)(s^2 + 4) = \frac{5}{s} + 5s
$$

$$
X(s) = \frac{5s^2 + 2}{s(s^2 + 4)}
$$

Aplicando fracciones parciales:

$$
\frac{5s^2 + 2}{s(s^2 + 4)} = \frac{A}{s} + \frac{Bs + C}{s^2 + 4}
$$

Multiplicando ambos lados por $$\( s(s^2 + 4) \):$$

$$
5s^2 + 2 = A(s^2 + 2) + (Bs + C)(s)
$$

$$
5s^2 + 2 = As^2 + 4A + Bs^2 + Cs
$$

Agrupando términos:

$$
5s^2 + 2 = (A + B)s^2 + Cs + 4A
$$

Igualando coeficientes:

- \( A + B = 5 \)
- \( C = 0 \)
- $$\( 4A = 2 \Rightarrow A = \frac{1}{2} \)$$

Entonces:

$$S= \frac{1}{2} + B$$
$$\frac{10}{2} - \frac{1}{2} = B$$
$$B = \frac{9}{2}$$

Sustituyendo en las fracciones parciales:

$$
X(s) = \frac{\frac{1}{2}}{s} + \frac{\frac{9}{2}s}{s^2+4}
$$

Aplicando la transformada inversa de Laplace:

$$
x(s) = \frac{1}{2} \mathcal{L}^{-1} \left( \frac{1}{s} \right) + \frac{9}{2} \mathcal{L}^{-1} \left( \frac{s}{s^2 + 4} \right)
$$


Entonces:

$$x(s) = \frac{1}{2} + \frac{9}{2} \cos(2t)$$

## 4. Ejercicio de parcial #2.
$$
F(s) = \frac{5(s + 2)}{s^2(s^2 - 4s + 8)}
$$

Verificamos si trae raiz imaginaria: 

$$\frac{-b\pm \sqrt{b^2-4ac}}{2a}$$

$$\frac{4\pm \sqrt{16-4(1)(8)}}{2}$$

$$\frac{4\pm \sqrt{16-32}}{2}$$

Raices imaginarias

$$\frac{4\pm \sqrt{-16}}{2}$$

$$\frac{4\pm \sqrt{16i}}{2}$$

$$\frac{2\pm \sqrt{4i}}{2}$$

Donde:
$$2\pm 2i$$

$$F(s) = \frac{5(s + 2)}{s^2(s^2 - 4s + 8)}$$

Realizando sustitución de la ecuación original con fracciones parciales:

$$5(s+2) = \frac{A}{s^2} + \frac{B}{s} + \frac{Cs+D}{s^2-4s+8}$$   

Realizando sustitución:

$$5(s+2) = A(s^2-4s+8)+ B(s)(s^2-4s+8)+cs+d(s^2)$$

## Fracciones parciales de:

$$
\frac{5(s+2)}{s^2(s^2 - 4s + 8)}
$$

### Forma general de la descomposición:

$$
\frac{5(s+2)}{s^2(s^2 - 4s + 8)} = \frac{A}{s} + \frac{B}{s^2} + \frac{Cs + D}{s^2 - 4s + 8}
$$

Multiplicamos ambos lados por el denominador común $$\( s^2(s^2 - 4s + 8) \)$$:

$$
5(s + 2) = A s(s^2 - 4s + 8) + B(s^2 - 4s + 8) + (Cs + D)s^2
$$

### Expandimos cada término:

**1.** $$\( A s(s^2 - 4s + 8) = A(s^3 - 4s^2 + 8s) \)$$

**2.** $$\( B(s^2 - 4s + 8) = B s^2 - 4B s + 8B \)$$

**3.** $$\( (Cs + D)s^2 = Cs^3 + Ds^2 \)$$

Sumamos todos los términos del lado derecho:

$$
(A + C)s^3 + (-4A + B + D)s^2 + (8A - 4B)s + 8B
$$

Igualamos con el lado izquierdo:

$$
5s + 10
$$

### Igualando coeficientes:

$$
\begin{aligned}
s^3: &\quad A + C = 0 \\
s^2: &\quad -4A + B + D = 0 \\
s^1: &\quad 8A - 4B = 5 \\
s^0: &\quad 8B = 10
\end{aligned}
$$

### Resolviendo el sistema:

De la última ecuación:

$$
8B = 10 \Rightarrow B = \frac{5}{4}
$$

Luego:

$$
8A - 4B = 5 \Rightarrow 8A - 4\cdot\frac{5}{4} = 5 \Rightarrow 8A - 5 = 5 \Rightarrow A = \frac{10}{8} = \frac{5}{4}
$$

Ahora:

$$
A + C = 0 \Rightarrow C = -\frac{5}{4}
$$

Y finalmente:

$$
-4A + B + D = 0 \Rightarrow -4\cdot\frac{5}{4} + \frac{5}{4} + D = 0 \Rightarrow -5 + \frac{5}{4} + D = 0
$$

$$
D = 5 - \frac{5}{4} = \frac{15}{4}
$$



### Resultado final:

Los coeficientes son:

- $$\( A = \frac{5}{4} \)$$
- $$\( B = \frac{5}{4} \)$$
- $$\( C = -\frac{5}{4} \)$$
- $$\( D = \frac{15}{4} \)$$



Fracción parcial completa:

$$
\frac{5(s+2)}{s^2(s^2 - 4s + 8)} = \frac{5}{4s} + \frac{5}{4s^2} + \frac{-\frac{5}{4}s + \frac{15}{4}}{s^2 - 4s + 8}
$$


La función a transformar es:

$$
\frac{5}{4s} + \frac{5}{4s^2} + \frac{-\frac{5}{4}s + \frac{15}{4}}{s^2 - 4s + 8}
$$



**Paso 1: Primer término**

$$
\mathcal{L}^{-1}\left(\frac{5}{4s}\right) = \frac{5}{4}
$$



**Paso 2: Segundo término**

$$
\mathcal{L}^{-1}\left(\frac{5}{4s^2}\right) = \frac{5}{4}t
$$


**Paso 3: Tercer término**

Completemos el trinomio:

$$
s^2 - 4s + 8 = (s - 2)^2 + 4
$$

Reescribimos el numerador:

$$
\frac{-\frac{5}{4}s + \frac{15}{4}}{(s - 2)^2 + 4}
= \frac{-\frac{5}{4}(s - 2) + \frac{5}{4}}{(s - 2)^2 + 4}
$$

Separando:

$$
\frac{-\frac{5}{4}(s - 2)}{(s - 2)^2 + 4} + \frac{\frac{5}{4}}{(s - 2)^2 + 4}
$$

Aplicando la transformada inversa:

$$
\mathcal{L}^{-1}\left(\frac{-\frac{5}{4}(s - 2)}{(s - 2)^2 + 4}\right) = -\frac{5}{4}e^{2t} \cos(2t)
$$

$$
\mathcal{L}^{-1}\left(\frac{\frac{5}{4}}{(s - 2)^2 + 4}\right) = \frac{5}{8}e^{2t} \sin(2t)
$$



**Resultado final:**

$$
\mathcal{L}^{-1}\left( \frac{5}{4s} + \frac{5}{4s^2} + \frac{-\frac{5}{4}s + \frac{15}{4}}{s^2 - 4s + 8} \right)
= \frac{5}{4} + \frac{5}{4}t - \frac{5}{4}e^{2t} \cos(2t) + \frac{5}{8}e^{2t} \sin(2t)
$$


## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos. En el contexto de la Transformada de Laplace, permite encontrar la transformada inversa de manera más sencilla, dividiendo expresiones complejas en términos más simples.  




