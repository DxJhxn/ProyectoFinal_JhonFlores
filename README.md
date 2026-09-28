# Proyecto Final - Migración de MariaDB a PostgreSQL

## Tecnología de Base de Datos I

**Estudiante:** Jhon Emanuel Flores Chambi  
**Docente:** Jared Lopez Leaños  
**Fecha:** Septiembre de 2026

---

## Descripción

Este repositorio contiene el Proyecto Final de la asignatura **Tecnología de Base de Datos I**, correspondiente a la migración de la base de datos `employees` desde MariaDB hacia PostgreSQL 18.

El proyecto comprende la migración y verificación de:

- 6 tablas.
- 2 vistas.
- 3.919.015 registros.
- Claves primarias y foráneas.
- Tipo ENUM nativo de PostgreSQL.
- Integridad referencial.
- Checksums de las tablas.
- Respaldo final de PostgreSQL.

---

## Tecnologías utilizadas

- MariaDB
- PostgreSQL 18
- pgloader
- Docker
- Docker Compose
- pgAdmin
- Adminer
- pgModeler

---

## Base de datos

### Origen

- SGBD: MariaDB
- Base de datos: `employees`

### Destino

- SGBD: PostgreSQL 18
- Base de datos: `pdb_employees`
- Esquema: `employees`

---

## Tablas migradas

Las tablas migradas fueron:

- `departments`
- `employees`
- `dept_emp`
- `dept_manager`
- `salaries`
- `titles`

La migración final contiene un total de:

```text
3.919.015 registros
```

Los conteos obtenidos en MariaDB y PostgreSQL coincidieron para las seis tablas.

---

## Vistas migradas

Se migraron y verificaron las siguientes vistas:

- `dept_emp_latest_date`
- `current_dept_emp`

Cada vista produjo:

```text
300024 registros
```

tanto en MariaDB como en PostgreSQL.

---

## Verificación de la migración

La validación final incluyó:

- Comparación de conteos entre MariaDB y PostgreSQL.
- Checksums MD5 de las seis tablas.
- Verificación de registros huérfanos.
- Verificación de claves foráneas.
- Pruebas de las vistas migradas.

Los resultados finales mostraron:

```text
Diferencia de registros: 0
Registros huérfanos:     0
Claves foráneas:         6
Checksums coincidentes:  6 de 6
```

---

## Respaldo

Se generó un respaldo de la base de datos PostgreSQL utilizando `pg_dump` en formato personalizado.

Archivo:

```text
backup/pdb_employees.dump
```

El respaldo fue verificado mediante `pg_restore`.

---

## Estructura del repositorio

```text
ProyectoFinal_JhonFlores/
├── ProyectoFinal_JhonFlores.md
├── ProyectoFinal_JhonFlores.pdf
├── README.md
├── backup/
│   └── pdb_employees.dump
└── imagenes/
    └── evidencias del proyecto
```

---

## Seguridad

Las credenciales utilizadas durante el entorno local de migración no se publican en este repositorio.

En los ejemplos de configuración se utilizan valores genéricos como:

```text
<PASSWORD_MARIADB>
<PASSWORD_POSTGRESQL>
```

---

## Resultado

La migración de la base de datos `employees` desde MariaDB hacia PostgreSQL fue completada y verificada.

Los conteos, checksums y verificaciones de integridad referencial realizadas permitieron comprobar la correspondencia de los datos entre ambos gestores.

El procedimiento completo, los comandos ejecutados y sus resultados se encuentran documentados en:

**`ProyectoFinal_JhonFlores.md`**