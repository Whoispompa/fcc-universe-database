# 🌌 Celestial Bodies Database - freeCodeCamp

Este repositorio contiene mi solución para el proyecto **"Build a Celestial Bodies Database"**, el cual forma parte de la certificación **Relational Database** de [freeCodeCamp.org](https://www.freecodecamp.org/).

El objetivo del proyecto es diseñar una base de datos relacional sobre el universo utilizando **PostgreSQL**, cumpliendo con una serie de restricciones estrictas de tipos de datos, llaves primarias, llaves foráneas y valores únicos.

---

## 🚀 Características del Proyecto

La base de datos se llama `universe` y cuenta con **5 tablas** interconectadas:
* **`galaxy`**: Contiene información sobre distintos tipos de galaxias, su edad y distancia.
* **`star`**: Almacena estrellas vinculadas a sus respectivas galaxias (Relación 1:N).
* **`planet`**: Registra planetas asociados a sus estrellas correspondientes (Relación 1:N).
* **`moon`**: Lista más de 20 lunas vinculadas de forma estricta a sus planetas (Relación 1:N).
* **`comet`**: Una quinta tabla requerida para registrar cuerpos celestes menores de forma independiente.

### 🛠️ Tecnologías y Restricciones Aplicadas
* **Base de datos:** PostgreSQL
* **Tipos de datos usados:** `SERIAL`, `VARCHAR`, `INT`, `NUMERIC`, `TEXT` y `BOOLEAN`.
* **Restricciones:** Claves primarias autoincrementales (`table_name_id`), llaves foráneas explícitas, valores únicos (`UNIQUE`) y campos obligatorios (`NOT NULL`).

---

## 📦 Cómo Reconstruir la Base de Datos

Si deseas clonar este proyecto y restaurar la base de datos en tu entorno local de PostgreSQL, sigue estos pasos:

1. Asegúrate de tener PostgreSQL instalado y corriendo.
2. Descarga el archivo `universe.sql` de este repositorio.
3. Abre tu terminal en la carpeta donde descargaste el archivo y ejecuta:

```bash
psql -U postgres < universe.sql
