Actúa como un desarrollador experto en Python y Pygame. Crea el desarrollo de un juego de supervivencia zombi estilo "Project Zomboid" en 2D (vista top-down o isométrica simplificada), implementado de forma modular y estructurada.

--- CONCEPTO DEL JUEGO: Outbreak: Quarantine Zero ---
- Vista: Superior / Top-down o isométrica simplificada.
- Ambientación: Zona en cuarentena post-brote biológico.
- Mecánicas clave: Gestión de necesidades (salud, hambre, sed, estamina), cono de visión/niebla de guerra, generación de ruido al correr/atacar, inventario por peso y exploración/looting de contenedores.

--- PLAN DE TRABAJO (FASE POR FASE) ---
Desarrolla la arquitectura del proyecto siguiendo este orden de trabajo:

Fase 1: Motor Base y Mapa
- Bucle principal de Pygame y gestión de delta time (FPS estables).
- Mapa basado en cuadrícula (Tilemap) que represente paredes, suelos, puertas y contenedores.
- Sistema de cámara que siga al jugador de forma fluida.

Fase 2: Jugador y Físicas
- Movimiento WASD con aceleración y sistema de estamina (Shift para correr).
- El personaje rota hacia la posición del cursor del ratón.
- Colisiones con paredes y obstáculos del Tilemap.
- Atributos base del jugador: Salud, Estamina, Hambre y Sed.

Fase 3: Visibilidad y Sonido
- Cono de visión (Fog of War) usando raycasting o máscaras de Pygame: las zonas a la espalda del jugador o tras paredes deben quedar en penumbra/oscuridad.
- Radio de ruido dinámico: caminar genera poco ruido, correr o atacar expande un radio de sonido que alerta a los enemigos cercanos.

Fase 4: IA de Zombis
- Estados de IA: Deambular aleatoriamente (Wander), Investigar ruido (Investigate) y Perseguir (Chase).
- Los zombis detectan al jugador por cono de visión propio o por el radio de ruido generado.
- Daño por contacto al jugador y sistema de salud/muerte de los zombis.

Fase 5: Sistema de Inventario y Loot
- Interacción con contenedores del mapa (tecla E).
- Interfaz gráfica limpia para el inventario con límite de peso.
- Objetos consumibles funcionales (comida para el hambre, agua para la sed, vendas para restaurar salud).

Fase 6: Pulido Visual
- Utiliza figuras geométricas básicas (rectángulos, círculos) y colores distintos para que el código sea 100% ejecutable sin assets externos.

--- REQUISITOS DE CÓDIGO ---
- Código limpio, modular y estructurado en clases (Player, Zombie, TileMap, Inventory, UI, GameEngine).
- Comentarios explicativos en las secciones complejas (raycasting de visión, lógica de IA y contenedores).
- Comienza entregando la estructura de archivos/clases y el código ejecutable de la Fase 1 y Fase 2 para probar el movimiento, la cámara y el mapa inicial.
