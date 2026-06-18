<template>
  <section class="faq-section theme-bg">
    <div class="faq-video-wrapper">
      <div class="faq-video">
        <img src="/img/faq/faq-img.jpg" alt="">
        <div class="video-btn">
          <a class="popup-video glightbox" href="#" @click.prevent><i class="lni lni-play"></i></a>
        </div>
      </div>
    </div>
    <div class="shape">
      <img src="/img/shapes/shape-8.svg" alt="" class="shape-faq">
    </div>
    <div class="container">
      <div class="row">
        <div class="col-xl-6 offset-xl-6 col-lg-8 col-md-10">
          <div class="faq-content-wrapper pt-90 pb-90">
            <div class="section-title">
              <span class="text-white wow fadeInDown" data-wow-delay=".2s">Preguntas Frecuentes</span>
              <h2 class="text-white mb-35 wow fadeInUp" data-wow-delay=".4s">Resuelve Todas Tus Dudas Aquí</h2>
            </div>
            <div class="faq-wrapper">
              <div v-for="(item, index) in faqItems" :key="index" class="faq-item mb-20">
                <h5 class="mb-0">
                  <button class="faq-btn btn" :class="{ collapsed: openIndex !== index }" type="button" @click="toggle(index)">
                    {{ item.question }} <i class="lni"></i>
                  </button>
                </h5>
                <div class="collapse" :class="{ show: openIndex === index }">
                  <div class="faq-content">
                    {{ item.answer }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const openIndex = ref(null)

function toggle(index) {
  openIndex.value = openIndex.value === index ? null : index
}

const faqItems = [
  {
    question: '¿Con qué frecuencia debo visitar al dentista?',
    answer: 'Se recomienda visitar al dentista cada 6 meses para limpiezas preventivas y exámenes de rutina. Sin embargo, algunos pacientes pueden necesitar visitas más frecuentes según sus necesidades específicas de salud bucal.'
  },
  {
    question: '¿Duele el tratamiento de conducto?',
    answer: 'Con la anestesia local moderna, el tratamiento de conducto no debería causar dolor durante el procedimiento. Utilizamos técnicas avanzadas para garantizar tu comodidad durante todo el tratamiento.'
  },
  {
    question: '¿Cuánto tiempo dura un blanqueamiento dental?',
    answer: 'Los resultados del blanqueamiento dental pueden durar entre 1 a 3 años, dependiendo de tus hábitos alimenticios, consumo de café, té, vino y tabaco. Un buen cuidado oral ayuda a mantener los resultados por más tiempo.'
  },
  {
    question: '¿Qué cuidados necesito después de una extracción?',
    answer: 'Después de una extracción, es importante morder una gasa durante 30-45 minutos, evitar enjuagues fuertes las primeras 24 horas, no fumar ni usar pajitas, y tomar los medicamentos prescritos según las indicaciones.'
  }
]
</script>
