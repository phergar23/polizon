# Polizón a Bordo

Juego 3D en primera persona, con estética de dibujos animados, sobre una tripulación que debe descubrir a los polizones escondidos en la nave Lucero. Funciona en el navegador, sin instalar nada.

## Cómo jugar

Abre `index.html` en el navegador (o la página de GitHub Pages del repositorio).

- **Crear partida:** de 1 a 10 jugadores, con opción de rellenar los huecos con NPCs y elegir cuántos polizones hay.
- **Modo práctica:** juegas solo, eligiendo ser tripulante o polizón, con NPCs quietos repartidos por la nave.
- **Unirse:** el modo multijugador por código solo funciona al abrir el juego desde su enlace de Claude; desde este repositorio se juega en solitario con NPCs o en modo práctica.

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

- Nave de 15 salas con pasillo en anillo alrededor del Comedor.
- 22 tareas con su propio objeto 3D y 20 minijuegos animados.
- Polizones con alcantarillas que se recorren andando por conductos y sabotajes (luces, reactor, comunicaciones y cierre de puertas).
- Sala de Seguridad con cuatro cámaras en directo.
- Reuniones con chat, votación, recuento de votos y animaciones.
- NPCs que hacen tareas, arreglan sabotajes, reportan cuerpos y votan.

Hecho con [Three.js](https://threejs.org/) r128. Personajes y nave de diseño original.
