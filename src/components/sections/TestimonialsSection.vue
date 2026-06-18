<template>
  <section id="testimonial" class="testimonial-section pt-150 pb-150">
    <div class="shape shape-5">
      <img src="/img/shapes/shape-2.svg" alt="">
    </div>
    <div class="shape shape-6">
      <img src="/img/shapes/shape-5.svg" alt="">
    </div>
    <div class="container">
      <div class="row">
        <div class="col-xl-8 mx-auto">
          <div class="section-title text-center mb-55">
            <span class="wow fadeInDown" data-wow-delay=".2s">Testimoniales</span>
            <h2 class="mb-15 wow fadeInUp" data-wow-delay=".4s">Lo Que Dicen Nuestros Pacientes</h2>
            <p class="wow fadeInUp" data-wow-delay=".6s">La satisfacción de nuestros pacientes es nuestra mayor recompensa. Conoce las experiencias de quienes han confiado en nosotros para cuidar su salud bucal.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div v-for="(item, index) in testimonials" :key="index" class="col-lg-4 col-md-6">
          <div class="testimonial-box wow fadeInUp" :data-wow-delay="item.delay">
            <div class="testimonial-header">
              <div class="testimonial-avatar">
                <img :src="item.img" :alt="item.name">
              </div>
              <div class="testimonial-info">
                <h4>{{ item.name }}</h4>
                <span class="treatment">{{ item.treatment }}</span>
              </div>
            </div>
            <div class="testimonial-rating">
              <i v-for="n in 5" :key="n" class="lni lni-star-filled"></i>
            </div>
            <p class="testimonial-text">
              "{{ item.text }}"
            </p>
            <div class="testimonial-quote">
              <i class="lni lni-quotation"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    img: '/img/testimonial/testimonial.1.jpg',
    name: 'María Carmen López',
    treatment: 'Paciente de Ortodoncia',
    text: 'Excelente atención y profesionalismo. Me realizaron un tratamiento de ortodoncia y el resultado superó mis expectativas. El equipo es muy amable y las instalaciones están impecables. Sin duda, la mejor clínica dental de la ciudad.',
    delay: '.2s'
  },
  {
    img: '/img/testimonial/testimonial.4.jpg',
    name: 'Juan Rodríguez',
    treatment: 'Implante Dental',
    text: 'Tenía mucho miedo al dentista, pero el Dr. y su equipo me hicieron sentir muy cómodo. Me realizaron un implante dental y todo el proceso fue indoloro. La tecnología que utilizan es de última generación. ¡Altamente recomendados!',
    delay: '.4s'
  },
  {
    img: '/img/testimonial/testimonial.3.jpg',
    name: 'Ana Martínez',
    treatment: 'Endodoncia',
    text: 'Mi hija necesitaba un tratamiento de endodoncia y estaba muy nerviosa. El equipo fue muy paciente y cariñoso con ella. Explicaron cada paso del proceso y los resultados fueron excelentes. Definitivamente volveremos.',
    delay: '.6s'
  },
  {
    img: '/img/testimonial/testimonial.2.jpg',
    name: 'Laura Gómez',
    treatment: 'Blanqueamiento Dental',
    text: 'Después de años buscando una clínica dental de confianza, finalmente la encontré. Me hicieron un blanqueamiento dental y el cambio fue increíble. La atención personalizada y el seguimiento post-tratamiento son impecables. ¡Mi sonrisa luce radiante!',
    delay: '.8s'
  },
  {
    img: '/img/testimonial/testimonial.5.jpg',
    name: 'Carlos Sánchez',
    treatment: 'Urgencia Dental',
    text: 'Tuve una emergencia dental un sábado y me atendieron de inmediato. El servicio de urgencias 24/7 es realmente efectivo. El dolor desapareció rápidamente y me dieron todas las indicaciones necesarias. Gracias por su pronta respuesta.',
    delay: '1s'
  },
  {
    img: '/img/testimonial/testimonial.6.jpg',
    name: 'Sofía Pérez',
    treatment: 'Limpieza Dental',
    text: 'La limpieza dental fue muy completa y profesional. Me explicaron técnicas de cepillado y cuidado bucal. Además, la clínica es muy moderna y limpia, lo que transmite mucha confianza. Los precios son justos para la calidad del servicio. ¡Totalmente satisfecha!',
    delay: '1.2s'
  }
]
</script>

<style scoped>
.testimonial-box {
  background: #fff;
  border-radius: 12px;
  padding: 2rem 1.5rem;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 100%;
  display: flex;
  flex-direction: column;
  position: relative;
}

.testimonial-box:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
}

.testimonial-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.testimonial-avatar {
  flex-shrink: 0;
}

.testimonial-avatar img {
  width: 56px;
  height: 56px;
  object-fit: cover;
  border-radius: 50%;
  border: 3px solid #00adb5;
}

.testimonial-info h4 {
  font-size: 1rem;
  font-weight: 700;
  color: #222;
  margin: 0 0 0.2rem;
}

.testimonial-info .treatment {
  font-size: 0.8rem;
  color: #00adb5;
  font-weight: 600;
}

.testimonial-rating {
  margin-bottom: 0.75rem;
}

.testimonial-rating i {
  color: #f5b50a;
  font-size: 0.95rem;
  margin-right: 2px;
}

.testimonial-text {
  font-size: 0.9rem;
  line-height: 1.6;
  color: #555;
  flex: 1;
}

.testimonial-quote {
  margin-top: 1rem;
  text-align: right;
}

.testimonial-quote i {
  font-size: 1.8rem;
  color: #00adb5;
  opacity: 0.2;
}
</style>
