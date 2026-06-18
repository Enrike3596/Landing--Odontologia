<template>
  <section id="about" class="about-section pt-120">
    <div class="shape shape-2">
      <img src="/img/shapes/shape-2.svg" alt="">
    </div>
    <div class="container">
      <div class="row">
        <div class="col-xl-10 col-lg-11 mx-auto">
          <div class="about-content text-center mb-55">
            <div class="section-title mb-30">
              <span class="wow fadeInDown" data-wow-delay=".2s">Acerca de Nosotros</span>
              <h2 class="mb-15 wow fadeInUp" data-wow-delay=".4s">Bienvenido a Nuestra Clínica Dental</h2>
            </div>
            <p class="mb-35 wow fadeInUp" data-wow-delay=".6s">Somos una clínica dental comprometida con brindar la mejor atención odontológica a nuestros pacientes. Contamos con un equipo de profesionales altamente capacitados y tecnología de vanguardia para garantizar tratamientos de calidad. Nuestra misión es cuidar tu salud bucal y devolverte la confianza en tu sonrisa. Ofrecemos un ambiente cómodo y seguro donde cada paciente recibe atención personalizada y un trato humano excepcional.</p>
            <a href="#contact" class="btn theme-btn wow fadeInUp" data-wow-delay=".8s" @click.prevent="scrollTo('#contact')">Conoce Más</a>
          </div>
        </div>
      </div>
    </div>
    <div class="about-img text-center">
      <img src="/img/about/about-img.png" alt="">
    </div>
  </section>
</template>

<script setup>
function scrollTo(hash) {
  const el = document.querySelector(hash)
  if (el) el.scrollIntoView({ behavior: 'smooth' })
}
</script>
