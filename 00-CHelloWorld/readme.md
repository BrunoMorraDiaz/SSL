# **TP#0: "Hello, World!" en C**

---

## 👤 Autor de la resolución:

- **BrunoMorraDiaz**  
- **2038869**  
- **Morra Díaz**  
- **Bruno**

---

## 🎯 **Objetivos**

- Demostrar capacidad para editar, compilar y ejecutar programas C mediante el desarrollo de un programa simple.  
- Tener un primer contacto con las herramientas necesarias para abordar la resolución de los trabajos posteriores.  
- Creación de repositorio personal git.  
- Armado de equipo de trabajo.

---

## 📚 **Temas**

- Sistema de control de versiones  
- Lenguaje de programación C  
- Proceso de compilación  
- Pruebas

---

## ❓ **Problema**

Adquirir y preparar los recursos necesarios para resolver los trabajos del curso.

---

## ✅ **Tareas**

1. **Cuenta en GitHub**  
2. **Repositorio público para la materia**  
3. **Compilador**  
   a. Seleccione, instale, configure y pruebe un compilador C23, que es la versión publicada oficialmente en 2024; también se lo conoce como **C2x**.  
      Otras versiones aceptables son **C11 (C1X)** o **C17 (C18)**.  
      Los más osados pueden buscar un compilador que soporte **C2Y**.  
   b. Registre los resultados anteriores de la siguiente manera:  
      i. Indique en el `README.md`:  
         A. El compilador seleccionado  
         B. La versión de ese compilador  
         C. La versión de C que el compilador compila  
      ii. Pruebe el compilador con un programa `hello.c` que envíe a stdout la línea **Hello, World!** o similar.  
      iii. Ejecute el programa y verifique que la salida es la esperada.  
      iv. Ejecute el programa con la salida redireccionada a un archivo `output.txt`; verifique su contenido.  
4. **Publicación**  
   a. Publique el trabajo en el repositorio personal SSL en la carpeta `00-CHelloWorld` con `README.md`, `hello.c` y `output.txt`.  
5. **Armado de Equipo**

---

## 📝 **Respuestas de la tarea 3b i**

### A) El compilador seleccionado fue:

- **Compilador**: GCC

### B) La versión de este compilador es:

- **Versión**: `gcc.exe (Rev2, Built by MSYS2 project) 14.2.0`  

Pude obtener la versión del compilador aplicando el siguiente comando en la consola:

```bash
gcc --version
gcc.exe (Rev2, Built by MSYS2 project) 14.2.0
Copyright (C) 2024 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO 
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

## C) 💻 Versión del estándar de C que el compilador compila
Versión del lenguaje estándar: C17 aunque puedo forzarlo a c2x

Obtuve esta información al compilar y ejecutar el siguiente código:
 
```c

#include <stdio.h>

int main(void) {
#ifdef __STDC_VERSION__
    printf("STDC version: %ld\n", __STDC_VERSION__);
#else
    printf("C90 or earlier\n");
#endif
    return 0;
}
```
Compilación:

```bash
gcc version.c -o version.exe
```
(Este comando crea un ejecutable llamado version.exe)
Ejecución:

```bash
./version.exe
```
Resultado obtenido:

```yaml
STDC version: 201710
```
Los primeros cuatro dígitos (2017) indican el año del estándar del lenguaje C que está utilizando el compilador.
Actualice la versión del compilador de c11 a c17 (con posibilidad de forzarlo a c2x)

