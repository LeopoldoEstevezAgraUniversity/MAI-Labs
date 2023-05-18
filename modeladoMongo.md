# Modelado de BBDD mongo

## Ej 1 ( Servicio de alumbrado )

### Materiales
```json
[
    {
        "codigo": 1,
        "descripcion": "Mat 1",
        "precio": 10
    },
    {
        "codigo": 2,
        "descripcion": "Mat 2",
        "precio": 2
    }
]
```

### Incidencias
```json
[
    {
        "numero": 1,
        "descripcion": "Incidencia 1",
        "causa": "Causa de la incidencia 1",
        "data": 2023-04-26T07:58:22Z,
        "direccion": {
            "numero": 1,
            "rua": "Calle",
            "poblacion": "Poblacion 1"
        },
        "equipo": "Equipo 1",
        "data_arreglo": 2023-04-27T07:58:22Z
    }
]
```

### Usos
```json
[
    {
        "id": 1,
        "incidencia": 1,
        "material": 1,
        "cantidad": 100
    }
]
```

### Equipos
```json
[
    {
        "codigo": 1,
        "alcume": "Equipo 1",
        "personal": [
            { "nss": "12345", "nome": "Nombre", "salario": 1000 },
            { "nss": "12346", "nome": "Nombre 2", "salario": 1001 },
            { "nss": "12347", "nome": "Nombre 3", "salario": 1002 },
        ]
    }
]
```

## Ej 2

### Persona

```json
[
    {
        "_id": 1,
        "nome": "Nombre 1",
        "salario": 10000,
        "tipo": ["e", "c"],
        "enderezo": "Calle 1",
        "departamento": "Dep 1",
        "tipo_cliente": "normal"
    },
    {
        "_id": 2,
        "nome": "Nombre 2",
        "tipo": ["c"],
        "enderezo": "Calle 2",
        "tipo_cliente": "premium"
    },
    {
        "_id": 3,
        "nome": "Nombre 3",
        "tipo": ["e"],
        "salario": 15000,
        "enderezo": "Calle 2",
        "departamento": "Dep 1",
    }
]
```

### Departamentos
```json
[
    {
        "codigo": "Dep 1",
        "nome": "Departamento 1"
    }
]
```

## EJ 3 ( Apps móbiles )

### Usuario
```json
[
    {
        "login": "username",
        "clave": "********",
        "nome": {
            "pila": "Leo",
            "apelidos": "Estevez"
        },
        "tipo": "p",
        "programador": {
            "linguaxes": ["TS", "JS"],
            "aplicaciones": ["App"]
        },
    },
    {
        "login": "usersomething",
        "clave": "*******",
        "nome": {
            "pila": "test",
            "apelidos": "testerino"
        },
        "tipo": "c",
        "cliente": {
            "status": "active",
            "subscripciones": ["App"]
        }
    },
    {
        "login": "admin",
        "clave": "*******",
        "nome": {
            "pila": "admin",
            "apelidos": "user"
        },
        "admin": { "nivel": "Defcon 1" }
    }
]
```

### Aplicaciones
```json
[
    {
        "numero": 1,
        "nome": "App",
        "descripcion": "Ninguna",
        "categoria": 1,
        "versiones": [
            { "numero": 0, "comentarios": [] }
        ]
    }
]
```

### Categorias
```json
[
    {
        "numero": 1,
        "nome": "Cat 1",
        "descripcion": "Una nueva categoría",
        "aplicaiones": ["App"]
    }
]
```

## Ej: extra ( Gasolineras )

### Coche
```json
[
    {
        "matricula": "1235-xyz",
        "marca": "Seat",
        "modelo": "Ibiza"
    }
]
```

### Gasolinera
```json
[
    {
        "codigo": 1,
        "nome": "Repsol 1",
        "enderezo": "Alfonso molina",
        "surtidores": [
            { "numero": 1, "a_instalacion": 2020, "alimentado_por": ["dep1", "dep2"] }
        ]
    }
]
```

### Repostaxe
```json
[
    {
        "gasolinera": 1,
        "coche": "1235-xyz",
        "data": 2023-04-26T07:58:22Z
    }
]
```

### Depositos
```json
[
    {
        "codigo": 1,
        "capacidade": 2000,
        "gasolinera": 1,
        "combustible": 1
    }
]
```

### Combustibles
```json
[
    {
        "codigo": 1,
        "nome": "Gasoleo A",
        "prezo": 1.2
    }
]
```