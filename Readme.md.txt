index 
======
Este programa es una aplicación web que muestra productos de una API ficticia de tienda en línea y permite a los usuarios buscar y agregar productos a un carrito de compras. A continuación, describiré las partes principales del programa y lo que hace:

URL_API: Esta constante almacena la URL de la API ficticia que proporciona los datos de productos.
cardsContainerHTML: Selecciona un elemento del DOM con la clase ".cards-container" donde se mostrarán los productos.
searchInputHTML: Selecciona un elemento del DOM con el id "searchInput" que se utilizará para buscar productos.
Clase CartManager:

Esta clase se encarga de administrar el carrito de compras.
El constructor inicializa un carrito vacío.
saveCart(): Guarda el contenido del carrito en el almacenamiento local (localStorage).
getLocalCart(): Obtiene el carrito almacenado en el localStorage, si existe.
addToCart(productToAdd): Agrega un producto al carrito. Si el producto ya existe en el carrito, aumenta la cantidad. Si no existe, lo agrega al carrito.
Clase ProductsManager:

Esta clase administra los productos obtenidos de la API y su visualización en la página.
El constructor inicializa dos listas: una para almacenar todos los productos y otra para los productos que se deben mostrar.
addProduct(product): Agrega un producto a la lista de productos.
getProducts(): Devuelve la lista de todos los productos.
renderProducts(): Renderiza los productos en la página web.
filterProducts(value): Filtra los productos en función del valor de búsqueda y actualiza la lista de productos a mostrar.
Creación de Instancias:

Se crea una instancia de ProductsManager llamada productsManager.
Se crea una instancia de CartManager llamada cartManager.
Se llama a cartManager.getLocalCart() para cargar el carrito desde el almacenamiento local.
Se llama a productsManager.renderProducts() para mostrar los productos iniciales en la página.
Petición a la API y Renderizado de Productos:

Se realiza una solicitud fetch a la API (URL_API) para obtener datos de productos.
Los productos obtenidos se agregan a productsManager utilizando addProduct.
Luego, se llama a productsManager.renderProducts() para mostrar los productos en la página.
Event Listener para la Búsqueda:

Se agrega un event listener al elemento de entrada de búsqueda (searchInputHTML).
Cuando el valor de búsqueda cambia, se llama a productsManager.filterProducts() para filtrar y mostrar los productos que coinciden con la búsqueda.


Carrito de compras
==================
Se define una constante URL_API que almacena la URL de una API falsa que se utiliza para obtener información de productos.

Se selecciona elementos del DOM (Document Object Model) y almacena referencias a ellos en variables para su posterior manipulación. Estos elementos incluyen botones, contenedores y un elemento para mostrar el total del carrito.

Asociamos eventos de clic a los botones "Limpiar carrito" y "Confirmar carrito". Cuando se hace clic en estos botones, se ejecutan las funciones correspondientes para limpiar el carrito o confirmar la compra.

Llama a getLocalCart para cargar el carrito almacenado en el almacenamiento local y luego llama a renderCart para mostrar los productos del carrito en la interfaz de usuario.


La variable total se calcula en la función renderCart,