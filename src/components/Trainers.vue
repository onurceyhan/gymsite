<template>
  <section id="trainers" class="trainers">
    <div class="container">
      <div class="section-header fade-in-up">
        <h2 class="section-title">Meet Our Trainers</h2>
        <p class="section-subtitle">Expert coaches dedicated to your success</p>
      </div>

      <div class="trainers-grid">
        <div class="trainer-card fade-in-up" style="animation-delay: 0.1s">
          <div class="trainer-image">
            <img src="https://images.unsplash.com/photo-1567013127542-490d757e51fc?w=600&q=80" alt="Coach Marcus" />
            <div class="trainer-overlay">
              <div class="social-links">
                <a href="#" aria-label="Instagram">📷</a>
                <a href="#" aria-label="Twitter">🐦</a>
              </div>
            </div>
          </div>
          <div class="trainer-info">
            <h3 class="trainer-name">Marcus Steel</h3>
            <p class="trainer-specialty">Strength & Conditioning</p>
            <p class="trainer-bio">10+ years experience in powerlifting and bodybuilding</p>
          </div>
        </div>

        <div class="trainer-card fade-in-up" style="animation-delay: 0.2s">
          <div class="trainer-image">
            <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=600&q=80" alt="Coach Sarah" />
            <div class="trainer-overlay">
              <div class="social-links">
                <a href="#" aria-label="Instagram">📷</a>
                <a href="#" aria-label="Twitter">🐦</a>
              </div>
            </div>
          </div>
          <div class="trainer-info">
            <h3 class="trainer-name">Sarah Phoenix</h3>
            <p class="trainer-specialty">HIIT & CrossFit</p>
            <p class="trainer-bio">CrossFit Level 3 trainer with athletic background</p>
          </div>
        </div>

        <div class="trainer-card fade-in-up" style="animation-delay: 0.3s">
          <div class="trainer-image">
            <img src="https://images.unsplash.com/photo-1622782914767-404fb9ab3f57?w=600&q=80" alt="Coach Alex" />
            <div class="trainer-overlay">
              <div class="social-links">
                <a href="#" aria-label="Instagram">📷</a>
                <a href="#" aria-label="Twitter">🐦</a>
              </div>
            </div>
          </div>
          <div class="trainer-info">
            <h3 class="trainer-name">Alex Thunder</h3>
            <p class="trainer-specialty">Boxing & MMA</p>
            <p class="trainer-bio">Former professional fighter and certified boxing coach</p>
          </div>
        </div>

        <div class="trainer-card fade-in-up" style="animation-delay: 0.4s">
          <div class="trainer-image">
            <img src="https://images.unsplash.com/photo-1594381898411-846e7d193883?w=600&q=80" alt="Coach Mia" />
            <div class="trainer-overlay">
              <div class="social-links">
                <a href="#" aria-label="Instagram">📷</a>
                <a href="#" aria-label="Twitter">🐦</a>
              </div>
            </div>
          </div>
          <div class="trainer-info">
            <h3 class="trainer-name">Mia Zen</h3>
            <p class="trainer-specialty">Yoga & Wellness</p>
            <p class="trainer-bio">Certified yoga instructor specializing in mindfulness</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.trainers {
  padding: 8rem 0;
  background: linear-gradient(180deg, var(--mid-purple) 0%, var(--dark-purple) 100%);
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

.trainers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2.5rem;
  max-width: 1200px;
  margin: 0 auto;
}

.trainer-card {
  background: rgba(45, 27, 78, 0.5);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(200, 255, 0, 0.2);
  overflow: hidden;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 30px) 0, 100% 30px, 100% 100%, 0 100%);
}

.trainer-card:hover {
  transform: translateY(-10px);
  border-color: var(--neon-green);
  box-shadow: 0 10px 40px rgba(200, 255, 0, 0.3);
}

.trainer-image {
  position: relative;
  width: 100%;
  height: 350px;
  overflow: hidden;
}

.trainer-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.trainer-card:hover .trainer-image img {
  transform: scale(1.1);
}

.trainer-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, transparent 0%, rgba(26, 15, 46, 0.9) 100%);
  display: flex;
  align-items: flex-end;
  justify-content: center;
  padding: 2rem;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.trainer-card:hover .trainer-overlay {
  opacity: 1;
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
}

.trainer-info {
  padding: 2rem;
  text-align: center;
}

.trainer-name {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.8rem;
  font-weight: 400;
  color: var(--neon-green);
  margin-bottom: 0.5rem;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.trainer-specialty {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.1rem;
  color: var(--text-light);
  margin-bottom: 1rem;
  font-weight: 400;
  opacity: 0.9;
  letter-spacing: 1px;
}

.trainer-bio {
  font-size: 0.95rem;
  color: var(--text-light);
  opacity: 0.7;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .trainers-grid {
    grid-template-columns: 1fr;
    max-width: 400px;
    margin: 0 auto;
  }
}
</style>

