# Descomposición en fracciones parciales
## 1. Fracciones parciales
La descomposición en fracciones parciales se utiliza principalmente en la Transformada de Laplace y en la resolución de ecuaciones diferenciales, ya que permite expresar una fracción racional compleja como una suma de fracciones más simples. Esto facilita la aplicación de la transformada inversa de Laplace y la resolución de integrales en cálculo. En general, se usa para:


## 2. Definiciones   
>🔑*Transformada inversa de Laplace:* Se emplea para convertir funciones en el dominio de la frecuencia (s) al dominio del tiempo (t).  
  
>🔑*Resolución de ecuaciones diferenciales:* Ayuda a descomponer funciones para resolver ecuaciones diferenciales en sistemas dinámicos.  
      
>🔑*Cálculo integral:* Permite resolver integrales complicadas de manera más sencilla al descomponerlas en términos más manejables.  
  
>🔑*Análisis de sistemas de control y circuitos eléctricos:* Se usa para encontrar la respuesta temporal de sistemas eléctricos y mecánicos modelados por ecuaciones diferenciales.

# **3. Casos de descomposición de fracciones parciales**
### **Caso 1: Descomposición en Fracciones Parciales con Raíces Reales Distintas**

Cuando el denominador \( Q(s) \) de una fracción racional tiene **raíces reales distintas**, la descomposición se hace expresando la fracción como una suma de términos simples con denominadores lineales.  
  
**Forma General**    
Si tenemos una función racional de la forma:  
  
$$G(s) = \frac{P(s)}{(s + p_1)(s + p_2) \dots (s + p_n)}$$  
  
donde $$\( p_1, p_2, \dots, p_n \)$$ son **raíces reales distintas**, entonces se puede descomponer en fracciones parciales como:  
  
$$G(s) = \frac{A}{s + p_1} + \frac{B}{s + p_2} + \dots + \frac{N}{s + p_n}$$  
  
donde $$\( A, B, \dots, N \)$$ son constantes que se deben determinar.  
  


**Ejemplo Resuelto**    
Descomponer en fracciones parciales la siguiente función:  
  
$$G(s) = \frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)}$$  
  
**Paso 1: Plantear la ecuación de fracciones parciales**    
Como los términos del denominador son raíces reales distintas, proponemos la siguiente descomposición:  
  
$$\frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = \frac{A}{s + 1} + \frac{B}{s - 2} + \frac{C}{s - 3}$$  
  
Multiplicamos todo por $$\( (s + 1)(s - 2)(s - 3) \)$$ para eliminar los denominadores:  
  
$$2s^2 - 4 = A(s - 2)(s - 3) + B(s + 1)(s - 3) + C(s + 1)(s - 2)$$



**Paso 2: Hallar los coeficientes $$\( A, B, C \)$$**    
Para encontrar \( A, B, C \), evaluamos la ecuación en valores estratégicos de \( s \).  
  
1. **Para $$\( s = -1 \)$$** (anula los términos con \( B \) y \( C \)):    
   $$2(-1)^2 - 4 = A(-1 - 2)(-1 - 3)$$
   
   $$2 - 4 = A(-3)(-4)$$
   
   $$-2 = 12A\]$$
   
   $$A = -\frac{1}{6}$$
     
  
2. **Para $$\( s = 2 \)$$** (anula los términos con $$\( A \) y \( C \))$$:  
   $$2(2)^2 - 4 = B(2 + 1)(2 - 3)\$$
   
   $$8 - 4 = B(3)(-1)\$$
   
   $$4 = -3B\$$
   
   $$B = -\frac{4}{3}$$
   

3. **Para $$\( s = 3 \)$$** (anula los términos con $$\( A \) y \( B \))$$:  
   $$2(3)^2 - 4 = C(3 + 1)(3 - 2)\$$
   
   $$18 - 4 = C(4)(1)$$  
     
   $$14 = 4C $$
   
   entonces: C = $$\frac{7}{2}$$  
     


**Paso 3: Escribir la solución final**    
Reemplazamos los valores de $$\( A, B, C \)$$:

$$\frac{2s^2 - 4}{(s + 1)(s - 2)(s - 3)} = \frac{-\frac{1}{6}}{s + 1} + \frac{-\frac{4}{3}}{s - 2} + \frac{\frac{7}{2}}{s - 3}$$  

  

### **Caso 2: Descomposición en Fracciones Parciales con Raíces Repetidas**  

Cuando el denominador $$\( Q(s) \)$$ de una fracción racional tiene **raíces reales repetidas**, la descomposición cambia respecto al caso anterior.  

**Forma General**  
Si el denominador tiene factores repetidos, es decir,


$$G(s) = \frac{P(s)}{(s + p)^n}$$  


donde $$\( (s + p)^n \)$$ es un **factor elevado a una potencia**, la descomposición se hace de la forma:

$$G(s) = \frac{A}{s + p} + \frac{B}{(s + p)^2} + \frac{C}{(s + p)^3} + \dots + \frac{N}{(s + p)^n}$$

donde $$\( A, B, C, \dots, N \)$$ son constantes que se deben determinar.



**Ejemplo Resuelto**  
Descomponer en fracciones parciales la siguiente función:

$$G(s) = \frac{2s^2 + 6s + 5}{(s + 2)(s + 1)^2}$$  

**Paso 1: Plantear la ecuación de fracciones parciales**  
Como el denominador tiene un factor lineal simple \( (s + 2) \) y un factor cuadrático repetido \( (s + 1)^2 \), la descomposición se plantea así:  
  
$$\frac{2s^2 + 6s + 5}{(s + 2)(s + 1)^2} = \frac{A}{s + 2} + \frac{B}{s + 1} + \frac{C}{(s + 1)^2}$$  

Multiplicamos todo por $$\( (s + 2)(s + 1)^2 \)$$ para eliminar los denominadores:  

$$2s^2 + 6s + 5 = A(s + 1)^2 + B(s + 2)(s + 1) + C(s + 2)$$  
  
  
  
**Paso 2: Hallar los coeficientes \( A, B, C \)**    
Para encontrar $$\( A, B, C \)$$, evaluamos la ecuación en valores estratégicos de $$\( s \)$$.    
    
1. **Para \( s = -2 \)** (anula los términos con \( B \) y \( C \)):    
 
   $$2(-2)^2 + 6(-2) + 5 = A(-2 + 1)^2$$  
     
   $$8 - 12 + 5 = A(1)$$  
     
   $$1 = A$$  

3. **Para $$\( s = -1 \)$$** (anula los términos con $$\( A \) y \( C \))$$:
   
   $$2(-1)^2 + 6(-1) + 5 = C(-1 + 2)$$  
     
   $$2 - 6 + 5 = C(1)$$  
    
   $$1 = C$$    
  
5. **Para hallar $$\( B \)$$**, expandimos la ecuación original:

   $$2s^2 + 6s + 5 = A(s^2 + 2s + 1) + B(s^2 + 3s + 2) + C(s + 2)$$  
  
   Sustituyendo \( A = 1 \) y \( C = 1 \):    
  
   $$2s^2 + 6s + 5 = (s^2 + 2s + 1) + B(s^2 + 3s + 2) + (s + 2)$$  

   Agrupando términos:  
  
   $$2s^2 + 6s + 5 = s^2 + 2s + 1 + B s^2 + 3B s + 2B + s + 2$$  
  
   $$2s^2 + 6s + 5 = (1 + B)s^2 + (2 + 3B + 1)s + (1 + 2B + 2)$$  
    
   Comparando coeficientes con $$\( 2s^2 + 6s + 5 \)$$:  
  
   1. Para $$\( s^2 \)$$:    
      $$1 + B = 2 \quad \Rightarrow \quad B = 1$$  
    
   2. Para $$\( s \)$$:    
      $$2 + 3(1) + 1 = 6  \quad \text{(Cumple)}$$  
    
   3. Para términos constantes:    
      $$1 + 2(1) + 2 = 5  \quad \text{(Cumple)}$$  
  

**Paso 3: Escribir la solución final**    
Reemplazamos los valores de \( A, B, C \):  
  
$$\frac{2s^2 + 6s + 5}{(s + 2)(s + 1)^2} = \frac{1}{s + 2} + \frac{1}{s + 1} + \frac{1}{(s + 1)^2}$$  


### **Caso 3: Descomposición en Fracciones Parciales con Raíces Complejas Conjugadas** 

Cuando el denominador \( Q(s) \) de una fracción racional tiene **raíces complejas conjugadas**, la descomposición debe tener en cuenta los términos cuadráticos irreducibles.

**Forma General**  
Si el denominador tiene factores cuadráticos irreducibles de la forma \( s^2 + bs + c \), la descomposición se realiza de la forma:
  
$$G(s) = \frac{P(s)}{(s^2 + b_1s + c_1)(s^2 + b_2s + c_2) \dots (s^2 + b_n s + c_n)}$$  
  
La descomposición en fracciones parciales se expresa como:  
  
$$G(s) = \frac{A s + B}{s^2 + b_1 s + c_1} + \frac{C s + D}{s^2 + b_2 s + c_2} + \dots$$  

donde $$\( A, B, C, D, \dots \)$$ son constantes que se deben determinar.

**Ejemplo Resuelto**  
Descomponer en fracciones parciales la siguiente función:  
  
$$G(s) = \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)}$$  
  
**Paso 1: Plantear la ecuación de fracciones parciales**  
Como el denominador tiene dos factores cuadráticos irreducibles, la descomposición se plantea así:  
  
$$\frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} = \frac{A s + B}{s^2 + 2s + 2} + \frac{C s + D}{s^2 + 2s + 5}$$

Multiplicamos todo por $$\( (s^2 + 2s + 2)(s^2 + 2s + 5) \)$$ para eliminar los denominadores:

$$s^2 + 2s + 3 = (A s + B)(s^2 + 2s + 5) + (C s + D)(s^2 + 2s + 2)$$
  
  
**Paso 2: Expandir los productos**    
Expandimos cada término:  
  
$$(A s + B)(s^2 + 2s + 5) = A s^3 + 2A s^2 + 5A s + B s^2 + 2B s + 5B$$  
  
$$(C s + D)(s^2 + 2s + 2) = C s^3 + 2C s^2 + 2C s + D s^2 + 2D s + 2D$$  
  
Sumamos todos los términos:    
  
$$(A s^3 + 2A s^2 + 5A s + B s^2 + 2B s + 5B) + (C s^3 + 2C s^2 + 2C s + D s^2 + 2D s + 2D)$$  

Agrupamos por potencias de \( s \):  

$$(A + C)s^3 + (2A + B + 2C + D)s^2 + (5A + 2B + 2C + 2D)s + (5B + 2D)$$  
  
Esto debe ser igual a la ecuación original:  
  
$$s^2 + 2s + 3$$  
  


**Paso 3: Igualar coeficientes**    
Comparando coeficientes:  
  
1. **Para $$\( s^3 \)$$:**
    
   $$A + C = 0 \quad \Rightarrow \quad C = -A$$

2. **Para $$\( s^2 \)$$:**  
     
   $$2A + B + 2C + D = 1$$    
  
3. **Para $$\( s^1 \)$$:**  
    
   $$5A + 2B + 2C + 2D = 2$$    
  
4. **Para términos constantes:**  
     
  $$5B + 2D = 3$$  


**Paso 4: Resolver el sistema de ecuaciones**  
Sustituyendo $$\( C = -A \)$$ en la segunda ecuación:  

$$2A + B + 2(-A) + D = 1$$  

$$2A - 2A + B + D = 1$$  

$$B + D = 1$$  

Sustituyendo $$\( C = -A \)$$ en la tercera ecuación:  

$$5A + 2B + 2(-A) + 2D = 2$$  

$$3A + 2B + 2D = 2$$  
  
El sistema queda:  
  
1. $$\( A + C = 0 \)$$   
2. $$\( B + D = 1 \)$$    
3. $$\( 3A + 2B + 2D = 2 \)$$    
4. $$\( 5B + 2D = 3 \)$$    

Resolviendo paso a paso:
  
- De $$\( B + D = 1 \Rightarrow D = 1 - B \)$$
    
- Sustituyéndolo en $$\( 5B + 2D = 3 \)$$:  
  
  $$5B + 2(1 - B) = 3$$  
  
  $$5B + 2 - 2B = 3$$  
  
  $$3B = 1 \quad \Rightarrow \quad B = \frac{1}{3}$$  
  
  $$D = 1 - \frac{1}{3} = \frac{2}{3}$$  
  
Sustituyendo $$\( B = \frac{1}{3} \) y \( D = \frac{2}{3} \) en la ecuación \( 3A + 2B + 2D = 2 \)$$:

$$3A + 2\left(\frac{1}{3}\right) + 2\left(\frac{2}{3}\right) = 2$$  
  
$$3A + \frac{2}{3} + \frac{4}{3} = 2$$  
  
$$3A + 2 = 2$$  
  
$$3A = 0 \quad \Rightarrow \quad A = 0$$  
  
De $$\( A + C = 0 \)$$, obtenemos $$\( C = 0 \)$$.
  
  
**Paso 5: Escribir la solución final**    
Reemplazamos los valores de \( A, B, C, D \):  

$$\frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} = \frac{\frac{1}{3}}{s^2 + 2s + 2} + \frac{\frac{2}{3}}{s^2 + 2s + 5}$$  
  





## 4. Ejercicios
📚 # Ejemplo 1: Caso de Raíces Reales Distintas

  
Descomponer en fracciones parciales la siguiente función:  

$$G(s) = \frac{5s + 4}{(s + 1)(s + 2)}$$  
  
**Paso 1: Plantear la ecuación**    
  
Como el denominador tiene raíces reales distintas, la descomposición se plantea así:  
  
$$\frac{5s + 4}{(s + 1)(s + 2)} = \frac{A}{s + 1} + \frac{B}{s + 2}$$  
  
Multiplicamos todo por \( (s + 1)(s + 2) \) para eliminar los denominadores:  
  
$$5s + 4 = A(s + 2) + B(s + 1)$$

**Paso 2: Hallar los coeficientes \( A \) y \( B \)**  
  
1. **Para $$\( s = -1 \)$$** (anula el término con $$\( B \))$$:  

   $$5(-1) + 4 = A(-1 + 2)$$  
  
   $$-5 + 4 = A(1)$$  
  
   $$A = -1$$  
    
2. **Para $$\( s = -2 \)$$** (anula el término con $$\( A \)$$:  
  
   $$5(-2) + 4 = B(-2 + 1)$$  
    
   $$-10 + 4 = B(-1)$$    
    
   $$B = 6$$    
  
**Paso 3: Escribir la solución final**    
  
$$\frac{5s + 4}{(s + 1)(s + 2)} = \frac{-1}{s + 1} + \frac{6}{s + 2}$$  

-----

📚 # Ejemplo 2: Caso de Raíces Repetidas**  
  
Descomponer en fracciones parciales la siguiente función:    
  
$$G(s) = \frac{3s + 2}{(s + 1)^2}$$    
  
**Paso 1: Plantear la ecuación**  
  
Como el denominador tiene un factor cuadrático repetido, la descomposición se plantea así:  
  
$$\frac{3s + 2}{(s + 1)^2} = \frac{A}{s + 1} + \frac{B}{(s + 1)^2}$$  
  
  
Multiplicamos todo por $$\( (s + 1)^2 \)$$ para eliminar los denominadores:  
  
$$3s + 2 = A(s + 1) + B$$  
  
**Paso 2: Hallar los coeficientes $$\( A \) y \( B \)$$**  

1. **Para \( s = -1 \)** (anula el término con \( A \)):  
  
   $$3(-1) + 2 = B$$
  
   $$-3 + 2 = B$$
  
  $$B = -1$$

2. **Para hallar $$\( A \)$$**, expandimos la ecuación original:    
  
   $$3s + 2 = A s + A + B$$  

   Como los términos con $$\( s \)$$ deben ser iguales:  
    
   $$3s = A s \Rightarrow A = 3$$  

**Paso 3: Escribir la solución final**    
  
$$\frac{3s + 2}{(s + 1)^2} = \frac{3}{s + 1} + \frac{-1}{(s + 1)^2}$$  



## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos. En el contexto de la Transformada de Laplace, permite encontrar la transformada inversa de manera más sencilla, dividiendo expresiones complejas en términos más simples.  



