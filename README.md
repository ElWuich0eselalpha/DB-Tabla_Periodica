# DB-Tabla_Periodica
Actividad 4 de certificación de freecodecamp base de datos relacional
# Periodic Table Database Project

## Descripción

Este proyecto consiste en la creación y administración de una base de datos de la tabla periódica. La creación de un script en Bash para consultar información sobre los elementos químicos, y la implementación del control de versiones con Git.

## Estructura del Proyecto

El proyecto se divide en tres partes principales:

1. **Corrección de la Base de Datos**: Se realizaron varios cambios en la estructura y los datos de la base de datos para asegurar la integridad y consistencia de la información.

2. **Control de Versiones con Git**: Se creó un repositorio Git para el proyecto y se realizaron múltiples commits para rastrear los cambios y mejoras.

3. **Creación de un Script Bash**: Se desarrolló un script en Bash (`element.sh`) que acepta un argumento (número atómico, símbolo o nombre del elemento) y devuelve información detallada sobre el elemento.

## Instrucciones

### Parte 1: Corrección de la Base de Datos

1. **Renombrar columnas**:
   - `weight` a `atomic_mass`
   - `melting_point` a `melting_point_celsius`
   - `boiling_point` a `boiling_point_celsius`

2. **Agregar restricciones**:
   - Las columnas `melting_point_celsius` y `boiling_point_celsius` no aceptan valores nulos.
   - Las columnas `symbol` y `name` en la tabla `elements` tienen las restricciones `UNIQUE` y `NOT NULL`.

3. **Llaves foráneas y nuevas tablas**:
   - Se estableció `atomic_number` en la tabla `properties` como llave foránea que referencia `atomic_number` en la tabla `elements`.
   - Se creó una tabla `types` para almacenar los tipos de elementos.

4. **Capitalización y eliminación de ceros**:
   - Se capitalizó la primera letra de los valores en la columna `symbol`.
   - Se eliminaron los ceros finales de los valores en la columna `atomic_mass`.

5. **Agregar nuevos elementos**:
   - Fluorine (F)
   - Neon (Ne)

### Parte 2: Control de Versiones con Git

1. **Inicializar el repositorio**:
   ```bash
   git init periodic_table
   cd periodic_table

