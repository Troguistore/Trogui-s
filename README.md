<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI Store - Envíos a toda Colombia</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --orange: #FF5500;
  --orange-light: #FF7733;
  --dark: #1a1a2e;
  --text: #222;
  --light-bg: #f7f7f7;
  --white: #fff;
  --green: #00b050;
  --red: #e00;
  --gray: #888;
  --border: #e0e0e0;
  --card-shadow: 0 2px 16px rgba(0,0,0,0.09);
}
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: 'Nunito', sans-serif; background: var(--light-bg); color: var(--text); font-size: 15px; }

/* TOP BAR */
.top-bar { background: var(--dark); color: #fff; text-align: center; padding: 7px; font-size: 13px; font-weight: 600; letter-spacing: .3px; }
.top-bar span { color: var(--orange); }

/* HEADER */
header { background: #fff; border-bottom: 2px solid var(--orange); position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,.08); }
.header-inner { max-width: 1200px; margin: 0 auto; display: flex; align-items: center; gap: 18px; padding: 10px 16px; flex-wrap: wrap; }
.logo-wrap { display: flex; align-items: center; gap: 8px; text-decoration: none; }
.logo-box { background: var(--orange); padding: 6px 14px; border-radius: 8px; }
.logo-box span { font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 22px; color: #1a1a2e; letter-spacing: -1px; }
.search-wrap { flex: 1; min-width: 200px; display: flex; align-items: center; background: var(--light-bg); border: 2px solid var(--border); border-radius: 30px; overflow: hidden; padding: 0 6px 0 16px; }
.search-wrap input { flex: 1; border: none; background: transparent; font-size: 14px; padding: 9px 0; outline: none; font-family: 'Nunito', sans-serif; }
.search-wrap button { background: var(--orange); border: none; color: #fff; padding: 8px 14px; border-radius: 24px; cursor: pointer; font-size: 16px; }
.header-icons { display: flex; gap: 16px; align-items: center; }
.wa-header { display: flex; align-items: center; gap: 7px; text-decoration: none; color: var(--dark); font-weight: 700; font-size: 13px; }
.wa-header .wa-circle { width: 38px; height: 38px; background: #25D366; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: #fff; font-size: 20px; }
.cart-btn { position: relative; background: var(--orange); color: #fff; border: none; border-radius: 50%; width: 42px; height: 42px; font-size: 20px; cursor: pointer; display: flex; align-items: center; justify-content: center; }
.cart-count { position: absolute; top: -4px; right: -4px; background: var(--dark); color: #fff; font-size: 10px; width: 18px; height: 18px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: 700; }
.social-icons { display: flex; gap: 8px; }
.social-icons a { width: 34px; height: 34px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: #fff; font-size: 15px; text-decoration: none; }
.ig-icon { background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%); }
.tt-icon { background: #010101; }

/* NAV */
nav { background: var(--orange); }
.nav-inner { max-width: 1200px; margin: 0 auto; display: flex; gap: 0; padding: 0 16px; overflow-x: auto; }
nav a { color: #fff; text-decoration: none; font-weight: 700; font-size: 14px; padding: 12px 20px; display: block; white-space: nowrap; transition: background .2s; }
nav a:hover { background: rgba(0,0,0,.15); }

/* HERO SLIDER */
.hero-slider { max-width: 1200px; margin: 20px auto 0; border-radius: 14px; overflow: hidden; position: relative; height: 220px; box-shadow: var(--card-shadow); }
.slide { position: absolute; width: 100%; height: 100%; display: flex; align-items: center; padding: 30px 40px; opacity: 0; transition: opacity .8s; }
.slide.active { opacity: 1; }
.slide:nth-child(1) { background: linear-gradient(135deg, #1a1a2e 60%, #FF5500 100%); }
.slide:nth-child(2) { background: linear-gradient(135deg, #0f3460 60%, #e94560 100%); }
.slide:nth-child(3) { background: linear-gradient(135deg, #16213e 60%, #00b050 100%); }
.slide-content h2 { font-family: 'Poppins', sans-serif; font-size: 28px; font-weight: 900; color: #fff; line-height: 1.1; }
.slide-content h2 span { color: var(--orange); }
.slide-content p { color: rgba(255,255,255,.8); margin: 8px 0 16px; font-size: 14px; }
.slide-btn { background: var(--orange); color: #fff; border: none; padding: 10px 24px; border-radius: 25px; font-weight: 800; font-size: 14px; cursor: pointer; font-family: 'Nunito', sans-serif; }
.slide-badges { margin-top: 12px; display: flex; gap: 8px; flex-wrap: wrap; }
.badge { background: rgba(255,255,255,.15); color: #fff; border: 1px solid rgba(255,255,255,.3); border-radius: 20px; padding: 4px 12px; font-size: 12px; font-weight: 700; }
.badge.green { background: var(--green); border-color: var(--green); }
.slide-dots { position: absolute; bottom: 12px; left: 50%; transform: translateX(-50%); display: flex; gap: 6px; }
.dot { width: 8px; height: 8px; border-radius: 50%; background: rgba(255,255,255,.4); cursor: pointer; transition: background .2s; }
.dot.active { background: #fff; width: 20px; border-radius: 4px; }

/* TRUST BAR */
.trust-bar { max-width: 1200px; margin: 16px auto; display: flex; gap: 0; background: #fff; border-radius: 12px; overflow: hidden; box-shadow: var(--card-shadow); }
.trust-item { flex: 1; display: flex; align-items: center; gap: 10px; padding: 14px 18px; border-right: 1px solid var(--border); }
.trust-item:last-child { border-right: none; }
.trust-icon { font-size: 26px; }
.trust-text strong { display: block; font-weight: 800; font-size: 13px; color: var(--dark); }
.trust-text span { font-size: 11px; color: var(--gray); }

/* SECTION TITLE */
.section-title { max-width: 1200px; margin: 24px auto 14px; padding: 0 16px; display: flex; align-items: center; gap: 12px; }
.section-title h3 { font-family: 'Poppins', sans-serif; font-size: 20px; font-weight: 800; color: var(--dark); }
.section-title .line { flex: 1; height: 2px; background: var(--border); }
.section-title .see-all { color: var(--orange); font-weight: 700; font-size: 13px; cursor: pointer; text-decoration: none; }

/* PRODUCTS GRID */
.products-grid { max-width: 1200px; margin: 0 auto 24px; padding: 0 16px; display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 16px; }
.product-card { background: #fff; border-radius: 14px; overflow: hidden; box-shadow: var(--card-shadow); cursor: pointer; transition: transform .2s, box-shadow .2s; position: relative; }
.product-card:hover { transform: translateY(-4px); box-shadow: 0 8px 30px rgba(0,0,0,.13); }
.product-img-wrap { position: relative; height: 180px; overflow: hidden; background: #f0f0f0; display: flex; align-items: center; justify-content: center; }
.product-img-wrap img { width: 100%; height: 100%; object-fit: cover; }
.product-img-placeholder { font-size: 60px; }
.badge-oferta { position: absolute; top: 8px; left: 8px; background: var(--orange); color: #fff; font-size: 11px; font-weight: 800; padding: 3px 8px; border-radius: 6px; }
.badge-pct { position: absolute; top: 8px; right: 8px; background: var(--green); color: #fff; font-size: 11px; font-weight: 800; padding: 3px 8px; border-radius: 6px; }
.badge-units { position: absolute; bottom: 8px; left: 8px; background: #fff; color: var(--red); font-size: 10px; font-weight: 800; padding: 3px 8px; border-radius: 6px; border: 1px solid var(--red); }
.product-info { padding: 12px; }
.product-name { font-weight: 700; font-size: 13px; color: var(--dark); line-height: 1.3; margin-bottom: 6px; min-height: 34px; }
.stars { color: #f5a623; font-size: 13px; margin-bottom: 4px; }
.stars span { color: var(--gray); font-size: 11px; }
.price-wrap { display: flex; align-items: center; gap: 8px; margin-bottom: 8px; flex-wrap: wrap; }
.price-old { color: var(--gray); font-size: 12px; text-decoration: line-through; }
.price-new { color: var(--orange); font-size: 18px; font-weight: 900; font-family: 'Poppins', sans-serif; }
.countdown-box { background: #fff3f0; border: 1px solid #ffccbb; border-radius: 8px; padding: 5px 10px; margin-bottom: 8px; display: flex; align-items: center; gap: 6px; font-size: 12px; font-weight: 700; color: var(--red); }
.countdown-box .clock { font-size: 14px; animation: shake .5s infinite alternate; }
@keyframes shake { 0% { transform: rotate(-8deg); } 100% { transform: rotate(8deg); } }
.btn-add { width: 100%; background: var(--orange); color: #fff; border: none; padding: 10px; border-radius: 8px; font-weight: 800; font-size: 14px; cursor: pointer; font-family: 'Nunito', sans-serif; transition: background .2s; }
.btn-add:hover { background: var(--orange-light); }
.free-ship-tag { color: var(--green); font-size: 11px; font-weight: 800; display: flex; align-items: center; gap: 3px; margin-bottom: 4px; }
.cod-tag { color: #0057d9; font-size: 11px; font-weight: 700; display: flex; align-items: center; gap: 3px; }

/* REVIEWS */
.review-card { background: #fff; border-radius: 12px; padding: 12px; margin-bottom: 8px; box-shadow: 0 1px 6px rgba(0,0,0,.06); }
.reviewer { display: flex; align-items: center; gap: 8px; margin-bottom: 6px; }
.reviewer-avatar { width: 34px; height: 34px; border-radius: 50%; background: var(--orange); color: #fff; display: flex; align-items: center; justify-content: center; font-weight: 800; font-size: 14px; }
.reviewer-name { font-weight: 700; font-size: 13px; }
.reviewer-city { font-size: 11px; color: var(--gray); }
.review-text { font-size: 13px; color: #444; line-height: 1.5; }

/* PRODUCT MODAL */
.modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.5); z-index: 2000; overflow-y: auto; }
.modal-overlay.open { display: flex; align-items: flex-start; justify-content: center; padding: 20px; }
.modal-box { background: #fff; border-radius: 18px; max-width: 700px; width: 100%; margin: auto; overflow: hidden; }
.modal-header { background: var(--orange); padding: 16px 20px; display: flex; justify-content: space-between; align-items: center; }
.modal-header h3 { color: #fff; font-size: 17px; font-weight: 800; }
.modal-close { background: none; border: none; color: #fff; font-size: 24px; cursor: pointer; }
.modal-body { padding: 20px; }
.modal-img { width: 100%; height: 200px; object-fit: cover; border-radius: 10px; margin-bottom: 14px; background: #f0f0f0; display: flex; align-items: center; justify-content: center; font-size: 70px; }
.modal-prices { display: flex; gap: 14px; align-items: center; margin: 10px 0; }
.modal-price-old { font-size: 18px; color: var(--gray); text-decoration: line-through; }
.modal-price-new { font-size: 28px; font-weight: 900; color: var(--orange); font-family: 'Poppins', sans-serif; }
.modal-saving { background: #e8fff0; color: var(--green); font-weight: 700; padding: 4px 10px; border-radius: 6px; font-size: 13px; }
.modal-desc { font-size: 14px; color: #444; line-height: 1.6; margin: 12px 0; }
.modal-badges { display: flex; gap: 8px; flex-wrap: wrap; margin: 10px 0; }
.modal-badge { padding: 5px 12px; border-radius: 20px; font-size: 12px; font-weight: 700; }
.mb-green { background: #e8fff0; color: var(--green); }
.mb-blue { background: #e8f0ff; color: #0057d9; }
.mb-orange { background: #fff3ed; color: var(--orange); }
.delivery-calc { background: var(--light-bg); border-radius: 10px; padding: 14px; margin: 14px 0; }
.delivery-calc h4 { font-size: 14px; font-weight: 800; margin-bottom: 8px; color: var(--dark); }
.delivery-dates { display: flex; align-items: center; gap: 8px; font-size: 13px; }
.delivery-dates .from { color: var(--gray); }
.delivery-dates .to { font-weight: 800; color: var(--dark); }
.btn-buy { width: 100%; background: var(--orange); color: #fff; border: none; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 900; cursor: pointer; font-family: 'Nunito', sans-serif; margin-top: 10px; }

/* ORDER FORM */
.order-form-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.6); z-index: 3000; overflow-y: auto; }
.order-form-overlay.open { display: flex; align-items: flex-start; justify-content: center; padding: 20px; }
.order-form-box { background: #fff; border-radius: 18px; max-width: 520px; width: 100%; margin: auto; overflow: hidden; }
.form-header { background: var(--orange); padding: 16px 20px; display: flex; justify-content: space-between; align-items: center; }
.form-header h3 { color: #fff; font-size: 17px; font-weight: 800; }
.form-header button { background: none; border: none; color: #fff; font-size: 24px; cursor: pointer; }
.form-body { padding: 20px; }
.form-product-summary { background: var(--light-bg); border-radius: 10px; padding: 14px; margin-bottom: 16px; display: flex; justify-content: space-between; align-items: center; }
.form-product-name { font-weight: 700; font-size: 14px; }
.form-product-id { font-size: 11px; color: var(--gray); }
.form-prices { text-align: right; }
.form-price-old { text-decoration: line-through; color: var(--gray); font-size: 13px; }
.form-price-new { color: var(--orange); font-size: 20px; font-weight: 900; font-family: 'Poppins', sans-serif; }
.form-group { margin-bottom: 14px; }
.form-group label { display: block; font-weight: 700; font-size: 13px; margin-bottom: 5px; color: var(--dark); }
.form-group label span { color: var(--red); }
.form-group input, .form-group textarea, .form-group select { width: 100%; border: 2px solid var(--border); border-radius: 8px; padding: 10px 14px; font-size: 14px; font-family: 'Nunito', sans-serif; outline: none; transition: border-color .2s; }
.form-group input:focus, .form-group textarea:focus { border-color: var(--orange); }
.form-group .hint { font-size: 11px; color: var(--gray); margin-top: 4px; }
.form-submit { width: 100%; background: var(--green); color: #fff; border: none; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 900; cursor: pointer; font-family: 'Nunito', sans-serif; display: flex; align-items: center; justify-content: center; gap: 8px; }
.form-whatsapp-note { background: #e8fff0; border-radius: 8px; padding: 10px 14px; margin-top: 12px; font-size: 12px; color: #006620; font-weight: 600; display: flex; align-items: center; gap: 6px; }

/* CART */
.cart-overlay { display: none; position: fixed; right: 0; top: 0; height: 100%; width: 360px; background: #fff; z-index: 4000; box-shadow: -4px 0 30px rgba(0,0,0,.15); flex-direction: column; }
.cart-overlay.open { display: flex; }
.cart-header { background: var(--orange); padding: 16px 20px; display: flex; justify-content: space-between; align-items: center; }
.cart-header h3 { color: #fff; font-weight: 800; font-size: 17px; }
.cart-header button { background: none; border: none; color: #fff; font-size: 24px; cursor: pointer; }
.cart-body { flex: 1; overflow-y: auto; padding: 16px; }
.cart-empty { text-align: center; padding: 40px 20px; color: var(--gray); font-size: 15px; }
.cart-item { display: flex; gap: 12px; padding: 12px 0; border-bottom: 1px solid var(--border); }
.cart-item-img { width: 60px; height: 60px; background: var(--light-bg); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 28px; flex-shrink: 0; }
.cart-item-info { flex: 1; }
.cart-item-name { font-weight: 700; font-size: 13px; }
.cart-item-price { color: var(--orange); font-weight: 800; font-size: 15px; }
.cart-item-remove { color: var(--red); cursor: pointer; font-size: 18px; background: none; border: none; }
.cart-footer { padding: 16px; border-top: 2px solid var(--border); }
.cart-total { display: flex; justify-content: space-between; font-size: 17px; font-weight: 900; margin-bottom: 14px; }
.cart-checkout { width: 100%; background: var(--orange); color: #fff; border: none; padding: 14px; border-radius: 10px; font-size: 16px; font-weight: 900; cursor: pointer; font-family: 'Nunito', sans-serif; }

/* ADMIN */
.admin-btn { position: fixed; bottom: 16px; right: 16px; display: flex; gap: 6px; z-index: 9000; }
.admin-btn button { width: 32px; height: 32px; border-radius: 50%; border: 2px solid #ccc; background: rgba(255,255,255,.9); color: #888; font-size: 11px; font-weight: 800; cursor: pointer; display: flex; align-items: center; justify-content: center; }
.admin-modal { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.5); z-index: 9500; align-items: center; justify-content: center; }
.admin-modal.open { display: flex; }
.admin-box { background: #fff; border-radius: 14px; padding: 28px; width: 340px; }
.admin-box h3 { font-weight: 800; margin-bottom: 14px; }
.admin-box input { width: 100%; border: 2px solid var(--border); border-radius: 8px; padding: 10px 14px; font-size: 16px; margin-bottom: 12px; outline: none; }
.admin-box button { width: 100%; background: var(--orange); color: #fff; border: none; padding: 12px; border-radius: 8px; font-size: 15px; font-weight: 800; cursor: pointer; }
.admin-panel { display: none; position: fixed; inset: 0; background: #fff; z-index: 9600; overflow-y: auto; }
.admin-panel.open { display: block; }
.admin-panel-header { background: var(--orange); padding: 16px 20px; display: flex; justify-content: space-between; align-items: center; }
.admin-panel-header h2 { color: #fff; font-weight: 800; }
.admin-panel-header button { background: none; border: none; color: #fff; font-size: 22px; cursor: pointer; }
.admin-panel-body { padding: 20px; max-width: 900px; margin: 0 auto; }
.admin-product-row { background: var(--light-bg); border-radius: 10px; padding: 14px; margin-bottom: 12px; display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
.admin-product-row h4 { grid-column: 1/-1; font-weight: 800; margin-bottom: 4px; }
.admin-product-row input, .admin-product-row textarea { width: 100%; border: 1px solid var(--border); border-radius: 6px; padding: 7px 10px; font-size: 13px; font-family: 'Nunito', sans-serif; }
.admin-save-btn { background: var(--green); color: #fff; border: none; padding: 8px 16px; border-radius: 6px; font-weight: 800; cursor: pointer; margin-top: 6px; grid-column: 1/-1; }
.orders-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
.orders-table th { background: var(--orange); color: #fff; padding: 8px 12px; text-align: left; font-size: 13px; }
.orders-table td { padding: 8px 12px; border-bottom: 1px solid var(--border); font-size: 13px; }

/* WA FLOAT */
.wa-float { position: fixed; bottom: 70px; right: 16px; z-index: 8000; }
.wa-float a { display: flex; align-items: center; justify-content: center; width: 54px; height: 54px; background: #25D366; border-radius: 50%; color: #fff; font-size: 28px; text-decoration: none; box-shadow: 0 4px 16px rgba(37,211,102,.4); animation: pulse 2s infinite; }
@keyframes pulse { 0%,100% { box-shadow: 0 4px 16px rgba(37,211,102,.4); } 50% { box-shadow: 0 4px 30px rgba(37,211,102,.7); } }

/* FOOTER */
footer { background: var(--dark); color: rgba(255,255,255,.8); padding: 40px 20px 20px; margin-top: 30px; }
.footer-inner { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 30px; }
.footer-col h4 { color: #fff; font-weight: 800; margin-bottom: 14px; font-size: 15px; }
.footer-col p, .footer-col a { font-size: 13px; color: rgba(255,255,255,.65); margin-bottom: 7px; display: block; text-decoration: none; }
.footer-col a:hover { color: var(--orange); }
.footer-bottom { max-width: 1200px; margin: 24px auto 0; border-top: 1px solid rgba(255,255,255,.1); padding-top: 16px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }
.footer-bottom span { font-size: 12px; color: rgba(255,255,255,.4); }
.footer-social { display: flex; gap: 10px; }
.footer-social a { width: 34px; height: 34px; border-radius: 50%; background: rgba(255,255,255,.1); display: flex; align-items: center; justify-content: center; color: #fff; font-size: 15px; text-decoration: none; }

/* SEARCH RESULTS */
.search-results-overlay { display: none; position: fixed; top: 70px; left: 50%; transform: translateX(-50%); width: 500px; max-width: 95vw; background: #fff; border-radius: 14px; box-shadow: 0 8px 30px rgba(0,0,0,.15); z-index: 1500; padding: 10px; max-height: 400px; overflow-y: auto; }
.search-results-overlay.open { display: block; }
.search-result-item { display: flex; gap: 10px; padding: 10px; border-radius: 8px; cursor: pointer; align-items: center; }
.search-result-item:hover { background: var(--light-bg); }
.search-result-img { width: 44px; height: 44px; background: #f0f0f0; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 22px; flex-shrink: 0; }
.search-result-name { font-weight: 700; font-size: 13px; }
.search-result-price { color: var(--orange); font-weight: 800; font-size: 14px; }

/* REVIEWS SECTION */
.reviews-section { max-width: 1200px; margin: 0 auto 30px; padding: 0 16px; }
.reviews-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 14px; }

/* RESPONSIVE */
@media(max-width: 600px) {
  .trust-bar { flex-direction: column; }
  .trust-item { border-right: none; border-bottom: 1px solid var(--border); }
  .hero-slider { height: 180px; }
  .slide-content h2 { font-size: 20px; }
  .products-grid { grid-template-columns: repeat(2, 1fr); }
  .cart-overlay { width: 100%; }
}

/* notification */
.notif { position: fixed; bottom: 130px; right: 16px; background: var(--dark); color: #fff; padding: 10px 18px; border-radius: 10px; font-size: 13px; font-weight: 700; z-index: 9000; transform: translateY(20px); opacity: 0; transition: all .3s; }
.notif.show { transform: translateY(0); opacity: 1; }
</style>
</head>
<body>

<!-- TOP BAR -->
<div class="top-bar">🚚 <span>ENVÍO GRATIS</span> a toda Colombia · Pago Contra Entrega · Envíos por Envia, Interrapidísimo, Coordinadora y más</div>

<!-- HEADER -->
<header>
  <div class="header-inner">
    <a class="logo-wrap" href="#">
      <div class="logo-box"><span>TROGÜI</span></div>
    </a>
    <div class="search-wrap">
      <input type="text" id="searchInput" placeholder="🔍 Buscar productos..." oninput="handleSearch(this.value)" onkeydown="if(event.key==='Enter')handleSearch(this.value)">
      <button onclick="handleSearch(document.getElementById('searchInput').value)">🔍</button>
    </div>
    <div class="header-icons">
      <a href="https://wa.link/lhneng" target="_blank" class="wa-header">
        <div class="wa-circle">📲</div>
        <div><strong>WhatsApp</strong><br><span>320 657 2598</span></div>
      </a>
      <div class="social-icons">
        <a href="https://www.instagram.com/store_trog" target="_blank" class="ig-icon">📷</a>
        <a href="https://www.tiktok.com/@trogui_store" target="_blank" class="tt-icon">🎵</a>
      </div>
      <button class="cart-btn" onclick="openCart()">🛒<span class="cart-count" id="cartCount">0</span></button>
    </div>
  </div>
</header>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#">🏠 Tienda</a>
    <a href="#">💄 Belleza</a>
    <a href="#">🏠 Hogar</a>
    <a href="#">👟 Moda</a>
    <a href="#">🧴 Salud</a>
    <a href="#">🍳 Cocina</a>
    <a href="#">🎁 Combos</a>
    <a href="#">⭐ Más Vendidos</a>
  </div>
</nav>

<!-- HERO SLIDER -->
<div class="hero-slider" id="heroSlider">
  <div class="slide active">
    <div class="slide-content">
      <h2>🛒 TROGÜI Store<br><span>¡Llegamos a toda Colombia!</span></h2>
      <p>Los mejores productos al mejor precio</p>
      <div class="slide-badges">
        <span class="badge green">✅ Envío GRATIS</span>
        <span class="badge">💳 Pago Contra Entrega</span>
        <span class="badge">⚡ Entrega 3-7 días</span>
      </div>
    </div>
  </div>
  <div class="slide">
    <div class="slide-content">
      <h2>🔥 ¡Ofertas<br><span>Exclusivas Hoy!</span></h2>
      <p>Hasta 50% de descuento en productos seleccionados</p>
      <div class="slide-badges">
        <span class="badge green">🚚 Interrapidísimo</span>
        <span class="badge">📦 Coordinadora</span>
        <span class="badge">⚡ Envia</span>
      </div>
    </div>
  </div>
  <div class="slide">
    <div class="slide-content">
      <h2>💰 Pago<br><span>Contra Entrega</span></h2>
      <p>Paga cuando recibas tu pedido. ¡100% seguro!</p>
      <div class="slide-badges">
        <span class="badge green">✅ Garantía Total</span>
        <span class="badge">🔒 Compra Segura</span>
      </div>
    </div>
  </div>
  <div class="slide-dots" id="slideDots">
    <div class="dot active" onclick="goSlide(0)"></div>
    <div class="dot" onclick="goSlide(1)"></div>
    <div class="dot" onclick="goSlide(2)"></div>
  </div>
</div>

<!-- TRUST BAR -->
<div class="trust-bar">
  <div class="trust-item"><span class="trust-icon">🚚</span><div class="trust-text"><strong>Envío Gratis</strong><span>A toda Colombia</span></div></div>
  <div class="trust-item"><span class="trust-icon">💳</span><div class="trust-text"><strong>Pago Contra Entrega</strong><span>Paga al recibir</span></div></div>
  <div class="trust-item"><span class="trust-icon">⚡</span><div class="trust-text"><strong>3 a 7 Días Hábiles</strong><span>Envíos rápidos</span></div></div>
  <div class="trust-item"><span class="trust-icon">🔒</span><div class="trust-text"><strong>Compra 100% Segura</strong><span>Garantía respaldada</span></div></div>
</div>

<!-- PRODUCTS -->
<div class="section-title">
  <h3>🔥 Productos en Oferta</h3>
  <div class="line"></div>
  <a class="see-all" href="#">Ver todos →</a>
</div>
<div class="products-grid" id="productsGrid"></div>

<!-- REVIEWS -->
<div class="section-title">
  <h3>⭐ Opiniones de Clientes</h3>
  <div class="line"></div>
</div>
<div class="reviews-section">
  <div class="reviews-grid" id="reviewsGrid"></div>
</div>

<!-- SEARCH RESULTS -->
<div class="search-results-overlay" id="searchResults"></div>

<!-- PRODUCT MODAL -->
<div class="modal-overlay" id="productModal">
  <div class="modal-box">
    <div class="modal-header">
      <h3 id="modalTitle">Producto</h3>
      <button class="modal-close" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-body" id="modalBody"></div>
  </div>
</div>

<!-- ORDER FORM -->
<div class="order-form-overlay" id="orderForm">
  <div class="order-form-box">
    <div class="form-header">
      <h3>📦 Confirmar Pedido</h3>
      <button onclick="closeOrderForm()">✕</button>
    </div>
    <div class="form-body" id="formBody"></div>
  </div>
</div>

<!-- CART -->
<div class="cart-overlay" id="cartOverlay">
  <div class="cart-header">
    <h3>🛒 Mi Carrito</h3>
    <button onclick="closeCart()">✕</button>
  </div>
  <div class="cart-body" id="cartBody"></div>
  <div class="cart-footer" id="cartFooter"></div>
</div>

<!-- WA FLOAT -->
<div class="wa-float">
  <a href="https://wa.link/lhneng" target="_blank" title="Escríbenos por WhatsApp">📲</a>
</div>

<!-- ADMIN BUTTONS -->
<div class="admin-btn">
  <button onclick="openAdmin('C')" title="Pedidos">C</button>
  <button onclick="openAdmin('R')" title="Editar">R</button>
</div>

<!-- ADMIN MODAL (password) -->
<div class="admin-modal" id="adminModal">
  <div class="admin-box">
    <h3 id="adminModalTitle">🔐 Acceso Administrador</h3>
    <input type="password" id="adminPass" placeholder="Contraseña" onkeydown="if(event.key==='Enter')checkAdmin()">
    <button onclick="checkAdmin()">Ingresar</button>
    <p style="margin-top:10px;font-size:12px;color:var(--gray);text-align:center" id="adminErr"></p>
    <button onclick="closeAdminModal()" style="background:var(--light-bg);color:var(--text);margin-top:8px">Cancelar</button>
  </div>
</div>

<!-- ADMIN PANEL -->
<div class="admin-panel" id="adminPanel">
  <div class="admin-panel-header">
    <h2 id="adminPanelTitle">Panel</h2>
    <button onclick="closeAdminPanel()">✕</button>
  </div>
  <div class="admin-panel-body" id="adminPanelBody"></div>
</div>

<!-- NOTIFICATION -->
<div class="notif" id="notif"></div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-col">
      <div class="logo-box" style="display:inline-block;margin-bottom:12px"><span style="font-family:Poppins;font-weight:900;font-size:20px;color:#1a1a2e">TROGÜI</span></div>
      <p>Tienda colombiana con los mejores productos al mejor precio. Envíos a toda Colombia.</p>
      <p>📍 Colombia</p>
      <p>📞 320 657 2598</p>
    </div>
    <div class="footer-col">
      <h4>Transportadoras</h4>
      <a href="#">🚚 Interrapidísimo</a>
      <a href="#">📦 Coordinadora</a>
      <a href="#">⚡ Envia</a>
      <a href="#">🏪 Servientrega</a>
    </div>
    <div class="footer-col">
      <h4>Información</h4>
      <a href="#">Políticas de entrega</a>
      <a href="#">Garantías</a>
      <a href="#">Preguntas frecuentes</a>
      <a href="#">Contacto</a>
    </div>
    <div class="footer-col">
      <h4>Síguenos</h4>
      <a href="https://www.instagram.com/store_trog" target="_blank">📷 Instagram</a>
      <a href="https://www.tiktok.com/@trogui_store" target="_blank">🎵 TikTok</a>
      <a href="https://wa.link/lhneng" target="_blank">📲 WhatsApp</a>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2025 TROGÜI Store · Todos los derechos reservados</span>
    <div class="footer-social">
      <a href="https://wa.link/lhneng" target="_blank">📲</a>
      <a href="https://www.instagram.com/store_trog" target="_blank">📷</a>
      <a href="https://www.tiktok.com/@trogui_store" target="_blank">🎵</a>
    </div>
  </div>
</footer>

<script>
// ===== PRODUCTS DATA =====
let products = [
  { id: "TRG-001", name: "Quita Callos Eléctrico Profesional", emoji: "🦶", price: 49000, oldPrice: 89000, desc: "Elimina callos, durezas y piel muerta fácilmente. Recargable USB. Ideal para pies suaves y sin dolor.", category: "Salud", units: 6, countdown: 7200, rating: 5, reviews: 127 },
  { id: "TRG-002", name: "Crema Blanqueadora Axilas y Zonas Oscuras", emoji: "✨", price: 49000, oldPrice: 85000, desc: "Aclara y unifica el tono de axilas, codos, rodillas e ingles. Resultados visibles en 2 semanas.", category: "Belleza", units: 4, countdown: 1800, rating: 5, reviews: 89 },
  { id: "TRG-003", name: "Rodillo Masajeador Facial Jade", emoji: "💆", price: 45000, oldPrice: 79000, desc: "Piedra jade natural. Reduce inflamación, mejora circulación y tonifica el rostro.", category: "Belleza", units: 8, countdown: 3600, rating: 5, reviews: 234 },
  { id: "TRG-004", name: "Organizador de Cables Magnético", emoji: "🔌", price: 35000, oldPrice: 65000, desc: "Mantén tu escritorio ordenado. 10 clips magnéticos para cables USB, audífonos y más.", category: "Hogar", units: 12, countdown: 86400, rating: 4, reviews: 56 },
  { id: "TRG-005", name: "Removedor de Pelusa Ropa Eléctrico", emoji: "👕", price: 39000, oldPrice: 72000, desc: "Elimina el pelaje, pelusas y bolitas de la ropa. Recargable. Incluye 3 hojas.", category: "Hogar", units: 5, countdown: 5400, rating: 5, reviews: 178 },
  { id: "TRG-006", name: "Colágeno Hidrolizado Premium 500g", emoji: "💊", price: 55000, oldPrice: 95000, desc: "Para piel, cabello, uñas y articulaciones. Sin azúcar, sin sabor. 100% natural.", category: "Salud", units: 3, countdown: 900, rating: 5, reviews: 312 },
  { id: "TRG-007", name: "Tapete Antideslizante para Baño", emoji: "🛁", price: 38000, oldPrice: 68000, desc: "Material premium con ventosas. Evita accidentes en la ducha. 40x70cm. Varios colores.", category: "Hogar", units: 9, countdown: 43200, rating: 4, reviews: 67 },
  { id: "TRG-008", name: "Set Pinceles Maquillaje Profesional x12", emoji: "💄", price: 49000, oldPrice: 88000, desc: "12 pinceles profesionales con estuche. Cerdas suaves. Para contorno, sombras y base.", category: "Belleza", units: 7, countdown: 7200, rating: 5, reviews: 203 },
  { id: "TRG-009", name: "Aromatizador Eléctrico Difusor USB", emoji: "🌸", price: 45000, oldPrice: 82000, desc: "Difusor ultrasónico. Incluye 5 aceites esenciales. Cambia colores LED. Para hogar y oficina.", category: "Hogar", units: 11, countdown: 3600, rating: 5, reviews: 145 },
  { id: "TRG-010", name: "Faja Reductora Térmica Colombiana", emoji: "👙", price: 55000, oldPrice: 99000, desc: "Faja de neopreno térmica. Reduce medidas, quema grasa y moldea la silueta durante el ejercicio.", category: "Moda", units: 6, countdown: 1800, rating: 5, reviews: 289 },
  { id: "TRG-011", name: "Crema para Estrías y Cicatrices", emoji: "🧴", price: 49000, oldPrice: 85000, desc: "Con vitamina E, aceite de argán y retinol. Previene y reduce estrías visibles en pocas semanas.", category: "Salud", units: 4, countdown: 7200, rating: 4, reviews: 98 },
  { id: "TRG-012", name: "Masajeador de Pies con Calor", emoji: "🦵", price: 65000, oldPrice: 120000, desc: "Masajeador eléctrico con calor y vibración. Alivia el cansancio y dolor de pies.", category: "Salud", units: 3, countdown: 3600, rating: 5, reviews: 167 },
  { id: "TRG-013", name: "Bicarbonato de Sodio 1kg Premium", emoji: "🫙", price: 32000, oldPrice: 58000, desc: "Multiusos: limpieza, belleza, cocina. 100% natural. Calidad alimentaria.", category: "Hogar", units: 15, countdown: 86400, rating: 4, reviews: 78 },
  { id: "TRG-014", name: "Máscara LED Antiedad Facial", emoji: "🤖", price: 75000, oldPrice: 140000, desc: "7 colores de luz LED. Reafirma, rejuvenece y trata el acné. Uso en casa como spa.", category: "Belleza", units: 4, countdown: 1800, rating: 5, reviews: 211 },
  { id: "TRG-015", name: "Cepillo Secador Alisador 3 en 1", emoji: "💇", price: 59000, oldPrice: 110000, desc: "Alisa, seca y da volumen al mismo tiempo. Cerámica iónica. Para todo tipo de cabello.", category: "Belleza", units: 5, countdown: 5400, rating: 5, reviews: 334 },
  { id: "TRG-016", name: "Kit Limpieza Hogar x8 Piezas", emoji: "🧹", price: 45000, oldPrice: 82000, desc: "Incluye escoba, trapero, recogedor, cepillo y más. Mango telescópico ajustable.", category: "Hogar", units: 8, countdown: 43200, rating: 4, reviews: 45 },
  { id: "TRG-017", name: "Aceite de Coco Virgen 500ml", emoji: "🥥", price: 38000, oldPrice: 68000, desc: "100% orgánico. Para cocinar, hidratar cabello y piel. Prensado en frío.", category: "Salud", units: 10, countdown: 86400, rating: 5, reviews: 156 },
  { id: "TRG-018", name: "Pantalón de Mujer Tiro Alto Wide Leg", emoji: "👖", price: 55000, oldPrice: 95000, desc: "Corte ancho de pierna, cintura alta. Material fluido y cómodo. Tallas S-XL.", category: "Moda", units: 6, countdown: 3600, rating: 4, reviews: 89 },
  { id: "TRG-019", name: "Cinturón Masajeador Eléctrico Abdomen", emoji: "⚡", price: 65000, oldPrice: 120000, desc: "Electroestimulación muscular para abdomen y cintura. 6 modos, 10 intensidades. USB.", category: "Salud", units: 4, countdown: 1800, rating: 5, reviews: 145 },
  { id: "TRG-020", name: "Organizador Cajón Ropa Interior x6", emoji: "📦", price: 35000, oldPrice: 62000, desc: "6 separadores para cajones. Organiza ropa interior, medias y accesorios.", category: "Hogar", units: 13, countdown: 86400, rating: 4, reviews: 67 },
  { id: "TRG-021", name: "Suero Vitamina C Facial 30ml", emoji: "🍋", price: 49000, oldPrice: 89000, desc: "Con vitamina C, ácido hialurónico y niacinamida. Ilumina, reduce manchas y unifica.", category: "Belleza", units: 5, countdown: 7200, rating: 5, reviews: 278 },
  { id: "TRG-022", name: "Almohadilla Térmica Eléctrica Cervical", emoji: "🛏", price: 55000, oldPrice: 98000, desc: "Calor terapéutico para cuello, hombros y espalda. 3 temperaturas. Apagado automático.", category: "Salud", units: 7, countdown: 3600, rating: 5, reviews: 189 },
  { id: "TRG-023", name: "Crema de Caracol Hidratante 50g", emoji: "🐌", price: 45000, oldPrice: 79000, desc: "Baba de caracol pura. Regenera, hidrata y reduce cicatrices y manchas.", category: "Belleza", units: 9, countdown: 5400, rating: 5, reviews: 234 },
  { id: "TRG-024", name: "Taza Térmica Acero Inoxidable 500ml", emoji: "☕", price: 39000, oldPrice: 72000, desc: "Mantiene caliente 12h y fría 24h. Con tapa anti-derrame. Apta para lavavajillas.", category: "Hogar", units: 11, countdown: 43200, rating: 5, reviews: 123 },
  { id: "TRG-025", name: "Zapatos Deportivos Mujer Livianos", emoji: "👟", price: 65000, oldPrice: 120000, desc: "Material transpirable, suela antideslizante. Para caminar, trotar y gym. Tallas 35-40.", category: "Moda", units: 5, countdown: 3600, rating: 4, reviews: 78 },
  { id: "TRG-026", name: "Removedor Cutículas Eléctrico", emoji: "💅", price: 39000, oldPrice: 72000, desc: "Elimina cutículas suavemente. Batería recargable. Incluye 3 cabezales.", category: "Belleza", units: 8, countdown: 1800, rating: 5, reviews: 167 },
  { id: "TRG-027", name: "Colchoneta Yoga Antideslizante 6mm", emoji: "🧘", price: 55000, oldPrice: 98000, desc: "Material TPE ecológico. 183x61cm. Perfecta para yoga, pilates y ejercicio en casa.", category: "Salud", units: 6, countdown: 7200, rating: 5, reviews: 112 },
  { id: "TRG-028", name: "Plancha de Vapor Portátil", emoji: "👔", price: 49000, oldPrice: 88000, desc: "Plancha vertical de vapor rápido. Elimina arrugas en 30 segundos. Compacta para viaje.", category: "Hogar", units: 7, countdown: 5400, rating: 4, reviews: 89 },
  { id: "TRG-029", name: "Suplemento de Biotina 10000mcg", emoji: "💊", price: 45000, oldPrice: 82000, desc: "Fortalece cabello, uñas y piel. 60 cápsulas. Sin gluten. 2 meses de tratamiento.", category: "Salud", units: 4, countdown: 3600, rating: 5, reviews: 245 },
  { id: "TRG-030", name: "Cortador de Cebollas Verduras Multicortador", emoji: "🥕", price: 42000, oldPrice: 75000, desc: "Corta, pica y ralla verduras en segundos. Incluye 5 cuchillas intercambiables. Sin BPA.", category: "Cocina", units: 10, countdown: 86400, rating: 4, reviews: 78 },
  { id: "TRG-031", name: "Batidora de Mano Eléctrica 300W", emoji: "🍳", price: 55000, oldPrice: 99000, desc: "300W de potencia. 5 velocidades + turbo. Para batir, mezclar y hacer puré.", category: "Cocina", units: 8, countdown: 43200, rating: 5, reviews: 134 },
  { id: "TRG-032", name: "Crema para Manchas de la Piel", emoji: "🌟", price: 49000, oldPrice: 88000, desc: "Elimina manchas oscuras, melasma y pecas. Con ácido kójico y glicólico. Resultados rápidos.", category: "Belleza", units: 5, countdown: 1800, rating: 5, reviews: 198 },
  { id: "TRG-033", name: "Pesas Mancuernas Ajustables 2kg c/u", emoji: "🏋", price: 59000, oldPrice: 108000, desc: "Par de mancuernas de 2kg cada una. Material antideslizante. Para tonificar y fortalecer.", category: "Salud", units: 6, countdown: 7200, rating: 4, reviews: 67 },
  { id: "TRG-034", name: "Lavadora de Ropa Portátil Mini", emoji: "🫧", price: 75000, oldPrice: 140000, desc: "Mini lavadora ultrasónica. Lava sin detergente, sin dañar telas delicadas. USB.", category: "Hogar", units: 4, countdown: 3600, rating: 5, reviews: 89 },
  { id: "TRG-035", name: "Desodorante Natural de Alumbre 100g", emoji: "🌿", price: 32000, oldPrice: 58000, desc: "Sin aluminio ni parabenos. Dura todo el día. Para piel sensible. 100% mineral natural.", category: "Salud", units: 14, countdown: 86400, rating: 5, reviews: 178 },
  { id: "TRG-036", name: "Cortadora de Cabello Profesional Inalámbrica", emoji: "✂️", price: 65000, oldPrice: 120000, desc: "Batería litio 3h autonomía. 4 guías de corte. Para hombres y niños. Carga USB.", category: "Belleza", units: 5, countdown: 5400, rating: 5, reviews: 156 },
  { id: "TRG-037", name: "Bandas de Resistencia Elásticas x5", emoji: "🏃", price: 45000, oldPrice: 82000, desc: "5 niveles de resistencia. Para glúteos, piernas y brazos. Con bolso incluido.", category: "Salud", units: 9, countdown: 7200, rating: 5, reviews: 201 },
  { id: "TRG-038", name: "Spray Repelente Natural Citronela 200ml", emoji: "🦟", price: 35000, oldPrice: 62000, desc: "100% natural. Protege 8 horas. Para toda la familia. Sin DEET.", category: "Salud", units: 12, countdown: 43200, rating: 4, reviews: 89 },
  { id: "TRG-039", name: "Cojín Cervical Ergonómico para Cuello", emoji: "😴", price: 59000, oldPrice: 108000, desc: "Memory foam. Diseño ergonómico para cuello y cervical. Ideal para viajes.", category: "Hogar", units: 7, countdown: 3600, rating: 5, reviews: 134 },
  { id: "TRG-040", name: "Bolsa Hermética Reutilizable Silicona x3", emoji: "🥗", price: 39000, oldPrice: 72000, desc: "Set x3 bolsas de silicona hermética. Sin BPA. Para alimentos, freezer y microondas.", category: "Cocina", units: 10, countdown: 86400, rating: 4, reviews: 56 },
  { id: "TRG-041", name: "Champú Anti Caída Cabello con Keratina", emoji: "🧖", price: 49000, oldPrice: 89000, desc: "Fortalece el cabello desde la raíz. Con queratina, biotina y aceite de argán.", category: "Belleza", units: 6, countdown: 1800, rating: 5, reviews: 189 },
  { id: "TRG-042", name: "Tenis de Hombre Casual Urbano", emoji: "👟", price: 65000, oldPrice: 118000, desc: "Diseño moderno casual. Suela antifatiga. Material cuero sintético. Tallas 38-45.", category: "Moda", units: 5, countdown: 5400, rating: 4, reviews: 78 },
  { id: "TRG-043", name: "Licuadora Portátil USB Recargable", emoji: "🥤", price: 49000, oldPrice: 88000, desc: "Licua frutas y vegetales en segundos. Batería 4000mAh. Perfecta para el trabajo.", category: "Cocina", units: 8, countdown: 7200, rating: 5, reviews: 212 },
  { id: "TRG-044", name: "Crema Anticelulitis Reafirmante 300g", emoji: "🌺", price: 55000, oldPrice: 98000, desc: "Con cafeína, retinol y centella asiática. Reduce la apariencia de celulitis en 30 días.", category: "Belleza", units: 4, countdown: 3600, rating: 5, reviews: 267 },
  { id: "TRG-045", name: "Cargador Solar Portátil 20000mAh", emoji: "☀️", price: 75000, oldPrice: 140000, desc: "Panel solar + batería 20000mAh. Carga 3 dispositivos al mismo tiempo. Para viajes.", category: "Tecnología", units: 3, countdown: 1800, rating: 5, reviews: 145 }
];

// Cart data
let cart = [];
let currentProduct = null;
let adminMode = null; // 'R' or 'C'
let orders = JSON.parse(localStorage.getItem('trogui_orders') || '[]');

// ===== RENDER PRODUCTS =====
function formatPrice(p) {
  return '$' + p.toLocaleString('es-CO');
}
function starsHtml(rating) {
  let s = '';
  for(let i=0;i<5;i++) s += i < rating ? '⭐' : '☆';
  return s;
}
function pct(oldP, newP) {
  return Math.round((1 - newP/oldP)*100);
}
function countdown(secs, productId) {
  // returns formatted string
  const h = Math.floor(secs/3600);
  const m = Math.floor((secs%3600)/60);
  const s = secs%60;
  if(h > 0) return `${h}h ${m}m`;
  if(m > 0) return `${m}m ${s}s`;
  return `${s}s`;
}

function renderProducts() {
  const grid = document.getElementById('productsGrid');
  grid.innerHTML = '';
  products.forEach(p => {
    const div = document.createElement('div');
    div.className = 'product-card';
    div.onclick = () => openProduct(p);
    const pctVal = pct(p.oldPrice, p.price);
    div.innerHTML = `
      <div class="product-img-wrap">
        <div class="product-img-placeholder">${p.emoji}</div>
        <span class="badge-oferta">OFERTA</span>
        <span class="badge-pct">-${pctVal}%</span>
        <span class="badge-units">⚠️ Solo ${p.units} uds</span>
      </div>
      <div class="product-info">
        <div class="product-name">${p.name}</div>
        <div class="stars">${starsHtml(p.rating)} <span>(${p.reviews})</span></div>
        <div class="price-wrap">
          <span class="price-old">${formatPrice(p.oldPrice)}</span>
          <span class="price-new">${formatPrice(p.price)}</span>
        </div>
        <div class="countdown-box" data-id="${p.id}"><span class="clock">⏰</span> Oferta termina en: <strong class="timer-${p.id}">${countdown(p.countdown, p.id)}</strong></div>
        <div class="free-ship-tag">🚚 Envío GRATIS a Colombia</div>
        <div class="cod-tag">💳 Pago Contra Entrega</div>
        <button class="btn-add" onclick="event.stopPropagation();addToCart(${products.indexOf(p)})">🛒 Añadir al carrito</button>
      </div>
    `;
    grid.appendChild(div);
  });
  startTimers();
}

// ===== TIMERS =====
const timers = {};
function startTimers() {
  products.forEach(p => {
    if(timers[p.id]) clearInterval(timers[p.id]);
    let secs = p.countdown;
    timers[p.id] = setInterval(() => {
      secs = Math.max(0, secs - 1);
      const els = document.querySelectorAll(`.timer-${p.id}`);
      els.forEach(el => el.textContent = countdown(secs, p.id));
      if(secs === 0) clearInterval(timers[p.id]);
    }, 1000);
  });
}

// ===== HERO SLIDER =====
let slideIndex = 0;
function goSlide(i) {
  const slides = document.querySelectorAll('.slide');
  const dots = document.querySelectorAll('.dot');
  slides[slideIndex].classList.remove('active');
  dots[slideIndex].classList.remove('active');
  slideIndex = i;
  slides[slideIndex].classList.add('active');
  dots[slideIndex].classList.add('active');
}
setInterval(() => goSlide((slideIndex+1) % 3), 6000);

// ===== PRODUCT MODAL =====
function openProduct(p) {
  currentProduct = p;
  document.getElementById('modalTitle').textContent = p.name;
  const today = new Date();
  const d1 = new Date(today); d1.setDate(d1.getDate()+3);
  const d2 = new Date(today); d2.setDate(d2.getDate()+7);
  const fmt = d => d.toLocaleDateString('es-CO',{day:'numeric',month:'long'});
  const body = document.getElementById('modalBody');
  body.innerHTML = `
    <div class="modal-img">${p.emoji}</div>
    <div class="stars" style="font-size:18px">${starsHtml(p.rating)} <span style="font-size:14px">(${p.reviews} opiniones)</span></div>
    <div class="modal-prices">
      <span class="modal-price-old">${formatPrice(p.oldPrice)}</span>
      <span class="modal-price-new">${formatPrice(p.price)}</span>
      <span class="modal-saving">Ahorras ${formatPrice(p.oldPrice - p.price)}</span>
    </div>
    <div class="modal-badges">
      <span class="modal-badge mb-green">🚚 Envío GRATIS</span>
      <span class="modal-badge mb-blue">💳 Pago Contra Entrega</span>
      <span class="modal-badge mb-orange">⚠️ Solo ${p.units} unidades</span>
    </div>
    <p class="modal-desc">${p.desc}</p>
    <p style="font-size:12px;color:var(--gray);margin-bottom:6px">ID Producto: ${p.id}</p>
    <div class="delivery-calc">
      <h4>📦 Calculadora de entrega</h4>
      <div class="delivery-dates">
        <span class="from">Pedido hoy →</span>
        <span class="to">🗓 Llega entre el ${fmt(d1)} y el ${fmt(d2)}</span>
      </div>
      <p style="font-size:12px;color:var(--gray);margin-top:6px">Vía Interrapidísimo, Coordinadora o Envia</p>
    </div>
    <div class="countdown-box" style="margin-bottom:12px"><span class="clock">⏰</span> Esta oferta vence en: <strong class="timer-${p.id}">--</strong></div>
    <button class="btn-buy" onclick="closeModal();openOrderForm(currentProduct)">🛍 ¡Pedir Ahora - Pago Contra Entrega!</button>
    <button style="width:100%;background:var(--light-bg);color:var(--text);border:none;padding:12px;border-radius:10px;font-size:15px;font-weight:700;cursor:pointer;margin-top:8px;font-family:Nunito,sans-serif" onclick="addToCart(products.indexOf(currentProduct));closeModal()">🛒 Agregar al carrito</button>
  `;
  document.getElementById('productModal').classList.add('open');
}
function closeModal() {
  document.getElementById('productModal').classList.remove('open');
}

// ===== ORDER FORM =====
function openOrderForm(p) {
  currentProduct = p;
  const today = new Date();
  const d1 = new Date(today); d1.setDate(d1.getDate()+3);
  const d2 = new Date(today); d2.setDate(d2.getDate()+7);
  const fmt = d => d.toLocaleDateString('es-CO',{day:'numeric',month:'long'});
  const fb = document.getElementById('formBody');
  fb.innerHTML = `
    <div class="form-product-summary">
      <div>
        <div class="form-product-name">${p.emoji} ${p.name}</div>
        <div class="form-product-id">ID: ${p.id}</div>
        <div style="font-size:12px;color:var(--gray);margin-top:4px">📦 Llega: ${fmt(d1)} - ${fmt(d2)}</div>
      </div>
      <div class="form-prices">
        <div class="form-price-old">${formatPrice(p.oldPrice)}</div>
        <div class="form-price-new">${formatPrice(p.price)}</div>
        <div style="font-size:11px;color:var(--green);font-weight:700">🚚 Envío GRATIS</div>
      </div>
    </div>
    <div class="form-group">
      <label>Nombre <span>*</span></label>
      <input type="text" id="f_nombre" placeholder="Digita tu nombre completo" required>
      <div class="hint">Escribe tu nombre como aparece en tu cédula</div>
    </div>
    <div class="form-group">
      <label>Apellido <span>*</span></label>
      <input type="text" id="f_apellido" placeholder="Digita tu apellido" required>
    </div>
    <div class="form-group">
      <label>Ciudad o Municipio <span>*</span></label>
      <input type="text" id="f_ciudad" placeholder="Ej: Bogotá, Medellín, Cali..." required>
      <div class="hint">Cubrimos todos los municipios de Colombia</div>
    </div>
    <div class="form-group">
      <label>Dirección <span>*</span></label>
      <input type="text" id="f_direccion" placeholder="Ej: Calle 45 #23-10 Apto 301" required>
      <div class="hint">📍 Entregar directamente en casa o dejar en oficina de Interrapidísimo para recoger allá</div>
    </div>
    <div class="form-group">
      <label>Teléfono <span>*</span></label>
      <input type="tel" id="f_telefono" placeholder="Ej: 3001234567" required>
      <div class="hint">La transportadora te llamará para coordinar la entrega</div>
    </div>
    <div class="form-group">
      <label>Nota adicional <span>*</span></label>
      <textarea id="f_nota" rows="2" placeholder="Ej: Llamar antes de entregar, vecino puede recibir, horario de entrega preferido..." required></textarea>
    </div>
    <button class="form-submit" onclick="submitOrder()">
      <span>📲</span> Confirmar Pedido por WhatsApp
    </button>
    <div class="form-whatsapp-note">📱 Al confirmar, serás redirigido a WhatsApp para enviar tu pedido. ¡Solo dale Enviar!</div>
  `;
  document.getElementById('orderForm').classList.add('open');
}
function closeOrderForm() {
  document.getElementById('orderForm').classList.remove('open');
}
function submitOrder() {
  const nombre = document.getElementById('f_nombre').value.trim();
  const apellido = document.getElementById('f_apellido').value.trim();
  const ciudad = document.getElementById('f_ciudad').value.trim();
  const direccion = document.getElementById('f_direccion').value.trim();
  const telefono = document.getElementById('f_telefono').value.trim();
  const nota = document.getElementById('f_nota').value.trim();
  if(!nombre||!apellido||!ciudad||!direccion||!telefono||!nota) {
    showNotif('⚠️ Por favor completa todos los campos');
    return;
  }
  const p = currentProduct;
  const order = { id: Date.now(), product: p.name, productId: p.id, precio: p.price, nombre, apellido, ciudad, direccion, telefono, nota, fecha: new Date().toLocaleString('es-CO') };
  orders.push(order);
  localStorage.setItem('trogui_orders', JSON.stringify(orders));
  const msg = encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI Store*\n\n` +
    `📦 *Producto:* ${p.name}\n` +
    `🔖 *ID:* ${p.id}\n` +
    `💰 *Precio a cobrar:* ${formatPrice(p.price)}\n` +
    `~~Antes: ${formatPrice(p.oldPrice)}~~\n` +
    `🚚 *Envío:* GRATIS\n\n` +
    `👤 *Cliente:* ${nombre} ${apellido}\n` +
    `📍 *Ciudad:* ${ciudad}\n` +
    `🏠 *Dirección:* ${direccion}\n` +
    `📞 *Teléfono:* ${telefono}\n` +
    `📝 *Nota:* ${nota}\n\n` +
    `✅ Pago Contra Entrega`
  );
  closeOrderForm();
  window.open(`https://wa.me/573206572598?text=${msg}`, '_blank');
  showNotif('✅ ¡Pedido confirmado! Abriendo WhatsApp...');
}

// ===== CART =====
function addToCart(i) {
  const p = products[i];
  const existing = cart.find(c => c.id === p.id);
  if(existing) existing.qty++;
  else cart.push({...p, qty: 1});
  updateCartCount();
  showNotif(`✅ ${p.name} añadido al carrito`);
}
function updateCartCount() {
  document.getElementById('cartCount').textContent = cart.reduce((a,c)=>a+c.qty,0);
}
function openCart() {
  renderCart();
  document.getElementById('cartOverlay').classList.add('open');
}
function closeCart() {
  document.getElementById('cartOverlay').classList.remove('open');
}
function renderCart() {
  const body = document.getElementById('cartBody');
  const footer = document.getElementById('cartFooter');
  if(cart.length === 0) {
    body.innerHTML = '<div class="cart-empty">🛒<br>Tu carrito está vacío</div>';
    footer.innerHTML = '';
    return;
  }
  body.innerHTML = cart.map((p,i) => `
    <div class="cart-item">
      <div class="cart-item-img">${p.emoji}</div>
      <div class="cart-item-info">
        <div class="cart-item-name">${p.name}</div>
        <div class="cart-item-price">${formatPrice(p.price)} x${p.qty}</div>
        <div style="font-size:11px;color:var(--green)">🚚 Envío gratis</div>
      </div>
      <button class="cart-item-remove" onclick="removeCart(${i})">🗑</button>
    </div>
  `).join('');
  const total = cart.reduce((a,c)=>a+c.price*c.qty, 0);
  footer.innerHTML = `
    <div class="cart-total"><span>Total:</span><span style="color:var(--orange)">${formatPrice(total)}</span></div>
    <div style="font-size:12px;color:var(--green);text-align:center;margin-bottom:12px">🚚 Envío GRATIS · 💳 Pago Contra Entrega</div>
    <button class="cart-checkout" onclick="checkoutCart()">✅ Confirmar Pedido</button>
  `;
}
function removeCart(i) {
  cart.splice(i,1);
  updateCartCount();
  renderCart();
}
function checkoutCart() {
  if(cart.length===0) return;
  // Open form for all cart items
  const p = cart[0];
  currentProduct = p;
  const today = new Date();
  const d1 = new Date(today); d1.setDate(d1.getDate()+3);
  const d2 = new Date(today); d2.setDate(d2.getDate()+7);
  const fmt = d => d.toLocaleDateString('es-CO',{day:'numeric',month:'long'});
  const total = cart.reduce((a,c)=>a+c.price*c.qty,0);
  const totalOld = cart.reduce((a,c)=>a+c.oldPrice*c.qty,0);
  const fb = document.getElementById('formBody');
  const itemsList = cart.map(c=>`${c.emoji} ${c.name} x${c.qty} - ${formatPrice(c.price*c.qty)}`).join('\n');
  fb.innerHTML = `
    <div class="form-product-summary">
      <div>
        <div class="form-product-name">🛒 ${cart.length} producto(s)</div>
        <div style="font-size:12px;color:var(--gray);margin-top:4px">📦 Llega: ${fmt(d1)} - ${fmt(d2)}</div>
      </div>
      <div class="form-prices">
        <div class="form-price-old">${formatPrice(totalOld)}</div>
        <div class="form-price-new">${formatPrice(total)}</div>
        <div style="font-size:11px;color:var(--green);font-weight:700">🚚 Envío GRATIS</div>
      </div>
    </div>
    <div class="form-group"><label>Nombre <span>*</span></label><input type="text" id="f_nombre" placeholder="Digita tu nombre completo" required></div>
    <div class="form-group"><label>Apellido <span>*</span></label><input type="text" id="f_apellido" placeholder="Digita tu apellido" required></div>
    <div class="form-group"><label>Ciudad o Municipio <span>*</span></label><input type="text" id="f_ciudad" placeholder="Ej: Bogotá, Medellín..." required><div class="hint">Cubrimos todos los municipios de Colombia</div></div>
    <div class="form-group"><label>Dirección <span>*</span></label><input type="text" id="f_direccion" placeholder="Ej: Calle 45 #23-10" required><div class="hint">📍 Entrega en casa o en oficina Interrapidísimo</div></div>
    <div class="form-group"><label>Teléfono <span>*</span></label><input type="tel" id="f_telefono" placeholder="Ej: 3001234567" required></div>
    <div class="form-group"><label>Nota adicional <span>*</span></label><textarea id="f_nota" rows="2" placeholder="Instrucciones adicionales..." required></textarea></div>
    <button class="form-submit" onclick="submitCartOrder('${encodeURIComponent(itemsList)}',${total},${totalOld})">📲 Confirmar Pedido por WhatsApp</button>
    <div class="form-whatsapp-note">📱 Al confirmar, serás redirigido a WhatsApp</div>
  `;
  closeCart();
  document.getElementById('orderForm').classList.add('open');
}
function submitCartOrder(itemsEnc, total, totalOld) {
  const nombre = document.getElementById('f_nombre').value.trim();
  const apellido = document.getElementById('f_apellido').value.trim();
  const ciudad = document.getElementById('f_ciudad').value.trim();
  const direccion = document.getElementById('f_direccion').value.trim();
  const telefono = document.getElementById('f_telefono').value.trim();
  const nota = document.getElementById('f_nota').value.trim();
  if(!nombre||!apellido||!ciudad||!direccion||!telefono||!nota) { showNotif('⚠️ Completa todos los campos'); return; }
  const items = decodeURIComponent(itemsEnc);
  const order = { id: Date.now(), product: 'Múltiples productos', productId: 'CART', precio: total, nombre, apellido, ciudad, direccion, telefono, nota, fecha: new Date().toLocaleString('es-CO') };
  orders.push(order);
  localStorage.setItem('trogui_orders', JSON.stringify(orders));
  const msg = encodeURIComponent(
    `🛍️ *NUEVO PEDIDO - TROGÜI Store*\n\n` +
    `📦 *Productos:*\n${items}\n\n` +
    `💰 *Total a cobrar:* ${formatPrice(total)}\n` +
    `~~Antes: ${formatPrice(totalOld)}~~\n` +
    `🚚 *Envío:* GRATIS\n\n` +
    `👤 *Cliente:* ${nombre} ${apellido}\n` +
    `📍 *Ciudad:* ${ciudad}\n` +
    `🏠 *Dirección:* ${direccion}\n` +
    `📞 *Teléfono:* ${telefono}\n` +
    `📝 *Nota:* ${nota}\n\n` +
    `✅ Pago Contra Entrega`
  );
  closeOrderForm();
  cart = [];
  updateCartCount();
  window.open(`https://wa.me/573206572598?text=${msg}`, '_blank');
  showNotif('✅ Pedido confirmado!');
}

// ===== SEARCH =====
function similarity(a, b) {
  a = a.toLowerCase().normalize("NFD").replace(/[\u0300-\u036f]/g,"");
  b = b.toLowerCase().normalize("NFD").replace(/[\u0300-\u036f]/g,"");
  if(b.includes(a) || a.includes(b)) return true;
  // simple fuzzy: check if most chars match
  let matches = 0;
  for(let c of a) if(b.includes(c)) matches++;
  return matches/a.length > 0.6;
}
function handleSearch(q) {
  const res = document.getElementById('searchResults');
  if(!q || q.length < 2) { res.classList.remove('open'); return; }
  const found = products.filter(p => similarity(q, p.name) || similarity(q, p.category) || similarity(q, p.desc));
  if(found.length === 0) { res.innerHTML = '<div style="padding:14px;color:var(--gray);text-align:center">No encontramos resultados, intenta con otra palabra</div>'; res.classList.add('open'); return; }
  res.innerHTML = found.slice(0,6).map(p => `
    <div class="search-result-item" onclick="openProduct(p_${p.id.replace('-','_')});document.getElementById('searchResults').classList.remove('open')">
      <div class="search-result-img">${p.emoji}</div>
      <div>
        <div class="search-result-name">${p.name}</div>
        <div class="search-result-price">${formatPrice(p.price)}</div>
      </div>
    </div>
  `).join('');
  // Store refs
  found.forEach(p => window[`p_${p.id.replace('-','_')}`] = p);
  res.classList.add('open');
}
document.addEventListener('click', e => {
  if(!e.target.closest('#searchResults') && !e.target.closest('.search-wrap')) {
    document.getElementById('searchResults').classList.remove('open');
  }
});

// ===== REVIEWS =====
const reviewsData = [
  { name: "Valentina Moreno", city: "Bogotá", avatar: "V", rating: 5, text: "Me llegó en 4 días por interrapidísimo. El quita callos eléctrico es una maravilla, mis pies quedaron suavisimos!! Lo recomiendo 100% 🙌", product: "Quita Callos Eléctrico" },
  { name: "Carlos Andres P.", city: "Medellín", avatar: "C", rating: 5, text: "Escelente producto, la crema blanqueadora si funciona. Ya la compre 3 veces. El envio llego rapido y el pago contra entrega es lo mejor", product: "Crema Blanqueadora" },
  { name: "Luisa Fernanda G.", city: "Cali", avatar: "L", rating: 5, text: "El set de pinceles es profesional de verdad!! Los use para una boda y todos me preguntaron donde los compré 😍 El envío llegó antes de lo esperado", product: "Set Pinceles Maquillaje" },
  { name: "Juan David R.", city: "Barranquilla", avatar: "J", rating: 4, text: "Buena tienda, la licuadora portátil funciona muy bien. Solo le doy 4 porque demoro 6 días pero el producto vale la pena", product: "Licuadora Portátil" },
  { name: "Maria del Carmen S.", city: "Pereira", avatar: "M", rating: 5, text: "La fagia reductora es increible! ya perdi 2 centimetros en una semana usandola en el gym. El pago contra entrega me dio confianza para comprar 🥰", product: "Faja Reductora" },
  { name: "Andres Felipe T.", city: "Bucaramanga", avatar: "A", rating: 5, text: "El masajeador de pies con calor es lo mejor que he comprado. Llegó bien empacado y en perfecto estado. Ya pedí el cinturón masajeador tambien!", product: "Masajeador de Pies" },
];
function renderReviews() {
  const grid = document.getElementById('reviewsGrid');
  grid.innerHTML = reviewsData.map(r => `
    <div class="review-card">
      <div class="reviewer">
        <div class="reviewer-avatar">${r.avatar}</div>
        <div>
          <div class="reviewer-name">${r.name}</div>
          <div class="reviewer-city">📍 ${r.city} · ${r.product}</div>
        </div>
        <div style="margin-left:auto;font-size:13px">${starsHtml(r.rating)}</div>
      </div>
      <p class="review-text">"${r.text}"</p>
    </div>
  `).join('');
}

// ===== ADMIN =====
function openAdmin(mode) {
  adminMode = mode;
  document.getElementById('adminModalTitle').textContent = mode === 'R' ? '🔐 Editar Tienda' : '📋 Ver Pedidos';
  document.getElementById('adminPass').value = '';
  document.getElementById('adminErr').textContent = '';
  document.getElementById('adminModal').classList.add('open');
}
function closeAdminModal() {
  document.getElementById('adminModal').classList.remove('open');
}
function checkAdmin() {
  const pass = document.getElementById('adminPass').value;
  if(pass === '4325') {
    closeAdminModal();
    if(adminMode === 'R') openEditorPanel();
    else openOrdersPanel();
  } else {
    document.getElementById('adminErr').textContent = '❌ Contraseña incorrecta';
  }
}
function closeAdminPanel() {
  document.getElementById('adminPanel').classList.remove('open');
}
function openEditorPanel() {
  document.getElementById('adminPanelTitle').textContent = '✏️ Editar Productos';
  const body = document.getElementById('adminPanelBody');
  body.innerHTML = `<p style="margin-bottom:16px;color:var(--gray)">Edita nombre, precio, precio anterior, descripción e emoji de cada producto.</p>` +
    products.map((p,i) => `
      <div class="admin-product-row" id="row_${i}">
        <h4>${p.id} · ${p.emoji} ${p.name}</h4>
        <input type="text" value="${p.emoji}" placeholder="Emoji" id="ae_emoji_${i}">
        <input type="text" value="${p.name}" placeholder="Nombre" id="ae_name_${i}">
        <input type="number" value="${p.price}" placeholder="Precio" id="ae_price_${i}">
        <input type="number" value="${p.oldPrice}" placeholder="Precio anterior" id="ae_oldprice_${i}">
        <textarea id="ae_desc_${i}" style="grid-column:1/-1">${p.desc}</textarea>
        <button class="admin-save-btn" onclick="saveProduct(${i})">💾 Guardar cambios</button>
      </div>
    `).join('');
  document.getElementById('adminPanel').classList.add('open');
}
function saveProduct(i) {
  products[i].emoji = document.getElementById(`ae_emoji_${i}`).value;
  products[i].name = document.getElementById(`ae_name_${i}`).value;
  products[i].price = parseInt(document.getElementById(`ae_price_${i}`).value);
  products[i].oldPrice = parseInt(document.getElementById(`ae_oldprice_${i}`).value);
  products[i].desc = document.getElementById(`ae_desc_${i}`).value;
  renderProducts();
  showNotif('✅ Producto actualizado');
}
function openOrdersPanel() {
  document.getElementById('adminPanelTitle').textContent = '📋 Pedidos Recibidos';
  const body = document.getElementById('adminPanelBody');
  if(orders.length === 0) { body.innerHTML = '<p style="color:var(--gray);padding:20px">No hay pedidos aún.</p>'; document.getElementById('adminPanel').classList.add('open'); return; }
  body.innerHTML = `<p style="margin-bottom:12px;color:var(--gray)">${orders.length} pedido(s) recibido(s)</p>
    <table class="orders-table">
      <thead><tr><th>Fecha</th><th>Producto</th><th>Cliente</th><th>Ciudad</th><th>Teléfono</th><th>Precio</th></tr></thead>
      <tbody>${orders.map(o=>`<tr><td>${o.fecha}</td><td>${o.product}<br><small>${o.productId}</small></td><td>${o.nombre} ${o.apellido}</td><td>${o.ciudad}</td><td>${o.telefono}</td><td style="font-weight:700;color:var(--orange)">${formatPrice(o.precio)}</td></tr>`).join('')}</tbody>
    </table>`;
  document.getElementById('adminPanel').classList.add('open');
}

// ===== NOTIFICATION =====
function showNotif(msg) {
  const n = document.getElementById('notif');
  n.textContent = msg;
  n.classList.add('show');
  setTimeout(()=>n.classList.remove('show'), 2800);
}

// ===== INIT =====
renderProducts();
renderReviews();
</script>
</body>
</html>
