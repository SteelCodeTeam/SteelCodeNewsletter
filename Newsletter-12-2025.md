# SteelCodeNews(letter) #3 - Especial Diciembre 2025

¡Buenas!

El pasado mes no pude estar presente debido a la reciente muerte de un familiar debido un cancer. Aprovecho para comunicaros que el análisis mensual de los mercados volverá en enero de 2025 de forma especialmente extensa, analizando todo el año 2025 en perspectiva. Será un análisis completo que valdrá la pena la espera.

Dicho esto, esta edición de diciembre es especial. Vamos a profundizar en temas que me apasionan y que creo que son fundamentales para entender hacia dónde yo desearía ver el futuro de la tecnología: la verdadera libertad del software, el hardware libre, y el futuro de la inteligencia artificial como bien común.

Espero que disfrutéis esta edición y, como siempre, comentad vuestras impresiones por el canal general :)

---

## ⚖️ 1. Open Source vs Libre Software (Parte 2): Hablemos de licencias

El mes pasado hablamos de la diferencia filosófica entre FOSS y FLOSS. Este mes vamos al grano: **las licencias son el campo de batalla donde se decide quién controla realmente el software**.

### GPL: El Copyleft que Asusta a las Corporaciones

La **GNU General Public License (GPL)**, especialmente en su versión 3, es el arma nuclear del software libre. No es solo una licencia: es un **manifiesto político**. La GPL dice algo muy simple pero revolucionario: "Puedes usar, modificar y distribuir este software, pero **cualquier obra derivada debe mantener las mismas libertades**". 

Esto es el **copyleft**: usar el copyright contra sí mismo para garantizar la libertad. Y por eso las grandes corporaciones la odian.

**¿Por qué la GPL molesta tanto?**

Porque impide exactamente lo que las empresas quieren hacer: tomar código propietario, liberarlo tras una licencia "trampa", mejorarlo con contribuciones de la comunidad, y luego cerrar esas mejoras en productos privativos y venderlos. La GPL dice: "Si tomas, debes dar. Si mejoras, esas mejoras son para todos".

Ejemplo real: Linux usa GPL. Por eso Amazon, Google, y Microsoft no pueden simplemente tomar Linux, modificarlo, y venderte una versión cerrada. Tienen que devolver sus cambios a la comunidad. Esto no es altruismo, es la licencia obligándolos.

### MIT y BSD: El Caballo de Troya Corporativo

Las licencias permisivas como **MIT** y **BSD** son el sueño húmedo de las corporaciones. Te dan libertad total... incluyendo la libertad de quitarle libertades al código.

Bajo MIT/BSD puedes:
- Tomar el código
- Modificarlo
- Cerrarlo completamente
- Venderlo como software privativo
- No contribuir nada de vuelta

Apple hace esto constantemente. macOS está basado en Darwin (BSD). ¿Cuánto de las mejoras de Apple vuelven a BSD? Casi nada. Tomaron código libre y lo usaron para construir un jardín amurallado.

Ojo, no digo que MIT/BSD sean malas per se. Son útiles para bibliotecas que quieres que sean adoptadas masivamente. Pero llamémoslas por lo que son: licencias que facilitan la apropiación corporativa del trabajo comunitario.

### AGPL: La GPL para la Era del Cloud

La **Affero GPL (AGPL)** cierra un agujero que las corporaciones descubrieron en la GPL: la "laguna del SaaS".

Con GPL, si modificas software y lo ejecutas en tu servidor sin distribuirlo, no estás obligado a liberar tus cambios. Google hizo esto durante años: tomaba código GPL, lo modificaba para sus servicios internos, y nunca compartía nada porque técnicamente no lo "distribuía".

La AGPL cierra esto: **si alguien interactúa con el software a través de una red (como un servicio web), eso cuenta como distribución**. Debes liberar el código.

Por eso MongoDB cambió de AGPL a SSPL (Server Side Public License): empresas como AWS tomaban MongoDB, lo ofrecían como servicio, y no contribuían nada. La AGPL los habría forzado a liberar su infraestructura propietaria.

### Apache 2.0: El Pragmatismo Corporativo

La **Apache License 2.0** es el punto medio que muchas empresas prefieren. No es copyleft, pero tampoco es el "todo vale" de MIT/BSD.

Apache 2.0 te permite:
- Usar el código comercialmente
- Modificarlo sin liberar cambios
- Sublicenciar bajo otras licencias

**Pero** con obligaciones importantes:
- Debes mantener los avisos de copyright
- Debes indicar qué archivos modificaste
- **Concede automáticamente licencia de patentes**: si contribuyes código, otorgas licencia gratuita de cualquier patente relacionada

Este último punto es crucial. Apache 2.0 incluye una **cláusula de represalia de patentes**: si demandas a alguien por patentes relacionadas con el software, pierdes automáticamente tu licencia. Es una protección contra trolls de patentes.

¿Por qué proyectos como Kubernetes, Android, o Swift usan Apache 2.0? Porque permite adopción corporativa masiva sin el "miedo" al copyleft, pero mantiene protecciones mínimas contra guerras de patentes. Es el "mal menor" que las empresas aceptan para participar en proyectos open source sin comprometerse totalmente a GPL.


### La Elección es Política

Elegir una licencia no es técnico, es **político**:

- **GPL/AGPL**: "El código debe permanecer libre, siempre"
- **MIT/BSD**: "Haz lo que quieras, incluso apropiártelo"
- **Apache 2.0**: "Equilibrio entre libertad y adopción corporativa"

Yo soy claro en mi postura: para proyectos que quiero que permanezcan libres, uso **GPLv3**. Para bibliotecas donde busco adopción masiva, uso **Apache 2.0**. Nunca uso MIT/BSD en proyectos principales porque he visto demasiadas veces cómo el trabajo de la comunidad termina siendo un producto cerrado de alguna corporación.

**La libertad no se negocia. Y las licencias son el contrato que la garantiza.**

---

## 🔧 2. Hardware Libre: La Revolución Silenciosa

Si el software libre es importante, el **hardware libre es crítico**. Porque de nada sirve tener software libre si el hardware que lo ejecuta es una caja negra controlada por corporaciones.

### El Problema de las Licencias en Hardware

Aquí viene la parte compleja: **la GPL fue diseñada para software, no para hardware**. Y aplicarla a hardware tiene limitaciones importantes.

La GPL protege el **diseño** (los esquemas, los archivos CAD, el código HDL), pero no puede controlar qué hace alguien con el hardware físico que fabrica. Es decir:

- Puedes licenciar un diseño de placa bajo GPL
- Alguien puede fabricar esa placa, modificarla, y venderla
- **No están obligados a liberar sus modificaciones** si solo venden hardware, no diseños

Esto es porque la GPL está basada en copyright, y el copyright cubre obras expresivas (diseños, código), no objetos físicos.

### Soluciones: Licencias Específicas para Hardware

Por eso surgieron licencias específicas como:

**CERN Open Hardware License (OHL)**
- Creada por el CERN (sí, los del LHC)
- Tres versiones: Permissive, Weakly Reciprocal, Strongly Reciprocal
- La versión "Strongly Reciprocal" intenta lograr un copyleft similar a GPL

**TAPR Open Hardware License**
- Creada por la comunidad de radioaficionados
- Intenta cubrir tanto copyright como patentes
- Requiere que distribuidores de hardware proporcionen documentación

Pero la realidad es que **el hardware libre está en un terreno más complicado que el software**. Fabricar hardware cuesta dinero, requiere cadenas de suministro, y las patentes son más relevantes que el copyright.

### El Verdadero Hardware Libre: Casos Reales

A pesar de las dificultades, hay proyectos increíbles:

**RISC-V**
La arquitectura de procesadores completamente abierta. No es GPL (es un estándar abierto), pero representa lo que necesitamos: procesadores que cualquiera puede fabricar sin pagar royalties a Intel o ARM.

**Arduino** (con matices)
Los diseños son Creative Commons, el software es GPL/LGPL. Pero cuidado: el nombre "Arduino" es marca registrada. Puedes fabricar clones (y de hecho hay cientos), pero no llamarlos "Arduino oficial".

**Framework Laptop**
Aunque no es totalmente "libre" en el sentido GPL, es reparable, modular, y con documentación abierta. Es un paso en la dirección correcta a mi parecer.

**Coreboot / Libreboot**
Firmware libre para la BIOS. El BIOS es el software que arranca antes de tu sistema operativo, y en la mayoría de ordenadores es completamente privativo. Coreboot es una alternativa libre que te permite tener el control de lo que pasa en tu pc.

### ¿Por Qué Importa?

Imagina que tienes un ordenador. El hardware tiene **firmware** (software grabado en chips). Si ese firmware es privativo:

- No sabes qué hace realmente
- Puede tener puertas traseras
- No puedes auditarlo por seguridad
- Dependes del fabricante para actualizaciones

Con hardware libre y firmware libre (GPL):
- Puedes auditar todo el código
- Puedes modificarlo
- No dependes de nadie
- **Soberanía tecnológica real**

La FSF (Free Software Foundation) tiene una política clara: solo compran hardware que soporte **Libreboot** (firmware GPL para BIOS). Porque de nada sirve GNU/Linux si tu BIOS es una caja negra de Intel.

### El Futuro del Hardware Libre

El hardware libre está creciendo, pero enfrenta enormes desafíos:

**Ventajas:**
- Diseños auditables por seguridad
- Sin obsolescencia programada
- Reparable y modificable
- No dependencia de fabricantes únicos

**Desafíos:**
- Costos de fabricación
- Economías de escala favorecen a gigantes
- Patentes más problemáticas que en software
- Cadenas de suministro complejas

Pero cada placa Arduino clonada, cada procesador RISC-V fabricado, cada laptop reparable vendida... es un golpe contra el monopolio del hardware privativo.

**La batalla por la libertad tecnológica se gana también en el hardware.**

---

## 🤖 3. IA: ¿Futuro Común o Feudalismo Digital?

La inteligencia artificial está en cada rincon de internet hoy dia. Y la pregunta no es técnica, es política: **¿Quién controlará la IA del futuro?**

### El Presente: Feudalismo de la IA

Ahora mismo vivimos en un **feudalismo digital de la IA**:

**Los Señores Feudales:**
- OpenAI/Microsoft: GPT-4 y superiores, completamente cerrados
- Google: Gemini, parcialmente cerrado
- Anthropic: Claude, cerrado

**Los Siervos:**
- Nosotros. Usando sus APIs, pagando por tokens, sin acceso real al modelo, y con los sesgos propios de sus creadores.

La situación es perversa: estas empresas **entrenan con datos públicos** (internet entero, incluyendo código GPL, contenido CC, y en casos mas concretos, contenido protegido con Copyrigth inclusive sin tener permiso previo, etc.), pero los modelos resultantes son **propiedad privativa**.

Es como si alguien tomara toda Wikipedia, la procesara, y luego te cobrara por acceder a ese conocimiento procesado. Wikipedia es CC-BY-SA (copyleft), pero GPT-4 que se entrenó con Wikipedia es privativo.

### El Modelo Corporativo: Extractivismo de Datos

El modelo de negocio actual es **extractivismo puro**:

1. Toman datos públicos, esten o no protegidos por una licencia (gratis para ellos)
2. Usan poder computacional masivo (barato a su escala)
3. Entrenan modelos
4. **Cierran los modelos**
5. Te cobran por usarlos
6. Tú generas más datos usándolos
7. Vuelven al paso 1

Es un ciclo de acumulación donde **el conocimiento público se privatiza**.

Y lo peor: ni siquiera puedes auditar qué hacen estos modelos. ¿Tienen sesgos? ¿Censuras políticas? ¿Puertas traseras? No lo sabes. Es una caja negra que te dice "confía en nosotros".

### La Alternativa: IA Distribuida y Comunitaria

Ahora imaginemos un mundo diferente. Un mundo donde la IA funciona como **Linux**, no como Windows.

#### Características de una IA Verdaderamente Libre:

**1. Modelos Abiertos y Auditables**
- Pesos del modelo publicados (como hacer código fuente disponible)
- Datasets de entrenamiento documentados
- Arquitectura completamente pública
- Licencia copyleft (AGPL para los servicios, GPL para el código)

**2. Entrenamiento Distribuido**
En lugar de un datacenter de OpenAI, imagina:
- Miles de personas aportando poder computacional (como BOINC o Folding@home)
- Sistema de incentivos basado en contribución
- Sin necesidad de infraestructura centralizada masiva

**3. Propiedad Colectiva**
- El modelo pertenece a la comunidad que lo entrenó
- Gobernanza democrática sobre evolución del modelo
- Sin empresa única que pueda "cerrar" el modelo

**4. Inferencia P2P**
- No llamar a una API de OpenAI
- Red distribuida donde múltiples nodos pueden ejecutar inferencia
- Como BitTorrent pero para consultas a IA
- Resistente a censura y control centralizado

#### ¿Cómo Funcionaría en la Práctica?

Imagina este escenario:

**Fase 1: Entrenamiento Colaborativo**
- Un protocolo abierto define arquitectura y objetivos
- Miles de participantes aportan GPUs en tiempo no usado. (Como los malwares cuando bajas pelis piratas, pero de forma voluntaria)
- Sistema de tokens/reputación como recompensa por contribuciones
- Dataset es público, auditable, y filtrado por la comunidad, permitiendo agregar datos o eliminar datos revisado por pares.
- Cada iteración del modelo se publica bajo AGPL

**Fase 2: Distribución P2P**
- El modelo final se distribuye en fragmentos (sharding)
- Diferentes nodos almacenan diferentes partes
- Para hacer una consulta, contactas nodos que pueden procesarla
- Sistema de caché distribuida acelera respuestas comunes
- Como Kademlia/DHT pero para modelos de IA

**Fase 3: Mejora Continua**
- Usuarios pueden proponer mejoras al modelo
- Votación comunitaria decide qué mejoras integrar
- Fine-tuning distribuido para especialización
- Sin punto único de control o censura

### ¿Por Qué Esto No Existe Aún?

**Desafíos económicos (o cómo el capitalismo sabotea lo colectivo):**
- ¿Quién o Cómo paga la electricidad inicial?
- Competir con gigantes financiados por Capitales financieros que usan tus datos para generar beneficios y que pueden quemar millones en pérdidas hasta monopolizar es increiblemente complicado.

**Desafíos políticos (la guerra sucia, otra vez):**
- Regulaciones escritas por lobbies corporativos para favorecer centralización
- Presión política para prohibir alternativas bajo excusas de "seguridad"

**La historia se repite:**

Esto ya lo vivimos con Linux vs Windows en los 90. Microsoft lanzó una campaña de FUD (Fear, Uncertainty, Doubt): "Linux es inseguro", "Linux es comunista", "nadie da soporte". Ejecutivos de Microsoft llamaron a Linux "cáncer" públicamente.

¿El resultado? Linux no solo sobrevivió, sino que **ganó**: hoy domina servidores, Android, supercomputadoras, internet. Microsoft tuvo que rendirse y ahora "ama" Linux (porque no le queda otra).

En el sistema actual, las grandes corporaciones tratan de impedir cualquier proyecto comunitario porque no puede monetizarlos. Y cuando no puede monetizar, intenta destruir. Pero la historia demuestra que **lo que se construye colectivamente es más fuerte que lo que se acumula corporativamente**.

### La Pregunta Fundamental

**¿La IA será la próxima internet (descentralizada, abierta, resistente)?**
**¿O será la próxima televisión (centralizada, controlada, unidireccional)?**

La respuesta no es técnica. Es política y social.

Si permitimos que OpenAI, Google, y Microsoft monopolicen la IA, habremos entregado el futuro de la cognición artificial a tres corporaciones estadounidenses.

Si luchamos por IA libre, distribuida, y comunitaria, podemos tener un futuro donde **todos controlemos estas herramientas, no al revés**.

**La IA no tiene que ser feudalismo digital. Puede ser commons digital.**

Pero tenemos que construirlo. Y tenemos que hacerlo ahora, antes de que sea demasiado tarde.

---

## 🎄 4. ArnoldC: Programando como el Terminator en Navidad

Después de tanta seriedad política y tecnológica, es momento de reírnos un poco. Y qué mejor manera que con **ArnoldC**, un lenguaje de programación completamente funcional... basado en frases de Arnold Schwarzenegger.

### ¿Qué demonios es ArnoldC?

ArnoldC es un **lenguaje esotérico** creado por Lauri Hartikka donde **cada palabra clave es una frase icónica** de las películas de Schwarzenegger. Y sí, es completamente funcional. Compila a bytecode de Java y puedes escribir programas reales con él.

**Algunos ejemplos de sintaxis:**

| Concepto | Código Normal | ArnoldC |
|----------|--------------|---------|
| main | `int main()` | `IT'S SHOWTIME` |
| fin main | `}` | `YOU HAVE BEEN TERMINATED` |
| declarar variable | `int x = 0` | `HEY CHRISTMAS TREE x`<br>`YOU SET US UP 0` |
| print | `print()` | `TALK TO THE HAND` |
| true | `true` | `NO PROBLEMO` |
| false | `false` | `I LIED` |
| while | `while` | `STICK AROUND` |
| end while | `}` | `CHILL` |
| if | `if` | `BECAUSE I'M GOING TO SAY PLEASE` |
| else | `else` | `BULLSHIT` |
| +1 | `x++` | `GET UP` |
| -1 | `x--` | `GET DOWN` |
| * | `a * b` | `YOU'RE FIRED` |
| / | `a / b` | `HE HAD TO SPLIT` |

### Conexión Navideña

Y aquí viene lo mejor para esta newsletter de diciembre: **para declarar variables en ArnoldC usas "HEY CHRISTMAS TREE"** (oye árbol de navidad). ¿Por qué? Porque en "Jingle All The Way" (1996), Arnold hace esa escena icónica discutiendo con un árbol de navidad.

### Ejemplo: Hello World

```arnoldc
IT'S SHOWTIME
TALK TO THE HAND "hello world"
YOU HAVE BEEN TERMINATED
```

Cada programa es como un mini guion de acción. Y me parece increible.

### Ejemplo: Contador Navideño

Vamos a hacer algo más interesante: contar hasta 10.

```arnoldc
IT'S SHOWTIME
HEY CHRISTMAS TREE isLessThan10
YOU SET US UP @NO PROBLEMO
HEY CHRISTMAS TREE n
YOU SET US UP 0
STICK AROUND isLessThan10
    GET TO THE CHOPPER n
    HERE IS MY INVITATION n
    GET UP 1
    ENOUGH TALK
    TALK TO THE HAND n
    GET TO THE CHOPPER isLessThan10
    HERE IS MY INVITATION 10
    LET OFF SOME STEAM BENNET n
    ENOUGH TALK
CHILL
YOU HAVE BEEN TERMINATED
```

Traducido sería algo como:
```
¡ES HORA DEL ESPECTÁCULO!
OYE ÁRBOL DE NAVIDAD esMenorQue10
TÚ NOS CONFIGURASTE VERDADERO
OYE ÁRBOL DE NAVIDAD n
TÚ NOS CONFIGURASTE 0
QUÉDATE POR AHÍ mientras esMenorQue10
    VE AL HELICÓPTERO n
    AQUÍ ESTÁ MI INVITACIÓN n
    LEVÁNTATE 1
    SUFICIENTE CHARLA
    HABLA A LA MANO n
    VE AL HELICÓPTERO esMenorQue10
    AQUÍ ESTÁ MI INVITACIÓN 10
    DESAHÓGATE BENNETT n
    SUFICIENTE CHARLA
RELÁJATE
HAS SIDO TERMINADO
```

### ¿Por Qué Lenguajes Esotéricos?

Los lenguajes esotéricos como ArnoldC no son prácticos para producción, pero son **valiosos** por varias razones:

**1. Cuestionan Convenciones**
Nos hacen preguntarnos: ¿por qué usamos "if" y no "PORQUE VOY A DECIR POR FAVOR"? ¿Qué hace que una sintaxis sea "buena"?

**2. Educación**
Entender cómo funciona ArnoldC (que compila a bytecode Java) te enseña sobre compiladores, parsers, y AST de forma divertida.

**3. Arte Conceptual**
Son **software art**. Como Piet (el lenguaje que vimos en octubre), son expresiones artísticas que usan código como medio.

**4. Diversión**
Porque programar también debe ser divertido. Y hay algo hilariante en escribir `BULLSHIT` en lugar de `else`.


### Conclusión Festiva

En un mundo donde la tecnología se vuelve cada vez más seria, corporativa, y cerrada... es importante recordar que **programar puede ser juego, arte, y diversión**.

ArnoldC nos recuerda que el código no es solo para resolver problemas empresariales. Es un medio de expresión. Y a veces, esa expresión es gritar "GET TO THE CHOPPER!" mientras sumas dos números.

**¡Felices fiestas, y que la fuerza del copyleft os acompañe!**

---

## 🧱 5. Progresos del Equipo

En esta edicion de la newsletter hay mucho que comentar, vayamos por partes.

- **Metallics Arts**: Empezamos el port a NeoForge 1.21.10. Estos dos meses hemos empezado el port, creado la generacion de mundo, los items basicos y los poderes alomanticos. ¡Estamos avanzando super rapido para estar reescribiendo todo el mod desde 0!

- **Newsletters**: He creado un rol para los interesados en las newsletter. Tambien quería haceros llegar, que lo que se expresa en esta newsletter es *MI* vision del mundo, y no la del equipo en su conjunto, ya que soy yo la persona que hace esto.

- **Ready Crossbow**: Hemos lanzado un nuevo mod sencillo, simple, y funcional. Cualquier mob que use una ballesta aparecerá con ella cargada. ¿Quien va a la guerra con la ballesta sin cargar? 

- **Simple Auths**: He estado trabajando un poco mas en el, realizando temas de logs para administradores, pero no ha sido un avance sustancial (que no llegará hasta terminar el port de Metallics Arts)

- **Proyectos Personales**: Hoy, aunque no pertenece al equipo quiero comentaros que estoy inmerso en otro proyecto (¡Soy Secretario de Nuevas Tecnologias de uno de los sindicatos de mi region desde el pasado mes!), he estado automatizando generacion de imagenes y redes sociales, si os interesa, os puedo compartir los proyectos.

- **Comunidad**: Quiero desearos a todos unas felices fiestas y que paseis unas fiestas fantasticas. Espero veros por el chat charlando tranquilamente estos dias con mas tiempo libre :D.

---

**¡Gracias por leer esta edición especial de SteelCodeNews!**

Ha sido una newsletter más larga de lo habitual, pero creo que estos temas merecían la profundidad. En enero volveremos con el análisis extenso de mercados 2025 y más contenido técnico.

Mientras tanto, os dejo con una reflexión: **Cada línea de código bajo GPL, cada diseño de hardware abierto, cada modelo de IA liberado... es un acto de resistencia contra el monopolio corporativo de la tecnología.**

Y esa resistencia se construye colectivamente, con comunidad, no con individualismo.

**Nos vemos en 2025. Que sea un año de código libre, hardware abierto, y mods libres para vosotros.**

*— Rubén*
