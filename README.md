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
#### 1. Clonar el repositorio
```bash
git clone https://github.com/LeonidasDiaz/python-task-manager
cd python-task-manager
```
#### 2. Ejecutar directamente (sin instalación adicional)
```bash
python main.py

```
## Uso
### Comandos disponibles en el menú

| Opción | Acción | Descripción |
|--------|--------|-------------|
| **1** | Añadir tarea | Crea una nueva tarea con nombre y categoría |
| **2** | Listar tareas | Muestra todas las tareas en formato tabla |
| **3** | Eliminar tarea | Elimina una tarea específica por su ID |
| **4** | Salir | Termina la ejecución del programa |

## Estructura del Proyecto

task-manager-cli/
- **main.py** - Script principal
- **README.md** - Documentación del proyecto (este archivo)

## Tecnologías 
- Python 3.8+ - Lenguaje de programación principal
- Estructuras de datos nativas - Listas y diccionarios para almacenamiento
- f-strings avanzadas - Formateo tabular profesional con alineación
- Manejo de excepciones - Validación robusta de entradas del usuario
- Funciones modulares - Código organizado y mantenible
- Programación imperativa - Flujo claro y lógico


## Ejemplos de Código
### Función principal para listar tareas
```python
def listar_tareas(tareas):
    """Muestra las tareas en formato tabla con ID."""
    if not tareas:
        print(" No hay tareas registradas.")
        return
    print(f"{'ID':>3} | {'Tarea':<25} | {'Categoría':<15} | {'Estado':<10}")
    print("-" * 62)
    for t in tareas:
        print(f"{t['id']:>3} | {t['nombre']:<25} | {t['categoria']:<15} | {t['estado']:<10}")
```
### Función para añadir tareas con validación de duplicados
```python
def anadir_tarea(tareas, next_id):
    """Añade una tarea con ID incremental único."""
    nombre = input("Nombre de la tarea: ").strip()
    categoria = input("Categoría: ").strip()

    # Verificar duplicados por nombre (opcional)
    for t in tareas:
        if t["nombre"].casefold() == nombre.casefold():
            print(" Esa tarea ya existe (evitamos duplicados).")
            return next_id

    tareas.append({
        "id": next_id,
        "nombre": nombre,
        "categoria": categoria,
        "estado": "pendiente",
    })
    print(f" Tarea añadida con ID {next_id}.")
    return next_id + 1
```
### Función para eliminar tareas por ID
```python
def eliminar_por_id(tareas):
    """Elimina una tarea según su ID único."""
    try:
        id_obj = int(input("Ingrese el ID de la tarea a eliminar: "))
    except ValueError:
        print(" Debe ingresar un número entero.")
        return

    for i, t in enumerate(tareas):
        if t["id"] == id_obj:
            tareas.pop(i)
            print(" Tarea eliminada.")
            return

    print(" No existe una tarea con ese ID.")

```
## Licencia

Este proyecto está bajo la **Licencia MIT**.  
Consulta el archivo [LICENSE](LICENSE) para el texto completo.

## Autor
### Leonidas Diaz
GitHub: [@LeonidasDiaz](https://github.com/LeonidasDiaz)

## Acerca del proyecto
Este proyecto fue desarrollado como parte de mi aprendizaje y portafolio de programación en Python. El objetivo era crear una aplicación funcional y práctica que demuestre habilidades en desarrollo de software, manejo de datos y creación de interfaces de línea de comandos.
