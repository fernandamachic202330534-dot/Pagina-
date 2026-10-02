<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ATHLEX - Vive el deporte. Viste ATHLEX.</title>
<!-- Tipografía Poppins (identidad de marca) -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?
family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<!-- Iconos FontAwesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-
awesome/6.4.0/css/all.min.css">
<style>
/* --- VARIABLES DE MARCA (Manual CMI) --- */
:root {
--naranja: #FF6B00; /* Energía y dinamismo */
--negro: #1E1E1E; /* Fuerza y elegancia */
--blanco: #FFFFFF; /* Limpieza y equilibrio */
--gris-oscuro: #2a2a2a;
--gris-claro: #f4f4f4;
}
/* --- RESET Y ESTILOS GLOBALES --- */
* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
font-family: 'Poppins', sans-serif;
background-color: var(--negro);
color: var(--blanco);
line-height: 1.6;
overflow-x: hidden;
}
a { text-decoration: none; color: inherit; transition: 0.3s; }
ul { list-style: none; }
/* --- HEADER / LOGO (Parte superior) --- */
header {
background-color: rgba(30, 30, 30, 0.95);
padding: 15px 5%;
display: flex;
justify-content: space-between;
align-items: center;
position: sticky;
top: 0;
z-index: 1000;
border-bottom: 2px solid var(--naranja);
backdrop-filter: blur(10px);
}
.logo-container { display: flex; align-items: center; gap: 15px; }
.logo-container img {
height: 55px;
width: auto;
border-radius: 50%;
border: 2px solid var(--naranja);
}
.logo-text { font-size: 1.8rem; font-weight: 700; letter-spacing: 1px; }
.logo-text span { color: var(--naranja); }
nav ul { display: flex; gap: 25px; }
nav ul li a { font-weight: 500; font-size: 0.95rem; text-transform: uppercase; }
nav ul li a:hover { color: var(--naranja); }
/* --- HERO SECTION --- */
.hero {
background: linear-gradient(rgba(0,0,0,0.75), rgba(0,0,0,0.85)),
url('https://images.unsplash.com/photo-1552674605-db6ffd4facb5?
q=80&w=2070&auto=format&fit=crop') no-repeat center center/cover;
height: 85vh;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
text-align: center;
padding: 0 20px;
position: relative;
}
.hero h1 {
font-size: 4rem;
font-weight: 700;
margin-bottom: 10px;
text-transform: uppercase;
line-height: 1.1;
text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
}
.hero h1 span { color: var(--naranja); }
.hero p {
font-size: 1.3rem;
max-width: 700px;
margin-bottom: 30px;
font-weight: 300;
}
.btn {
background-color: var(--naranja);
color: var(--blanco);
padding: 15px 35px;
border: none;
border-radius: 5px;
font-weight: 600;
font-size: 1rem;
cursor: pointer;
text-transform: uppercase;
transition: 0.3s;
display: inline-block;
}
.btn:hover { background-color: #e05e00; transform: scale(1.05); }
.btn-outline {
background-color: transparent;
border: 2px solid var(--naranja);
color: var(--naranja);
}
.btn-outline:hover { background-color: var(--naranja); color: var(--blanco); }
/* --- SECCIONES GENERALES --- */
section { padding: 80px 5%; }
.section-title {
text-align: center;
font-size: 2.5rem;
margin-bottom: 15px;
text-transform: uppercase;
}
.section-title span { color: var(--naranja); }
.section-subtitle {
text-align: center;
margin-bottom: 50px;
color: #ccc;
font-weight: 300;
max-width: 800px;
margin-left: auto;
margin-right: auto;
}
/* --- SECCIÓN MARCA (Manual CMI) --- */
.brand-section {
display: flex;
flex-wrap: wrap;
align-items: center;
justify-content: center;
background-color: #151515;
gap: 50px;
}
.brand-text { flex: 1; min-width: 300px; max-width: 600px; }
.brand-text h2 { font-size: 2.5rem; margin-bottom: 20px; text-transform: uppercase; }
.brand-text h2 span { color: var(--naranja); }
.brand-text p { margin-bottom: 15px; color: #ccc; }
.brand-text ul { margin-top: 20px; }
.brand-text ul li { margin-bottom: 10px; display: flex; align-items: center; gap: 10px; }
.brand-text ul li i { color: var(--naranja); }
.brand-image { flex: 1; min-width: 300px; max-width: 500px; text-align: center; }
.brand-image img { width: 100%; border-radius: 15px; border: 3px solid var(--naranja);
box-shadow: 0 10px 30px rgba(255,107,0,0.2); }
/* --- CATÁLOGO --- */
.catalog-section { background-color: var(--negro); }
.grid-catalog {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 30px;
max-width: 1200px;
margin: 0 auto;
}
.card {
background-color: var(--gris-oscuro);
border-radius: 10px;
overflow: hidden;
transition: 0.3s;
border: 1px solid #333;
}
.card:hover { transform: translateY(-10px); border-color: var(--naranja); box-shadow: 0
10px 20px rgba(255, 107, 0, 0.2); }
.card-img { height: 300px; overflow: hidden; background-color: #333; }
.card-img img { width: 100%; height: 100%; object-fit: cover; transition: 0.5s; }
.card:hover .card-img img { transform: scale(1.1); }
.card-info { padding: 20px; text-align: center; }
.card-info h3 { font-size: 1.3rem; margin-bottom: 5px; }
.card-info .category { font-size: 0.8rem; color: var(--naranja); text-transform:
uppercase; letter-spacing: 1px; margin-bottom: 10px; display: block; }
.card-info p { font-size: 0.9rem; color: #aaa; margin-bottom: 15px; }
.btn-small {
display: inline-block;
background-color: transparent;
border: 2px solid var(--naranja);
color: var(--naranja);
padding: 8px 20px;
border-radius: 5px;
font-weight: 600;
font-size: 0.85rem;
transition: 0.3s;
}
.btn-small:hover { background-color: var(--naranja); color: var(--blanco); }
/* --- PROMOCIONES (Mes del Deportista) --- */
.promo-section {
background: linear-gradient(135deg, var(--negro) 0%, #2a1200 100%);
border-top: 2px solid var(--naranja);
border-bottom: 2px solid var(--naranja);
}
.promo-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 30px;
max-width: 1200px;
margin: 0 auto;
}
.promo-card {
background-color: rgba(255,255,255,0.05);
border: 1px solid rgba(255,107,0,0.3);
padding: 30px;
border-radius: 10px;
text-align: center;
transition: 0.3s;
}
.promo-card:hover { background-color: rgba(255,107,0,0.1); border-color: var(--
naranja); }
.promo-card i { font-size: 2.5rem; color: var(--naranja); margin-bottom: 15px; }
.promo-card h3 { font-size: 1.5rem; margin-bottom: 10px; }
.promo-card p { font-size: 0.95rem; color: #ccc; }
/* --- ATHLEX CLUB --- */
.club-section { background-color: #111; text-align: center; }
.club-card {
background: linear-gradient(135deg, #1a1a1a, #333);
border: 2px solid var(--naranja);
border-radius: 15px;
padding: 50px;
max-width: 800px;
margin: 0 auto;
box-shadow: 0 0 30px rgba(255,107,0,0.2);
}
.club-card h2 { font-size: 2.5rem; margin-bottom: 20px; color: var(--naranja); text-
transform: uppercase; }
.club-card p { font-size: 1.1rem; margin-bottom: 30px; }
.club-benefits { display: flex; justify-content: center; gap: 40px; flex-wrap: wrap;
margin-bottom: 30px; }
.club-benefits div { display: flex; flex-direction: column; align-items: center; gap: 10px;
}
.club-benefits i { font-size: 2rem; color: var(--naranja); }
/* --- CMI / RESPONSABILIDAD SOCIAL --- */
.cmi-section { background-color: var(--gris-claro); color: var(--negro); }
.cmi-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
gap: 40px; max-width: 1200px; margin: 0 auto; }
.cmi-item h3 { color: var(--naranja); margin-bottom: 15px; font-size: 1.5rem; }
.cmi-item p { font-size: 0.95rem; color: #333; }
.cmi-item ul { margin-top: 10px; }
.cmi-item ul li { margin-bottom: 8px; font-size: 0.9rem; display: flex; gap: 10px; }
.cmi-item ul li i { color: var(--naranja); margin-top: 5px; }
/* --- FOOTER --- */
footer {
background-color: #0a0a0a;
padding: 50px 5% 20px;
text-align: center;
border-top: 2px solid var(--naranja);
}
.footer-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
gap: 30px;
max-width: 1200px;
margin: 0 auto 40px;
text-align: left;
}
.footer-col h4 { color: var(--naranja); margin-bottom: 20px; text-transform: uppercase;
font-size: 1.1rem; }
.footer-col p, .footer-col a { color: #aaa; font-size: 0.9rem; display: block; margin-
bottom: 10px; }
.footer-col a:hover { color: var(--naranja); }
.social-links { display: flex; gap: 15px; margin-top: 15px; }
.social-links a { font-size: 1.5rem; color: var(--blanco); }
.social-links a:hover { color: var(--naranja); transform: scale(1.1); }
.footer-bottom { border-top: 1px solid #333; padding-top: 20px; font-size: 0.8rem;
color: #777; }
.footer-bottom span { color: var(--naranja); }
/* --- RESPONSIVE --- */
@media (max-width: 768px) {
header { flex-direction: column; gap: 15px; padding: 15px; }
nav ul { gap: 15px; flex-wrap: wrap; justify-content: center; }
.hero h1 { font-size: 2.5rem; }
.hero p { font-size: 1rem; }
.brand-section { flex-direction: column-reverse; text-align: center; }
.brand-text ul li { justify-content: center; }
.club-benefits { flex-direction: column; gap: 20px; }
.footer-grid { text-align: center; }
.social-links { justify-content: center; }
}
</style>
</head>
<body>
<!-- HEADER CON LOGO -->
<header>
<div class="logo-container">
<!-- REEMPLAZA ESTA URL CON TU LOGO REAL -->
<img src="https://i.ibb.co/6P0R9Xb/logo-athlex.png" alt="Logo ATHLEX"
onerror="this.src='https://placehold.co/100x100/FF6B00/FFFFFF?text=ATHLEX'">
<div class="logo-text">ATH<span>LEX</span></div>
</div>
<nav>
<ul>
<li><a href="#inicio">Inicio</a></li>
<li><a href="#marca">Nosotros</a></li>
<li><a href="#catalogo">Catálogo</a></li>
<li><a href="#promociones">Promociones</a></li>
<li><a href="#club">ATHLEX CLUB</a></li>
<li><a href="#contacto">Contacto</a></li>
</ul>
</nav>
</header>
<!-- HERO SECTION -->
<section class="hero" id="inicio">
<h1>Vive el deporte.<br>Viste <span>ATHLEX</span>.</h1>
<p>Equípate con calidad, comodidad y estilo. Más que una marca, un estilo de vida.
</p>
<div style="display: flex; gap: 15px; flex-wrap: wrap; justify-content: center;">
<a href="#catalogo" class="btn">Ver Catálogo</a>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20información%20sobre%20ATHLEX" class="btn btn-outline"
target="_blank">Consultar por WhatsApp</a>
</div>
</section>
<!-- SECCIÓN MARCA (Manual CMI) -->
<section class="brand-section" id="marca">
<div class="brand-text">
<h2>ATHLEX, <span>Más que una marca</span></h2>
<p>En ATHLEX no solo vendemos ropa deportiva; impulsamos un estilo de vida.
Nuestra mascota, <strong>AXEL</strong>, representa la fuerza, elegancia y determinación
que necesitas para superar cada límite.</p>
<p>Nuestra misión es inspirar a las personas a vivir el deporte como un estilo de
vida, ofreciendo productos de alta calidad, asesoría personalizada y precios competitivos.
</p>
<ul>
<li><i class="fas fa-check-circle"></i> Calidad, diseño y precios competitivos.
</li>
<li><i class="fas fa-check-circle"></i> Asesoría personalizada por disciplina
deportiva.</li>
fidelización.</li>
<li><i class="fas fa-check-circle"></i> Promociones constantes y programa de
<li><i class="fas fa-check-circle"></i> Compromiso con la comunidad deportiva
local.</li>
</ul>
</div>
<div class="brand-image">
<!-- REEMPLAZA CON LA IMAGEN DE LA MASCOTA AXEL -->
<img src="https://i.ibb.co/3s7Kq0R/axel-pantera.png" alt="Mascota AXEL - Pantera
ATHLEX" onerror="this.src='https://placehold.co/600x600/1E1E1E/FF6B00?
text=AXEL+ATHLEX'">
</div>
</section>
<!-- CATÁLOGO -->
<section class="catalog-section" id="catalogo">
<h2 class="section-title">Nuestro <span>Catálogo</span></h2>
<p class="section-subtitle">Descubre nuestra colección diseñada para rendir al
máximo. *Precios disponibles próximamente.</p>
<div class="grid-catalog">
<!-- Producto 1 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1556821840-3a63f95609a7?
q=80&w=1000&auto=format&fit=crop" alt="Sudadera ATHLEX">
</div>
<div class="card-info">
<span class="category">Línea Caballero</span>
<h3>Sudadera con Capucha</h3>
<p>Diseño ergonómico con materiales premium para entrenamiento y uso
diario.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20la%20Sudadera%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
<!-- Producto 2 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1506152983158-
b4a74a01c721?q=80&w=1000&auto=format&fit=crop" alt="Leggings ATHLEX">
</div>
<div class="card-info">
<span class="category">Línea Damas</span>
<h3>Leggings Deportivos</h3>
<p>Compresión, flexibilidad y estilo para tus rutinas de gimnasio o running.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20los%20Leggings%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
<!-- Producto 3 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?
q=80&w=1000&auto=format&fit=crop" alt="Tenis ATHLEX">
</div>
<div class="card-info">
<span class="category">Calzado</span>
<h3>Tenis Running / Casual</h3>
<p>Amortiguación y ligereza para cada paso. Disponibles en varias tallas.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20los%20Tenis%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
<!-- Producto 4 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?
q=80&w=1000&auto=format&fit=crop" alt="Playera ATHLEX">
</div>
<div class="card-info">
<span class="category">Línea Caballero</span>
<h3>Playera Dry Fit</h3>
<p>Transpirable y ligera, ideal para mantenerte fresco durante el ejercicio.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20la%20Playera%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
<!-- Producto 5 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1588850561407-
ed78c282e89b?q=80&w=1000&auto=format&fit=crop" alt="Gorra ATHLEX">
</div>
<div class="card-info">
<span class="category">Accesorios</span>
<h3>Gorra Deportiva</h3>
<p>Protección y estilo para tus entrenamientos al aire libre.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20la%20Gorra%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
<!-- Producto 6 -->
<div class="card">
<div class="card-img">
<img src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?
q=80&w=1000&auto=format&fit=crop" alt="Mochila ATHLEX">
</div>
<div class="card-info">
<span class="category">Línea Niños</span>
<h3>Mochila Deportiva</h3>
<p>Espacio y durabilidad para llevar todo tu equipo a donde vayas.</p>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20consultar%20por%20la%20Mochila%20ATHLEX" class="btn-
small" target="_blank">Consultar</a>
</div>
</div>
</div>
</section>
<!-- PROMOCIONES (Mes del Deportista) -->
<section class="promo-section" id="promociones">
<h2 class="section-title">Mes del <span>Deportista ATHLEX</span></h2>
<p class="section-subtitle">Aprovecha nuestras promociones exclusivas por tiempo
limitado. ¡Equípate con lo mejor!</p>
<div class="promo-grid">
<div class="promo-card">
<i class="fas fa-percent"></i>
<h3>20% Descuento</h3>
<p>En prendas seleccionadas (sudaderas, playeras, pants y shorts).</p>
</div>
<div class="promo-card">
<i class="fas fa-shoe-prints"></i>
<h3>15% Descuento</h3>
<p>En calzado deportivo de todas las marcas participantes.</p>
</div>
<div class="promo-card">
<i class="fas fa-gift"></i>
<h3>Regalo Especial</h3>
<p>Botella deportiva de regalo por compras mayores a Q500.</p>
</div>
<div class="promo-card">
<i class="fas fa-trophy"></i>
<h3>Sorteo de Kit</h3>
<p>Participa en el sorteo de un kit deportivo completo entre todos los
compradores.</p>
</div>
</div>
</section>
<!-- ATHLEX CLUB -->
<section class="club-section" id="club">
<div class="club-card">
<h2>ATHLEX CLUB</h2>
<p>Más que una tienda, una comunidad que te impulsa. Únete a nuestro programa
de beneficios y lleva tu pasión por el deporte al siguiente nivel.</p>
<div class="club-benefits">
<div>
<i class="fas fa-star"></i>
<span>Acumula Puntos</span>
</div>
<div>
<i class="fas fa-tags"></i>
<span>Descuentos Exclusivos</span>
</div>
<div>
<i class="fas fa-clock"></i>
<span>Acceso Anticipado</span>
</div>
</div>
<a href="https://wa.me/50212345678?
text=Hola,%20quiero%20activar%20mi%20ATHLEX%20CLUB" class="btn"
target="_blank">Activar mi ATHLEX CLUB</a>
</div>
</section>
<!-- CMI / RESPONSABILIDAD SOCIAL -->
<section class="cmi-section" id="cmi">
<h2 class="section-title" style="color: var(--negro);">Comunicación y
<span>Responsabilidad</span></h2>
<p class="section-subtitle" style="color: #555;">Nuestro compromiso es comunicar
con una sola voz y actuar de manera responsable con nuestra comunidad.</p>
<div class="cmi-grid">
<div class="cmi-item">
<h3>Comunicación Integrada (CMI)</h3>
<p>Todos nuestros mensajes, desde redes sociales hasta la atención en tienda,
hablan con una sola voz: calidad, pasión y superación.</p>
<ul>
<li><i class="fas fa-bullhorn"></i> Publicidad digital (Facebook, Instagram,
TikTok, Google Ads).</li>
<li><i class="fas fa-store"></i> Venta personal y asesoría en tienda.</li>
<li><i class="fas fa-hands-helping"></i> Relaciones públicas con la comunidad
deportiva.</li>
</ul>
</div>
<div class="cmi-item">
<h3>Compromiso Responsable</h3>
<p>Creemos en el deporte como herramienta de bienestar y desarrollo social. Por
eso, nos comprometemos a:</p>
<ul>
<li><i class="fas fa-check"></i> Publicidad veraz y transparente.</li>
<li><i class="fas fa-check"></i> Promoción de la salud y el deporte.</li>
<li><i class="fas fa-check"></i> Inclusión de tallas para toda la familia.</li>
<li><i class="fas fa-check"></i> Apoyo a equipos y academias locales.</li>
<li><i class="fas fa-check"></i> Uso responsable de datos de clientes.</li>
</ul>
</div>
</div>
</section>
<!-- FOOTER / CONTACTO -->
<footer id="contacto">
<div class="footer-grid">
<div class="footer-col">
<h4>ATHLEX</h4>
<p>Vive el deporte. Viste ATHLEX.</p>
<div class="social-links">
<a href="https://www.tiktok.com/@athlex.gt" target="_
blank" title="TikTok"><i
class="fab fa-tiktok"></i></a>
<a href="https://www.instagram.com/athlex.gt" target="_
blank"
title="Instagram"><i class="fab fa-instagram"></i></a>
<a href="https://wa.me/50212345678" target="_blank" title="WhatsApp"><i
class="fab fa-whatsapp"></i></a>
<a href="#" target="_
blank" title="Facebook"><i class="fab fa-facebook-f">
</i></a>
</div>
</div>
<div class="footer-col">
<h4>Enlaces Rápidos</h4>
<a href="#inicio">Inicio</a>
<a href="#marca">Nosotros</a>
<a href="#catalogo">Catálogo</a>
<a href="#promociones">Promociones</a>
<a href="#club">ATHLEX CLUB</a>
</div>
<div class="footer-col">
<h4>Contacto</h4>
<p><i class="fas fa-map-marker-alt" style="color: var(--naranja); margin-right:
8px;"></i> Ciudad y municipios cercanos</p>
<p><i class="fas fa-phone" style="color: var(--naranja); margin-right: 8px;"></i>
+502 1234 5678</p>
<p><i class="fas fa-envelope" style="color: var(--naranja); margin-right: 8px;">
</i> info@athlexgt.com</p>
<p><i class="fas fa-globe" style="color: var(--naranja); margin-right: 8px;"></i>
www.athlexgt.com</p>
</div>
</div>
<div class="footer-bottom">
<p>© 2026 ATHLEX. Todos los derechos reservados. <br> <span>Vive el deporte.
Viste ATHLEX.</span></p>
</div>
</footer>
<!-- JavaScript para suavizar el scroll (opcional) -->
<script>
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
anchor.addEventListener('click', function (e) {
e.preventDefault();
document.querySelector(this.getAttribute('href')).scrollIntoView({
behavior: 'smooth'
});
});
});
</script>
</body>
</html>
