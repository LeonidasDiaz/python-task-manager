# Task Manager CLI - Python

Una aplicación de línea de comandos desarrollada en Python para gestionar tareas de manera eficiente. Ofrece un menú interactivo con operaciones CRUD completas, IDs autoincrementales y validaciones robustas.

## Tabla de Contenido
- [Características](#características)
- [Instalacion](#instalacion)
- [Uso](#uso)
- [Estructura del proyecto](#estructura-del-proyecto)
- [Tecnologías](#tecnologías)
- [Ejemplos de codigo](#ejemplos-de-codigo)
- [Licencia](#licencia)
- [Autor](#autor)


##  Características
- Menú interactivo - Navegación intuitiva por consola
- CRUD completo - Crear, Leer, Eliminar tareas
- IDs autoincrementales - Identificadores únicos automáticos
- Formato tabular profesional - Salida alineada y legible
- Validación de duplicados - Evita tareas repetidas
- Manejo de errores - Validación de entradas con try/except
- Código modular - Funciones separadas y documentadas
- Sin dependencias externas - Python puro, sin instalaciones adicionales
- Este proyecto refuerza fundamentos de programación y construcción de aplicaciones CLI.

## Instalacion
### Prerrequisitos
- Python 3.8 o superior
- Git (opcional, para clonar el repositorio)
### Pasos de instalación
#### 1.Clonar el repositorio
```bash
git clone https://github.com/LeonidasDiaz/python-task-manager
cd python-task-manager
```
#### 2.Ejecutar directamente (sin instalación adicional)
```bash
python main.py

```
## Estructura del Proyecto

task-manager-cli/
- **main.py** - Script principal
- **README.md** - Documentación del proyecto (este archivo)

## Tecnologías usadas
- Python 3
- Manejo de listas y diccionarios
- Validaciones
- Formateo de texto con f-strings

## Cómo ejecutar
```bash
git clone https://github.com/LeonidasDiaz/python-task-manager
cd python-task-manager
python main.py
```
## EJemplo de Salida
```
===== MENÚ =====
1. Añadir tarea
2. Listar tareas
3. Eliminar tarea por ID
4. Salir
================

Tareas:
ID   |  Nombre
--------------------
1    | Comprar leche
2    | Estudiar Python
3    | Hacer ejercicio

```
## Fragmento de código principal
```python
def listar_tareas(tareas):
    print(f"{'ID':<4} | {'Nombre':<20}")
    print("-" * 26)
    for tarea in tareas:
        print(f"{tarea['id']:<4} | {tarea['nombre']:<20}")
```

## Autor
### Leonidas Diaz
GitHub: [@LeonidasDiaz](https://github.com/LeonidasDiaz)

