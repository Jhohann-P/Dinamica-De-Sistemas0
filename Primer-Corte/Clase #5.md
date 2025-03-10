# Fracciones parciales
## 1. Ejercicio Fracciones parciales
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
  
# Clase 5

## Factorización

Comenzamos a factorizar todos los términos.

Factorizamos:

$$
S^5 + 5S^4 + 10S^3 + 10S^2 + 9S + 9
$$

$$
(S+1)(S^4 + 4S^3 + 6S^2 + 6S + 9)
$$

$$
(S+1)(S^2 + 2S + 3)(S^2 + 2S + 3)
$$

La factorización sería:

$$
(S+1)(S^2 + 2S + 3)^2
$$

Como resultado:

Factorizamos:

$$
S^6 + 6S^5 + 15S^4 + 22S^3 + 26S^2 + 24S + 18
$$

$$
(S+2)(S^5 + 4S^4 + 7S^3 + 8S^2 + 10S + 9)
$$

$$
(S+2)(S+3+i)(S+3-i)(S+4+i)(S+4-i)
$$

La factorización sería:

$$
(S+2)(S+3+i)(S+3-i)(S+4+i)(S+4-i)
$$

Como resultado:

Reescribimos nuevamente todas las ecuaciones:

$$
\frac{S+1}{(S+2)(S+3+i)(S+3-i)(S+4+i)(S+4-i)}
$$

Ahora como fracción parcial:

$$
\frac{A}{S+2} + \frac{B}{S+3+i} + \frac{C}{S+3-i} + \frac{D}{S+4+i} + \frac{E}{S+4-i}
$$

Escribiendo como ecuación:

$$
S+1 = A(S+3+i)(S+3-i)(S+4+i)(S+4-i) + B(S+2)(S+3-i)(S+4+i)(S+4-i) + C(S+2)(S+3+i)(S+4+i)(S+4-i)
$$

$$
+ D(S+2)(S+3+i)(S+3-i)(S+4-i) + E(S+2)(S+3+i)(S+3-i)(S+4+i)
$$

Cuando \( S=1 \), todas se cancelan menos \( C \):

$$
1+1 = C(1+2)(1+4+i)(1+4-i)
$$

$$
2 = C(3)(2^2+1)(2^2+1)
$$

$$
2 = C(3)(5)(5)
$$

$$
2 = C(75)
$$

$$
C = \frac{2}{75}
$$

Cuando \( S=-2 \), todas se cancelan menos \( B \):

$$
-2+1 = B(-2+3-i)(-2+4+i)(-2+4-i)
$$

$$
-1 = B(1-i)(2+i)(2-i)
$$

$$
-1 = B(1-1-2i+2i)(4-1)
$$

$$
-1 = B(3)(3)
$$

$$
B = -\frac{1}{9}
$$

Cuando \( S=-3-i \), todas se cancelan menos \( D \):

$$
-3-i+1 = D(-3-i+2)(-3-i+4+i)
$$

$$
-2-i = D(-1-i)(1)
$$

$$
D = \frac{-2-i}{-1-i}
$$

Cuando \( S=-3+i \), todas se cancelan menos \( E \):

$$
-3+i+1 = E(-3+i+2)(-3+i+4-i)
$$

$$
-2+i = E(-1+i)(1)
$$

$$
E = \frac{-2+i}{-1+i}
$$

Cuando \( S=-4-i \), todas se cancelan menos \( F \):

$$
-4-i+1 = F(-4-i+2)(-4-i+3+i)
$$

$$
-3-i = F(-2-i)(-1)
$$

$$
F = \frac{-3-i}{-2-i}
$$

Cuando \( S=-4+i \), todas se cancelan menos \( G \):

$$
-4+i+1 = G(-4+i+2)(-4+i+3-i)
$$

$$
-3+i = G(-2+i)(-1)
$$

$$
G = \frac{-3+i}{-2+i}
$$

Para hallar \( A \), decimos que \( s=0 \):

$$
0+1 = A(0+3+i)(0+3-i)(0+4+i)(0+4-i) + B(0+2)(0+3-i)(0+4+i)(0+4-i)
$$

$$
+ C(0+2)(0+3+i)(0+4+i)(0+4-i) + D(0+2)(0+3+i)(0+3-i)(0+4-i) + E(0+2)(0+3+i)(0+3-i)(0+4+i)
$$

Reemplazando cada término:

$$
1 = A(3+i)(3-i)(4+i)(4-i) + B(2)(3-i)(4+i)(4-i) + C(2)(3+i)(4+i)(4-i)
$$

$$
+ D(2)(3+i)(3-i)(4-i) + E(2)(3+i)(3-i)(4+i)
$$

$$
1 = A(3^2- i^2)(4^2 - i^2) + B(2)(3-i)(16 - i^2) + C(2)(3+i)(16 - i^2)
$$

$$
+ D(2)(3^2-i^2)(4-i) + E(2)(3^2-i^2)(4+i)
$$

Reduciendo sería:

$$
1 = A(9+1)(16+1) + B(2)(3-i)(16+1) + C(2)(3+i)(16+1)
$$

$$
+ D(2)(9+1)(4-i) + E(2)(9+1)(4+i)
$$

$$
1 = A(10)(17) + B(2)(3-i)(17) + C(2)(3+i)(17)
$$

$$
+ D(2)(10)(4-i) + E(2)(10)(4+i)
$$

$$
1 = 170A + 34B(3-i) + 34C(3+i) + 20D(4-i) + 20E(4+i)
$$

Reemplazando:

$$
1 = 170A + 34(3B - Bi) + 34(3C + Ci) + 20(4D - Di) + 20(4E + Ei)
$$

$$
1 = 170A + 102B - 34Bi + 102C + 34Ci + 80D - 20Di + 80E + 20Ei
$$

$$
1 = 170A + 102B + 102C + 80D + 80E + (-34B + 34C - 20D + 20E)i
$$

Entonces:

$$
170A + 102B + 102C + 80D + 80E = 1
$$

$$
-34B + 34C - 20D + 20E = 0
$$


## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos. En el contexto de la Transformada de Laplace, permite encontrar la transformada inversa de manera más sencilla, dividiendo expresiones complejas en términos más simples.  



