<template>
  <footer class="footer pt-100 img-bg" style="background-image:url('/img/bg/footer-bg.jpg');">
    <div class="container">
      <div class="footer-widget-wrapper">
        <div class="row">
          <div class="col-xl-4 col-lg-5 col-md-6">
            <div class="footer-widget mb-30">
              <a href="#" class="logo" @click.prevent="scrollTo('#home')"><img src="/img/logo/logo.svg" alt="Clínica Dental Logo"></a>
              <p>Somos una clínica dental comprometida con brindar la mejor atención odontológica. Nuestro equipo de profesionales utiliza tecnología de vanguardia para cuidar tu sonrisa y salud bucal.</p>
              <div class="footer-social-links">
                <ul>
                  <li><a href="https://www.facebook.com/clinicadental" target="_blank" title="Facebook"><i class="lni lni-facebook-filled"></i></a></li>
                  <li><a href="https://www.instagram.com/clinicadental" target="_blank" title="Instagram"><i class="lni lni-instagram-original"></i></a></li>
                  <li><a href="https://wa.me/573012345678" target="_blank" title="WhatsApp"><i class="lni lni-whatsapp"></i></a></li>
                  <li><a href="mailto:info@clinicadental.com" title="Email"><i class="lni lni-envelope"></i></a></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="col-xl-2 col-lg-3 col-md-6">
            <div class="footer-widget mb-30">
              <h4>Enlaces Rápidos</h4>
              <ul class="footer-links">
                <li><a href="#home" @click.prevent="scrollTo('#home')">Inicio</a></li>
                <li><a href="#about" @click.prevent="scrollTo('#about')">Acerca de Nosotros</a></li>
                <li><a href="#services" @click.prevent="scrollTo('#services')">Servicios</a></li>
                <li><a href="#team" @click.prevent="scrollTo('#team')">Odontólogos</a></li>
                <li><a href="#blog" @click.prevent="scrollTo('#blog')">Blog</a></li>
                <li><a href="#contact" @click.prevent="scrollTo('#contact')">Contacto</a></li>
              </ul>
            </div>
          </div>
          <div class="col-xl-2 col-lg-3 col-md-5">
            <div class="footer-widget mb-30">
              <h4>Servicios</h4>
              <ul class="footer-links">
                <li><a href="#" @click.prevent>Odontología General</a></li>
                <li><a href="#" @click.prevent>Ortodoncia</a></li>
                <li><a href="#" @click.prevent>Endodoncia</a></li>
                <li><a href="#" @click.prevent>Consulta de Rutina</a></li>
                <li><a href="#" @click.prevent>Periodoncia</a></li>
                <li><a href="#" @click.prevent>Cirugía Dental</a></li>
              </ul>
            </div>
          </div>
          <div class="col-xl-4 col-lg-12 col-md-7">
            <div class="footer-widget mb-30">
              <h4>Ubicación de la Clínica</h4>
              <div class="map-canvas">
                <iframe class="map" id="gmap_canvas"
                  src="https://www.openstreetmap.org/export/embed.html?bbox=-74.0823%2C4.5981%2C-74.0723%2C4.6081&amp;layer=mapnik&amp;marker=4.6031%2C-74.0773"
                  style="border: 0;"
                  allowfullscreen=""
                  loading="lazy"
                  referrerpolicy="no-referrer-when-downgrade"></iframe>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="copyright-area">
        <p class="mb-0 text-center">© 2025 Medic|Todos los derechos reservados</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
function scrollTo(hash) {
  const el = document.querySelector(hash)
  if (el) el.scrollIntoView({ behavior: 'smooth' })
}
</script>
