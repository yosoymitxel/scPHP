# Librería de funciones útiles PHP - scPHP

Librería con funciones varias para PHP que nace a fin de simplicar ciertas tareas del lenguaje o versatilizar funciones ya existentes en este por medio de la parametrización y la evasión de excepciones.

## Grupos de funcionalidades

Este se divide en distintas finalidades de funciones usando como prefijo `sc_`

#### Ejemplo:
```
sc_dev_var_dump('prueba')
```

### DEV
Aquí encontramos funciones para hacer testeos rápidos siguiendo la filosofía "echo a todo lo que se mueva" asímismo poner información solo visible desde el DOM, etc.

#### Ejemplos:

```
sc_dev_echo('Título', 'Valor') // <p id='' class='' style='' name=''>Título: Valor</p>

sc_dev_var_dump([1,2]); // Imprime con una etiqueta <pre> un var_dump

sc_dev_activar_depurar_global(true); // Activa o desactiva el modo debug de php

sc_dev_echo_oculto('Esto solo lo veremos desde el HTML del sitio', true, 'id-para-ubicar-en-el-dom') // Imprime un var dump oculto dentro del DOM
```

### DOM
Se utiliza para creación de elementos HTML

#### Ejemplos:
```
sc_dom_crear_elemento();
```

## URL
Es informativo así como sirve para manejo de urls.

### Ejemplos:
```
sc_url_informacion_sitio_actual()
```

### SQL
Manejo de sql (actualmente requiere una variable $pdoLibreria en un escope anterior para obtenerlo como global $pdoLibreria)

#### Ejemplos:
```
sc_sql_lookup('SELECT * FROM usuario');
```

### STR

* Sirve para el manejo de strings desde expresiones regulares, cambios de casos (lower, upper, etc.), quitar espacios en blanco, saber si comieza o termina con alguna expresion, etc.

#### Ejemplos:
```
sc_str_reemplazar_expresion_regular('Hola mundo 123', '\d+',' '); //Hola mundo 

sc_str_quitar_espacios_blancos('Hola mundo,   esto es una      prueba'); //Holamundo,estoesunaprueba

sc_str_sin_caracteres_especiales('Eso está ahí'); //Eso esta ahi

sc_str_contiene('Hola mundo', 'Hola'); // true

sc_str_extraer_expresion_regular('1 - Hola mundo 2','\d'); // [1,2]

sc_str_incluye_expresion_regular('Hola mundo', '\d') // false
```

### JS
Opciones típicas de JS

#### Ejemplos

```
sc_js_alert('texto')
```
### IS
Saber que tipo de dato es

#### Ejemplos

```
sc_is_array(array('valor'))
```

### ARR
Manejo de array.

#### Ejemplos

```
sc_arr_incluye_expresion_regular(array('prueba'),'\w+')
```
### FEC
Manejo de fechas.

#### Ejemplos

```
sc_fec_formatear('2021-12-12 02:20:00','Y-m-d')
```

## Instalación 
#### Al descargarla para añadir se incluye con un require

```
require_once '/scPHP.php'
```

## Ejecutando las pruebas

Puedes escribir `sc_var_dump('prueba')` o `sc_dev_var_dump('prueba')` para saber si esta fue instalada correctamente

## Construido con 

* PHP - Lenguaje de programación

## Licencia 

Este proyecto está bajo la Licencia (MIT) 


---
Con ❤️ por [yosoymitxel](https://github.com/yosoymitxel)

