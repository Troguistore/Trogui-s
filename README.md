export default function TroguiStore() {
  const products = [
    { id: 'TR001', name: 'Quita Callos Profesional', price: 49000, oldPrice: 89000, sold: 320, rating: 5, delivery: '20 de mayo', image: 'https://images.unsplash.com/photo-1542291026-7eec264c27ff?q=80&w=1200&auto=format&fit=crop', stock: 9 },
    { id: 'TR002', name: 'Mini Selladora Portátil', price: 59000, oldPrice: 99000, sold: 120, rating: 4, delivery: '21 de mayo', image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop', stock: 13 },
    { id: 'TR003', name: 'Cepillo Removedor de Pelos', price: 54000, oldPrice: 95000, sold: 85, rating: 5, delivery: '22 de mayo', image: 'https://images.unsplash.com/photo-1517849845537-4d257902454a?q=80&w=1200&auto=format&fit=crop', stock: 7 },
    { id: 'TR004', name: 'Organizador Multifuncional', price: 69000, oldPrice: 119000, sold: 205, rating: 5, delivery: '20 de mayo', image: 'https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=1200&auto=format&fit=crop', stock: 6 },
    { id: 'TR005', name: 'Mini Licuadora USB', price: 79000, oldPrice: 139000, sold: 178, rating: 4, delivery: '23 de mayo', image: 'https://images.unsplash.com/photo-1570222094114-d054a817e56b?q=80&w=1200&auto=format&fit=crop', stock: 15 },
    { id: 'TR006', name: 'Masajeador Cervical', price: 85000, oldPrice: 145000, sold: 410, rating: 5, delivery: '21 de mayo', image: 'https://images.unsplash.com/photo-1515377905703-c4788e51af15?q=80&w=1200&auto=format&fit=crop', stock: 5 },
    { id: 'TR007', name: 'Cámara Wifi Inteligente', price: 99000, oldPrice: 169000, sold: 260, rating: 5, delivery: '20 de mayo', image: 'https://images.unsplash.com/photo-1516035069371-29a1b244cc32?q=80&w=1200&auto=format&fit=crop', stock: 8 },
    { id: 'TR008', name: 'Lámpara LED Decorativa', price: 45000, oldPrice: 79000, sold: 95, rating: 4, delivery: '24 de mayo', image: 'https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=1200&auto=format&fit=crop', stock: 18 },
    { id: 'TR009', name: 'Corrector de Postura', price: 65000, oldPrice: 110000, sold: 340, rating: 5, delivery: '20 de mayo', image: 'https://images.unsplash.com/photo-1518611012118-696072aa579a?q=80&w=1200&auto=format&fit=crop', stock: 11 },
    { id: 'TR010', name: 'Dispensador Automático', price: 72000, oldPrice: 129000, sold: 98, rating: 4, delivery: '22 de mayo', image: 'https://images.unsplash.com/photo-1586201375761-83865001e31c?q=80&w=1200&auto=format&fit=crop', stock: 9 },
    ...Array.from({ length: 35 }, (_, i) => ({
      id: `TR${String(i + 11).padStart(3, '0')}`,
      name: `Producto Viral Colombia ${i + 11}`,
      price: 45000 + i * 2500,
      oldPrice: 95000 + i * 3500,
      sold: 80 + i * 10,
      rating: i % 2 === 0 ? 5 : 4,
      delivery: '21 de mayo',
      image: 'https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200&auto=format&fit=crop',
      stock: 5 + (i % 12)
    }))
  ];

  const reviews = [
    {
      name: 'Juan Camilo - Medellín',
      text: 'Me llegó rápido y sí funciona como en el video, recomendado.',
      stars: 5
    },
    {
      name: 'Luisa Fernanda - Cali',
      text: 'Pensé que no servía pero me sorprendió mucho, muy buena calidad.',
      stars: 5
    },
    {
      name: 'Andrés Felipe - Bogotá',
      text: 'Llegó en 4 días, todo bien empacado.',
      stars: 4
    },
    {
      name: 'Maira - Bucaramanga',
      text: 'La verdad quede feliz con la compra 😍',
      stars: 5
    }
  ];

  const whatsappLink = 'https://wa.link/lhneng';

  return (
    <div className="min-h-screen bg-gray-100 text-gray-900">
      <header className="sticky top-0 z-50 bg-white shadow-md">
        <div className="max-w-7xl mx-auto flex items-center justify-between px-4 py-3">
          <div className="flex items-center gap-3">
            <div className="w-14 h-14 rounded-full bg-black text-white flex items-center justify-center text-2xl font-bold">
              T
            </div>
            <div>
              <h1 className="text-2xl font-extrabold">TROGUI</h1>
              <p className="text-sm text-gray-600">Tienda Colombiana • Envíos Gratis</p>
            </div>
          </div>

          <div className="hidden md:flex items-center gap-3 w-1/2">
            <input
              type="text"
              placeholder="Buscar productos..."
              className="w-full border rounded-full px-5 py-3 outline-none"
            />
          </div>

          <div className="flex items-center gap-3">
            <a href={whatsappLink} target="_blank" className="bg-green-500 text-white px-4 py-2 rounded-full font-semibold">
              WhatsApp
            </a>
            <button className="bg-black text-white px-4 py-2 rounded-full">🛒</button>
          </div>
        </div>

        <div className="bg-red-600 text-white text-center py-2 text-sm font-semibold animate-pulse">
          🚚 Envío Gratis a Toda Colombia • Pago Contra Entrega • Últimas Unidades Disponibles
        </div>
      </header>

      <section className="relative overflow-hidden">
        <div className="grid md:grid-cols-2 gap-5 p-5 max-w-7xl mx-auto">
          <div className="bg-gradient-to-r from-black to-gray-700 rounded-3xl text-white p-10 flex flex-col justify-center">
            <h2 className="text-5xl font-extrabold leading-tight mb-4">
              Ofertas VIRAL 🔥
            </h2>
            <p className="text-lg mb-5">
              Productos tendencia en Colombia con envío gratis y pago contra entrega.
            </p>
            <div className="flex gap-3 flex-wrap">
              <span className="bg-red-500 px-4 py-2 rounded-full animate-bounce">Promo termina en 2h</span>
              <span className="bg-green-500 px-4 py-2 rounded-full">Más de 1.500 pedidos</span>
            </div>
          </div>

          <div className="rounded-3xl overflow-hidden shadow-xl h-[350px]">
            <img
              src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=1600&auto=format&fit=crop"
              className="w-full h-full object-cover hover:scale-105 duration-500"
            />
          </div>
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5">
        <div className="grid grid-cols-2 md:grid-cols-4 gap-4 mb-10">
          <div className="bg-white rounded-2xl p-5 shadow text-center">
            <h3 className="font-bold text-xl">🚚 Envíos Gratis</h3>
            <p className="text-sm text-gray-600 mt-2">A toda Colombia</p>
          </div>

          <div className="bg-white rounded-2xl p-5 shadow text-center">
            <h3 className="font-bold text-xl">💵 Contra Entrega</h3>
            <p className="text-sm text-gray-600 mt-2">Paga al recibir</p>
          </div>

          <div className="bg-white rounded-2xl p-5 shadow text-center">
            <h3 className="font-bold text-xl">📦 Transportadoras</h3>
            <p className="text-sm text-gray-600 mt-2">Interrapidísimo, Envía y más</p>
          </div>

          <div className="bg-white rounded-2xl p-5 shadow text-center">
            <h3 className="font-bold text-xl">⭐ Garantía</h3>
            <p className="text-sm text-gray-600 mt-2">Compra segura</p>
          </div>
        </div>

        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
          {products.map((product, index) => (
            <div key={index} className="bg-white rounded-3xl shadow-lg overflow-hidden hover:-translate-y-1 duration-300">
              <div className="relative">
                <img src={product.image} className="w-full h-64 object-cover" />
                <div className="absolute top-3 left-3 bg-red-600 text-white text-xs px-3 py-1 rounded-full animate-pulse">
                  Promo termina pronto
                </div>
                <div className="absolute bottom-3 left-3 bg-black/80 text-white text-xs px-3 py-1 rounded-full">
                  {product.sold}+ vendidos
                </div>
              </div>

              <div className="p-5">
                <p className="text-xs text-gray-500 mb-1">ID {product.id}</p>
                <h3 className="font-bold text-lg min-h-[60px]">{product.name}</h3>

                <div className="flex items-center gap-1 mt-2 text-yellow-500">
                  {'★'.repeat(product.rating)}
                  <span className="text-gray-500 text-sm ml-2">({product.rating}.0)</span>
                </div>

                <div className="mt-4 flex items-center gap-3">
                  <span className="text-3xl font-extrabold text-red-600">
                    ${product.price.toLocaleString('es-CO')}
                  </span>
                  <span className="line-through text-gray-400">
                    ${product.oldPrice.toLocaleString('es-CO')}
                  </span>
                </div>

                <p className="text-sm text-green-600 mt-2 font-semibold">
                  🚚 Llega aproximadamente el {product.delivery}
                </p>

                <p className="text-sm mt-1 text-red-500">
                  ⚠️ Solo quedan {product.stock} unidades
                </p>

                <button className="w-full mt-5 bg-black text-white py-3 rounded-2xl font-bold hover:bg-gray-800 duration-300">
                  Ver Producto
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5 mt-10">
        <div className="bg-white rounded-3xl shadow-xl p-8">
          <h2 className="text-4xl font-extrabold mb-8 text-center">
            Finalizar Pedido
          </h2>

          <div className="grid md:grid-cols-2 gap-5">
            <input type="text" placeholder="Digita tu nombre" className="border rounded-2xl p-4" />
            <input type="text" placeholder="Digita tu apellido" className="border rounded-2xl p-4" />
            <input type="text" placeholder="Ciudad o municipio" className="border rounded-2xl p-4" />
            <input type="text" placeholder="Número de teléfono" className="border rounded-2xl p-4" />
            <input type="text" placeholder="Dirección exacta de entrega" className="border rounded-2xl p-4 md:col-span-2" />
            <textarea placeholder="Nota adicional para el pedido" className="border rounded-2xl p-4 md:col-span-2 min-h-[120px]"></textarea>
          </div>

          <button className="w-full mt-6 bg-green-500 text-white py-4 rounded-2xl text-xl font-extrabold hover:bg-green-600 duration-300">
            Confirmar Pedido por WhatsApp
          </button>
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5 mt-10">
        <h2 className="text-4xl font-extrabold mb-8 text-center">
          Opiniones de Clientes
        </h2>

        <div className="grid md:grid-cols-2 gap-6">
          {reviews.map((review, index) => (
            <div key={index} className="bg-white rounded-3xl shadow-lg p-6">
              <div className="flex items-center gap-4 mb-4">
                <div className="w-14 h-14 rounded-full bg-black text-white flex items-center justify-center font-bold">
                  {review.name.charAt(0)}
                </div>
                <div>
                  <h3 className="font-bold">{review.name}</h3>
                  <p className="text-yellow-500">{'★'.repeat(review.stars)}</p>
                </div>
              </div>

              <p className="text-gray-700">“{review.text}”</p>
            </div>
          ))}
        </div>
      </section>

      <footer className="bg-black text-white mt-16 p-10">
        <div className="max-w-7xl mx-auto grid md:grid-cols-3 gap-8">
          <div>
            <h2 className="text-3xl font-extrabold mb-3">TROGUI</h2>
            <p className="text-gray-300">
              Tienda colombiana con productos tendencia y envíos gratis a todo el país.
            </p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-3">Contacto</h3>
            <p>📞 3206572598</p>
            <p>🚚 Envía • Interrapidísimo • Coordinadora</p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-3">Redes Sociales</h3>
            <div className="flex gap-4 text-2xl">
              <a href="https://www.instagram.com/store_trog?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr" target="_blank">📸</a>
              <a href="https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-96QXU6BiNk2" target="_blank">🎵</a>
              <a href={whatsappLink} target="_blank">💬</a>
            </div>
          </div>
        </div>
      </footer>

      <a
        href={whatsappLink}
        target="_blank"
        className="fixed bottom-5 right-5 bg-green-500 text-white w-16 h-16 rounded-full flex items-center justify-center text-3xl shadow-2xl animate-bounce"
      >
        💬
      </a>

      <div className="fixed bottom-5 left-5 bg-white shadow-xl rounded-2xl px-4 py-3 text-sm animate-pulse">
        🔥 Juan Camilo hizo un pedido para Medellín
      </div>

      <button className="fixed bottom-3 left-1/2 text-xs opacity-30">
        R
      </button>

      <button className="fixed bottom-3 left-[55%] text-xs opacity-30">
        C
      </button>

      <button className="fixed bottom-3 left-[60%] text-xs opacity-30">
        E
      </button>
    </div>
  )
}
