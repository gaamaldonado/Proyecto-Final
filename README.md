# ArsenalBalancer CLI 🚀🎮

ArsenalBalancer es una microherramienta de consola (CLI) programada en Python utilizando la biblioteca `openpyxl`. Está diseñada específicamente para optimizar y automatizar el flujo de trabajo de los diseñadores de videojuegos (Game Designers) durante la etapa de balanceo de armamento para juegos de tipo shooter.

## 📋 ¿Para qué sirve?

La herramienta actúa como un puente inteligente entre el diseño conceptual de mecánicas y la base de datos técnica que lee el motor del juego (Unity, Unreal Engine, Godot, etc.). Sus funciones principales son:

*   **Centralizar el arsenal:** Permite crear, listar y editar de forma rápida la base de datos de armamento desde la terminal.
*   **Automatizar métricas de combate:** Inyecta fórmulas dinámicas directamente en celdas de Excel para calcular el Daño por Segundo (DPS) real y el tiempo de baja (Time to Kill / TTK).
*   **Control de calidad visual:** Aplica formatos condicionales y alertas de colores automáticas en la hoja de cálculo cuando un arma se encuentra desbalanceada (ej. si está rota o muy débil).
*   **Exportación ágil:** Genera archivos nativos `.xlsx` limpios y estructurados, listos para ser importados por los programadores al código del juego.

---

## 🛠️ Requisitos e Instalación

Para ejecutar esta microherramienta necesitas tener instalado **Python 3.x** y la biblioteca encargada de la manipulación de las hojas de cálculo.

1. **Clonar o descargar** este repositorio en tu máquina.
2. **Instalar la dependencia** requerida ejecutando el siguiente comando en tu terminal:

```bash
pip install openpyxl
```

---

## 💻 Instrucciones de Uso

1. Ejecutá el script principal desde la consola:
   ```bash
   python main.py
   ```
2. El programa validará si existe el archivo de base de datos (`balance_armas.xlsx`). Si no lo encuentra, lo creará automáticamente con la estructura de títulos y estilos base.
3. Interactuá con el menú de consola para agregar nuevas armas introduciendo sus atributos (Daño base, Cadencia de tiro, Capacidad del cargador).
4. Abrí el archivo de Excel generado para revisar las estadísticas calculadas dinámicamente y los reportes visuales de balanceo.

---

## 📅 Plan de Desarrollo (Cronograma de Trabajo)

*   **Fase 1 (Días 1-2):** Investigación, modelado de variables del shooter y arquitectura de celdas en la hoja de cálculo.
*   **Fase 2 (Días 3-5):** Configuración del núcleo en Python, integración de `openpyxl` y lógica de inyección de fórmulas de Excel.
*   **Fase 3 (Días 6-8):** Creación de la interfaz CLI interactiva e implementación de reglas de formato condicional por colores.
*   **Fase 4 (Días 9-10):** Pruebas de estrés de datos, control de errores (input handling) y entrega de la documentación final para Antigravity.
