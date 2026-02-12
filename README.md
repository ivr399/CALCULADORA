# CALCULADORA
# Documentación de la Calculadora HTML

## Descripción General

Esta es una calculadora web sencilla construida completamente con HTML, CSS y JavaScript. Permite realizar operaciones matemáticas básicas como suma, resta, multiplicación y división a través de una interfaz visual atractiva y funcional.

## Estructura del Documento

### Encabezado HTML

El documento comienza con la declaración DOCTYPE HTML5 y configura el idioma español. En la sección head se definen:

- La codificación de caracteres UTF-8
- La configuración del viewport para diseño responsivo
- El título de la página
- Los estilos CSS embebidos

### Estilos CSS

#### Estilos del Body

El cuerpo de la página utiliza Flexbox para centrar la calculadora tanto vertical como horizontalmente en la ventana del navegador. Se aplica un degradado de fondo con tonos púrpura que va desde un color más claro hacia uno más oscuro, creando un efecto visual agradable.

#### Contenedor de la Calculadora

El contenedor principal tiene un fondo blanco con bordes redondeados y una sombra que le da profundidad y la hace destacar sobre el fondo degradado. El padding interno proporciona espacio entre los bordes y el contenido.

#### Pantalla de Visualización

La pantalla es un campo de entrada de texto de solo lectura con las siguientes características:

- Fondo oscuro con texto blanco para buen contraste
- Alineación del texto a la derecha, imitando calculadoras tradicionales
- Tamaño de fuente grande para facilitar la lectura
- Bordes redondeados que mantienen la coherencia visual
- Margen inferior que la separa de los botones

#### Sistema de Botones

Los botones están organizados mediante CSS Grid en una cuadrícula de 4 columnas con espaciado uniforme entre ellos. Esta distribución permite una disposición ordenada y predecible.

#### Estilos de Botones Base

Todos los botones comparten características comunes:

- Padding generoso para facilitar la interacción
- Fuente de tamaño legible
- Sin bordes predeterminados
- Esquinas redondeadas
- Cursor de puntero al pasar sobre ellos
- Fondo gris claro
- Transiciones suaves para animaciones
- Efectos hover que cambian el color y escalan ligeramente el botón
- Efecto de presión que reduce el tamaño al hacer clic

#### Botones Especiales

**Botones de operadores**: Tienen un fondo púrpura con texto blanco, destacándose de los números.

**Botón igual**: Con fondo verde y ocupando dos columnas de la cuadrícula para mayor prominencia.

**Botón limpiar**: Con fondo rojo y ocupando dos columnas, indicando visualmente su función de reinicio.

### Estructura HTML del Cuerpo

El cuerpo contiene un div con clase calculadora que engloba:

- Un campo de entrada para la pantalla con ID único
- Un contenedor de botones con la disposición de la calculadora

#### Distribución de Botones

**Primera fila**: Botón de limpiar ocupando dos espacios, seguido de división y multiplicación.

**Segunda fila**: Números 7, 8, 9 y el operador de resta.

**Tercera fila**: Números 4, 5, 6 y el operador de suma.

**Cuarta fila**: Números 1, 2, 3 y botón de borrado.

**Quinta fila**: Número 0, punto decimal y botón igual ocupando dos espacios.

### Funcionalidad JavaScript

#### Función agregar

Esta función recibe un valor como parámetro y lo concatena al contenido actual de la pantalla. Se utiliza para números y operadores, permitiendo construir la expresión matemática.

#### Función limpiar

Elimina todo el contenido de la pantalla, dejándola vacía. Es útil para empezar un nuevo cálculo desde cero.

#### Función borrar

Remueve el último carácter del contenido de la pantalla utilizando el método slice. Permite corregir errores sin tener que limpiar toda la expresión.

#### Función calcular

Esta función evalúa la expresión matemática contenida en la pantalla:

- Utiliza la función eval para interpretar y calcular la expresión
- Está envuelta en un bloque try-catch para manejar errores
- Si la expresión es válida, muestra el resultado
- Si hay un error de sintaxis, muestra el texto "Error" en la pantalla

## Características Principales

### Operaciones Disponibles

- Suma
- Resta
- Multiplicación
- División
- Números decimales

### Funciones de Control

- Limpiar toda la pantalla
- Borrar el último carácter ingresado
- Evaluación de expresiones matemáticas

### Diseño Visual

- Interfaz moderna y atractiva
- Gradiente de fondo
- Efectos hover y de clic en botones
- Código de colores para diferentes tipos de botones
- Sombras y bordes redondeados para profundidad visual

### Usabilidad

- Disposición intuitiva similar a calculadoras físicas
- Pantalla de solo lectura para evitar entrada manual errónea
- Feedback visual al interactuar con botones
- Diseño responsivo que se adapta a diferentes tamaños de pantalla

## Consideraciones de Seguridad

El código utiliza la función eval para evaluar expresiones matemáticas. Aunque en este contexto controlado es aceptable, en aplicaciones de producción con entrada de usuarios externos sería recomendable usar alternativas más seguras como bibliotecas de parsing de expresiones matemáticas.

## Posibles Mejoras Futuras

- Agregar más operaciones como porcentajes, raíces cuadradas o exponentes
- Implementar historial de cálculos
- Añadir soporte para teclado físico
- Mejorar el manejo de errores con mensajes más descriptivos
- Implementar memoria de calculadora
- Agregar modo oscuro/claro
´´'mermaid
classDiagram
    %% Clase Producto
    class Producto {
        - String nombre
        - double precioBase
        + Producto(String nombre, double precioBase)
        + double getPrecioBase()
    }

    %% Clase CalculadoraIVA
    class CalculadoraIVA {
        - final double IVA = 0.21
        + double calcularPrecioFinal(double precio)
    }

    %% Clase Main
    class Main {
        + main(String[] args)
    }

    %% Relaciones
    Main --> Producto : usa
    Main --> CalculadoraIVA : usa
