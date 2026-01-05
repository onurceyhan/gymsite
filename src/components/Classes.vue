<template>
  <section id="classes" class="classes">
    <div class="container">
      <div class="section-header fade-in-up">
        <h2 class="section-title">Our Classes</h2>
        <p class="section-subtitle">Train with the best programs designed for maximum results</p>
      </div>

      <div class="classes-grid">
        <div class="class-card fade-in-up" style="animation-delay: 0.1s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1571902943202-507ec2618e8f?w=600&q=80" alt="Strength Training" />
            <div class="class-overlay">
              <span class="class-icon">💪</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">Strength Training</h3>
            <p class="class-description">Build muscle and increase your strength with our intensive weightlifting programs.</p>
            <div class="class-meta">
              <span>⏱️ 60 min</span>
              <span>🔥 High Intensity</span>
            </div>
          </div>
        </div>

        <div class="class-card fade-in-up" style="animation-delay: 0.2s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?w=600&q=80" alt="Cardio Blast" />
            <div class="class-overlay">
              <span class="class-icon">🏃</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">Cardio Blast</h3>
            <p class="class-description">Burn calories and improve cardiovascular health with high-energy cardio workouts.</p>
            <div class="class-meta">
              <span>⏱️ 45 min</span>
              <span>🔥 High Intensity</span>
            </div>
          </div>
        </div>

        <div class="class-card fade-in-up" style="animation-delay: 0.3s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1599901860904-17e6ed7083a0?w=600&q=80" alt="Yoga & Flexibility" />
            <div class="class-overlay">
              <span class="class-icon">🧘</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">Yoga & Flexibility</h3>
            <p class="class-description">Enhance flexibility, balance, and mental clarity through guided yoga sessions.</p>
            <div class="class-meta">
              <span>⏱️ 50 min</span>
              <span>🌿 Low Intensity</span>
            </div>
          </div>
        </div>

        <div class="class-card fade-in-up" style="animation-delay: 0.4s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1549060279-7e168fcee0c2?w=600&q=80" alt="HIIT Training" />
            <div class="class-overlay">
              <span class="class-icon">⚡</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">HIIT Training</h3>
            <p class="class-description">Maximize fat loss and boost metabolism with intense interval training.</p>
            <div class="class-meta">
              <span>⏱️ 30 min</span>
              <span>🔥 Extreme</span>
            </div>
          </div>
        </div>

        <div class="class-card fade-in-up" style="animation-delay: 0.5s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?w=600&q=80" alt="CrossFit" />
            <div class="class-overlay">
              <span class="class-icon">🏋️</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">CrossFit</h3>
            <p class="class-description">Challenge yourself with functional movements at high intensity for total fitness.</p>
            <div class="class-meta">
              <span>⏱️ 60 min</span>
              <span>🔥 Extreme</span>
            </div>
          </div>
        </div>

        <div class="class-card fade-in-up" style="animation-delay: 0.6s">
          <div class="class-image">
            <img src="https://images.unsplash.com/photo-1581009146145-b5ef050c2e1e?w=600&q=80" alt="Boxing" />
            <div class="class-overlay">
              <span class="class-icon">🥊</span>
            </div>
          </div>
          <div class="class-content">
            <h3 class="class-title">Boxing</h3>
            <p class="class-description">Develop power, speed, and coordination through boxing techniques and drills.</p>
            <div class="class-meta">
              <span>⏱️ 45 min</span>
              <span>🔥 High Intensity</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.classes {
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

.classes-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 2rem;
}

.class-card {
  background: rgba(45, 27, 78, 0.5);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(200, 255, 0, 0.2);
  overflow: hidden;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 30px) 0, 100% 30px, 100% 100%, 0 100%);
}

.class-card:hover {
  transform: translateY(-10px);
  border-color: var(--neon-green);
  box-shadow: 0 10px 40px rgba(200, 255, 0, 0.3);
}

.class-image {
  position: relative;
  width: 100%;
  height: 250px;
  overflow: hidden;
}

.class-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.class-card:hover .class-image img {
  transform: scale(1.1);
}

.class-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, transparent 0%, rgba(26, 15, 46, 0.8) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
}

.class-icon {
  font-size: 4rem;
  filter: drop-shadow(0 0 10px var(--neon-green));
}

.class-content {
  padding: 2rem;
}

.class-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.8rem;
  font-weight: 400;
  color: var(--neon-green);
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.class-description {
  color: var(--text-light);
  margin-bottom: 1.5rem;
  line-height: 1.6;
  opacity: 0.9;
}

.class-meta {
  display: flex;
  gap: 1.5rem;
  font-size: 0.9rem;
  color: var(--text-light);
  opacity: 0.8;
}

@media (max-width: 768px) {
  .classes-grid {
    grid-template-columns: 1fr;
  }
}
</style>

