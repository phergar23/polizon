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
