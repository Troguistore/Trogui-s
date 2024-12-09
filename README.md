<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TROGUI - Organizador Esquinero</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #000;
        }
        header {
            background-color: #ffa500;
            color: #000;
            text-align: center;
            padding: 10px;
        }
        header h1 {
            margin: 0;
            font-size: 24px;
        }
        header p {
            margin: 5px 0;
            font-size: 14px;
        }
        .carousel {
            display: flex;
            overflow: hidden;
            width: 100%;
            position: relative;
            max-width: 600px;
            margin: 20px auto;
        }
        .carousel img {
            width: 100%;
            cursor: pointer;
        }
        .carousel-container {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        .carousel-controls {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }
        .carousel-controls button {
            background-color: rgba(0, 0, 0, 0.5);
            color: #fff;
            border: none;
            font-size: 18px;
            cursor: pointer;
            padding: 10px;
            border-radius: 50%;
        }
        .product-details {
            text-align: center;
            padding: 20px;
        }
        .product-details h2 {
            color: #ff6600;
        }
        .product-details p {
            margin: 10px 0;
        }
        .price {
            font-size: 18px;
            font-weight: bold;
        }
        .price .old-price {
            text-decoration: line-through;
            color: #888;
        }
        .price .new-price {
            color: #d00000;
        }
        .buttons {
            margin: 20px 0;
            display: flex;
            justify-content: center;
            gap: 10px;
        }
        .buttons a {
            text-decoration: none;
            padding: 10px 20px;
            font-size: 14px;
            color: #fff;
            border-radius: 5px;
            cursor: pointer;
        }
        .buy {
            background-color: #d00000;
        }
        .whatsapp {
            background-color: #25d366;
        }
        .more-products {
            display: block;
            margin: 20px auto;
            text-align: center;
            padding: 10px 20px;
            font-size: 14px;
            background-color: #ffa500;
            color: #000;
            text-decoration: none;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>TROGUI</h1>
        <p>Envíos gratis y pagos contra entrega a toda Colombia</p>
    </header>
    <div class="carousel">
        <div class="carousel-container" id="carousel-container">
            <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/591305/1704986444ESQUINERO%20BA%C3%91O%20GRANDE.webp" alt="Imagen 1" onclick="openImage(this.src)">
            <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/810509/17141685231712011594a06bc159-c69a-4f1c-915c-f830d16219ab.jpg" alt="Imagen 2" onclick="openImage(this.src)">
            <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/870695/1716066120170187249717018724972.jpg" alt="Imagen 3" onclick="openImage(this.src)">
        </div>
        <div class="carousel-controls">
            <button onclick="prevSlide()">&#10094;</button>
            <button onclick="nextSlide()">&#10095;</button>
        </div>
    </div>
    <div class="product-details">
        <h2>Organizador Esquinero</h2>
        <p>Altura ajustable: De 1 m a 2.29 m, se adapta a cualquier espacio. 4 estantes amplios, material duradero, instalación fácil y más.</p>
        <p class="price">
            <span class="old-price">75,000</span>
            <span class="new-price">59,000 COP</span>
        </p>
        <div class="buttons">
            <a href="https://forms.gle/ocFidTiYodHjo1QB7" class="buy">Comprar</a>
            <a href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20%C2%BFPuedes%20ayudarme%20con%20los%20detalles%20de" class="whatsapp">WhatsApp</a>
        </div>
    </div>
    <a href="https://troguistore.github.io/TROGUIROPA/" class="more-products">Ver más productos</a>
    <script>
        let currentIndex = 0;

        function nextSlide() {
            const container = document.getElementById('carousel-container');
            const images = container.children;
            currentIndex = (currentIndex + 1) % images.length;
            container.style.transform = `translateX(-${currentIndex * 100}%)`;
        }

        function prevSlide() {
            const container = document.getElementById('carousel-container');
            const images = container.children;
            currentIndex = (currentIndex - 1 + images.length) % images.length;
            container.style.transform = `translateX(-${currentIndex * 100}%)`;
        }

        function openImage(src) {
            window.open(src, '_blank');
        }
    </script>
</body>
</html>
