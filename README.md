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

<br><code> transform: traslate (x);</code></br>
<br><code> transform: traslate (x , y);</code></br>
<br><code> transform: traslateX (px);</code></br>
<br><code> transform: traslateY (px);</code></br>
<br><code> transform: traslateZ (px);</code></br>
<br><code> transform: traslate3d (x , y , z);</code></br>

## Transformaciones de escala
###### clase 7

<br><code> transform: scale (xy);</code></br>
<br><code> transform: scale (x , y);</code></br>


## Transformaciones de sesgados
###### clase 8

<br><code> transform: skew (x);</code></br>
<br><code> transform: skew (x , y);</code></br> / skew(deg)

## Punto de transformación
###### clase 10

<br><code>transform-origin: x , y ; </code> / cambia el punto de referencia para la animacion</br>
<br><code> transform-origin right, top;</code></br>

## Sintaxis (animation)
###### clase 11

<br><code> animation-name: [nombre];</code> / Se coloca un nombre al elemento que se quiere animar</br>
<br><code> animation-delay: 1000ms;</code> / tiempo que tarda en ejecutarse la animacion desde que carga o es acitvada</br>
<br><code> animation-duration: 1s ;</code>/ tiempo que dura 1 ciclo de la animacion</br>
<br><code> animation-direction: [reverse,alternate];</code> / en que sentido se ejecuta la animacion.</br>
<br><code> animation-iteration-count: [#, infinite];</code> / define cuantas veces se repite el ciclo de animacion</br>
<br><code> animation-timming-funtion: [ease, ease-in, ease-out, ease-in-out, linear, steps(#), cubic-bezeir(1,1,1,1)] ;</code> / define si la animacion entra o sale suavizada (aceleracion)</br>
<br>ease: por defecto</br>
<br>ease-in: se suaviza al entrar o al inicio</br>
<br>ease-out: se suaviza al salir o al finalizar</br>
<br>ease-in-out: se suaviza al entrar y salir, básicamente se acelera solo la mitad de la animación</br>

<br><code> animation-play-state: [running, paused];</code> / permite pausar o iniciar una animacion</br>
<br><code> animation-fill-mode: [forward];</code> / fija en que estado quedara la animacion despues de ocurrir</br>


## Aceleración y curva de bezier
###### clase 12


cubic-bezier.com /para personalizar la curva
<br><code> animation-timming-funtion: cubic-bezeir(1,1,1,1);</code> / Se puede jugar con los valores para generar efectos como el rebote (aceleracion)</br>

## Multiples Animaciones
###### clase 13

<br><code> animation-name: [nombre1], [nombre2];</code> / Se coloca un nombre al elemento que se quiere animar</br>

Cada animacion tiene su keyframe donde se colocan las carcteristicas ha animar 

## Detectar eventos de animaciones CSS desde JS
###### clase 14

<br><code><script></code></br>
   <br><code> const $cuadrado = document.getElementById('cuadrado');</code> </br>
   <br><code> // $cuadrado.addEventListener('nombre del event', 'que hago cuando el evento ocurra') </code></br>
   <br><code> // $cuadrado.addEventListener('animationstart', (event) => { </code></br>
   <br><code> // $cuadrado.addEventListener('animationiteration', (event) => { </code></br>
   <br><code> $cuadrado.addEventListener('animationend', (event) => { </code></br>
    <br><code>  // console.log(event.animationName); </code> </br>
   <br> <code>  if (event.animationName === 'rebote') { </code></br> 
    <br>  <code>  $cuadrado.style.animationName = 'cuadrado escalera'; </code></br>
    <br> <code>   $cuadrado.style.animationDuration = '3s';</code></br> 
    <br> <code> }</code></br>
   <br> <code>});</code> </br>
 <br> <code></script></code></br>

## Optimizar render con will-change y developer tools
###### clase 15

 <br> <code>will-change: opacity, transform;</code></br>
 will-change se usa para avisar al navegador que una propiedad va a cambiar. las transformaciones y la opacidad estan optimizadas en los navegadores por eso conviene usa will-change
 
 
## Propiedades animables
###### clase 16
 
 https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

 
## element.animate
###### clase 17

Es el api de JS para escribir las animaciones en JS

 <script>
    const $pelota = document.getElementById('pelota');

    // element.animate(keyframes = [], option = {})
    const animation = $pelota.animate([
      // from
      {
        transform: 'translateX(0)'
      },
      // to
      {
        transform: 'translateX(500px)' // 250
      }
    ],{
      duration: 1000,
      delay: 1000,
      direction: 'normal',
      easing: 'linear',
      iterations: Infinity,
      fill: 'forwards',
      iterationStart: .5, // = 50%
      // endDelay: 5000,
    })
  </script>
