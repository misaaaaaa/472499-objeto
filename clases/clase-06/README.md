# Clase 06

### Anotaciones de la clase:
- Nivelación sobre el manejo de Github y reorganización de las bitácoras de los estudiantes.
- Explicación sobre lo que es un objeto según Graham Harman: Todo objeto tiene una composición y una relación. Las cualidades de los objetos pueden cambiar porque varían con el tiempo. Las metáforas combinan propiedades disímiles no esenciales de 2 objetos. Un objeto metafórico.

 Acá puedo anotar cosas

 Aprendimos a entrar en el editor de GitHub utilizando el punto (.)

 También se puede ingresar si cambiamos el .com por .dev en nuestro repositorio.

 ## Estructura de repositorios

Para meter bloques de código, o que respete la estructura de saltos de línea, es bueno usar comillas (```). Hay que encerrar nuestro bloque entre ambas estructuras.

```
 clase-00
 |- imagenes/      (ESTO ES UNA CARPETA)
 |- README.md

 
 clase-01
 |- imagenes/      (ESTO ES UNA CARPETA)
 |- README.md

entregas-01
|- imagenes/
|- códigos/
|- docs/
|- README.md
```

### Soy un título con 3 hashtags

Para cargar imágenes, usamos esta estrucutra

```
 ![texto alternativo](./imagenes/violetaparra.jpg)
```

 ![Violeta Parra con una máquina de escribir](./imagenes/violetaparra.jpg)

 Para cargar una imagen que está en otra carpeta, debo primero subir una jerarquía de archivo, lo que se hace con `../`. Esto se llama ruta relativa

 ![gif de prueba](../clase-01/gif-test.gif)

 ## Como agregar códigos de processing

Para que los bloques de código tengan estilo, después de las primeras comillas escribo el lenguaje de programación

 ` ```processing `

 ```processing
 /**
 * Mouse 2D. 
 * 
 * Moving the mouse changes the position and size of each box. 
 */
 
void setup() {
  size(640, 360); 
  noStroke();
  rectMode(CENTER);
}
 ```

## Bitácora de ejemplo

<https://github.com/disenoUDP/dis8644-2025-1-procesos/tree/main/10-Bernardita-lobo/sesion-07a
