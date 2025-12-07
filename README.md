
# Sistema de Administración de Cárcel - Cárcel Modelo de Ocaña

Proyecto de Programación 2 en Java, basado en consola, con persistencia en archivos de texto.

## Estructura del proyecto

- `src/domain`: Clases de dominio (Delito, Interno, Celda, Piso).
- `src/service`: Lógica del sistema y punto de entrada (`SistemaCarcel`).
- `data/delitos.txt`: Lista de delitos persistidos.
- `data/internos.txt`: Lista de internos persistidos, incluyendo ubicación.

## Compilación y ejecución

Desde la carpeta raíz del proyecto:

```bash
javac -d bin -sourcepath src src/domain/*.java src/service/*.java
java -cp bin service.SistemaCarcel
```

> Asegúrate de que la carpeta `data/` exista en la misma ruta desde donde ejecutas el programa.
