# Examen Trimestral LMSGI

Nombre: _______________________
Fecha: _______________________
IP local: _______________________

## Instrucciones

Antes de realizar el examen, rellena los campos de arriba con tu nombre, la fecha y la IP local de tu máquina.

> Usa `ip a` para obtener tu IP local en Linux. Debe estar en el rango `192.168.x.x`

Este examen cubre los conceptos aprendidos durante el trimestre en el curso de LMSGI.

Primero asegúrate de tener este repositorio clonado en tu máquina local.

Luego, borra la carpeta `.git` actual para eliminar el historial de versiones previo.

Finalmente, inicializa un nuevo repositorio Git y subelo a tu cuenta de GitHub en privado.

Una vez compruebes que todo está correcto, lee atentamente las preguntas y responde en los archivos correspondientes.

> Recuerda hacer commits frecuentes y descriptivos a lo largo del examen.

## Pregunta 1: Markdown (1 Punto)

En el repositorio encontrarás un **pdf** generado a partir de un archivo **markdown**.

Tu objetivo es crear manualmente un archivo markdown equivalente al pdf proporcionado, asegurándote de que el formato y la estructura sean lo más similares posibles.

## Pregunta 2: De Markdown a HTML (2 Puntos)

Convierte el archivo markdown que has creado a su HTML equivalente, el documento final debe tener una **estructura completa** típica de un documento HTML.

Describe brevemente a continuación los pasos que has seguido para realizar la conversión:

1. Ejecuto el comando `pandoc receta.md -o ejercicio2.html` para generar un html básico a partir de mi md.
2. Genero una estructura básica con `! + tab` en VSCode dentro de `ejercicio2.html`.
3. Selecciono el contenido generado por pandoc y con `alt` lo muevo dentro del `body` de la estructura básica.
4. Modifico el título del `head` para que sea más descriptivo.
5. Formateo el documento para que sea más legible.

## Pregunta 3: HTML sin usar HTML (2 Puntos)

1. Crea un nuevo archivo `html` con una estructura *básica*, pero que no tenga contenido.
2. Crea un tag `script` dentro del mismo.
3. Dentro del script, genera el mismo contenido que el HTML del paso anterior, pero solo usando *JavaScript* para crear y añadir los elementos al DOM. **NO** puedes usar HTML para crear el contenido, solo JavaScript.

## Pregunta 4: Elección aleatoria (3 Puntos)

Crea un archivo `html` llamado `eleccion.html` que contenga:

1. Un parrafo donde se mostrará inicialmente el texto *Haz clic en el botón*.
2. Un botón con el texto *Elegir*.
3. Un script en JavaScript que contenga un array con al menos 5 opciones (pueden ser nombres, colores, ciudades, etc).
4. Cuando el usuario haga clic en el botón, se debe elegir una opción aleatoria del array y mostrarla en el párrafo, reemplazando el texto inicial.

## Teoria (2 Puntos)

Responde brevemente a las siguientes preguntas:

1. ¿Qué es una etiqueta en HTML? Dame 3 ejemplos que no se mencionen o se usen en preguntas del examen.

Una etiqueta HTML es un elemento básico para estructurar y definir el contenido de una página web. Suelen tener la siguiente estructura:

```
<tag de apertura atributo="mas info">Contenido</tag de cierre>
```

Algunos tags que no se han usado antes en el examen:

- `<form>`
- `<a>`
- `<code>`

2. ¿Qué es un atributo? Dame 3 ejemplos junto a sus etiquetas correspondientes.

Un atributo añade información adicional a un tag HTML. En algunos casos es una parte obligatoria para que el tag cumpla su función:

- `<a href="https://www.google.com">Google</a>`
- `<img src="imagen.jpg" alt="Descripción de la imagen">`
- `<button onclick="miFuncion()">Clic aquí</button>`

3. ¿Como reconoces una etiqueta de apertura y una de cierre?

Las etiquetas de apertura no tienen una barra inclinada `/` después de abrir la etiqueta:

```
<tag>  --> Etiqueta de apertura
</tag> --> Etiqueta de cierre
```

4. ¿Para qué se usa la etiqueta `<head>` en un documento HTML?

Añade metadatos e información adicional para el navegador, es información que no se muestra directamente al usuario en la página web.

5. ¿Qué es un `id`? ¿Y una `class`? ¿En qué se diferencian?

Ambos sirven para identificar elementos HTML y capturarlos luego en *CSS* o *JavaScript*.

Los `id` son únicos, no deberiamos repetirlos en la misma página.

Las `class` pueden repetirse en varios elementos, y sirven para agruparlos bajo una misma categoría o estilo.

6. ¿Qué diferencia hay entre un `<div>` y un `<span>`?

Ambos son contenedores genéricos, pero `<div>` es un contenedor de bloque, esto hace que el contenido aparezca en una nueva línea, mientras que `<span>` es un contenedor de línea, haciendo que se vea en la misma línea que el anterior contenido.

7. ¿Qué diferencia hay entre `let` y `const` en JavaScript?

Ambos nos permiten declarar variables.

`let` nos deja reasignar un nuevo valor a la variable posteriormente.
`const` es inmutable, no podemos cambiar su valor una vez asignado.

Ambos son limitados al bloque donde se declaran.

8. ¿Qué es el DOM en JavaScript?

Es una representación estructurada del documento HTML, un objeto al que podemos acceder y manipular mediante JavaScript.

Se accede mediante el objeto global `document`.

9. ¿Como recorrerías el siguiente array en JavaScript para mostrar cada uno de sus elementos en la consola?

```javascript
const frutas = ['manzana', 'plátano', 'cereza', 'naranja', 'uva'];

for (let i = 0; i < frutas.length; i++) {
    console.log(frutas[i]);
}

frutas.forEach(fruta => {
    console.log(fruta);
});

frutas.forEach(fruta => console.log(fruta));
```

10. Sustituye el nombre de la siguiente función JavaScript por una palabra mas apropiada a su funcionalidad:

```javascript
function choose(a) {
    return a[Math.floor(Math.random() * a.length)];
}
```

> Otros nombres apropiados podrían ser `getRandomElement`, `selectRandomItem`, `pickRandomValue`, `seleccionarDesdeArray`, etc.

