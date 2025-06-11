# 🚌 Sistema de Gestión de Rutas de Transporte

Este proyecto contiene el volcado (`dump`) de una base de datos para un sistema de gestión de rutas de transporte. Incluye información sobre rutas, paradas, buses, conductores, boletos, horarios y tarifas.

## 📂 Contenido del Repositorio

- `Dump20250603cesarz.sql`: Volcado completo de la base de datos.

## 🧱 Estructura de la Base de Datos

### Tablas Principales

| Tabla          | Descripción                                                   |
|----------------|---------------------------------------------------------------|
| `Rutas`        | Información general de las rutas disponibles.                 |
| `asignaciones` | Registro de asignaciones de buses y conductores a rutas.      |
| `boletos`      | Gestión de boletos vendidos por ruta y fecha.                 |
| `buses`        | Datos de los buses disponibles.                               |
| `conductores`  | Información de los conductores.                               |
| `horarios`     | Horarios de salida por ruta y día.                            |
| `paradas`      | Puntos de parada de cada ruta, con ubicación geográfica.      |
| `ruta_parada`  | Relación ordenada entre rutas y sus paradas.                  |
| `tarifas`      | Tarifas entre paradas dentro de una misma ruta.               |

### Ejemplo de Columnas por Tabla

- **`Rutas`**: `idRutas`, `Nombre_rutas`, `Origen`, `destino`, `duracion_aproximada`
- **`boletos`**: `id`, `ruta_id`, `fecha`, `hora`, `parada_origen_id`
- *(Ver el archivo `.sql` para la estructura completa de cada tabla.)*

## 🛠 Restauración de la Base de Datos

1. Crear una base de datos vacía en MySQL:
    ```sql
    CREATE DATABASE sistema_rutas;
    ```

2. Importar el volcado:
    ```bash
    mysql -u [usuario] -p sistema_rutas < Dump20250603cesarz.sql
    ```

## 📌 Requisitos

- MySQL/MariaDB
- Cliente de línea de comandos (`mysql`)

## 📄 Licencia

Este repositorio puede ser utilizado con fines educativos o de desarrollo. Verifica la licencia o términos específicos si planeas usarlo comercialmente.
