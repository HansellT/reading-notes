# Tarea de la semana 11

## ¿Qué es el DOM?

- El DOM (Document Object Model) es una representación estructurada de un documento HTML o XML en forma de árbol. Permite que los lenguajes de programación, como JavaScript, interactúen con el contenido, la estructura y el estilo de una página web. Cada nodo en el árbol representa una parte del documento, como elementos HTML, atributos o texto.

## Relación entre el DOM y JavaScript

- JavaScript utiliza el DOM para acceder, manipular y modificar dinámicamente el contenido, estructura y estilos de una página web. Gracias al DOM, JavaScript puede realizar acciones como cambiar el texto de un elemento, agregar o eliminar nodos, y responder a eventos del usuario, como clics o teclas presionadas.

## ¿Qué método usarías para seleccionar un elemento del DOM por su ID y cómo se utiliza?

- El método que se utiliza es `document.getElementById()`. Este método selecciona un elemento del DOM que tiene un atributo `id` específico.

**Ejemplo:**
```javascript

const elemento = document.getElementById('miElemento')
console.log(elemento)
```

## ¿Qué método utilizarías para cambiar el color de fondo de un elemento en el DOM y cómo se implementaría?

- Para cambiar el color de fondo de un elemento, se utiliza la propiedad style.backgroundColor. Esta propiedad permite modificar el estilo background-color de un elemento.

**Ejemplo:**
```javascript

const elemento = document.getElementById('miElemento');
elemento.style.backgroundColor = 'lightblue'; // Cambia el color de fondo a azul claro
```







