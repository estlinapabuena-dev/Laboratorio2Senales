# Laboratorio2Senales
# Parte A: Convolución Discreta

## 1 Análisis inicial

En este primer análisis se realizaron las gráficas por separado del código estudiantil y de la cédula.  
Cada valor se colocó en su posición correspondiente, lo que permitió ver con claridad cómo está formada cada señal.  

- La secuencia `x[n]` representa los dígitos de la **cédula**.  
- La secuencia `h[n]` corresponde a los dígitos del **código estudiantil**.  

## 2. Definición teórica

## 3. Datos utilizados


## 4. Desarrollo a mano

### Cálculos paso a paso:

### Tabla final `y[n]`:  

## 5. Implementación en Python

```python
import numpy as np
import matplotlib.pyplot as plt

# Datos de Lina
x = np.array([1,0,1,1,0,8,2,1,5,0])   # cédula
h = np.array([5,6,0,0,8,2,2])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h[n]')
plt.title('h[n] Lina')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x[n]')
plt.title('x[n] Lina')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h[n] y x[n], Lina:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y[n]')
plt.title('Convolución y[n] = x[n] * h[n]')
plt.grid()
plt.show()
```
