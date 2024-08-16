 <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TROGUI ROPA - Tienda Online</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #000000;
            color: #ffffff;
        }
        header {
            background-color: #ff6600;
            color: #ffffff;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        header h1 {
            margin: 0;
            color: #ff8c00;
        }
        #search {
            width: 80%;
            padding: 10px;
            margin-top: 10px;
            font-size: 16px;
        }
        .product-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
        }
        .product {
            border: 1px solid #cccccc;
            border-radius: 10px;
            margin: 10px;
            padding: 20px;
            width: 250px;
            text-align: center;
            background-color: #f9f9f9;
            color: #000000;
        }
        .product img {
            max-width: 100%;
            border-radius: 10px;
        }
        .product h2 {
            color: #ff6600;
            font-size: 24px;
        }
        .product p {
            font-size: 16px;
        }
        .product .price {
            font-size: 20px;
            font-weight: bold;
        }
        .product button {
            background-color: #000000;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }
        .product button:hover {
            background-color: #ff6600;
        }
    </style>
</head>
<body>
    <header>
        <h1>TROGUI ROPA</h1>
        <p><strong>Envío gratis y pagos contra entrega a toda Colombia</strong></p>
        <input type="text" id="search" placeholder="Buscar productos...">
    </header>
    <main>
        <div class="product-list" id="product-list">
            <!-- Aquí se insertarán los productos -->
        </div>
    </main>
    <script>
        const products = [
            {
                name: 'Tenis adidas capellada',
                price: '89,000',
                description: 'Tallas: 35 36 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711254/1710444483WhatsApp%20Image%202024-03-14%20at%202.09.47%20PM%20(1).jpeg'
            },
            {
                name: 'Adidas 2k Blanco Naranja Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284293/17018822151701882215xltU3RMvvSS7M6N9juJct9FdtTbEV5GJG8JT46p7.jpg'
            },
            {
        "name": "Tapete Antideslizante Galaxia Tpcos07",
        "price": "29,000",
        "description": "Tapete de poliéster de 39.5 x 60 cm. Perfecto para decoración y múltiples usos. Ideal para la puerta delantera, cocina, baño, dormitorio, sala, entre otros. Adecuado para amantes del cosmos y mascotas. Textura suave y material antideslizante, duradero y fácil de lavar. Se despacha aleatorio según disponibilidad. Contenido: 1 tapete antideslizante de galaxia. 100% nuevo.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/79394/17030214261703021426Tapete%20Antideslizante%20Galaxia%20Cosmos%20Multiusos%20TPCOS%204.jpg"
    },
    {
        "name": "Tapete Antideslizante Absorbente Combo",
        "price": "49,000",
        "description": "Tapete de PVC y terciopelo técnico, con fuerte antideslizante y absorción de agua rápida. Ideal para baños, cocinas, lavanderías, y más. Alta calidad, duradero y fácil de limpiar. Disponible en dos tamaños: 120x40 cm y 60x40 cm. Colores y patrones modernos que combinan con cualquier decoración.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/565196/17027618531702498479Tapete%20de%20cocina08.jpg"
    },
    {
        "name": "Tapete Alfombra Para Baño Absorbente",
        "price": "37,000",
        "description": "Alfombra de baño super absorbente y antideslizante. Hecha de material suave y ecológico, con superficie que absorbe la humedad y capa de espuma que evapora rápidamente. Fácil de lavar y duradera. Medidas: 40x60 cm. Incluye 1 alfombrilla. Garantía de 30 días por defectos de fábrica.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/257672/17018993201701899320Tapete%20De%20Ba%C3%B1o%20Super%20Absorbente%20Y%20Antideslizante%20A.jpg"
    },
{
    name: 'Tapete Antideslizante Galaxia',
    price: '29,000',
    description: 'Tapete moderno de poliéster de 39,5 x 60 cm. Perfecto para decoración, uso en diversas superficies, y adecuado para mascotas. Material antideslizante, duradero y fácil de lavar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/79394/17030214261703021426Tapete%20Antideslizante%20Galaxia%20Cosmos%20Multiusos%20TPCOS%204.jpg'
},
{
    name: 'Tapete Antideslizante Absorbente Combo',
    price: '49,000',
    description: 'Tapete de PVC y terciopelo, con absorción de agua y secado rápido. Firme base antideslizante. Ideal para baños, cocinas, y más. Disponible en 120x40 cm y 60x40 cm.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/565196/17027618531702498479Tapete%20de%20cocina08.jpg'
},
{
    name: 'Tapete Alfombra Para Baño Absorbente',
    price: '37,000',
    description: 'Alfombrilla para baño de 40x60 cm, suave y respetuosa con la piel. Absorbe y evapora agua rápidamente. Borde de corte suave, fácil de limpiar y lavar. Amplia aplicación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/257672/17018993201701899320Tapete%20De%20Ba%C3%B1o%20Super%20Absorbente%20Y%20Antideslizante%20A.jpg'
},
{
    name: 'Tapete Mágico Ultra Absorbente 30x40',
    price: '35,000',
    description: 'Tapete absorbente y antideslizante de 30x40 cm. Ideal para mantener tu cocina seca al escurrir platos. Material duradero, fácil de limpiar y plegable sin deformarse.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/884774/1716561673Tapete-absorbente-cocina-FK23D-288.11.jpg'
},
{
    name: 'Soporte Base Computador Portátil Ajustable',
    price: '36,000',
    description: 'Soporte para laptop con 7 configuraciones de altura. Compacto, ligero y portátil. Soporta hasta 20kg, con almohadillas antideslizantes. Diseño ergonómico y plegable, fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/589038/1704838924BASE%20AJUSTABLE%20PARA%20PC.png'
},
{
    name: 'Soporte De Toallas Cocina Baño',
    price: '32,000',
    description: 'Soporte de toallas de acero inoxidable y material ABS, fácil de instalar sin perforar. Polos giratorios para un secado eficiente. Duradero y con diseño elegante para cualquier ambiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/212389/17023012281702301228Screenshot_176.jpg'
},
{
    name: 'Mini Masajeador De Cuello Electrico',
    price: '29,000',
    description: 'Masajeador de cuello portátil con 6 modos y 6 niveles de fuerza. Funciona con 2 pilas AAA. Compacto y fácil de usar, ideal para aliviar dolores musculares.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/624286/1706630140MASAJEADOR%20DE%20CEULLO%202.webp'
},
{
    name: 'Masajeador De Cuello Con Electrodos',
    price: '49,000',
    description: 'Masajeador con infrarrojo, ultrasonido y electro estimulación. Alivia el dolor muscular y mejora la circulación. Incluye collar masajeador, cable de conexión y electro estimuladores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918148/1718726800113574820_1.avif'
},
{
    name: 'Masajeador De Cuello Electrico Alivia Dolor',
    price: '89,000',
    description: 'Masajeador eléctrico con 9 niveles de fuerza y varios modos de masaje. Alivia el dolor muscular en cuello, espalda y más. Incluye sistema de auto cierre de seguridad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/415538/1695853630D_NQ_NP_2X_999480-MCO50742711359_072022-F.webp'
},
{
    name: 'Power Bank Super Cargador',
    price: '79,000',
    description: 'Power bank con carga rápida, 2 puertos USB 3.0 y 1 puerto tipo C. Pantalla indicadora, carga inalámbrica, 6,700mAh de capacidad. Garantía de 30 días por mal funcionamiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/850687/1715290627CARGADOR1.JPG'
},
{
    name: 'Power Bank Pb11',
    price: '75,000',
    description: 'Cargador portátil de 10,000 mAh con USB para todo tipo de teléfonos. Batería de polímero de litio. Tamaño compacto, fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/414601/1695830205powerbank-10000-mah-pb11-396294.jpg'
},
{
    name: 'Power Bank Multi Puertos 10000mah',
    price: '89,000',
    description: 'Power Bank de 10,000 mAh, diseño delgado con luz LED. Salidas USB y Tipo C, compatible con iPhone, Android, y más. Ideal para viajes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/454731/1698079425PILA%20PORTATIL%20CARGADOR%20%20POWER%20BANK%20GAR%20148%2004.png'
},
{
    name: 'Audífonos In Ear Inalámbricos F9 5 Negro',
    price: '39,000',
    description: 'Audífonos in-ear inalámbricos con tecnología TWS. Alcance de 10 m, 5 h de batería, cancelación de ruido, micrófono y estuche de carga. Resistente al agua.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/241251/1701975659170197565910000295_10374437_1253317.png'
},
{
    name: 'Audífonos Manos Libres Micrófono Vidvie',
    price: '29,000',
    description: 'Audífonos con micrófono, control de volumen y botón de control. Conector de 3.5mm. Práctico y cómodo para el uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/582944/17043128401.jpg'
},
{
    name: 'Audífonos Inalámbricos Bluetooth P9',
    price: '65,000',
    description: 'Audífonos Bluetooth con sonido estéreo claro, control de ruido, y diseño elegante. Alcance de 10-15 m. Livianos y cómodos para llevar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/770644/1712890413gsc_121751346_3168857_3.webp'
},
{
    name: 'Reloj Smart Watch + Audífonos +7 Pulsos',
    price: '109,000',
    description: 'Smartwatch con AirPods y 7 pulsos. Resistente al agua y sudor (IPX4). Ideal para deportes y entretenimiento con ajuste personalizado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/734216/1711486970I20.png'
},
{
    name: 'Funda Protectora Case Audífonos Serie 3',
    price: '29,000',
    description: 'Funda de silicona para Audífonos Serie 3. Protección contra golpes, caídas y suciedad. Disponible en varios colores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/252950/17019086881701908688IMG-20230505-WA0028.jpg'
},
{
    name: 'Audífonos M25',
    price: '59,000',
    description: 'Audífonos M25 con sonido superior y Bluetooth 5.3. A prueba de salpicaduras, 5 h de reproducción, diseño ergonómico. Perfectos para música y gaming.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/823617/1714671391D_NQ_NP_695218-MCO72871806146_112023-O.webp'
},
{
    name: 'Airpods Audífonos Serie 3 Inalámbricos',
    price: '59,000',
    description: 'AirPods con cancelación activa de ruido y modo ambiente. Conexión instantánea con iPhone y Apple Watch, cómodos para uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/71767/17030248951703024895WhatsApp%20Image%202022-08-02%20at%202.24.07%20PM.jpeg'
},
{
    name: 'Combo 2x1 Audífonos Air39',
    price: '69,000',
    description: 'Combo de audífonos Air39 con excelente calidad de sonido. Diseño ergonómico y conexión Bluetooth para una experiencia inalámbrica completa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/860340/17157030869combo.png'
},
{ 
  nombre: 'Impresora Portatil', 
  precio: '579,000', 
  descripción: 'Impresora compacta para viajes. Imprime PDF, fotos, y más. Conexión inalámbrica, batería de 1500 mAh. Tamaño de impresión A4, aplicación para edición gratuita, impresión térmica sin tinta.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/900351/1717095755WhatsApp%20Image%202024-05-30%20at%201.32.08%20PM.jpeg' 
},
{ 
  nombre: 'Rollo Para Impresora Térmica Celular X5', 
  precio: '34,000', 
  descripción: '', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/633780/1707152621IMPRESORA%20TERMICA%20PARA%20CELULAR%2007.png' 
},
{ 
  nombre: 'Smart Watch Z78 Ultra', 
  precio: '105,000', 
  descripción: 'Reloj inteligente con monitor de salud, impermeable IP67, pantalla HD de 1.52". Ideal para deportes, conexión sencilla a aplicaciones, múltiples idiomas.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/578944/1703859144cc65592e-d8ea-4498-a809-5f674d65a1a5.jpeg' 
},
{ 
  nombre: 'Reloj Smart Watch Ld6 Serie 7', 
  precio: '79,000', 
  descripción: 'Reloj inteligente con monitor de ritmo cardíaco, marcador de pasos, carga magnética, notificaciones.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/225802/17019846181701984618reloj-smart-watch-ld6-serie-7-dts-shop-plus-245065060.jpg' 
},
{ 
  nombre: 'Smart Watch T100 Plus', 
  precio: '119,000', 
  descripción: 'Reloj inteligente con pantalla IPS 1.75", 11 carátulas, 8-10 horas de uso continuo. Funciones avanzadas para deportes y notificaciones.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/48572/17030809051703080905SMART.jpeg' 
},
{ 
  nombre: 'Smart Watch P100', 
  precio: '129,000', 
  descripción: 'Incluye 2 relojes inteligentes (Serie 7 y 8), 4 pulseras, protector, batería MagSafe, cargador y cable Tipo C.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/747339/1712175705WhatsApp%20Image%202024-04-03%20at%203.06.56%20PM.jpeg' 
},
{ 
  nombre: 'Smart Watch K950 Ultra Waterproof', 
  precio: '129,000', 
  descripción: 'Reloj inteligente impermeable con monitor de salud, notificaciones, control de música, linterna y personalización de carátulas.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/445317/1697575434iiii.jpeg' 
},
{ 
  nombre: 'Smart Watch T800 Ultra 2 Doble Correa', 
  precio: '59,000', 
  descripción: '', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/669114/1714512204Imagen%20de%20WhatsApp%202024-04-30%20a%20las%2010.53.14_740e6025.jpg' 
},
{ 
  nombre: 'Smart Watch Ultra 2 Gama Alta', 
  precio: '139,000', 
  descripción: 'Reloj inteligente premium con alto rendimiento, carga rápida, personalización de carátulas, y monitoreo de salud.', 
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711848/1710453560WhatsApp%20Image%202024-03-14%20at%209.33.01%20AM.jpeg' 
},
{
  nombre: 'Reloj Smart Watch Táctil Redondo K700',
  precio: '129,000',
  descripción: 'Reloj inteligente redondo con GPS, pantalla táctil de 1.43", monitor de ritmo cardíaco, 100 modos deportivos, Bluetooth, carga rápida, batería de 3 días, llamadas, notificaciones, asistente de voz.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/916371/1718471497RELOJ%20K700.jpg'
},
{
  nombre: 'Smart Watch T800',
  precio: '65,000',
  descripción: 'Reloj inteligente con pantalla LCD HD 1.81", Bluetooth, 450mAh, carga inalámbrica, modos deportivos, monitoreo de salud, asistente de voz, personalización de carátulas.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803240/1713994717WhatsApp%20Image%202024-04-24%20at%204.35.03%20PM.jpeg'
},
{
  nombre: 'Reloj Smart Watch F8 Fitness Monitor',
  precio: '99,000',
  descripción: 'Reloj inteligente con monitor de ritmo cardiaco, podómetro, control de cámara, alertas de llamadas y mensajes, monitor de sueño, y múltiples aplicaciones de fitness.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/52129/17030803461703080346photo5172861897408621119%20(1).jpg'
},
{
  nombre: 'Reloj Inteligente Smart Watch T500 Pro',
  precio: '49,000',
  descripción: '',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/733689/1711480324T500%20PRO1.jpg'
},
{
  nombre: 'Patillera Y Afeitadora Buda',
  precio: '33,000',
  descripción: 'Patillera y rasuradora metálica con diseño antideslizante, corte de cabello potente y silencioso, recargable, incluye 3 guías de corte y cepillo de limpieza.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/88251/171157679217030150911703015091photo_4976845766182152946_x.jpg'
},
{
  nombre: 'Mini Afeitadora Bb 339d',
  precio: '49,000',
  descripción: 'Afeitadora eléctrica compacta con cuchillas de alta velocidad, cabezal flotante 3D, impermeable IPX7, carga rápida USB y 90 minutos de uso continuo.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/382606/17018728061701872806MIN-2.jpg'
},
{
  nombre: 'Afeitadora Electrica Profesional',
  precio: '85,000',
  descripción: 'Afeitadora recargable con cabezal flotante, impermeable IPX7, pantalla LED, batería de 1200mAh, y 150 minutos de uso con 2 horas de carga.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/666967/1708543344Afeitadora.png'
},
{
  nombre: 'Afeitadora Multifuncional 3 En 1 Dorada',
  precio: '65,000',
  descripción: 'Afeitadora eléctrica 3 en 1 con pantalla LCD, motor potente, diseño compacto y portátil, fácil limpieza, carga rápida y uso en cualquier momento.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/862656/1715787767maquina%203%20en%201112.jpg'
},
{
  nombre: 'Maquina Rasuradora Inalámbrica Wahl Prof',
  precio: '85,000',
  descripción: 'Rasuradora Wahl inalámbrica con batería de litio, 70 minutos de uso continuo, motor potente de 6500 RPM, cuchillas profesionales ajustables para cortes precisos.',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/164867/1702306003170230600310000295_10352990_1155538.png'
},
{
  nombre: 'Máquina De Afeitar 3 En 1 Rasuradora',
  precio: '59,000',
  descripción: '',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/438077/16971267472.jpg'
},
{
  nombre: 'Extractor De Leche Eléctrico Doble',
  precio: '69,000',
  descripción: '',
  imagen: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761617/1712617177EXTRACTOR%20M371%20JPG'
},
    {
        "name": "Tapete Mágico Ultra Absorbente 30 40",
        "price": "35,000",
        "description": "Tapete de cocina absorbente de caucho natural, súper absorbente y de secado rápido. Resistente a manchas, aceite y calor. Ideal para escurrir platos sin desbordar agua. Material ultra absorbente y antideslizante. Medidas: 30x40 cm. Colores: Negro, Azul, Beige. Incluye 1 tapete.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/884774/1716561673Tapete-absorbente-cocina-FK23D-288.11.jpg"
    },
    {
        "name": "Soporte Base Computador Portátil Ajustable",
        "price": "36,000",
        "description": "Soporte para laptop con 7 configuraciones de altura, protege tus ojos y mejora la postura. Compacto, ligero y portátil, soporta hasta 20 kg. Almohadillas antideslizantes y funda protectora incluidas. Garantía por defectos de fábrica si se devuelve en su empaque original.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/589038/1704838924BASE%20AJUSTABLE%20PARA%20PC.png"
    },
    {
        "name": "Soporte De Toallas Cocina Baño",
        "price": "32,000",
        "description": "Soporte de toallas fácil de instalar sin perforaciones. Polos giratorios de acero inoxidable y ABS para mayor durabilidad. Adecuado para uso comercial y doméstico. Diseño elegante que añade estilo al ambiente.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/212389/17023012281702301228Screenshot_176.jpg"
    },
    {
        "name": "Mini Masajeador De Cuello Eléctrico",
        "price": "29,000",
        "description": "Masajeador eléctrico de cuello con 6 modos y niveles de masaje. Compacto y portátil, funciona con 2 pilas AAA. Capacidad de batería de 120 mAh. Fácil de usar, ajustable a diferentes necesidades. Ideal para aliviar tensiones musculares.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/624286/1706630140MASAJEADOR%20DE%20CEULLO%202.webp"
    },
    {
        "name": "Masajeador De Cuello Con Electrodos",
        "price": "49,000",
        "description": "Masajeador de cuello recargable con 3 modalidades: calor infrarrojo, ultrasonido y electrofrecuencia. Tecnología de ajuste en 3D. Incluye collar masajeador, cable y 2 electroestimuladores. Dimensiones: 16x14x4.5 cm. Garantía de 10 días por defectos de fábrica.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/918148/1718726800113574820_1.avif"
    },
    {
        "name": "Masajeador De Cuello Eléctrico Alivia Dolor",
        "price": "89,000",
        "description": "Masajeador eléctrico para cuello, espalda y hombros con 9 niveles de fuerza y función de auto cierre de seguridad. Funcionalidad de masaje multidireccional. Tensión nominal: 220V, potencia: 55W. Garantía del vendedor: 1 mes.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/415538/1695853630D_NQ_NP_2X_999480-MCO50742711359_072022-F.webp"
    },
    {
        "name": "Power Bank Super Cargador",
        "price": "79,000",
        "description": "Power bank con convertidor USB de carga rápida. Incluye 2 puertos USB 3.0 y 1 puerto tipo C. Capacidad de 6700 mAh. Pantalla indicadora y carga inalámbrica rápida. Garantía: 10 días por pedido incompleto o roto, 30 días por mal funcionamiento.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/850687/1715290627CARGADOR1.JPG"
    },
    {
                name: 'Adidas Fresh Negro Naranja Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284335/17018949181701894918WhatsApp%20Image%202023-06-12%20at%206.09.43%20PM.jpeg'
            },
            {
                name: 'Adidas 2k Blanco Azul Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284302/17018822161701882216L6cf4BmoN0nQSiY96hojYNJVjrFPsWYe6Lh4Wzzt.jpg'
            }
        ];

        const productContainer = document.getElementById('product-list');

        function renderProducts(products) {
            productContainer.innerHTML = '';
            products.forEach((product, index) => {
                const productElement = document.createElement('div');
                productElement.className = 'product';
                productElement.innerHTML = `
                    <img src="${product.image}" alt="${product.name}">
                    <h2 contenteditable="true" data-index="${index}" data-attr="name">${product.name}</h2>
                    <p class="price" contenteditable="true" data-index="${index}" data-attr="price">${product.price}</p>
                    <p contenteditable="true" data-index="${index}" data-attr="description">${product.description}</p>
                    <button onclick="editProduct(${index})">Editar</button>
                    <button onclick="buyProduct('${product.name}')">Comprar</button>
                `;
                productContainer.appendChild(productElement);
            });
        }

        document.getElementById('search').addEventListener('input', (e) => {
            const query = e.target.value.toLowerCase();
            const filteredProducts = products.filter(product => 
                product.name.toLowerCase().includes(query)
            );
            renderProducts(filteredProducts);
        });

        renderProducts(products);

        function editProduct(index) {
            const password = prompt('Ingrese la contraseña para editar:');
            if (password === '12345') {
                const newName = document.querySelector(`[data-attr="name"][data-index="${index}"]`).innerText;
                const newPrice = document.querySelector(`[data-attr="price"][data-index="${index}"]`).innerText;
                const newDescription = document.querySelector(`[data-attr="description"][data-index="${index}"]`).innerText;

                products[index].name = newName;
                products[index].price = newPrice;
                products[index].description = newDescription;

                renderProducts(products);
            } else {
                alert('Contraseña incorrecta. No se pueden realizar cambios.');
            }
        }

        function buyProduct(productName) {
            window.location.href = `https://api.whatsapp.com/send?phone=+3206572598&text=*Hola%20quiero%20que%20me%20env%C3%ADes%20este%20producto*%20${productName}%20*aqu%C3%AD%20te%20env%C3%ADo%20mi%20nombre%20y%20direcci%C3%B3n%20completa*`;
        }
    </script>
</body>
</html>


