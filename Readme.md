<p align="center"><img src="https://raw.githubusercontent.com/carjavi/3d-studio-max-guide/master/img/3ds_max.jpg" height="100" alt=" " /></p>
<br>
<h1 align="center">3D Studio Max Guide</h1> 
<h4 align="right">Dic 22</h4>

<img src="https://img.shields.io/badge/OS-Windows%2011-blue">
<br>

# Hotkeys

## Básicos
Q = mouse normal <br>
Botón derecho del Mouse sueltas los botones que uno activa en los menús<br>
CTRL + Z = deshacer<br>
CTRL + N  = mueva escena<br>
Ctrl + L = Activa o desactiva la luz del visor <br>

## Manipulación de objetos
CTRL+ P = la manito <br>
R = escalar<br>
W= mover<br>
E = rotar<br>
H = seleccionar objeto por nombre<br>
SHIFT = pisado permite clonar objetos y key de animación<br>
ALT + E = extruir<br>

## Vistas
Para acercar suavemente a un objeto, poner la lupa y  tener pisado botón izquierdo y mover el mouse<br>
F2 = muestra las caras seleccionadas con el mouse<br>
F3 = vista de alambre o caras<br>
F4 =  ver alambre y caras<br>
T = vista superior<br>
U = isometría (sin perspectivas, todos misma medida)<br>
F = vista frontal<br>
L = vista izquierda<br>
Z = enfocar Objeto <br>
C = vista de la cámara<br>
B = vista por debajo<br>
I = centrar cámara<br>
O = ver caja del objeto <br>
P = perspectiva<br>
A = rotar ángulos exactos<br>
G = rejilla <br>
S = magnetizar una rejilla (para mover un objeto con respecto a la rejilla) <br>
ALT + W = aumenta la vista<br>
SHIFT + F = ver zona de seguridad<br>
CTRL+ C = te crea una cámara en vista de perspectiva<br>
SHIFT + Z = regresa a la vista anterior<br>

## Para agregar efectos 
M = materiales<br>
8 =  modificar fondo (aquí se puede poner una imagen o videos en el fondo)<br>
9 = configuración de efectos de luz<br>

## Animación
N = key auto<br>

### Configuraciones
En la parte superior donde dice la vista que tiene, con el botón derecho se puede reconfigurar las vistas.

 ### Para seleccionar un objeto por el material.
Cuando un material esta asignado a un objeto aparecen unos triángulos en las esquinas del material. Con el botón derecho “Select Objet”
<br>
<br>

# Guía Rápida de 3D Studio Max 
-	Clonar o copiar una geometría:
W / botón izquierdo del mouse pisado y mover

-	Agregar un video o foto de fondo:
8/environmet/use map/none/bitmap (elegir foto o video). Para hacer que la foto sea visible en el viewport es mejor arrastrar la foto al viewport. En el caso del video es mejor hacer un plano y proyectar el video allí, la velocidad de reproducción del video se controla en:
m/dynamics properties/ bounce coefficient: (puede variar 1/3,1/2,1,2 etc)

-	Hacer que los Objetos reflejen a otros:
m/mapas/refletion = raytrace, luego asignar al objeto.
Nota: el fondo influye en el brillo del objeto, con “8” ajustar  environment/background /color. 

-	Hacer perforaciones o cortar un polígono:
Seleccionamos en objeto al que queremos hacer una perforación, en CREAR GEOMETRIA, OBJETO DE DESCOMPOSICION, BOOLEANO, el botón DESIGNAR OPERADOR B, y le damos al objeto que queremos borrar y que deje la perforación.

-	Texto 3D:
Hacer texto, en modify/extruir o uvw map

- Objetos brillantes: 
En materiales:
Brillo metálico: 
Shader Basic parameters/anisotropic :( brillo vertical)
Anisotropic Basic parameters/Specular :(superficie de brillo)
Anisotropic Basic parameters/anisotropy: (grosor del brillo)
Nota: reflexión recomendada para los metales
m/canal de reflexión /bitmap/map/reflection/chromic o lake

- Plastico vidrio:
Shader Basic parameters/blinn: (brillo circular)
Blinn basic parameters/specular level: (superficie de brillo)
Blinn basic parameters/glossiness: (grosor del brillo)

-	Como introducir un objeto de otra escena u otro archivo:
File/Merge (objetos 3D) y file/Merge animation (objetos animados).

-	Importar archivos de Poser o AutoCad:
Copiar directamente al viewport

-	Como asignar material a un polígono por fuera y por dentro:
m/shader Basic parameters/2-sided

-	Como hacer objetos transparentes / imagen o efecto transparente:
m/blinn Basic parameters/opacity: (mientras menor es, mas transparente es)

-	Como hacer objetos transparentes como vidrio:
m/Blinn basic parameters/opacity = 0
ajustar:
Blinn basic parameters/specular level: (superficie de brillo)
Blinn basic parameters/glossiness: (grosor del brillo)
Nota: specular level= aprox.=120
En mapa refracción = raytrace=100 (refracción  es cuando vemos a través de un vidrio). Para mejorar la apariencia le colocamos en el canal de refracción = raytrace= aprox. Menos 10-50 
Nota: con una iluminación de luz cenital o skylight mejora la apariencia.
Para activar la Skylight pisamos 9 /select advanced lighting/Light trace/ ray/simple = 250 (con mas mejora la iluminación, con menos reduce la iluminación y le da un matizado de oscuridad a los objeto)
-	Para biselar y extruir fácilmente un objeto o unas letras:
Nota: Debería de ser algo grueso, sino no se va a ver bien la extruciòn. Convertir en malla editable seleccionar la cara y darle en “belen”.

<br>

## Cambiar de Motor de Render si no esta instalado el Pluing
Si no se tiene el motor de render adecuado no esta instalado lo mas seguro es que no se vea nada. Prueba esto:
1.	Ctrl + L activa  o desactiva la luz de la escena 
2.	Cambiar el motor de render. F10 /common/Assign Renderer/production
3.	Se debe cambiar todos lo materiales de la escena ya que se de debe usar los materiales del motor de render que elegiste.
<br>

## Desprender Maya (separar partes de un elemento sólido)
1er Método
1.	Convertir el objeto a polígono editable. Botón derecho “Convert to Editable Poly”
2.	F2 para ver el objeto en vista de alambre
3.	Seleccionamos por vértice si queremos desprender solo las esquinas del elemento. Selection/Edge (podemos seleccionar cada vértice con Ctrl pisado o marcamos varias esquinas y pisamos LOOP)
4.	después de tener la selecciona la parte que queremos desprender pisamos EDIT EDGES/SPLIT

Nota: Para texturizar el objeto todavía será un único elemento, para texturizar la parte desprendida hay que seleccionar el elemento SELECTION/POLYGON y pisar GROW, con esto seleccionáremos el polígono desprendido y podremos texturizarlo solo a este.

## TEXTURIZAR OBJETOS COMPLETOS
Método 1 (forma Automática)
1.	El Objeto debe ser un polígono Editable
2.	Con el objeto seleccionado Aplicamos Modificador UNWRAP UVW
3.	En PARAMETER/EDIT vemos la zona de trabajo para el mapeado
4.	Seleccionamos todo el objeto que nos muestra el visor
5.	MAPPING/FLATTEN MAPPING
6.	colocando una variación en el Angulo de FACE ANGLE THRESHOLD el programa desarmara el objeto en varias caras, dependiendo del valor. Mientras mas alto menos caras, y si es menor mas caras.

Método 2 (forma Manual)
7.	El Objeto debe ser un polígono Editable
8.	Con el objeto seleccionado Aplicamos Modificador UNWRAP UVW
9.	En PARAMETER/EDIT vemos la zona de trabajo para el mapeado
10.	Con la Herramientas de selección movemos y separamos las caras del objeto. 
11.	Seleccionamos todo y escalamos. 
12.	Movemos todas las caras hasta que entre en el cuadro de Mapeado
13.	En TOOL/RENDER UVW TEMPLATE
14.	Modificamos o dejamos el tamaño del render del mapeado. Para aceptar le damos  a GUESS ASPECT RATIO
15.	RENDER UV TEMPLANTE aquí nos da la imagen con el mapeado de la textura
16.	Guardamos para modificar con PhotoShop o cualquier otro programa.

<br>

## Unir objetos

Convertir en polígono editable

Render en archivos TGA (Objetos sin fondo) 
Si se rendea Archivos TGA en vez de un archivo AVI obtendremos un video sin fondo el cual podemos contrastar o componer con otro video. Para unir todas esas secuencias de fotos TGA se usa PREMIER. El video es de mejor calidad.

Nota: cuando se hace un video que tiene sombras sobre una pared o piso esas sombras no son completamente transparentes y se notan en el video final si se mezcla con otro video. Para solucionarlo la pared o piso debe tener una textura de MATTE SHADOW:
1.	Debemos Rendear con el motor de render METAL RAY REDERER
2.	Seleccionamos el objeto asignamos material (Get Material) MATTE/SHADOWS/REFLECTION
3.	Podemos rendear (F9) y en el DISPLAY ALPHA CHANNEL 
  
<br>

## PREMIER
Importar archivos TGA que vienen de 3D Studio
1.	Abrimos y creamos un archivo Estándar 32Khz y le ponemos Nombre
2.	Archivo/Importar buscamos la carpeta con los archivos TGA
3.	Seleccionamos el primer archivo numerado 000 y marcamos la casilla de IMÁGENES FIJAS NUMERADAS (automáticamente carga todas las secuencias de la animación)
4.	el archivo cargado lo pasamos a la línea de tiempo y pisando ENTER lo corremos


Archivos de alta calidad y poco peso Con Premier y Quick Time PRO
1.	Para guardarlo EXPORTAR/AJUSTES/TIPO DE ARCHIVO/ QUICK TIME
2.	Verificar que en la pestaña VIDEO el compresor sea ANIMATION. En esta pestaña también se modifica el tamaño del fotograma
3.	Salvamos la animación SAVE
4.	Abrimos con Quick Time Pro
5.	Exportar para web
6.	ahora si lo quieres en Flash hay que ver como coño se hace para que no pierda calidad

## MODIFICADORES

COMO DOBLAR UN FIGURA GEOMETRICA:
Modify/modifier/ bend

COMO DERRETIR UN FIGURA GEOMETRICA:
Modify/modifier/Melt
Nota: se puede derretir un cilindro para dar la impresión de que se riega por el piso.

EFECTO ONDA CIRCULARES EN EL AGUA:
Nota: para un mejor efecto se puede usar la tapa de un cilindro.

EFECTO ONDA ONDULNTES:

EFECTO BOMBA (en polígonos):

SUAVISAR (haciendo más polígonos):

EFECTO DE ILUMINACION:

LUZ VOLUMETRICA:

EFECTOS ESPECIALES DE LUZ:

LUZ CENITAL:

HACER OBJETOS CON AUTO-ILUMINACION:
m/blinn Basic parameters/self-ilumination: (aumentar)

HACER UNA ESCENA CON BASTATE EFECTO DE AUTO- ILUMINACION
(Produce un efecto aureola a todos los objetos en la escena)
Colocar los objetos con 100% de auto iluminación (los que queremos resaltar)
8/effects/add/blur (desenfocar)/píxel selections/
Whole image/brighten = aprox 9999
Blend% = aprox 5 a 25. ideal 15, si es menor menor sera la auto-iluminación de los objetos

NOTAS: para hacer que un objeto muestre 2 reflexiones colocar 2 fuentes de luz de colores diferentes, ejemplo ovni.


## Particulas

 Como hacer humo, agua, salpicaduras de líquidos, nubes, fuego etc.

### COMO CREAR LAS PARTICULAS:
Create/geometry/particles systems/ super Spray

Propiedades importantes:<br>
viewport display /porcentage of particle: cantidad de partículas que ves en el viewport, recomendado 100%
particle generation : <br>
particle Quantity /Use rate: cantidad de partículas<br>
particle Motion: velocidad y la variación sobre como va a salir la partícula<br>
particle Timing: para la animación de la partícula<br>
particle Timing/life: tiempo que va a durar la partícula en la escena<br>
particles type/ Estándar particles: partículas geométricas<br>
particles type/ Metaparticles: moléculas que se unen al chocar (agua, mercurio etc.) <br>
particles type/ instance geometry: cualquier figura geométrica editable (humo, nubes etc.)<br>


### AGUA, MERCURIO:
Crear particula tipo “Metaparticles”…

### HUMO por particulas:
Crear una esfera/canal opacity/falloff (atenuar)/swap colors (invertir colores en el mapa, lo hace con borde transparente) 
Crear particulas/tipo “instante geometry”
Instante parameter/pick object: tocar al objeto a transformase en partícula
Asignarle material a las partículas…

### NUBES y NIEBLA:
Create/helpers/atmospferic apparatus/object type: (crear el gizmo)
 Modify/ atmospheres & effects/add /volume fog (volume de niebla)/setup (configurar densidad, color etc.)

### FUEGO:
Create/helpers/atmospferic apparatus/object type: (crear el gizmo)
 Modify/ atmospheres & effects/add /fire effect/setup (configurar flama, explosion color etc.)<br>

## DEFLEXION, EFECTO DE GRAVEDAD, BOMBA, VIENTO EN PARTICULAS

### GRACEDAD:
Create/space warps/forces/gravity
Linkiar el efecto al gizmo  de partícula

### DEFLECTOR (chocar con un plano):
Create/space warps/forces/deflectors/deflector
Colocar el gizmo y linkiar  efecto al sistema  de partícula
Modify/deflector/bounce: (proporción de rebote)
Modify/deflector/friction: (hace que se peguen las partículas o que reboten del deflector)
Nota: no es rendeable.

### OBJETO GEOMETRICO DEFLECTOR:
Create/space warps/forces/deflectors/udeflector
Colocar gizmo y linkiar efecto al sistema de partículas
Modify/udeflector/pick object: (Seleccionar objeto donde van a rebotar las partículas)

### BOMBA en particulas:



<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="https://raw.githubusercontent.com/carjavi/markdown-guide/master/img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>