<template>
  <section id="contact" class="contact">
    <div class="container">
      <div class="section-header fade-in-up">
        <h2 class="section-title">Get In Touch</h2>
        <p class="section-subtitle">Ready to start your transformation? Contact us today</p>
      </div>

      <div class="contact-content">
        <div class="contact-info fade-in-up">
          <div class="info-card">
            <div class="info-icon">📍</div>
            <h3>Visit Us</h3>
            <p>123 Fitness Street<br>Gym City, GY 12345</p>
          </div>

          <div class="info-card">
            <div class="info-icon">📞</div>
            <h3>Call Us</h3>
            <p>+1 (555) 123-4567<br>Mon-Fri: 6AM - 10PM</p>
          </div>

          <div class="info-card">
            <div class="info-icon">✉️</div>
            <h3>Email Us</h3>
            <p>info@xeongym.com<br>support@xeongym.com</p>
          </div>

          <div class="info-card">
            <div class="info-icon">⏰</div>
            <h3>Hours</h3>
            <p>Mon-Fri: 6AM - 10PM<br>Sat-Sun: 8AM - 8PM</p>
          </div>
        </div>

        <form class="contact-form fade-in-up" @submit.prevent="handleSubmit">
          <div class="form-group">
            <input type="text" placeholder="Your Name" required v-model="form.name">
          </div>
          <div class="form-group">
            <input type="email" placeholder="Your Email" required v-model="form.email">
          </div>
          <div class="form-group">
            <input type="tel" placeholder="Your Phone" v-model="form.phone">
          </div>
          <div class="form-group">
            <select v-model="form.interest" required>
              <option value="" disabled>Select Your Interest</option>
              <option value="basic">Basic Plan</option>
              <option value="premium">Premium Plan</option>
              <option value="elite">Elite Plan</option>
              <option value="personal">Personal Training</option>
              <option value="other">Other</option>
            </select>
          </div>
          <div class="form-group">
            <textarea placeholder="Your Message" rows="5" v-model="form.message"></textarea>
          </div>
          <button type="submit" class="btn btn-primary">Send Message</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  phone: '',
  interest: '',
  message: ''
})

const handleSubmit = () => {
  alert('Thank you for your message! We will get back to you soon.')
  form.value = {
    name: '',
    email: '',
    phone: '',
    interest: '',
    message: ''
  }
}
</script>

<style scoped>
.contact {
  padding: 8rem 0;
  background: var(--dark-purple);
  position: relative;
}

.section-header {
  text-align: center;
  margin-bottom: 5rem;
}

.section-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 400;
  color: var(--neon-green);
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 3px;
  text-shadow: 2px 2px 0px rgba(0, 0, 0, 0.5);
}

.section-subtitle {
  font-size: 1.2rem;
  color: var(--text-light);
  opacity: 0.8;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.contact-info {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.info-card {
  background: rgba(45, 27, 78, 0.5);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(200, 255, 0, 0.2);
  padding: 2rem;
  text-align: center;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 20px) 0, 100% 20px, 100% 100%, 0 100%);
}

.info-card:hover {
  border-color: var(--neon-green);
  transform: translateY(-5px);
  box-shadow: 0 5px 20px rgba(200, 255, 0, 0.2);
}

.info-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 0 10px var(--neon-green));
}

.info-card h3 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.4rem;
  color: var(--neon-green);
  margin-bottom: 0.5rem;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.info-card p {
  color: var(--text-light);
  opacity: 0.8;
  line-height: 1.8;
}

.contact-form {
  background: rgba(45, 27, 78, 0.5);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(200, 255, 0, 0.2);
  padding: 3rem;
  clip-path: polygon(0 0, calc(100% - 30px) 0, 100% 30px, 100% 100%, 0 100%);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 1rem;
  background: rgba(26, 15, 46, 0.5);
  border: 2px solid rgba(200, 255, 0, 0.2);
  color: var(--text-light);
  font-family: 'Exo 2', sans-serif;
  font-size: 1rem;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 0 100%);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--neon-green);
  box-shadow: 0 0 15px rgba(200, 255, 0, 0.3);
}

.form-group textarea {
  resize: vertical;
}

.contact-form .btn {
  width: 100%;
}

@media (max-width: 968px) {
  .contact-content {
    grid-template-columns: 1fr;
  }

  .contact-info {
    grid-template-columns: 1fr;
  }
}
</style>

