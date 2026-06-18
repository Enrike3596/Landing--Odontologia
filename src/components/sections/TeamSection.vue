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
                  <a :href="social.url" target="_blank" rel="noopener noreferrer" :title="social.label"><i :class="social.icon"></i></a>
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
      { url: 'https://www.facebook.com/dra.mariagonzalez', icon: 'lni lni-facebook-filled', label: 'Facebook' },
      { url: 'https://twitter.com/dra_mariag', icon: 'lni lni-twitter-filled', label: 'Twitter' },
      { url: 'https://www.instagram.com/dra.mariagonzalez', icon: 'lni lni-instagram-filled', label: 'Instagram' },
      { url: 'https://www.linkedin.com/in/maria-gonzalez-dds', icon: 'lni lni-linkedin-original', label: 'LinkedIn' }
    ]
  },
  {
    img: '/img/team/team.2.jpg',
    name: 'Dr. Carlos Méndez',
    position: 'Ortodoncista Especializado',
    bio: 'Especialista en ortodoncia con certificación internacional. Experto en brackets, Invisalign y ortodoncia digital. Con más de 8 años de experiencia transformando sonrisas y mejorando la salud bucal de sus pacientes mediante tratamientos ortodónticos innovadores.',
    delay: '.4s',
    socials: [
      { url: 'https://www.facebook.com/dr.carlosmendez', icon: 'lni lni-facebook-filled', label: 'Facebook' },
      { url: 'https://twitter.com/dr_carlosm', icon: 'lni lni-twitter-filled', label: 'Twitter' },
      { url: 'https://www.instagram.com/dr.carlosmendez', icon: 'lni lni-instagram-filled', label: 'Instagram' },
      { url: 'https://www.linkedin.com/in/carlos-mendez-ortho', icon: 'lni lni-linkedin-original', label: 'LinkedIn' }
    ]
  },
  {
    img: '/img/team/team.3.jpg',
    name: 'Dr. Andrés Ruiz',
    position: 'Endodoncista y Cirujano Dental',
    bio: 'Especialista en endodoncia y cirugía dental con amplia experiencia en tratamientos de conductos e implantes dentales. Comprometido con ofrecer procedimientos mínimamente invasivos y resultados excepcionales utilizando la tecnología más avanzada disponible.',
    delay: '.6s',
    socials: [
      { url: 'https://www.facebook.com/dr.andresruiz', icon: 'lni lni-facebook-filled', label: 'Facebook' },
      { url: 'https://twitter.com/dr_andresruiz', icon: 'lni lni-twitter-filled', label: 'Twitter' },
      { url: 'https://www.instagram.com/dr.andresruiz', icon: 'lni lni-instagram-filled', label: 'Instagram' },
      { url: 'https://www.linkedin.com/in/andres-ruiz-endo', icon: 'lni lni-linkedin-original', label: 'LinkedIn' }
    ]
  }
]
</script>

<style scoped>
.team-box {
  background: #fff;
  border-radius: 16px;
  padding: 2rem 1.5rem 1.5rem;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 100%;
}

.team-box:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
}

.team-img {
  width: 140px;
  height: 140px;
  margin: 0 auto 1.25rem;
  border-radius: 50%;
  overflow: hidden;
  border: 4px solid #00adb5;
}

.team-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.team-content h4 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #222;
  margin-bottom: 0.3rem;
}

.team-content .position {
  font-size: 0.85rem;
  color: #00adb5;
  font-weight: 600;
  display: block;
  margin-bottom: 0.75rem;
}

.team-content p {
  font-size: 0.88rem;
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.25rem;
}

.team-social {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  gap: 0.5rem;
}

.team-social li {
  margin: 0;
}

.team-social li a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 38px;
  height: 38px;
  border-radius: 50%;
  background: #f5f7fa;
  color: #555;
  font-size: 1rem;
  transition: all 0.3s ease;
  text-decoration: none;
}

.team-social li a:hover {
  background: #00adb5;
  color: #fff;
  transform: translateY(-2px);
}
</style>
