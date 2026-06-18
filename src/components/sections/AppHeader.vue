<template>
  <header id="home" class="header">
    <div class="header-wrapper">
      <div class="header-top theme-bg">
        <div class="container">
          <div class="row">
            <div class="col-md-8">
              <div class="header-top-left text-center text-md-left">
                <ul>
                  <li><a href="tel:+5712345678"><i class="lni lni-phone"></i> +57 (1) 234-5678</a></li>
                  <li><a href="mailto:info@clinicadental.com"><i class="lni lni-envelope"></i> info@clinicadental.com</a></li>
                </ul>
              </div>
            </div>
            <div class="col-md-4">
              <div class="header-top-right d-none d-md-block">
                <ul>
                  <li><a href="https://www.facebook.com/clinicadental" target="_blank" title="Facebook"><i class="lni lni-facebook-filled"></i></a></li>
                  <li><a href="https://www.instagram.com/clinicadental" target="_blank" title="Instagram"><i class="lni lni-instagram-original"></i></a></li>
                  <li><a href="https://wa.me/573012345678" target="_blank" title="WhatsApp"><i class="lni lni-whatsapp"></i></a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="navbar-area" ref="navbarArea">
        <div class="container">
          <div class="row">
            <div class="col-lg-12">
              <nav class="navbar navbar-expand-lg">
                <a class="navbar-brand" href="#home">
                  <img src="/img/logo/logo.svg" alt="Logo">
                </a>
                <button
                  class="navbar-toggler"
                  type="button"
                  :class="{ active: isMenuOpen }"
                  @click="toggleMenu"
                  aria-controls="navbarSupportedContent"
                  aria-expanded="false"
                  aria-label="Toggle navigation"
                >
                  <span class="toggler-icon"></span>
                  <span class="toggler-icon"></span>
                  <span class="toggler-icon"></span>
                </button>
                <div
                  class="collapse navbar-collapse sub-menu-bar"
                  :class="{ show: isMenuOpen }"
                  id="navbarSupportedContent"
                >
                  <ul id="nav" class="navbar-nav ml-auto">
                    <li class="nav-item" :class="{ active: activeSection === 'home' }">
                      <a class="page-scroll" href="#home" @click.prevent="scrollTo('#home')">Inicio</a>
                    </li>
                    <li class="nav-item" :class="{ active: activeSection === 'about' }">
                      <a class="page-scroll" href="#about" @click.prevent="scrollTo('#about')">Acerca de</a>
                    </li>
                    <li class="nav-item" :class="{ active: activeSection === 'services' }">
                      <a class="page-scroll" href="#services" @click.prevent="scrollTo('#services')">Servicios</a>
                    </li>
                    <li class="nav-item" :class="{ active: activeSection === 'team' }">
                      <a class="page-scroll" href="#team" @click.prevent="scrollTo('#team')">Odontólogos</a>
                    </li>
                    <li class="nav-item" :class="{ active: activeSection === 'blog' }">
                      <a class="page-scroll" href="#blog" @click.prevent="scrollTo('#blog')">Blog</a>
                    </li>
                    <li class="nav-item" :class="{ active: activeSection === 'contact' }">
                      <a class="page-scroll" href="#contact" @click.prevent="scrollTo('#contact')">Contacto</a>
                    </li>
                  </ul>
                </div>
              </nav>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="slider-wrapper">
      <section class="slider-section">
        <div class="slider-active slick-style" ref="sliderRef">
          <div class="single-slider img-bg" style="background-image:url('/img/slider/slider-1.jpg');">
            <div class="container">
              <div class="row">
                <div class="col-xl-7 col-lg-8 col-md-10">
                  <div class="slider-content">
                    <h1 data-animation="fadeInDown" data-duration="1.5s" data-delay=".5s">Cuidado Dental Integral</h1>
                    <p data-animation="fadeInLeft" data-duration="1.5s" data-delay=".7s">Brindamos atención dental de calidad con tecnología de vanguardia y un equipo de especialistas comprometidos con tu salud bucal. Tu sonrisa es nuestra prioridad y trabajamos para que tengas una experiencia cómoda y satisfactoria.</p>
                    <a href="#contact" class="btn theme-btn page-scroll" data-animation="fadeInUp" data-duration="1.5s" data-delay=".9s" @click.prevent="scrollTo('#contact')">Conoce Más</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="single-slider img-bg" style="background-image:url('/img/slider/slider-2.jpg');">
            <div class="container">
              <div class="row">
                <div class="col-xl-7 col-lg-8 col-md-10">
                  <div class="slider-content">
                    <h1 data-animation="fadeInDown" data-duration="1.5s" data-delay=".5s">Contamos con los Mejores Especialistas</h1>
                    <p data-animation="fadeInLeft" data-duration="1.5s" data-delay=".7s">Los mejores odontólogos especializados y equipos de última tecnología para garantizar los mejores resultados en todos nuestros tratamientos. Experiencia y calidad al servicio de tu sonrisa.</p>
                    <a href="#contact" class="btn theme-btn page-scroll" data-animation="fadeInUp" data-duration="1.5s" data-delay=".9s" @click.prevent="scrollTo('#contact')">Agendar Cita</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="single-slider img-bg" style="background-image:url('/img/slider/slider-3.jpg');">
            <div class="container">
              <div class="row">
                <div class="col-xl-7 col-lg-8 col-md-10">
                  <div class="slider-content">
                    <h1 data-animation="fadeInDown" data-duration="1.5s" data-delay=".5s">Tu Salud Dental es Nuestra Prioridad</h1>
                    <p data-animation="fadeInLeft" data-duration="1.5s" data-delay=".7s">Nos dedicamos a cuidar tu salud bucal con tratamientos personalizados y preventivos. Nuestro compromiso es brindarte la mejor atención dental en un ambiente cómodo y profesional.</p>
                    <a href="#services" class="btn theme-btn page-scroll" data-animation="fadeInUp" data-duration="1.5s" data-delay=".9s" @click.prevent="scrollTo('#services')">Nuestros Servicios</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { tns } from 'tiny-slider'

const navbarArea = ref(null)
const sliderRef = ref(null)
const isMenuOpen = ref(false)
const activeSection = ref('home')

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value
}

function scrollTo(hash) {
  isMenuOpen.value = false
  const el = document.querySelector(hash)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}

function onScroll() {
  const scrollPos = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop

  if (navbarArea.value) {
    if (window.pageYOffset > navbarArea.value.offsetTop) {
      navbarArea.value.classList.add('sticky')
    } else {
      navbarArea.value.classList.remove('sticky')
    }
  }

  const sections = document.querySelectorAll('.page-scroll')
  sections.forEach((link) => {
    const val = link.getAttribute('href')
    if (val && val.startsWith('#')) {
      const refElement = document.querySelector(val)
      if (refElement) {
        const scrollTopMinus = scrollPos + 73
        if (
          refElement.offsetTop <= scrollTopMinus &&
          refElement.offsetTop + refElement.offsetHeight > scrollTopMinus
        ) {
          activeSection.value = val.replace('#', '')
        }
      }
    }
  })
}

onMounted(() => {
  if (sliderRef.value) {
    tns({
      container: sliderRef.value,
      items: 1,
      slideBy: 'page',
      autoplay: true,
      mouseDrag: true,
      gutter: 0,
      nav: true,
      controls: false,
      autoplayButtonOutput: false,
    })
  }

  window.addEventListener('scroll', onScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
})
</script>
