# Librería de funciones útiles PHP - scPHP

scPHP es una librería de PHP que contiene una serie de funciones y clases que facilitan el desarrollo de aplicaciones web en PHP. La librería incluye funciones para el manejo de string, la validación de formularios, gestión de bases de datos, la manipulación de expresiones regulares y mucho más.

## Categorías

scPHP está organizada en diferentes categorías que agrupan las funciones según su funcionalidad. Aquí hay una lista de las categorías disponibles:

* DEV: Debug
* DOM: Manejo de DOM - HTML
* URL: Manejo de URLs
* SQL: Manejo de SQL
* JS: Opciones de JavaScript
* STR: Manejo de strings
* FEC: Manejo de fechas
* ARR: Manejo de arrays
* IS: Tipo de variable
Cada categoría incluye una serie de funciones que facilitan el desarrollo de aplicaciones web en PHP.

## Categorías en sus grupos de funcionalidades

Este se divide en distintas finalidades de funciones usando como prefijo para toda la libería siempre primero `sc_` seguido de la abreviatura del grupo de funcionalidades.

#### Ejemplos:
```
sc_dev_var_dump('prueba')
```
Donde `sc_` es el prefijo de la librería y `dev_` indica que será del grupo development.
```
sc_str_contiene('Hola mundo', 'Hola');
```
Donde `sc_` es el prefijo de la librería y `str_` indica que será del grupo de manejo strings.

### 1) DEV
Aquí encontramos funciones para hacer testeos rápidos siguiendo la filosofía "echo a todo lo que se mueva" asímismo poner información solo visible desde el DOM, etc.

#### Ejemplos:

```
sc_dev_echo('Título', 'Valor') // <p id='' class='' style='' name=''>Título: Valor</p>

sc_dev_var_dump([1,2]); // Imprime con una etiqueta <pre> un var_dump

sc_dev_activar_depurar_global(true); // Activa o desactiva el modo debug de php

sc_dev_echo_oculto('Esto solo lo veremos desde el HTML del sitio', true, 'id-para-ubicar-en-el-dom') // Imprime un var dump oculto dentro del DOM
```

### 2) DOM
Se utiliza para creación de elementos HTML

#### Ejemplos:
```
sc_dom_crear_elemento();
```

### 3) URL
Es informativo así como sirve para manejo de urls.

#### Ejemplos:
```
sc_url_informacion_sitio_actual()
```

### 4) SQL
Manejo de sql (actualmente requiere una variable $pdoLibreria en un escope anterior para obtenerlo como global $pdoLibreria)

#### Ejemplos:
```
sc_sql_lookup('SELECT * FROM usuario');
```

### 5) STR
Sirve para el manejo de strings desde expresiones regulares, cambios de casos (lower, upper, etc.), quitar espacios en blanco, saber si comieza o termina con alguna expresion, etc.

#### Ejemplos:
```
sc_str_reemplazar_expresion_regular('Hola mundo 123', '\d+',' '); //Hola mundo 

sc_str_quitar_espacios_blancos('Hola mundo,   esto es una      prueba'); //Holamundo,estoesunaprueba

sc_str_sin_caracteres_especiales('Eso está ahí'); //Eso esta ahi

sc_str_contiene('Hola mundo', 'Hola'); // true

sc_str_extraer_expresion_regular('1 - Hola mundo 2','\d'); // [1,2]

sc_str_incluye_expresion_regular('Hola mundo', '\d') // false
```

### 6) JS
Opciones típicas de JS

#### Ejemplos

```
sc_js_alert('texto')
```
### 7) IS
Saber que tipo de dato es

#### Ejemplos

```
sc_is_array(array('valor'))
```

### 8) ARR
Manejo de array.

#### Ejemplos

```
sc_arr_incluye_expresion_regular(array('prueba'),'\w+')
```
### 9) FEC
Manejo de fechas.

#### Ejemplos

```
sc_fec_formatear('2021-12-12 02:20:00','Y-m-d')
```

## Instalación 
#### Al descargarla para añadir se incluye con un require:

```
require_once '/scPHP.php'
```

#### O... Instala vía composer:

Edita tu composer.json para incluir lo siguiente:

```json
{
    "require": {
        "yosoymitxel/scphp": "~2.0"
    }
}
```
## Ejecutando las pruebas

Puedes escribir `sc_var_dump('prueba')` o `sc_dev_var_dump('prueba')` para saber si esta fue instalada correctamente

## Construido con 

* PHP - Lenguaje de programación

## Licencia 

Este proyecto está bajo la Licencia (MIT) 


---
Con ❤️ por [yosoymitxel](https://github.com/yosoymitxel)

