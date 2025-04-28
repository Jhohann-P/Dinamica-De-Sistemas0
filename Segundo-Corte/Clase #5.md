# Introducción a Amplificadores en Dinámica de Sistemas
## 1. Tipos de Amplificadores
### Amplificador Inversor

- **Descripción**: Toma una señal de entrada, **la amplifica** y **la invierte** (cambia su signo).
- **Comportamiento**: Si la entrada es positiva, la salida será negativa, y viceversa.
- **Ganancia**: 
  $$A_v = -\frac{R_f}{R_{in}}$$
  Donde:
  - $$\( R_f \)$$ = Resistencia de realimentación.
  - $$\( R_{in} \)$$ = Resistencia de entrada.

### Amplificador No Inversor

- **Descripción**: Amplifica la señal **sin invertirla**.
- **Comportamiento**: Si la entrada es positiva, la salida también será positiva, solo que amplificada.
- **Ganancia**:
$$A_v = 1 + \frac{R_f}{R_{in}}$$


## 2. Definiciones   
>🔑*Amplificador:* Dispositivo que aumenta la magnitud de una señal de entrada sin alterar significativamente su forma.

>🔑*Amplificador Inversor:* Tipo de amplificador que invierte la fase de la señal de entrada mientras la amplifica.

>🔑*Amplificador No Inversor:* Amplificador que incrementa la magnitud de la señal de entrada manteniendo su misma fase.

>🔑*Ganancia:* Relación entre la señal de salida y la señal de entrada de un sistema, que indica cuánto se ha amplificado o atenuado la señal.

>🔑Amplificador Operacional (Op-Amp): Componente electrónico altamente versátil utilizado para amplificar señales, realizar operaciones matemáticas y construir sistemas de control.

>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
  
## 3. Ejercicio 1.
### Amplificador no inversor

![image](https://github.com/user-attachments/assets/2266b393-86ff-40e0-bc79-ff18525992cc)

$$i_1 - i_2 = 0$$

$$\frac{e_o - e_i}{R_2} - \frac{e_i}{R_1} = 0$$

$$\frac{e_o}{R_2} = e_i \left( \frac{1}{R_2} + \frac{1}{R_1} \right)$$

$$e_o = e_i \left( 1 + \frac{R_2}{R_1} \right)$$

### Con elementos almacenadores de energía

![image](https://github.com/user-attachments/assets/3a1f64a1-f2e4-48e3-a404-01ca1168a69f)


$$i_1 - i_2 - i_3 = 0$$

$$\frac{e_i - e'}{R_1} - \frac{e' - e_o}{R_2} - C \frac{d(e' - e_o)}{dt} = 0$$

$$e' = 0$$

$$\frac{e_i}{R_1} - \frac{e_o}{R_2} - C \frac{d(-e_o)}{dt} = 0$$

$$\frac{e_i}{R_1} = -\frac{e_o}{R_2} - C \frac{d(e_o)}{dt}$$

#### Fracciones parciales de:



#### Forma general de la descomposición:


#### Expandimos cada término:


#### Igualando coeficientes:


#### Resolviendo el sistema:




#### Resultado final:

## 4. Parcial #2
### Primer ejercicio parcial  #2

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


#### Fracciones parciales

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



#### Simplificamos

Dividimos el segundo término entre 2:

$$
X(s) = \frac{1}{s} - \frac{s}{s^2 + s + \frac{1}{2}} + \frac{1}{s^2 + s + \frac{1}{2}}
$$



#### Transformada Inversa

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

#### Paso 1: Forma de la descomposición

Como el denominador tiene:

- un factor lineal: $$\( s - \frac{5}{2} \)$$
- un trinomio cuadrático irreducible: $$\( s^2 - 4s + 8 \)$$

La descomposición en fracciones parciales será:

$$
\frac{6s}{(s - \frac{5}{2})(s^2 - 4s + 8)} = \frac{A}{s - \frac{5}{2}} + \frac{Bs + C}{s^2 - 4s + 8}
$$



#### Paso 2: Multiplicamos ambos lados por el denominador común

Multiplicamos ambos lados por $$\( (s - \frac{5}{2})(s^2 - 4s + 8) \)$$:

$$
6s = A(s^2 - 4s + 8) + (Bs + C)(s - \frac{5}{2})
$$



#### Paso 3: Expandimos ambos términos

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



#### Paso 4: Igualamos coeficientes

Comparando con el lado izquierdo \( 6s \):

- Coeficiente de $$\( s^2 \): \( A + B = 0 \)$$
- Coeficiente de $$\( s \): \( -4A + C - \frac{5}{2}B = 6 \)$$
- Término independiente: $$\( 8A - \frac{5}{2}C = 0 \)$$


#### Paso 5: Sistema de ecuaciones

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

#### Transformada Inversa de Laplace

Dada la función:

$$
\frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60s}{17(s^2 - 4s + 8)} + \frac{192}{17(s^2 - 4s + 8)}
$$

Aplicamos la transformada inversa de Laplace a cada término.



#### 1. Primer término

Sabemos que:

$$
\mathcal{L}^{-1}\left( \frac{1}{s - a} \right) = e^{at}
$$

Entonces:

$$
\mathcal{L}^{-1}\left( \frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} \right) = \frac{60}{17} e^{\frac{5}{2}t}
$$


#### 2. Segundo y tercer término

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



#### 3. Tercer término

$$
\mathcal{L}^{-1}\left( \frac{192}{17((s - 2)^2 + 4)} \right) = \frac{192}{17} \cdot \frac{1}{2} e^{2t} \sin(2t) = \frac{96}{17} e^{2t} \sin(2t)
$$



#### Resultado final

Juntamos los tres términos:

$$\mathcal{L}^{-1}\left(\frac{60}{17} \cdot \frac{1}{s - \frac{5}{2}} - \frac{60s}{17(s^2 - 4s + 8)} + \frac{192}{17(s^2 - 4s + 8)}\right)$$

$$= \frac{60}{17} e^{\frac{5}{2}t}- \frac{60}{17} e^{2t} \cos(2t)+ \left( -\frac{60}{17} + \frac{96}{17} \right) e^{2t} \sin(2t)$$

$$= \frac{60}{17} e^{\frac{5}{2}t}- \frac{60}{17} e^{2t} \cos(2t)+ \frac{36}{17} e^{2t} \sin(2t)$$

## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos.





