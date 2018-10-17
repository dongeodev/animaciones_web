# Animaciones web
Apuntes del curso de animaciones para la web de Platzi

## Sintaxis de transiciones
###### clase 3


 <code> transition-property: width, height;</code> / Qué propiedades va a cambiar en la transición
 

<code> transition-duration: 1s;</code> / Cuánto tiempo va a durar la transición


<code>transition-delay: 250ms;</code> / Cuánto tiempo va a tardar la transición en ocurrir


<code> transition-timing-function: ease; </code> / Función que determina de qué forma se calculan los valores intermedios de la transición

<code> transition: width 1s 250ms ease, height 1s 250ms ease; </code> / Cada propiedad a cambiar se separa con una coma


## Sintaxis de Transformaciones
###### clase 5


 <code> transform: rotate(deg) skew(deg) traslate(px) scale(0-1);</code> 
 rotate: rotar elemento    
 sesgar: inclina el elemento
 posicion: mueve el elemento
 escala: cambia el tamano (%)
 
 
 ## Transformaciones de rotación
###### clase 6


<code>transform: rotateX(45deg);</code> / Rotación en el eje X 

<code>transform: rotateY(45deg);</code> / Rotación en el eje Y

<code>transform: rotate(-45deg);</code> / Rotación a lado contrario de las manecillas del reloj 

<code>transform: rotateX(45deg) rotateY(45deg) rotateZ(45deg);</code> / Animación de transformaciones 

<code>transform: rotate3d(x,y,z,rotate); </code> / Rotación en 3D, se coloca 1 en los grados que se desea girar 

<code>transform: rotate3d(1,0,0,45deg);</code>   / Rotación en el eje X 

<code>transform: rotate3d(0,1,0,45deg);</code> / Rotación en el eje Y


 ## Transformaciones de traslación y perspectiva
###### clase 6

<code> perspective: 200px;</code> 
<code> perspective-origin: X Y;</code>
<code> perspective-origin: top right;</code> / mueve el punto de referencia para la perspectiva

<code> transform: traslate (xy);</code>
<code> transform: traslate (x , y);</code>
<code> transform: traslateX (px);</code>
<code> transform: traslateY (px);</code>
<code> transform: traslateZ (px);</code>
<code> transform: traslate3d (x , y , z);</code>

## Transformaciones de escala
###### clase 7

<code> transform: scale (xy);</code>
<code> transform: scale (x , y);</code>

