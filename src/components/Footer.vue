<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <div class="logo">
            <span class="logo-text" data-text="XEON">XEON</span>
          </div>
          <p class="footer-description">
            Transform your body, transform your life. Join the ultimate fitness revolution.
          </p>
          <div class="social-links">
            <a href="https://linkedin.com/in/onur.ceyhan" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">💼</a>
            <a href="https://github.com/onurceyhan" target="_blank" rel="noopener noreferrer" aria-label="GitHub">💻</a>
            <a href="#" aria-label="Instagram">📷</a>
            <a href="#" aria-label="Facebook">📘</a>
          </div>
        </div>

        <div class="footer-section">
          <h3>Quick Links</h3>
          <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#classes">Classes</a></li>
            <li><a href="#trainers">Trainers</a></li>
            <li><a href="#pricing">Pricing</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h3>Programs</h3>
          <ul>
            <li><a href="#classes">Strength Training</a></li>
            <li><a href="#classes">Cardio Blast</a></li>
            <li><a href="#classes">HIIT Training</a></li>
            <li><a href="#classes">CrossFit</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h3>Contact</h3>
          <ul class="contact-list">
            <li>📍 123 Fitness Street, Gym City</li>
            <li>📞 +1 (555) 123-4567</li>
            <li>✉️ info@xeongym.com</li>
            <li>⏰ Mon-Fri: 6AM - 10PM</li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <p>&copy; {{ currentYear }} XEON Gym. All rights reserved.</p>
        <p class="developer-credit">
          Designed & Developed by 
          <a href="https://github.com/onurceyhan" target="_blank" rel="noopener noreferrer">Onur Ceyhan</a>
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.footer {
  background: linear-gradient(180deg, var(--dark-purple) 0%, #0d0518 100%);
  padding: 4rem 0 2rem;
  position: relative;
  border-top: 1px solid rgba(200, 255, 0, 0.2);
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-section h3 {
  font-family: 'Bebas Neue', sans-serif;
  color: var(--neon-green);
  font-size: 1.5rem;
  font-weight: 400;
  margin-bottom: 1.5rem;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.logo-text {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.5rem;
  font-weight: 400;
  letter-spacing: 3px;
  color: var(--neon-green);
  font-style: italic;
  transform: skewX(-10deg);
  display: inline-block;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 0px rgba(0, 0, 0, 0.5);
}

.footer-description {
  color: var(--text-light);
  opacity: 0.8;
  line-height: 1.8;
  margin-bottom: 1.5rem;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-links a {
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(200, 255, 0, 0.1);
  border: 2px solid var(--neon-green);
  font-size: 1.5rem;
  text-decoration: none;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 0 100%);
}

.social-links a:hover {
  background: var(--neon-green);
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(200, 255, 0, 0.4);
}

.footer-section ul {
  list-style: none;
}

.footer-section ul li {
  margin-bottom: 0.8rem;
}

.footer-section ul li a {
  color: var(--text-light);
  text-decoration: none;
  opacity: 0.8;
  transition: all 0.3s ease;
  display: inline-block;
}

.footer-section ul li a:hover {
  color: var(--neon-green);
  transform: translateX(5px);
}

.contact-list li {
  color: var(--text-light);
  opacity: 0.8;
  line-height: 1.8;
}

.footer-bottom {
  padding-top: 2rem;
  border-top: 1px solid rgba(200, 255, 0, 0.1);
  text-align: center;
  color: var(--text-light);
  opacity: 0.8;
}

.footer-bottom p {
  margin: 0.5rem 0;
}

.developer-credit {
  font-size: 0.95rem;
}

.developer-credit a {
  color: var(--neon-green);
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
}

.developer-credit a:hover {
  text-shadow: 0 0 10px var(--neon-green);
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .social-links {
    justify-content: center;
  }

  .footer-section ul li a:hover {
    transform: none;
  }
}
</style>

