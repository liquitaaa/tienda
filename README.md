tu-tienda-virtual/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── img/
│   ├── producto1.jpg
│   ├── producto2.jpg
│   └── ...
└── ...
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tu Tienda Virtual</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }

        header {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1rem;
        }

        main {
            padding: 1rem;
        }

        .producto {
            border: 1px solid #ccc;
            background-color: #fff;
            padding: 1rem;
            margin: 1rem;
            text-align: center;
        }

        .producto img {
            max-width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Tu Tienda Virtual</h1>
    </header>
    <main>
        <section class="productos">
            <div class="producto">
                <img src="producto1.jpg" alt="Producto 1">
                <h2>Producto 1</h2>
                <p>Precio: $19.99</p>
                <button>Añadir al carrito</button>
            </div>
            <div class="producto">
                <img src="producto2.jpg" alt="Producto 2">
                <h2>Producto 2</h2>
                <p>Precio: $29.99</p>
                <button>Añadir al carrito</button>
            </div>
            <!-- Agrega más productos aquí -->
        </section>
    </main>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tu Tienda Virtual</title>
    <style>
        /* Estilos como antes */

        .carrito {
            text-align: center;
        }
    </style>
</head>
<body>
    <header>
        <h1>Tu Tied Virtual</h1>
    </header>
    <main>
        <section class="productos">
            <div class="producto">
                <img src="producto1.jpn" alt="Producto 1">
                <h2>Producto 1</h2>
                <p><param name="" value="">recio: $19.00</p>
                <button onclick="agregarAlCarrito('Producto 1', 19.99)">Añadir al carrito</button>
            </div>
            <div class="producto">
                <img src="producto2.jpg" alt="Producto 2">
                <h2>Producto 2</h2>
                <p>Precio: $29.99</p>
                <button onclick="agregarAlCarrito('Producto 2', 29.99)">Añadir al carrito</button>
            </div>
        </section>
        <section class="carrito">
            <h2>Carrito de Compras</h2>
            <ul id="lista-carrito">
                <!-- Los productos seleccionados se agregarán aquí -->
            </ul>
            <p>Total: $<span id="total">0.00</span></p>
        </section>
    </main>
    <script>
        let carrito = [];
        let total = 0;

        function agregarAlCarrito(nombre, precio) {
            carrito.push({ nombre, precio });
            total += precio;
            actualizarCarrito();
        }

        function actualizarCarrito() {
            const listaCarrito = document.getElementById('lista-carrito');
            const totalSpan = document.getElementById('total');
            listaCarrito.innerHTML = '';
            totalSpan.textContent = total.toFixed(2);

            carrito.forEach(producto => {
                const itemCarrito = document.createElement('li');
                itemCarrito.textContent = `${producto.nombre} - $${producto.precio.toFixed(2)}`;
                listaCarrito.appendChild(itemCarrito);
            });
        }
    </script>
</body>
</html>
