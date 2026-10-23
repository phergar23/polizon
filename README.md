# Polizón a Bordo

Juego 3D en primera persona, con estética de dibujos animados, sobre una tripulación que debe descubrir a los polizones escondidos en la nave Lucero. Funciona en el navegador, sin instalar nada.

## Cómo jugar

Abre `index.html` en el navegador (o la página de GitHub Pages del repositorio).

- **Crear partida:** de 1 a 10 jugadores, con opción de rellenar los huecos con NPCs y elegir cuántos polizones hay.
- **Modo práctica:** juegas solo, eligiendo ser tripulante o polizón, con NPCs quietos repartidos por la nave.
- **Unirse:** cada jugador entra desde su dispositivo con el código de 5 letras que aparece en la pantalla de quien crea la partida, o con el enlace de la sala que este puede copiar y enviar.

El multijugador conecta los dispositivos directamente entre sí con [PeerJS](https://peerjs.com/), sin servidor propio. Hace falta conexión a internet; en alguna red muy restringida (por ejemplo, algunas redes de empresa o de centros educativos) la conexión entre dispositivos puede no establecerse.

### Controles

| Ordenador | Móvil | Acción |
|---|---|---|
| W A S D + ratón | Joystick y arrastrar a la derecha | Moverse y mirar |
| E | Botón Usar | Hacer tareas, alcantarillas, cámaras, botón de emergencia |
| R | Botón Reportar | Reportar un cuerpo |
| Q | Botón Eliminar | Eliminar (polizón) |
| F | Botón Sabotear | Sabotear la nave (polizón) |
| M | Botón de mapa | Mapa de la nave |

En el móvil el juego se pone en horizontal automáticamente.

## Qué incluye

- Nave según un plano dibujado a mano: Comedor octogonal con el botón de emergencia en la mesa central, Sala de armas, Navegación, Observatorio, Administración, Comunicaciones, Reactor, Médico, Seguridad, Electricidad y Taquillas, unidas por pasillos con un cruce redondo y una zona de carga con cajas metálicas.
- 22 tareas con su propio objeto 3D y minijuegos animados.
- Polizones con alcantarillas que se recorren andando por conductos y sabotajes (luces, reactor, comunicaciones y cierre de puertas).
- Sala de Seguridad con cuatro cámaras en directo.
- Reuniones con chat, votación, recuento de votos y animaciones.
- NPCs que hacen tareas, arreglan sabotajes, reportan cuerpos y votan.
- El polizón tiene que esperar 25 segundos entre eliminación y eliminación.

Hecho con [Three.js](https://threejs.org/) r128. Personajes y nave de diseño original.

## Mapas

Al crear una partida o en el modo práctica puedes elegir el mapa:

- **Nave**: el mapa clásico, con pasillos, conductos y paseos espaciales.
- **Planeta Violeta**: una base densa en un planeta de suelo morado. Casi todo son bloques de salas pegadas con puertas interiores (Cúpula con Cocina, Dormitorios, Enfermería y Despensa; Electricidad, Taller, Almacén, Comunicaciones, Seguridad y Trastero; Laboratorio, Muestras, Invernadero y Bombas), con salas achaflanadas y un Observatorio octogonal. Pasillos-tubo con recodos llevan a dos torres apartadas y a la sala de Mando de la plaza central; el Hangar está solo, lejos del resto. Fuera el terreno es abierto, con lava, rocas, mesetas, cristales y fumarolas. Las alcantarillas son agujeros que bajan a túneles de roca, hay tormentas de polvo y el alien aterriza en dos plataformas.

Al cambiar de mapa la página se recarga. Si tus amigos se unen a una sala con otro mapa, su juego cambia solo al mapa de quien la ha creado.

## Roles especiales

Al crear la partida, el botón **Elegir** de "Roles especiales" abre un menú para activar los roles. Cada rol activado lo recibe un jugador al azar de su bando. La habilidad se usa con la tecla **C** (o el botón de habilidad en móvil).

**Tripulación**
- **Ingeniero**: puede viajar por las alcantarillas y reparar un sabotaje a distancia una vez por partida.
- **Mecánico de puertas**: cierra o abre las puertas de la sala más cercana (también las saboteadas).
- **Detective**: ve durante 8 s las huellas de colores que deja cada jugador.

**Polizón**
- **Cambiaformas**: copia el aspecto del jugador más cercano durante 15 s.
- **Fantasma de conductos**: salta entre todas las redes de conductos y las cámaras no le ven.
- **Limpiador**: hace desaparecer cuerpos para que nadie los reporte.
- **Araña**: anda pegada al techo durante 20 s mirando hacia abajo; solo se la ve mirando hacia arriba (ni las cámaras la ven) y desde arriba no puede eliminar.

Tras usar una habilidad hay que esperar a que se recargue: Mecánico 25 s, Detective 30 s, Cambiaformas 35 s, Fantasma 15 s, Limpiador 20 s y Araña 45 s. Al empezar la partida todas tardan 12 s en estar listas. El Ingeniero solo puede reparar a distancia una vez.

En el modo práctica también se puede elegir un rol especial para probar su habilidad.

## El Alien (rol aparte)

Se activa en el menú de roles (grupo "Rol aparte") y se puede probar en el modo práctica. No es tripulante ni polizón: **gana si quedan 2 o menos supervivientes** mientras su platillo siga entero.

El alien camina por su propia nave, de dos salas:

- **Puente**: los **mandos** para pilotar el platillo alrededor de la nave (R para levantarse) y una mesa con el holograma de la nave principal.
- **Sala de mecánicas**: el **teletransportador** (con el platillo acoplado a una esclusa, entra 30 s en la nave y puede eliminar a una sola persona), el **rayo tractor** (abduce a quien esté fuera), la consola de **sabotajes** (pulso EMP, antigravedad, interferencias), el **ariete** (embiste la nave: a todos les tiembla la pantalla y se les cierra la tarea) y los tubos con sus víctimas.

Para pararle, cualquiera puede usar el **cañón de defensa** de la Sala de armas: tres impactos y el platillo queda destruido.

Su nave ahora es más grande: puente de mando, sala central, **hangar de drones**, **arsenal** e **incubadora**, unidas por portales redondos.

- **Dron espía**: vuela 15 s dentro de la base principal (los demás ven el dron).
- **Lluvia de meteoritos**: caen meteoritos con aviso; en el planeta aturden 4 s a quien pille fuera.
- **Hipnosis**: eliges a alguien y durante 7 s se le invierten los controles.
- **Clon señuelo**: suelta en la base un clon de una víctima que camina solo y revienta si alguien lo toca.
- **Pilotaje**: cámara en tercera persona con inclinación en las curvas, estelas de velocidad, campo de visión que se abre al acelerar y un panel con radar, velocidad y altura. Con **V** cambias a la vista desde la cabina.

## El Asesino en serie (rol aparte)

Va por libre: puede eliminar a cualquiera, tripulantes y polizones, con su cuchillo (Q). Gana si se queda solo.

- **Guarida**: durante las votaciones puede entrar en su guarida (y volver a votar cuando quiera). Allí elige **arma** en el armero, marca a su **víctima** en el tablero de fotos con hilos rojos y escoge en la mesa del mapa **en qué sala aparecerá** en la siguiente ronda. En la sala de trofeos guarda un casco por cada víctima.
- **Armas** (un uso por ronda, tecla C): ballesta (dispara a 8 m), cepo (trampa que solo ve él), bomba de humo (dentro nadie ve y él desaparece) y máscara (se disfraza de otro 20 s).
- **Víctima marcada**: la ve con un anillo rojo y parpadea en su minimapa. Si la elimina, entra en **frenesí**: corre más y el cuchillo se recarga antes.
- **Carta negra**: junto a sus víctimas deja una carta, así se sabe que no ha sido un polizón.

## Sabotajes especiales

- **Gravedad cero**: todos flotan por la nave con inercia y rebotan contra paredes, suelo y techo. Se arregla reiniciando el generador del Observatorio (o vuelve sola a los 40 s).
- **Apagón total**: todo queda a oscuras y cada tripulante solo ve con su linterna; se ven los haces de luz de los demás. Se arregla en el panel de luces.

## Paseos espaciales

En la **Sala de armas** y en **Taquillas** hay una **esclusa**. Al usarla sales al espacio atado a una cuerda de 24 m:

- Flotas en gravedad cero: avanzas hacia donde miras (en ordenador, Espacio sube y Mayúsculas baja).
- El botón **Volver** (o la tecla R) hace que la cuerda tire de ti hasta dentro de la nave.
- Cada jugador tiene una **tarea exterior**: limpiar paneles solares, reparar la antena, soldar el casco o cambiar la baliza.
- Fuera no se puede eliminar ni reportar. Si empieza una reunión, vuelves dentro automáticamente.

## Pantalla completa en iPhone

En el iPhone, Safari y Chrome no permiten poner una web a pantalla completa. Para jugar sin barras del navegador, instala el juego como app:

1. Abre el juego en Safari (o Chrome) desde la página de GitHub.
2. Pulsa **Compartir** y elige **Añadir a pantalla de inicio**.
3. Abre **Polizón** desde el icono: se abre a pantalla completa.

El botón **Jugar a pantalla completa** del menú muestra estos pasos en el propio móvil. En Android ese botón pone el juego a pantalla completa directamente.
