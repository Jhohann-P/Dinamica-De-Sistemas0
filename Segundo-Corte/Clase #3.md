# Sistemas Mecanicos II
## 1. Sistemas de control en Dinámica de Sistemas 
En dinámica de sistemas, los **sistemas mecánicos** son aquellos compuestos por componentes físicos que interactúan mediante fuerzas y movimientos. Estos sistemas pueden incluir elementos como masas, resortes, ruedas, palancas, entre otros, y su comportamiento está determinado por las leyes de la física, como las de Newton. En términos de dinámica, se estudian cómo las fuerzas externas o internas afectan el movimiento y las interacciones entre los componentes del sistema.

## 2. Definiciones   
>🔑*Trabajo:* Es la energía transferida cuando una fuerza mueve un objeto a lo largo de una distancia.
  
>🔑*Energía potencial:* Es la energía almacenada en un objeto debido a su posición o estado (como una piedra en lo alto de una colina).
      
>🔑*Energía cinética:* Es la energía que tiene un objeto debido a su movimiento.
  
>🔑*Potencia:* Es la rapidez con la que se realiza un trabajo o se transfiere energía.

## 3. Aplicando a elementos mecánicos
1. Energía potencial en un resorte:
 
   Es el trabajo neto hecho sobre él por las fuerzas que actúan en sus extremos cuando es comprimido o estirado.
   
   ![image](https://github.com/user-attachments/assets/2c6bfd06-1154-4191-9e8b-b74564cc3b5e)

   De forma general el cambio de energía sería:

   ![image](https://github.com/user-attachments/assets/168ee97f-c038-4d0a-8a33-cee53847fc08)

2. Potencia en un resorte:
 
   Potencia requerida para estirar o comprimir un resorte

   ![image](https://github.com/user-attachments/assets/cee37471-ec35-43b0-b7ca-8415d6dfb06a)

   sabiendo que ![image](https://github.com/user-attachments/assets/cec48c46-c776-4f24-bd8e-fc19799f2689) (Energia potencial en un resorte)

   ![image](https://github.com/user-attachments/assets/6f10e9d4-090e-460e-8015-6f5d373de978)
3. Potencia en una masa:

    La potencia requerida para acelerar una masa en línea recta

   ![image](https://github.com/user-attachments/assets/e3c6d9f3-1216-4403-b886-fa576846ea4f)

   Sabiendo que ![image](https://github.com/user-attachments/assets/ff22939b-67b0-4821-8931-51e26218fa30) (Energia cinetica masa)

   ![image](https://github.com/user-attachments/assets/813635c1-5cfc-44ce-826f-8c3191a5c5a1)

4. Energía disipada:

   La energía disipada en un amortiguador corresponde al trabajo neto realizado sobre este

   ![image](https://github.com/user-attachments/assets/072d40fb-0aa9-4795-ad8f-5869452fde2b)
   ![image](https://github.com/user-attachments/assets/e4ca8e36-335d-48fb-b889-93f0b26ffe29)

5. Potencia disipada en amortiguador:

   La potencia disipada en el amortiguador de cilindro es:

![image](https://github.com/user-attachments/assets/53622d86-2989-4c7a-9c75-de0318bc9bcb)

Sabiendo que ![image](https://github.com/user-attachments/assets/993b9b21-dd74-43f4-97bb-0422239e20ec)

![image](https://github.com/user-attachments/assets/0459cb1e-b9de-4a3e-bbed-5cbd6fad7e7c)

### 4. Método de energía para obtener las ecuaciones de movimiento
  
1. Conservación de energía

Es posible obtener el modelo matemático considerando que la energía total de un sistema permanece igual si ninguna energía entra o sale del sistema.

En los sistemas mecánicos la fricción disipa energía en forma de calor.

Los sistemas que ni incluyen fricción se denominan sistemas conservativos.

2. Sistema conservativo:

Toda la energía (cinética y potencial) sale del sistema en forma de trabajo mecánico. No se disipa energía.

![image](https://github.com/user-attachments/assets/40f05132-129e-4e08-8632-993173bfc490) (Trabajo neto fuerza externa)

Si no entra energía externa entonces

![image](https://github.com/user-attachments/assets/00385329-dcf8-4461-859a-e0b39e13ba35) eso implica que ![image](https://github.com/user-attachments/assets/75d9db50-a61b-43ef-9b90-ef1ec289f628)




     
 Ejemplo 

 ![image](https://github.com/user-attachments/assets/9b18d543-e901-4b17-af6e-9ec272849897)

![image](https://github.com/user-attachments/assets/a967e239-ca87-437b-92d2-1b97e7199404)

Al derivar la energía total

![image](https://github.com/user-attachments/assets/210ca5ee-323a-4274-bdbe-e1417925c405)





### 5. Conversión movimiento Translacional - Rotacional  
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
# **Descomposición en Fracciones Parciales**

Dada la siguiente fracción:  

$$\[\frac{2s^2 - 4}{(s+1)(s-2)(s-3)} = \frac{A}{s+1} + \frac{B}{s-2} + \frac{C}{s-3}\]$$  

Multiplicamos por el denominador común para cancelar fracciones:  

$$\[2s^2 - 4 = A(s-2)(s-3) + B(s+1)(s-3) + C(s+1)(s-2)\]$$

Paso 2: Sustituimos valores para encontrar \( A, B, C \)**

Para $$\( s = 2 \)$$:  

$$\[2(4) - 4 = B(2+1)(2-3)\]$$  

$$\[8 - 4 = B(3)(-1)\]$$

$$\[4 = -3B\]$$

$$\[B = -\frac{4}{3}\]$$

Para $$\( s = 3 \)$$:


$$\[2(9) - 4 = C(4)(1)\]$$

$$\[18 - 4 = 4C\]$$

$$\[14 = 4C\]$$

$$\[C = \frac{7}{2}\]$$



Para $$\( s = -1 \)$$:

$$\[2(-1)^2 - 4 = A(-1-2)(-1-3)\]$$

$$\[2 - 4 = A(-3)(-4)\]$$

$$\[-2 = 12A\]$$

$$\[A = -\frac{1}{6}\]$$


Sustituyendo los valores de \( A, B, C \):

$$\[\frac{2s^2 - 4}{(s+1)(s-2)(s-3)} = \frac{-1/6}{s+1} + \frac{-4/3}{s-2} + \frac{7/2}{s-3}\]$$



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

![image](https://github.com/user-attachments/assets/d7a10955-a2ee-43b2-9339-4d96c638fbf5)

![image](https://github.com/user-attachments/assets/f5dbc523-3568-41b0-870d-a6c9e5ba18f4)

La energía cinética total ![image](https://github.com/user-attachments/assets/e1a845d7-6aa0-4551-90a3-1ab8cd5f2563)

Ecuacion del movimiento

![image](https://github.com/user-attachments/assets/0ac08e37-2cd1-49c1-90cc-cbe1d560bd25)

    


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
En dinámica de sistemas, los sistemas mecánicos se pueden analizar mediante conceptos de trabajo, energía y potencia. Estos principios permiten comprender cómo las fuerzas afectan el movimiento y la energía de los cuerpos. El uso de modelos energéticos, como la conservación de la energía, facilita la obtención de ecuaciones de movimiento, especialmente en sistemas conservativos donde no hay pérdida de energía. Sin embargo, cuando existen elementos como amortiguadores, parte de la energía se disipa en forma de calor, lo que debe considerarse en el análisis. En conjunto, estos enfoques proporcionan una base sólida para entender y predecir el comportamiento dinámico de sistemas mecánicos complejos.
