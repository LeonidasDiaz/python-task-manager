# Python-task-manager-cli

Aplicación de consola desarrollada en Python que permite gestionar tareas mediante un menú interactivo.  
Este proyecto demuestra uso de estructuras de datos, validaciones, funciones modulares, ciclos `while`, y una lógica realista para CRUD básico.

##Objetivo del Proyecto
Implementar un sistema sencillo de gestión de tareas que permita:

- Agregar tareas sin duplicados.
- Listarlas en formato tabular.
- Eliminarlas mediante ID.
- Persistir la lógica en memoria durante la ejecución.

Este proyecto refuerza fundamentos de programación y construcción de aplicaciones CLI.

## Funcionalidades
-  Menú interactivo  
- Agregar tareas con nombre único  
- Listar tareas con alineación tabular  
- Eliminar tareas por **ID**  
- Validaciones de entrada (`try / except`)  
- IDs autoincrementales  
- Separación clara por funciones
## Estructura del Proyecto
```
task-manager-cli/
├main.py # Script principal

```
##  Estructura del código
- `anadir_tarea()`
- `listar_tareas()`
- `eliminar_por_id()`
- `mostrar_menu()`
- `main()`
## Tecnologías usadas
- Python 3
- Manejo de listas y diccionarios
- Validaciones
- Formateo de texto con f-strings
## Ejecutar
```bash
python task_manager.py
