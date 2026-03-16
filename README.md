# 🐘 POSTGRESQL DESDE CERO - GUÍA COMPLETA

**PostgreSQL desde Cero** es un sitio educativo completo diseñado para enseñar PostgreSQL desde los fundamentos hasta conceptos avanzados, con explicaciones claras, ejemplos prácticos y código listo para usar.

> *"PostgreSQL es el sistema de base de datos relacional de código abierto más avanzado del mundo."*

---

## 🎯 ¿Qué es este Proyecto?

Este proyecto proporciona un recurso educativo gratuito para aprender PostgreSQL, incluyendo:

- **Documentación completa** de cada tema
- **Ejemplos de código** listos para ejecutar
- **Ejercicios prácticos** para reforzar el aprendizaje
- **Sitio web educativo** con navegación intuitiva

---

## 📚 Contenido del Curso

### Módulo 1: Fundamentos

1. **Introducción**
   - ¿Qué es PostgreSQL?
   - Historia y características
   - Casos de uso comunes

2. **Instalación**
   - Instalación en Windows
   - Instalación en Linux
   - Instalación en macOS
   - Configuración inicial

3. **Conceptos básicos**
   - Creación de bases de datos
   - Tipos de datos
   - Restricciones (constraints)
   - Claves primarias y foráneas

### Módulo 2: Intermedio

4. **Ejemplos prácticos**
   - Consultas SELECT
   - JOINs (INNER, LEFT, RIGHT, FULL)
   - Subconsultas
   - Funciones de agregación

5. **Buenas prácticas**
   - Indexación estratégica
   - Optimización de consultas
   - EXPLAIN y ANALYZE
   - Diseño de esquemas

### Módulo 3: Avanzado

6. **Casos reales**
   - Patrones de diseño comunes
   - Implementación en producción
   - Backup y recuperación

7. **Proyecto final**
   - Desarrollo de base de datos completa
   - Aplicación real con PostgreSQL

---

## 🗂️ Estructura del Proyecto

```
Practica-Nro13/
├── index.html          # Página principal
├── css/
│   └── styles.css      # Estilos del sitio
├── js/
│   └── main.js         # JavaScript del sitio
└── README.md
```

---

## 🚀 Cómo Usar este Proyecto

### Opción 1: Navegar el Sitio Web

1. Abre `index.html` en tu navegador
2. Navega por las secciones del curso
3. Haz clic en los temas para ver la documentación detallada

### Opción 2: Ejecutar los Ejemplos SQL

1. Abre pgAdmin o psql
2. Conéctate a tu instancia de PostgreSQL
3. Ejecuta los scripts SQL de ejemplo

### Requisitos

- **PostgreSQL 14** o superior
- **pgAdmin 4** o **psql** (línea de comandos)
- Navegador web moderno (Chrome, Firefox, Edge)

---

## 📝 Ejemplos Rápidos

### Crear Base de Datos

```sql
CREATE DATABASE mi_base_datos;

\c mi_base_datos;
```

### Crear Tabla

```sql
CREATE TABLE usuarios (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    fecha_registro TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    activo BOOLEAN DEFAULT true
);
```

### Consulta con JOIN

```sql
SELECT u.nombre, p.titulo
FROM usuarios u
INNER JOIN publicaciones p ON u.id = p.usuario_id
WHERE u.activo = true
ORDER BY p.fecha DESC;
```

### Función JSON

```sql
SELECT 
    nombre,
    datos->>'telefono' AS telefono
FROM usuarios
WHERE datos ? 'telefono';
```

---

## 🎓 Metodología de Aprendizaje

### 1. Leer la Teoría
Cada tema comienza con una explicación clara del concepto.

### 2. Ver Ejemplos
Los ejemplos de código muestran la aplicación práctica.

### 3. Practicar
Los ejercicios te permiten aplicar lo aprendido.

### 4. Experimentar
Modifica los ejemplos para entender cómo funcionan.

---

## 🔧 Comandos Esenciales

### Gestión de Bases de Datos

```sql
-- Listar bases de datos
\l

-- Conectar a una base de datos
\c nombre_base_datos;

-- Eliminar base de datos
DROP DATABASE IF EXISTS nombre_base_datos;
```

### Gestión de Tablas

```sql
-- Listar tablas
\dt

-- Ver estructura de tabla
\d nombre_tabla

-- Eliminar tabla
DROP TABLE IF EXISTS nombre_tabla;
```

### Consultas Comunes

```sql
-- Contar registros
SELECT COUNT(*) FROM nombre_tabla;

-- Ver primeros registros
SELECT * FROM nombre_tabla LIMIT 10;

-- Buscar datos
SELECT * FROM nombre_tabla WHERE columna LIKE '%valor%';
```

---

## 📖 Recursos Adicionales

### Documentación Oficial

- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
- [PostgreSQL Wiki](https://wiki.postgresql.org/)

### Herramientas Recomendadas

- **pgAdmin 4** - IDE oficial gratuito
- **DBeaver** - Cliente de base de datos universal
- **psql** - Línea de comandos oficial

### Comunidades

- [PostgreSQL Community](https://www.postgresql.org/community/)
- [Stack Overflow - PostgreSQL](https://stackoverflow.com/questions/tagged/postgresql)
- [Reddit r/PostgreSQL](https://www.reddit.com/r/PostgreSQL/)

---

## 💡 Consejos para Principiantes

1. **Practica regularmente**: La consistencia es clave para aprender SQL.
2. **Comienza simple**: Domina SELECT antes de avanzar a conceptos complejos.
3. **Entiende los JOINs**: Son fundamentales para consultas relacionales.
4. **Aprende EXPLAIN**: Te ayudará a optimizar consultas.
5. **Usa transacciones**: Para mantener la integridad de los datos.

---

## ⚠️ Mejores Prácticas

### Seguridad

- Nunca uses `SELECT *` en producción
- Usa parámetros para prevenir SQL Injection
- Valida siempre los datos de entrada

### Rendimiento

- Indexa columnas usadas en WHERE y JOIN
- Usa EXPLAIN ANALYZE para debuggear
- Evita N+1 queries

### Código

- Usa nombres descriptivos para tablas y columnas
- Comenta tu código SQL
- Mantén un formato consistente

---

## 🧪 Ejercicios Prácticos

### Nivel Básico

1. Crea una base de datos llamada `Biblioteca`
2. Crea tablas para `Libros`, `Socios` y `Prestamos`
3. Inserta al menos 5 registros en cada tabla
4. Consulta todos los libros disponibles

### Nivel Intermedio

1. Crea una función para registrar préstamos
2. Usa JOIN para mostrar libros con sus categorías
3. Crea una vista con el resumen de préstamos por socio

### Nivel Avanzado

1. Implementa un trigger para actualizar stock automáticamente
2. Crea índices para optimizar consultas frecuentes
3. Implementa transacciones para operaciones críticas

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
