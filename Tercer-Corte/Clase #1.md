# Correcion del parcial
## 1. Transformada de Laplace y Fracciones parciales en Dinámica de Sistemas 
En Dinámica de Sistemas, la Transformada de Laplace se utiliza para transformar ecuaciones diferenciales del dominio del tiempo al dominio de la frecuencia (espacio s), donde es más fácil analizarlas y resolverlas algebraicamente.``

Una vez obtenida la función de transferencia o la solución en el dominio de Laplace, se aplica la descomposición en fracciones parciales para simplificar la expresión. Esto permite utilizar tablas de transformadas inversas y regresar al dominio del tiempo con una expresión analítica clara de la respuesta del sistema.


## 2. Definiciones   
  
>🔑*Sistema:* Conjunto de componentes interconectados que trabajan juntos para alcanzar un objetivo específico.
      
>🔑*Fracciones Parciales:* Es una técnica algebraica que permite descomponer una fracción racional (cociente de dos polinomios) en una suma de fracciones más simples, lo cual facilita operaciones como la integración o la transformada inversa de Laplace.
  
>🔑*Transformada de Laplace:* Método matemático que convierte ecuaciones diferenciales en ecuaciones algebraicas en el dominio de la frecuencia compleja.
  
## 3. Parcial #2.
### Primer ejercicio del parcial #1

![image](https://github.com/user-attachments/assets/3395cfee-92fc-405a-8f88-cab69b7f2cd0)

![image](https://github.com/user-attachments/assets/fbe9358f-b649-4b5b-8fc4-0cce84b62e66)

$$ u - F_k - F_b = 0 $$

$$ u - K(y - x) - B(y' - x') = 0 $$

![image](https://github.com/user-attachments/assets/dbf48ab6-a8c3-46eb-9e0c-d3eb9b441366)


$$ K(y - x) + B(y' - x') = M y'' $$


### Segundo ejercicio del parcial #1.

![image](https://github.com/user-attachments/assets/3b44edb8-d573-471b-8f7d-35d35b1d5c82)

![image](https://github.com/user-attachments/assets/afd8ba4c-9fb4-49d7-8ae6-2e21fb8c152e)


$$ -e(t) + V_L + V_{200} + V_{50} = 0 $$

$$ -e(t) + 2(i_1) + 200(i_1) + 50(i_1 - i_2) = 0 $$

$$ V_{50} + V_{20} + V_2 = 0 $$

$$ 50(i_2 - i_1) + 20i_2 + \frac{1}{C} \int i_2\, dt = 0 $$

$$ i_1 - i_2 - i_3 = 0 $$

$$ i_1 - 0.2V_c - \frac{V_x}{50} = 0 $$

$$ V_x = 20 i_2 + V_c $$

$$ V_x = 4 V_c' + V_c $$

$$ e(t) = L i_1' + 200 i_1 + V_x $$

$$ i_C = 0.2 V_C $$

## 4. Parcial #2
### Primer ejercicio parcial  #2

![image](https://github.com/user-attachments/assets/eb5b9df1-c25f-42c0-b55d-792aa594eebe)

![image](https://github.com/user-attachments/assets/7172ae6a-8f73-44ca-a606-ac886ab3bff6)


$$u + F_{w1} - F_{k2} - F_{b1} - F_{b2} - F_{b3} - F_{k1} = m_1 \omega m_1$$

$$u + m_1 g - k_1 y_1 - b_1 y_2' - b_2 y_3' - b_3 (y_3 - y_2) - k_2 (y_1 - y_2) = m_1 y_1''$$

![image](https://github.com/user-attachments/assets/444a7bd0-4580-4490-a1f0-fba6d4a626e1)


$$F_{k1} - F_{w2} - F_{b3} = m_2 \omega m_2$$

$$k_1 (y_3 - y_2) + m_2 g - b_3 (y_1' - y_2') = m_2 y_2''$$
2


### Segundo ejercicio parcial  2


## **Conclusión**
La descomposición en fracciones parciales es una herramienta útil para simplificar expresiones racionales y facilitar su manipulación en distintos cálculos.




