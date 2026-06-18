<template>
  <section id="contact" class="team-section pt-150 pb-150">
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
            <span class="wow fadeInDown" data-wow-delay=".2s">Contacto</span>
            <h2 class="mb-15 wow fadeInUp" data-wow-delay=".4s">Agenda Tu Cita Hoy</h2>
            <p class="wow fadeInUp" data-wow-delay=".6s">Estamos aquí para cuidar tu salud bucal. Contáctanos para agendar una cita o resolver cualquier consulta. Nuestro equipo te brindará la atención personalizada que mereces.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-6 col-md-12">
          <form id="contactForm" class="contact-form" @submit.prevent>
            <div class="row">
              <div class="col-md-6">
                <div class="form-group">
                  <input type="text" class="form-control" id="name" name="name" placeholder="Nombre Completo" required v-model="form.name">
                  <div class="help-block with-errors"></div>
                </div>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <input type="email" class="form-control" id="email" name="email" placeholder="Correo Electrónico" required v-model="form.email">
                  <div class="help-block with-errors"></div>
                </div>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <input type="text" class="form-control" id="phone" name="phone" placeholder="Teléfono" required v-model="form.phone">
                  <div class="help-block with-errors"></div>
                </div>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <select class="form-control" id="subject" name="subject" required v-model="form.subject">
                    <option value="" selected disabled>Selecciona un Servicio</option>
                    <option value="odontologia-general">Odontología General</option>
                    <option value="ortodoncia">Ortodoncia</option>
                    <option value="endodoncia">Endodoncia</option>
                    <option value="periodoncia">Periodoncia</option>
                    <option value="odontologia-estetica">Odontología Estética</option>
                    <option value="cirugia-dental">Cirugía Dental</option>
                    <option value="consulta-general">Consulta General</option>
                    <option value="emergencia">Emergencia Dental</option>
                  </select>
                  <div class="help-block with-errors"></div>
                </div>
              </div>
              <div class="col-md-12">
                <div class="form-group">
                  <textarea class="form-control" id="message" name="message" placeholder="Escribe tu Mensaje" rows="4" required v-model="form.message"></textarea>
                  <div class="help-block with-errors"></div>
                </div>
                <div class="submit-button text-center">
                  <button class="btn theme-btn" id="submit" type="submit">Enviar Mensaje</button>
                  <div id="msgSubmit" class="h3 hidden"></div>
                  <div class="clearfix"></div>
                </div>
              </div>
            </div>
          </form>
        </div>
        <div class="col-lg-6 col-md-12">
          <div class="contact-info-wrapper">
            <div class="contact-info-item mb-30">
              <div class="contact-icon">
                <i class="lni lni-map-marker"></i>
              </div>
              <div class="contact-content">
                <h5>Ubicación</h5>
                <p>Calle 123 #45-67<br>Bogotá, Colombia</p>
              </div>
            </div>
            <div class="contact-info-item mb-30">
              <div class="contact-icon">
                <i class="lni lni-phone"></i>
              </div>
              <div class="contact-content">
                <h5>Teléfono</h5>
                <p>+57 (1) 234-5678<br>+57 301 234 5678</p>
              </div>
            </div>
            <div class="contact-info-item mb-30">
              <div class="contact-icon">
                <i class="lni lni-envelope"></i>
              </div>
              <div class="contact-content">
                <h5>Email</h5>
                <p>info@clinicadental.com<br>citas@clinicadental.com</p>
              </div>
            </div>
            <div class="contact-info-item">
              <div class="contact-icon">
                <i class="lni lni-timer"></i>
              </div>
              <div class="contact-content">
                <h5>Horario de Atención</h5>
                <p>Lunes - Viernes: 8:00 AM - 6:00 PM<br>Sábados: 9:00 AM - 2:00 PM</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  phone: '',
  subject: '',
  message: ''
})
</script>
