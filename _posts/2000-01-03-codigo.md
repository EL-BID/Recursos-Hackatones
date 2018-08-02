---
title: "codigo"
bg: green 
color: blue
fa-icon: code
---

# Código Abierto

### Reutiliza las soluciones digitales disponibles en el catálogo de Código para el Desarrollo


-**[MapMap](http://code.iadb.org/es/repositorio/45/mapmap)** 
Aplicación móvil para mapear rutas.
[Reutiliza el código aquí](https://github.com/codeandoxalapa/mapmap) 

-**[GMapdistance](http://code.iadb.org/es/repositorio/57/gmapsdistance)** 
Calcula la distancia y tiempo de recorrido  entre millones de puntos
[Reutiliza el código aquí](https://github.com/rodazuero/gmapsdistance)

-**[Consul](http://code.iadb.org/es/repositorio/47/consul)** 
Aplicación web de participación ciudadana abierta para gobiernos.
[Reutiliza el código aquí](https://github.com/consul/consul)

-**[Vota inteligente](http://code.iadb.org/es/repositorio/46/vota-inteligente)** 
Plataforma web de participación ciudadana.  
[Reutiliza el código aquí](https://github.com/ciudadanointeligente/votainteligente-portal-electoral) 

-**[SmartMap](http://code.iadb.org/es/repositorio/22/smartmap)** 
Plataforma web para el análisis y visualización de datos espaciales. 
[Reutiliza el código aquí](https://github.com/el-BID/SmartMap)

Consulta la totalidad del Catálogo de Código para el Desarrollo [aquí](http://code.iadb.org/es). 



### Utiliza estas soluciones recopiladas por nuestro equipo 

- #### [GitHub Student Developer Pack](https://education.github.com/pack)

Si eres estudiante, puedes usar gratuitamente a herramientas que son comunmente de paga, después de una rápida incripción recibirás un pack de permisos con los que podrás acceder a múltiples herramientas como AWS cloud, Carto, bitnami, etc.

¡Ten listo tu pack antes de la hackaton! [Aquí!](https://education.github.com/pack)

- #### [ngrok](https://ngrok.com/)

Pasa más tiempo programando. Con un comando puedes obtener una URL instantánea y segura para tu servidor localhost a través de cualquier NAT o firewall.

Lee la documentación [Aquí!](https://ngrok.com/docs)

- #### [Caffeine](http://lightheadsw.com/caffeine/)

Caffeine es un pequeño programa que pone un ícono en el lado derecho de la barra de menú. Hazle clic para evitar que tu Mac se apague automáticamente, oscureciendo la pantalla o iniciando protectores de pantalla. Cuando estés presentando tu demo tendrás todo controlado.

Descárgalo [Aquí!](http://lightheadsw.com/caffeine/)


- #### [Studio 3T](https://studio3t.com/)

Una GUI que hará que navegar MongoDB sea mucho más rápido y fácil.

Descárgalo [Aquí!](https://studio3t.com/download/)


- #### [Vagrant](https://www.vagrantup.com/)

Crea y configura entornos de desarrollo ligeros, reproducibles y portátiles. No estropees tu caja de desarrollo instalando todo tipo de cosas que pueden entrar en conflicto con tu configuración de desarrollo existente. En su lugar, use entornos dev usando Vagrant o incluso Docker.

No empieces de cero, busca tu box [Aquí!](https://app.vagrantup.com/boxes/search)

 <script>
var colors = new Array(
  [62,35,255],
  [60,255,60],
  [255,35,98],
  [45,175,230],
  [255,0,255],
  [255,128,0]);

var step = 0;
//color table indices for: 
// current color left
// next color left
// current color right
// next color right
var colorIndices = [0,1,2,3];

//transition speed
var gradientSpeed = 0.002;

function updateGradient()
{
  
  if ( $===undefined ) return;
  
var c0_0 = colors[colorIndices[0]];
var c0_1 = colors[colorIndices[1]];
var c1_0 = colors[colorIndices[2]];
var c1_1 = colors[colorIndices[3]];

var istep = 1 - step;
var r1 = Math.round(istep * c0_0[0] + step * c0_1[0]);
var g1 = Math.round(istep * c0_0[1] + step * c0_1[1]);
var b1 = Math.round(istep * c0_0[2] + step * c0_1[2]);
var color1 = "rgb("+r1+","+g1+","+b1+")";

var r2 = Math.round(istep * c1_0[0] + step * c1_1[0]);
var g2 = Math.round(istep * c1_0[1] + step * c1_1[1]);
var b2 = Math.round(istep * c1_0[2] + step * c1_1[2]);
var color2 = "rgb("+r2+","+g2+","+b2+")";

 $('#codigo').css({
   background: "-webkit-gradient(linear, left top, right top, from("+color1+"), to("+color2+"))"}).css({
    background: "-moz-linear-gradient(left, "+color1+" 0%, "+color2+" 100%)"});
  
  step += gradientSpeed;
  if ( step >= 1 )
  {
    step %= 1;
    colorIndices[0] = colorIndices[1];
    colorIndices[2] = colorIndices[3];
    
    //pick two new target color indices
    //do not pick the same as the current one
    colorIndices[1] = ( colorIndices[1] + Math.floor( 1 + Math.random() * (colors.length - 1))) % colors.length;
    colorIndices[3] = ( colorIndices[3] + Math.floor( 1 + Math.random() * (colors.length - 1))) % colors.length;
    
  }
}

setInterval(updateGradient,10);
</script>
