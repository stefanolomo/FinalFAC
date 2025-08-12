# Guión del video final

Tema: IEEE 754 - Historia y funcionamiento

## Secciones

1. Introducción
2. Historia
3. ¿Como se compone un numero en IEEE754?
4. Pasaje de un numero decimal al estandar
5. Pasaje del estandar a decimal
6. Suma con IEEE754 (?)

### Introducción

### Historia

### ¿Como se compone un numero en IEEE754?

### Pasaje de decimal al estandar

El pasaje de un numero del sistema decimal al estandar IEEE754 se puede hacer siguiendo distintos pasos. En terminos generales, se debe:

+ Establecer el valor del bit de signo
+ Establecer el valor del decimal en binario con punto fijo
+ Normalizar, "Correr la coma" en el número
+ Determinar el exponente sesgado
+ Organizar en la disposicion del estandar

### Pasaje del estandar a decimal

El pasaje de un numero expresado mediante el estandar IEEE754 se realiza con los siguientes pasos: 

+ Interpretar el bit de signo
+ Interpretar el exponente y transformarlo en exponente real
+ Interpretar la mantisa
+ Posicionar el numero y calcularlo en decimal

La siguiente formula nos ayuda a visualizar como se interpreta un numero decimal codificado con el estandar IEEE754:

\begin{equation}
(-1)^A \times (1,m) \times 2^{e}
\end{equation}

donde:

+ "s" es el bit de signo. de manera que si es 0, el numero debe ser positivo entonces anula el factor -1; Y si es 1, el numero debe ser negativo entonces involucra el factor -1 en el producto.
+ "m" es la mantisa interpretada en decimal. Notar que se le antepone un entero 1,m ya que en el proceso de codificación ese 1 se transforma en bit implicito, siendo dejado fuera de la mantisa.
+ "e" es el exponente real. Esto quiere decir que es el exponente interpretado en decimal y des-sesgado de manera correspondiente ($2^{\(n-1)} - 1$).