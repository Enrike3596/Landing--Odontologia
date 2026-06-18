<template>
  <section id="team" class="team-section pt-150 pb-150">
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
            <span class="wow fadeInDown" data-wow-delay=".2s">Nuestro Equipo</span>
            <h2 class="mb-15 wow fadeInUp" data-wow-delay=".4s">Odontólogos Especializados</h2>
            <p class="wow fadeInUp" data-wow-delay=".6s">Contamos con un equipo de profesionales altamente capacitados y especializados en diferentes áreas de la odontología, comprometidos con brindar la mejor atención personalizada a cada paciente.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div v-for="(member, index) in teamMembers" :key="index" class="col-lg-4 col-md-6">
          <div class="team-box text-center mb-30 wow fadeInUp" :data-wow-delay="member.delay">
            <div class="team-img mb-25">
              <img :src="member.img" :alt="member.name">
            </div>
            <div class="team-content">
              <h4>{{ member.name }}</h4>
              <span class="position">{{ member.position }}</span>
              <p>{{ member.bio }}</p>
              <ul class="team-social">
                <li v-for="(social, sIndex) in member.socials" :key="sIndex">
                  <a :href="social.url" target="_blank" rel="noopener noreferrer"><i :class="social.icon"></i></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const teamMembers = [
  {
    img: '/img/team/team.1.jpg',
    name: 'Dra. María González',
    position: 'Odontóloga General y Estética',
    bio: 'Especialista en odontología general con más de 10 años de experiencia. Certificada en odontología estética y blanqueamientos dentales. Su pasión es ayudar a cada paciente a lograr la sonrisa de sus sueños con tratamientos personalizados y de alta calidad.',
    delay: '.2s',
    socials: [
      { url: 'https://www.facebook.com/dra.mariagonzalez', icon: 'lni lni-facebook-filled' },
      { url: 'https://twitter.com/dra_mariag', icon: 'lni lni-twitter-filled' },
      { url: 'https://www.instagram.com/dra.mariagonzalez', icon: 'lni lni-instagram-filled' },
      { url: 'https://www.linkedin.com/in/maria-gonzalez-dds', icon: 'lni lni-linkedin-original' }
    ]
  },
  {
    img: '/img/team/team.2.jpg',
    name: 'Dr. Carlos Méndez',
    position: 'Ortodoncista Especializado',
    bio: 'Especialista en ortodoncia con certificación internacional. Experto en brackets, Invisalign y ortodoncia digital. Con más de 8 años de experiencia transformando sonrisas y mejorando la salud bucal de sus pacientes mediante tratamientos ortodónticos innovadores.',
    delay: '.4s',
    socials: [
      { url: 'https://www.facebook.com/dr.carlosmendez', icon: 'lni lni-facebook-filled' },
      { url: 'https://twitter.com/dr_carlosm', icon: 'lni lni-twitter-filled' },
      { url: 'https://www.instagram.com/dr.carlosmendez', icon: 'lni lni-instagram-filled' },
      { url: 'https://www.linkedin.com/in/carlos-mendez-ortho', icon: 'lni lni-linkedin-original' }
    ]
  },
  {
    img: '/img/team/team.3.jpg',
    name: 'Dr. Andrés Ruiz',
    position: 'Endodoncista y Cirujano Dental',
    bio: 'Especialista en endodoncia y cirugía dental con amplia experiencia en tratamientos de conductos e implantes dentales. Comprometido con ofrecer procedimientos mínimamente invasivos y resultados excepcionales utilizando la tecnología más avanzada disponible.',
    delay: '.6s',
    socials: [
      { url: 'https://www.facebook.com/dr.andresruiz', icon: 'lni lni-facebook-filled' },
      { url: 'https://twitter.com/dr_andresruiz', icon: 'lni lni-twitter-filled' },
      { url: 'https://www.instagram.com/dr.andresruiz', icon: 'lni lni-instagram-filled' },
      { url: 'https://www.linkedin.com/in/andres-ruiz-endo', icon: 'lni lni-linkedin-original' }
    ]
  }
]
</script>
