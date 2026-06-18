<template>
  <section id="blog" class="blog-section pt-150">
    <div class="shape shape-7">
      <img src="/img/shapes/shape-6.svg" alt="">
    </div>
    <div class="container">
      <div class="row">
        <div class="col-xl-8 mx-auto">
          <div class="section-title text-center mb-55">
            <span class="wow fadeInDown" data-wow-delay=".2s">Blog</span>
            <h2 class="mb-15 wow fadeInUp" data-wow-delay=".4s">Noticias y Consejos</h2>
            <p class="wow fadeInUp" data-wow-delay=".4s">Mantente informado sobre cuidado dental y novedades en
              <br class="d-none d-lg-block"> tratamientos odontológicos con nuestros artículos especializados.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div v-for="(post, index) in blogPosts" :key="index" class="col-xl-4 col-lg-4 col-md-6">
          <div class="single-blog mb-30 wow fadeInUp" :data-wow-delay="post.delay">
            <div class="blog-img">
              <a href="#" @click.prevent><img :src="post.img" alt=""></a>
            </div>
            <div class="blog-content">
              <h4><a href="#" @click.prevent>{{ post.title }}</a></h4>
              <p>{{ post.excerpt }}</p>
              <a class="read-more" href="#" @click.prevent>Leer Más <i class="lni lni-arrow-right"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const blogPosts = [
  {
    img: '/img/blog/blog-1.png',
    title: '10 Consejos Esenciales para una Sonrisa Saludable',
    excerpt: 'Descubre los mejores consejos profesionales para mantener tu salud bucal en óptimas condiciones y prevenir problemas dentales comunes.',
    delay: '.2s'
  },
  {
    img: '/img/blog/blog-2.png',
    title: 'Guía Completa de Cuidado Dental en Casa',
    excerpt: 'Aprende las mejores técnicas de cepillado, uso de hilo dental y productos recomendados para el cuidado diario.',
    delay: '.4s'
  },
  {
    img: '/img/blog/blog-3.png',
    title: 'Tecnologías Innovadoras en Odontología',
    excerpt: 'Conoce las últimas tendencias en tratamientos dentales y cómo la tecnología mejora tu experiencia.',
    delay: '.6s'
  }
]
</script>
