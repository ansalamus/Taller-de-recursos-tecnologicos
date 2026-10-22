# Fórmula Matemática y Tabla de Frecuencias: Síntesis Aditiva

## Fórmula general para un tono con ondas senoidales
Partiendo de una frecuencia fundamental ($f_1$) de 220 Hz hasta el parcial 16 ($N=16$) en función del tiempo ($t$):

$$x(t) = \sum_{n=1}^{16} A_n \cdot \operatorname{sen}(2\pi \cdot (n \cdot 220) \cdot t + \phi_n)$$

### Expresión expandida
Si se asume una fase inicial de cero ($\phi_n = 0$) para todos los parciales, la sumatoria se expresa como la adición de cada una de las 16 ondas:

$$x(t) = A_1\operatorname{sen}(440\pi t) + A_2\operatorname{sen}(880\pi t) + A_3\operatorname{sen}(1320\pi t) + \dots + A_{16}\operatorname{sen}(7040\pi t)$$

### Parámetros de la fórmula
* **$x(t)$**: Es la amplitud resultante de la señal de audio en el instante de tiempo $t$.
* **$n$**: El número de parcial o armónico (desde $n=1$ hasta $n=16$).
* **$f_n = n \cdot 220$**: La frecuencia de cada parcial en Hertz (Hz). La fundamental ($n=1$) es de 220 Hz, el segundo parcial es de 440 Hz, el tercero de 660 Hz, hasta llegar al parcial 16 que tiene una frecuencia de **3520 Hz**.
* **$A_n$**: La amplitud (volumen) de cada parcial individual. Estos valores determinan el **timbre** del sonido resultante (por ejemplo, si usas $A_n = \frac{1}{n}$, generarás una aproximación a una onda de diente de sierra).
* **$\phi_n$**: La fase inicial de cada parcial en radianes (frecuentemente configurada en $0$).

---

## Tabla de Frecuencias y Amplitudes
Diseño clásico de la **onda de diente de sierra ideal** ($A_n = \frac{1}{n}$), el cual decae progresivamente y utiliza los 16 parciales para dar un sonido brillante y rico en armónicos.

| Número de Parcial ($n$) | Tipo de Componente | Fórmula de Frecuencia | Frecuencia Exacta (Hz) | Amplitud Sugerida ($A_n = \frac{1}{n}$) | Valor Decimal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1** | **Fundamental** | $1 \times 220$ | **220 Hz** | $1$ | 1.0000 |
| **2** | 2° Armónico | $2 \times 220$ | **440 Hz** | $\frac{1}{2}$ | 0.5000 |
| **3** | 3° Armónico | $3 \times 220$ | **660 Hz** | $\frac{1}{3}$ | 0.3333 |
| **4** | 4° Armónico | $4 \times 220$ | **880 Hz** | $\frac{1}{4}$ | 0.2500 |
| **5** | 5° Armónico | $5 \times 220$ | **1100 Hz** | $\frac{1}{5}$ | 0.2000 |
| **6** | 6° Armónico | $6 \times 220$ | **1320 Hz** | $\frac{1}{6}$ | 0.1667 |
| **7** | 7° Armónico | $7 \times 220$ | **1540 Hz** | $\frac{1}{7}$ | 0.1428 |
| **8** | 8° Armónico | $8 \times 220$ | **1760 Hz** | $\frac{1}{8}$ | 0.1250 |
| **9** | 9° Armónico | $9 \times 220$ | **1980 Hz** | $\frac{1}{9}$ | 0.1111 |
| **10** | 10° Armónico | $10 \times 220$ | **2200 Hz** | $\frac{1}{10}$ | 0.1000 |
| **11** | 11° Armónico | $11 \times 220$ | **2420 Hz** | $\frac{1}{11}$ | 0.0909 |
| **12** | 12° Armónico | $12 \times 220$ | **2640 Hz** | $\frac{1}{12}$ | 0.0833 |
| **13** | 13° Armónico | $13 \times 220$ | **2860 Hz** | $\frac{1}{13}$ | 0.0769 |
| **14** | 14° Armónico | $14 \times 220$ | **3080 Hz** | $\frac{1}{14}$ | 0.0714 |
| **15** | 15° Armónico | $15 \times 220$ | **3300 Hz** | $\frac{1}{15}$ | 0.0667 |
| **16** | **16° Armónico** | $16 \times 220$ | **3520 Hz** | $\frac{1}{16}$ | 0.0625 |