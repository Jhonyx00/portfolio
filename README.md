# portfolio

#Cuby
Cuby es un simulador semi-genérico de rompecabezas en 3d, permite interactuar mediante gestos en pantalla para girar las capas y girar el rompecabezas. Está construido artesanalmente pieza por pieza y con HTML, CSS3D y JavaScript.   

## Nacimiento
Este proyecto nace de mi obsesión por los rompecabezas mecánicos, me fascina la geometría tridimensional, las formas cubicas y los colores, un día decidí que iba a programar un cubo de rubik en 3d desde cero, y al final terminé desarrollando un mini motor 3d que renderiza rompecabezas mecanicos y responde a gestos en pantalla.

## Metodologia
El simulador funciona extrictamente bajo las reglas del álgebra lineal, cada pieza tiene una matriz 4x4 que define su posición y rotación en el espacio tridimensional, cada pieza inicia con una matriz identidad [1,0,0,0,0,1,0,0,0,0,1,0,0,0,0,1] y se le asigna la posición individual modificando solo los componentes de traslación de la matriz, para cada giro de las capas en tiempo real simplemente se realiza una multiplicación de matrices en grupo: $M_{cubelet} \times R_{angle}$, donde $R_{angle}$ representa la matriz de rotación del ángulo de arrastre, cada rotación se aplica mediante las fórmulas fundamentales:
$$
R_x(\theta) = 
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & \cos\theta & -\sin\theta & 0 \\
0 & \sin\theta & \cos\theta & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$


