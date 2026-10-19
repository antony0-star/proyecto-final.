# README --- Proyecto Eclipse Artesano

## 1. ¿Qué es Eclipse Artesano?

Eclipse Artesano es una página web de una tienda de productos
artesanales. Presenta colecciones de barro, artículos inspirados en la
cultura maya y tejidos. También incluye un carrito de compras.

## 2. Estructura del archivo

El proyecto principal está escrito en HTML, CSS y JavaScript dentro de
un mismo archivo.

### HTML

HTML organiza el contenido de la página: encabezado, menú, presentación,
categorías, historia, carrito y pie de página.

### CSS

CSS define el diseño visual: colores, tamaños, espacios, fuentes,
animaciones, distribución de elementos y adaptación a pantallas
pequeñas.

### JavaScript

JavaScript agrega interactividad. Permite añadir productos al carrito,
actualizar el contador y el total, eliminar productos, vaciar el
carrito, abrirlo y cerrarlo, y mostrar un mensaje al finalizar la
compra.

## 3. Partes principales de la página

### `<!DOCTYPE html>` y `<html lang="es">`

Indican que el documento utiliza HTML5 y que el idioma principal de la
página es español.

### `<head>`

Contiene información de configuración que normalmente no se muestra
directamente en la página.

-   `meta charset="UTF-8"` permite mostrar correctamente tildes, eñes y
    otros caracteres.
-   `meta name="viewport"` ayuda a que la página se adapte al tamaño de
    la pantalla.
-   `<title>` establece el título que aparece en la pestaña del
    navegador.
-   Los enlaces de Google Fonts cargan las fuentes DM Serif Display,
    Poppins y Permanent Marker.
-   `<style>` contiene las reglas CSS que dan formato a la página.

### `body`

Contiene todo el contenido visible de la página web.

### Encabezado (`header`)

Es la barra superior que permanece visible al desplazarse por la página.
Incluye el logotipo de Eclipse Artesano, el menú de navegación y el
botón del carrito.

### Logotipo (`.logo`, `.logo-icon` y `.logo-text`)

Muestra el símbolo decorativo y el nombre de la tienda.

### Menú de navegación (`nav`)

Incluye enlaces para ir al inicio, ver los productos, conocer la tienda
y visitar la sección de contacto.

### Botón del carrito (`.cart-button`)

Abre el carrito de compras. El elemento con `id="contador"` muestra
cuántos productos se han agregado.

### Presentación principal (`.hero`)

Es la sección grande que aparece al inicio. Incluye una imagen de fondo,
un título, una descripción y botones para explorar las colecciones o
conocer la historia del negocio.

### Barra de características (`.features`)

Presenta tres cualidades de la tienda: productos hechos a mano, piezas
únicas y trabajo realizado con pasión.

### Categorías (`#categorias`)

Muestra tres colecciones principales: - **Manos de barro:** productos
elaborados con barro. - **Legado Maya:** artículos inspirados en la
cultura maya. - **Casa de tejidos:** telas y tejidos artesanales.

Cada tarjeta tiene una imagen, un texto y un enlace que lleva a la
página correspondiente.

### Historia (`.story`)

Explica la idea y la misión de Eclipse Artesano, destacando el valor de
la creatividad, el trabajo manual y las tradiciones.

### Estadísticas (`.stats`)

Muestra datos visuales sobre la creatividad artesanal, las colecciones
disponibles y las historias por contar.

### Llamado a la acción (`.cta`)

Es una sección que invita a los visitantes a explorar los productos.

### Fondo oscuro del carrito (`.overlay`)

Es la capa semitransparente que aparece detrás del carrito cuando se
abre. Al hacer clic en ella, el carrito se cierra.

### Panel del carrito (`.cart-panel`)

Es el panel lateral donde aparecen los productos seleccionados, el
precio de cada uno y el total de la compra.

-   `#listaCarrito`: zona donde se muestran los productos agregados.
-   `#total`: muestra el costo total.
-   `hacerCompra()`: función que se ejecuta al pulsar «Finalizar
    compra».
-   `vaciarCarrito()`: botón para quitar todos los productos.
-   `eliminarProducto(indice)`: botón para quitar un producto
    específico.

### Pie de página (`footer`)

Es la parte inferior del sitio. Contiene el nombre del negocio, una
descripción, enlaces de navegación y el aviso de derechos reservados.

### Diseño adaptable (`@media`)

Las reglas `@media` cambian la distribución y los tamaños en pantallas
medianas y pequeñas, para facilitar la navegación desde teléfonos y
tabletas.

## 4. Funciones de JavaScript

### `let carrito = [];`

Crea una lista vacía donde se guardan temporalmente los productos
seleccionados.

### `agregarCarrito(nombre, precio = 0)`

Agrega un producto a la lista con su nombre y precio. Después actualiza
el carrito y lo abre.

### `actualizarCarrito()`

Actualiza el contador, dibuja los productos dentro del panel y calcula
el total de los precios.

### `eliminarProducto(indice)`

Elimina de la lista el producto que corresponde a la posición indicada y
actualiza el carrito.

### `abrirCarrito()`

Muestra el panel lateral del carrito y la capa oscura de fondo.

### `cerrarCarrito()`

Oculta el panel del carrito y la capa de fondo.

### `vaciarCarrito()`

Elimina todos los productos del carrito. Si ya está vacío, muestra una
alerta.

### `hacerCompra()`

Comprueba si el carrito tiene productos. Si contiene artículos, calcula
el total, muestra un mensaje de agradecimiento y vacía el carrito.

**Importante:** en la versión actual, la compra solo muestra un mensaje
de confirmación; todavía no genera ni imprime un recibo formal y tampoco
procesa pagos reales.

### Evento de la tecla Escape

Permite cerrar el carrito cuando se presiona la tecla Escape.

## 5. Clases, identificadores y funciones

-   **Clase CSS (`class`)**: se usa para aplicar el mismo estilo a uno o
    varios elementos, por ejemplo `.hero` o `.cart-button`.
-   **Identificador (`id`)**: identifica un elemento concreto para poder
    seleccionarlo desde CSS o JavaScript, por ejemplo `id="total"`.
-   **Función**: bloque de JavaScript que realiza una tarea específica,
    como abrir el carrito o calcular el total.
-   **Evento `onclick`**: ejecuta una acción cuando el usuario hace clic
    en un elemento.
-   **Enlace `href`**: dirige a otra sección de la página o a otro
    archivo HTML.
-   **Imagen `img`**: muestra una imagen y usa el atributo `alt` para
    describirla.

## 6. Archivos relacionados

El código enlaza a otros archivos HTML, como `barro.html`, `telas.html`,
`TRADICIONAL.HTML`, `nosotros.html` y `contacto.html`. Para que todos
los enlaces funcionen, esos archivos deben existir en las ubicaciones y
con los nombres indicados. En algunos enlaces los nombres no coinciden
exactamente, por lo que conviene revisarlos.

## 7. Cómo abrir el proyecto

1.  Guarda el archivo principal con extensión `.html`.
2.  Abre la carpeta del proyecto en Visual Studio Code.
3.  Comprueba que los demás archivos HTML enlazados estén en la carpeta
    correcta.
4.  Abre el archivo principal en un navegador, por ejemplo Google
    Chrome.
5.  Para probar el carrito, entra en una colección y agrega productos.
    Las funciones de carrito solo podrán mostrar precios correctos si
    las páginas de productos llaman a `agregarCarrito()` con el nombre y
    el precio correspondientes.

## 8. Resumen

Eclipse Artesano combina HTML para la estructura, CSS para el diseño y
JavaScript para las acciones interactivas. Su objetivo es mostrar
productos artesanales de forma atractiva y permitir que el visitante los
agregue a un carrito antes de finalizar una compra de demostración.
