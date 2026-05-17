export default function TroguiStore() {
  const whatsappLink = 'https://wa.link/lhneng';

  const products = [
    {
      id: 'TR001',
      name: 'Quita Callos Profesional',
      price: 49000,
      oldPrice: 89000,
      sold: 320,
      rating: 5,
      stock: 8,
      delivery: '20 de mayo',
      image: 'https://images.unsplash.com/photo-1542291026-7eec264c27ff?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 'TR002',
      name: 'Mini Selladora Portátil',
      price: 59000,
      oldPrice: 99000,
      sold: 120,
      rating: 4,
      stock: 12,
      delivery: '21 de mayo',
      image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 'TR003',
      name: 'Cepillo Removedor de Pelos',
      price: 54000,
      oldPrice: 95000,
      sold: 80,
      rating: 5,
      stock: 6,
      delivery: '22 de mayo',
      image: 'https://images.unsplash.com/photo-1517849845537-4d257902454a?q=80&w=1200&auto=format&fit=crop'
    }
  ];

  for (let i = 4; i <= 45; i++) {
    products.push({
      id: `TR${String(i).padStart(3, '0')}`,
      name: `Producto Viral Colombia ${i}`,
      price: 45000 + i * 2000,
      oldPrice: 90000 + i * 3000,
      sold: 50 + i * 5,
      rating: i % 2 === 0 ? 5 : 4,
      stock: 5 + (i % 10),
      delivery: '21 de mayo',
      image: 'https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200&auto=format&fit=crop'
    });
  }

  const reviews = [
    {
      name: 'Juan Camilo - Medellín',
      stars: 5,
      text: 'Muy bueno el producto, llegó rápido y sí funciona.'
    },
    {
      name: 'Luisa Fernanda - Cali',
      stars: 5,
      text: 'Me encantó 😍 volveré a comprar.'
    },
    {
      name: 'Andrés Felipe - Bogotá',
      stars: 4,
      text: 'Todo bien empacado y llegó en pocos días.'
    }
  ];

  return (
    <div className="min-h-screen bg-gray-100">
      <header className="bg-white shadow sticky top-0 z-50">
        <div className="max-w-7xl mx-auto flex items-center justify-between p-4 gap-4">
          <div className="flex items-center gap-3">
            <div className="w-14 h-14 rounded-full bg-black text-white flex items-center justify-center font-bold text-2xl">
              T
            </div>
            <div>
              <h1 className="font-extrabold text-3xl">TROGUI</h1>
              <p className="text-sm text-gray-500">
                Tienda Colombiana • Envíos Gratis
              </p>
            </div>
          </div>

          <input
            type="text"
            placeholder="Buscar productos..."
            className="border rounded-full px-5 py-3 w-full max-w-xl"
          />

          <a
            href={whatsappLink}
            target="_blank"
            className="bg-green-500 text-white px-5 py-3 rounded-full font-bold"
          >
            WhatsApp
          </a>
        </div>

        <div className="bg-red-600 text-white text-center py-2 font-bold animate-pulse">
          🚚 ENVÍO GRATIS A TODA COLOMBIA • PAGO CONTRA ENTREGA
        </div>
      </header>

      <section className="max-w-7xl mx-auto p-5 grid md:grid-cols-2 gap-6">
        <div className="bg-black text-white rounded-3xl p-10 flex flex-col justify-center">
          <h2 className="text-5xl font-extrabold mb-5">
            Ofertas VIRAL 🔥
          </h2>

          <p className="text-lg mb-5">
            Productos tendencia en Colombia con envío gratis.
          </p>

          <div className="flex gap-3 flex-wrap">
            <span className="bg-red-500 px-4 py-2 rounded-full animate-bounce">
              Promo termina en 2 horas
            </span>

            <span className="bg-green-500 px-4 py-2 rounded-full">
              Más de 1500 pedidos
            </span>
          </div>
        </div>

        <div className="overflow-hidden rounded-3xl shadow-xl h-[350px]">
          <img
            src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=1600&auto=format&fit=crop"
            className="w-full h-full object-cover"
          />
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5">
        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
          {products.map((product) => (
            <div
              key={product.id}
              className="bg-white rounded-3xl overflow-hidden shadow-lg hover:-translate-y-1 duration-300"
            >
              <div className="relative">
                <img
                  src={product.image}
                  className="w-full h-64 object-cover"
                />

                <div className="absolute top-3 left-3 bg-red-600 text-white px-3 py-1 rounded-full text-xs animate-pulse">
                  Últimas unidades
                </div>

                <div className="absolute bottom-3 left-3 bg-black/80 text-white px-3 py-1 rounded-full text-xs">
                  {product.sold}+ vendidos
                </div>
              </div>

              <div className="p-5">
                <p className="text-xs text-gray-500 mb-1">
                  ID {product.id}
                </p>

                <h3 className="font-bold text-lg min-h-[60px]">
                  {product.name}
                </h3>

                <div className="text-yellow-500 mt-2">
                  {'★'.repeat(product.rating)}
                </div>

                <div className="flex items-center gap-3 mt-4">
                  <span className="text-3xl font-extrabold text-red-600">
                    ${product.price.toLocaleString('es-CO')}
                  </span>

                  <span className="line-through text-gray-400">
                    ${product.oldPrice.toLocaleString('es-CO')}
                  </span>
                </div>

                <p className="text-green-600 text-sm mt-2 font-semibold">
                  🚚 Llega aproximadamente el {product.delivery}
                </p>

                <p className="text-red-500 text-sm mt-1">
                  ⚠️ Solo quedan {product.stock} unidades
                </p>

                <button className="w-full bg-black text-white py-3 rounded-2xl mt-5 font-bold hover:bg-gray-800">
                  Ver Producto
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5 mt-10">
        <div className="bg-white rounded-3xl shadow-xl p-8">
          <h2 className="text-4xl font-extrabold text-center mb-8">
            Finalizar Pedido
          </h2>

          <div className="grid md:grid-cols-2 gap-5">
            <input
              type="text"
              placeholder="Digita tu nombre"
              className="border rounded-2xl p-4"
            />

            <input
              type="text"
              placeholder="Digita tu apellido"
              className="border rounded-2xl p-4"
            />

            <input
              type="text"
              placeholder="Ciudad o municipio"
              className="border rounded-2xl p-4"
            />

            <input
              type="text"
              placeholder="Número de teléfono"
              className="border rounded-2xl p-4"
            />

            <input
              type="text"
              placeholder="Dirección exacta"
              className="border rounded-2xl p-4 md:col-span-2"
            />

            <textarea
              placeholder="Nota adicional para el pedido"
              className="border rounded-2xl p-4 md:col-span-2 min-h-[120px]"
            ></textarea>
          </div>

          <button className="w-full bg-green-500 text-white py-4 rounded-2xl mt-6 text-xl font-extrabold hover:bg-green-600">
            Confirmar Pedido
          </button>
        </div>
      </section>

      <section className="max-w-7xl mx-auto p-5 mt-10">
        <h2 className="text-4xl font-extrabold text-center mb-8">
          Opiniones de Clientes
        </h2>

        <div className="grid md:grid-cols-3 gap-6">
          {reviews.map((review, index) => (
            <div key={index} className="bg-white rounded-3xl shadow-lg p-6">
              <div className="flex items-center gap-4 mb-4">
                <div className="w-14 h-14 rounded-full bg-black text-white flex items-center justify-center font-bold text-xl">
                  {review.name.charAt(0)}
                </div>

                <div>
                  <h3 className="font-bold">{review.name}</h3>
                  <p className="text-yellow-500">
                    {'★'.repeat(review.stars)}
                  </p>
                </div>
              </div>

              <p className="text-gray-700">
                “{review.text}”
              </p>
            </div>
          ))}
        </div>
      </section>

      <footer className="bg-black text-white mt-16 p-10">
        <div className="max-w-7xl mx-auto grid md:grid-cols-3 gap-8">
          <div>
            <h2 className="text-3xl font-extrabold mb-3">TROGUI</h2>
            <p className="text-gray-300">
              Tienda colombiana con productos tendencia y envíos gratis.
            </p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-3">Contacto</h3>
            <p>📞 3206572598</p>
            <p>🚚 Interrapidísimo • Envía • Coordinadora</p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-3">Redes Sociales</h3>

            <div className="flex gap-4 text-3xl">
              <a
                href="https://www.instagram.com/store_trog?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr"
                target="_blank"
              >
                📸
              </a>

              <a
                href="https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-96QXU6BiNk2"
                target="_blank"
              >
                🎵
              </a>

              <a href={whatsappLink} target="_blank">
                💬
              </a>
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
  );
}
