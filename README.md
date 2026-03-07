# Proyecto: API de las peliculas mas valoradas de todos los tiempos

**Estudiante:** Sergio Alejandro Atehortua Perez

**URL de la API:** https://698777b68bacd1d773ed745d.mockapi.io/Titulos

## 1. Modelo de datos diseñado

Se configuró el recurso `Titulos` con la siguiente estructura de datos:

```json
[

    {
        "Titulo": "Sueño de fuga",
        "Fecha": 1994,
        "Generos": [
        "Drama",
        "Intriga"
        ],
        "Detalles": {
        "Clasificacion": "B",
        "Disponibilidad": "Disp"
        },
        "Calificacion": 9.3,
        "Duracion": "2h 22m",
        "Stok": "true",
        "id": "1"
    }
]
```

## 2. Bitácora de operaciones CRUD (Respuestas de Postman)

### A. Obtener todos los registros (GET)
- Status Code: `200 OK`
- Respuesta de Postman:

```json
[
    {
        "Titulo": "Sueño de fuga",
        "Fecha": 1994,
        "Generos": [
            "Drama",
            "Intriga"
        ],
        "Detalles": {
            "Clasificacion": "B",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 9.3,
        "Duracion": "2h 22m",
        "Stok": "true",
        "id": "1"
    },
    {
        "Titulo": "El padrino",
        "Fecha": 1972,
        "Generos": [
            "Epica",
            "Crimen"
        ],
        "Detalles": {
            "Clasificacion": "C",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 9.2,
        "Duracion": "2h 55m",
        "Stok": "true",
        "id": "2"
    },
    {
        "Titulo": "Batman: El caballero de la noche",
        "Fecha": 2008,
        "Generos": [
            "Superheroe",
            "Accion"
        ],
        "Detalles": {
            "Clasificacion": "B",
            "Disponibilidad": "NoDisp"
        },
        "Calificacion": 9.1,
        "Duracion": "2h 32m",
        "Stok": "false",
        "id": "3"
    },
    {
        "Titulo": "El padrino (parte II)",
        "Fecha": 1974,
        "Generos": [
            "Crimen",
            "Drama"
        ],
        "Detalles": {
            "Clasificacion": "C",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 9,
        "Duracion": "3h 22m",
        "Stok": "true",
        "id": "4"
    },
    {
        "Titulo": "12 hombres en pugna",
        "Fecha": 1957,
        "Generos": [
            "Juridico",
            "Crimen"
        ],
        "Detalles": {
            "Clasificacion": "B",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 9,
        "Duracion": "1h 36m",
        "Stok": "true",
        "id": "5"
    },
    {
        "Titulo": "El señor de los anillos: La comunidad del anillo",
        "Fecha": 2001,
        "Generos": [
            "Aventura",
            "Epica"
        ],
        "Detalles": {
            "Clasificacion": "B",
            "Disponibilidad": "NoDisp"
        },
        "Calificacion": 9,
        "Duracion": "3h 21m",
        "Stok": "false",
        "id": "6"
    },
    {
        "Titulo": "La lista de Schindler",
        "Fecha": 1993,
        "Generos": [
            "Acción",
            "Intriga"
        ],
        "Detalles": {
            "Clasificacion": "B15",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 9,
        "Duracion": "3h 15m",
        "Stok": "true",
        "id": "7"
    },
    {
        "Titulo": "El señor de los anillos: La comunidad del anillo",
        "Fecha": 2001,
        "Generos": [
            "Epica",
            "Fantasia"
        ],
        "Detalles": {
            "Clasificacion": "B",
            "Disponibilidad": "NoDisp"
        },
        "Calificacion": 8.9,
        "Duracion": "2h 58m",
        "Stok": "false",
        "id": "8"
    },
    {
        "Titulo": "Tiempos violentos",
        "Fecha": 1994,
        "Generos": [
            "Comedia",
            "Crimen"
        ],
        "Detalles": {
            "Clasificacion": "C",
            "Disponibilidad": "NoDisp"
        },
        "Calificacion": 8.8,
        "Duracion": "2h 34m",
        "Stok": "false",
        "id": "9"
    },
    {
        "Titulo": "El bueno, el malo y el feo",
        "Fecha": 1966,
        "Generos": [
            "Epica",
            "Comedia"
        ],
        "Detalles": {
            "Clasificacion": "C",
            "Disponibilidad": "Disp"
        },
        "Calificacion": 8.8,
        "Duracion": "2h 41m",
        "Stok": "true",
        "id": "10"
    }
]
```

### B. Creación de un nuevo regiistro (POST)
- Status Code: `201 Created`
- Cuerpo enviado en Postman:

```json
{
    "Titulo": "El señor de los anillos: Las dos torres",
    "Fecha": 2002,
    "Generos": [
        "Epica",
        "Fantasia"
    ],
    "Detalles": {
        "Clasificacion": "B",
        "Disponibilidad": "Disp"
    },
    "Calificacion": 8.8,
    "Duracion": "2h 59m",
    "Stok": "TRUE",
}

```

- Respuesta de Postman:

```json
{
"Titulo": "El señor de los anillos: Las dos torres",
"Fecha": 2002,
    "Generos": [
    "Epica",
    "Fantasia"
    ],
    "Detalles": {
    "Clasificacion": "B",
    "Disponibilidad": "Disp"
    },
    "Calificacion": 8.8,
    "Duracion": "2h 59m",
    "Stok": "TRUE",
    "id": "11"
}

```

### C. Consulta de registro individual (GET)
- Endpoint: `Titulos/2`
- Status Code: `200 OK`
- Respuesta de Postman:

```json
{
    "Titulo": "El padrino",
    "Fecha": 1972,
    "Generos": [
        "Epica",
        "Crimen"
    ],
    "Detalles": {
        "Clasificacion": "C",
        "Disponibilidad": "Disp"
    },
    "Calificacion": 9.2,
    "Duracion": "2h 55m",
    "Stok": "TRUE",
    "id": "2"
}

```

### D. Actualizacion de un registro (PUT)
- Status Code: `200 OK`
- Modificación: Se actualizó el Stock, Disponibilidad y la calificación del registro con el ID 11.

```json

{
    "Titulo": "El señor de los anillos: Las dos torres",
    "Fecha": 2002,
    "Generos": [
    "Epica",
    "Fantasia"
    ],
    "Detalles": {
    "Clasificacion": "B",
    "Disponibilidad": "NoDisp"
    },
    "Calificacion": 8.7,
    "Duracion": "2h 59m",
    "Stok": "FALSE",
    "id": "11"
}

```

### E. Eliminación de un regristro (DELETE)
- Status Code: `200 OK`
- Respuesta de Postman:

```json

{
    "id": "11",
    "Titulo": "El señor de los anillos: Las dos torres"
}

```

### F. Validación de recurso inexistente (GET404)
- Status Code: `404 Not Found`
- Respuesta de Postman:

```json

    "Not found"

```

## 3. Resumen de Endpoint y Codigos HTTP

| Acción      | Método | Endpoint   | Código HTTP  |
|-------------|--------|------------|--------------|
| Listar todo | GET    | /Titulos   | 200 OK       |
| Crear       | POST   | /Titulos   | 201 Created  |
| Ver por ID  | GET    | /Titulos/2 | 200 OK       |
| Actualizar  | PUT    | /Titulos/11| 200 OK       |
| Borrar      | DELETE | /Titulos/11| 200 OK       |
| Error       | GET    | /Titulos/11| 404 Not Found|