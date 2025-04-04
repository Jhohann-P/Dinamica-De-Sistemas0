# Correcion del parcial
## 1. Transformada de Laplace y Fracciones parciales en Dinámica de Sistemas 
En Dinámica de Sistemas, la Transformada de Laplace se utiliza para transformar ecuaciones diferenciales del dominio del tiempo al dominio de la frecuencia (espacio s), donde es más fácil analizarlas y resolverlas algebraicamente.

Una vez obtenida la función de transferencia o la solución en el dominio de Laplace, se aplica la descomposición en fracciones parciales para simplificar la expresión. Esto permite utilizar tablas de transformadas inversas y regresar al dominio del tiempo con una expresión analítica clara de la respuesta del sistema.


## 2. Definiciones   
  
>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
>🔑*Fracciones Parciales:* Es una técnica algebraica que permite descomponer una fracción racional (cociente de dos polinomios) en una suma de fracciones más simples, lo cual facilita operaciones como la integración o la transformada inversa de Laplace.
  
>🔑*Transformada de Laplace:* Método matemático que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia compleja.
  
## 3. Parcial #1.
### Primer ejercicio del parcial #1
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

### Segundo ejercicio del parcial #1.
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

---

## 4. Parcial #2
### Primer ejercicio parcial  2

Dada la ecuación diferencial:

$$
2x'' + 2x' + x = 1 \quad \text{con condiciones iniciales} \quad x(0) = 0, \quad x'(0) = 2
$$

Aplicamos la Transformada de Laplace:

$$
2(s^2 X(s) - sX(0) - x'(0)) + 2(sX(s) - X(0)) + X(s) = \frac{1}{s}
$$

Sustituimos las condiciones iniciales:

$$
2(s^2 X(s) - 2) + 2sX(s) + X(s) = \frac{1}{s}
$$

Distribuimos:

$$
2s^2 X(s) - 4 + 2sX(s) + X(s) = \frac{1}{s}
$$

Agrupamos los términos con \( X(s) \):

$$
(2s^2 + 2s + 1) X(s) = \frac{1}{s} + 4
$$

Reescribimos el lado derecho:

$$
(2s^2 + 2s + 1) X(s) = \frac{1 + 4s}{s}
$$

Despejamos \( X(s) \):

$$
X(s) = \frac{1 + 4s}{s(2s^2 + 2s + 1)}
$$


### Fracciones parciales

Queremos escribir:

$$
\frac{1 + 4s}{s(2s^2 + 2s + 1)} = \frac{A}{s} + \frac{Bs + C}{2s^2 + 2s + 1}
$$

Multiplicamos ambos lados por el denominador común:

$$
1 + 4s = A(2s^2 + 2s + 1) + (Bs + C)s
$$

Usamos \( s = 0 \):

$$
1 = A(1) \Rightarrow A = 1
$$

Expandimos el lado derecho:

$$
1 + 4s = A(2s^2 + 2s + 1) + Bs^2 + Cs
$$

Agrupamos por potencias de \( s \):

$$
1 + 4s = (2A + B)s^2 + (2A + C)s + A
$$

Comparando coeficientes:

- $$\( A = 1 \)$$
- $$\( 2A + B = 0 \Rightarrow B = -2 \)$$
- $$\( 2A + C = 4 \Rightarrow C = 2 \)$$

Entonces:

$$
\frac{1 + 4s}{s(2s^2 + 2s + 1)} = \frac{1}{s} + \frac{-2s + 2}{2s^2 + 2s + 1}
$$



### Simplificamos

Dividimos el segundo término entre 2:

$$
X(s) = \frac{1}{s} - \frac{s}{s^2 + s + \frac{1}{2}} + \frac{1}{s^2 + s + \frac{1}{2}}
$$



### Transformada Inversa

Completamos el cuadrado:

$$
s^2 + s + \frac{1}{2} = \left( s + \frac{1}{2} \right)^2 + \frac{1}{4}
$$

Entonces:

$$
X(s) = \frac{1}{s} - \frac{s}{\left( s + \frac{1}{2} \right)^2 + \left( \frac{1}{2} \right)^2} + \frac{3}{\left( s + \frac{1}{2} \right)^2 + \left( \frac{1}{2} \right)^2}
$$

Aplicamos la transformada inversa:

- $$\( \mathcal{L}^{-1}\left( \frac{1}{s} \right) = 1 \)$$
- $$\( \mathcal{L}^{-1}\left( \frac{s + a}{(s + a)^2 + b^2} \right) = e^{-a t} \cos(bt) \)$$
- $$\( \mathcal{L}^{-1}\left( \frac{b}{(s + a)^2 + b^2} \right) = e^{-a t} \sin(bt) \)$$

Resultado:

$$
X(t) = 1 + e^{-t/2} \left( -\cos\left( \frac{1}{2} t \right) + 3 \sin\left( \frac{1}{2} t \right) \right)
$$


### Segundo ejercicio parcial  2

$$\frac{6s}{(s-\frac{s}{2})(s^2-4s+8)}$$

### Paso 1: Forma de la descomposición

Como el denominador tiene:

- un factor lineal: $$\( s - \frac{5}{2} \)$$
- un trinomio cuadrático irreducible: $$\( s^2 - 4s + 8 \)$$

La descomposición en fracciones parciales será:

$$
\frac{6s}{(s - \frac{5}{2})(s^2 - 4s + 8)} = \frac{A}{s - \frac{5}{2}} + \frac{Bs + C}{s^2 - 4s + 8}
$$



### Paso 2: Multiplicamos ambos lados por el denominador común

Multiplicamos ambos lados por $$\( (s - \frac{5}{2})(s^2 - 4s + 8) \)$$:

$$
6s = A(s^2 - 4s + 8) + (Bs + C)(s - \frac{5}{2})
$$



### Paso 3: Expandimos ambos términos

Expandiendo el primer término:

$$
A(s^2 - 4s + 8) = As^2 - 4As + 8A
$$

Expandiendo el segundo término:

$$
(Bs + C)(s - \frac{5}{2}) = Bs^2 - \frac{5}{2}Bs + Cs - \frac{5}{2}C
$$

Agrupamos todo:

$$
6s = (A + B)s^2 + (-4A + C - \frac{5}{2}B)s + (8A - \frac{5}{2}C)
$$



### Paso 4: Igualamos coeficientes

Comparando con el lado izquierdo \( 6s \):

- Coeficiente de $$\( s^2 \): \( A + B = 0 \)$$
- Coeficiente de $$\( s \): \( -4A + C - \frac{5}{2}B = 6 \)$$
- Término independiente: $$\( 8A - \frac{5}{2}C = 0 \)$$


### Paso 5: Sistema de ecuaciones

De la primera ecuación:

$$
A + B = 0 \Rightarrow B = -A
$$

Sustituimos en las otras ecuaciones:

**Segunda ecuación:**

$$
-4A + C - \frac{5}{2}(-A) = 6
$$

$$
-4A + C + \frac{5}{2}A = 6
$$

$$
(-4 + \frac{5}{2})A + C = 6 \Rightarrow -\frac{3}{2}A + C = 6 \quad (1)
$$

**Tercera ecuación:**

$$
8A - \frac{5}{2}C = 0 \Rightarrow \frac{5}{2}C = 8A \Rightarrow C = \frac{16}{5}A \quad (2)
$$

Sustituyendo (2) en (1):

$$
-\frac{3}{2}A + \frac{16}{5}A = 6
$$

$$
\left( -\frac{3}{2} + \frac{16}{5} \right)A = 6
$$

$$
\frac{-15 + 32}{10}A = 6 \Rightarrow \frac{17}{10}A = 6
$$

$$
A = \frac{60}{17}
$$

Luego:

$$
B = -A = -\frac{60}{17}
$$

$$
C = \frac{16}{5}A = \frac{16}{5} \cdot \frac{60}{17} = \frac{960}{85} = \frac{192}{17}
$$


$$
\frac{6s}{(s - \frac{5}{2})(s^2 - 4s + 8)} = \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60s}{17(s^2 - 4s + 8)} + \frac{192}{17(s^2 - 4s + 8)}
$$

### Transformada Inversa de Laplace

Dada la función:

$$
\frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60s}{17(s^2 - 4s + 8)} + \frac{192}{17(s^2 - 4s + 8)}
$$

Aplicamos la transformada inversa de Laplace a cada término.



### 1. Primer término

Sabemos que:

$$
\mathcal{L}^{-1}\left( \frac{1}{s - a} \right) = e^{at}
$$

Entonces:

$$
\mathcal{L}^{-1}\left( \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} \right) = \frac{60}{17} e^{\frac{5}{2}t}
$$


### 2. Segundo y tercer término

Completamos el trinomio:

$$
s^2 - 4s + 8 = (s - 2)^2 + 4
$$

Entonces:

$$
\frac{60s}{17((s - 2)^2 + 4)} = \frac{60}{17} \cdot \frac{s}{(s - 2)^2 + 4}
$$

Como:

$$
s = (s - 2) + 2
$$

Entonces:

$$
\frac{s}{(s - 2)^2 + 4} = \frac{s - 2}{(s - 2)^2 + 4} + \frac{2}{(s - 2)^2 + 4}
$$

Usamos las transformadas conocidas:

$$
\mathcal{L}^{-1}\left( \frac{s - a}{(s - a)^2 + b^2} \right) = e^{at} \cos(bt)
$$

$$
\mathcal{L}^{-1}\left( \frac{b}{(s - a)^2 + b^2} \right) = e^{at} \sin(bt)
$$

Aplicando esto:

$$
\mathcal{L}^{-1}\left( \frac{60s}{17((s - 2)^2 + 4)} \right) =
\frac{60}{17} \left( e^{2t} \cos(2t) + e^{2t} \sin(2t) \right)
$$



### 3. Tercer término

$$
\mathcal{L}^{-1}\left( \frac{192}{17((s - 2)^2 + 4)} \right) = \frac{192}{17} \cdot \frac{1}{2} e^{2t} \sin(2t) = \frac{96}{17} e^{2t} \sin(2t)
$$



### Resultado final

Juntamos los tres términos:

$$\mathcal{L}^{-1}\left(\frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60s}{17(s^2 - 4s + 8)} + \frac{192}{17(s^2 - 4s + 8)}\right)$$

$$= \frac{60}{17} e^{\frac{5}{2}t}- \frac{60}{17} e^{2t} \cos(2t)+ \left( -\frac{60}{17} + \frac{96}{17} \right) e^{2t} \sin(2t)$$

$$= \frac{60}{17} e^{\frac{5}{2}t}- \frac{60}{17} e^{2t} \cos(2t)+ \frac{36}{17} e^{2t} \sin(2t)$$

## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos.




