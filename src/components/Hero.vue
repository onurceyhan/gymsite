<template>
  <section id="home" class="hero">
    <div class="hero-background">
      <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=1920&q=80" alt="Gym Background" class="hero-img" />
      <div class="overlay"></div>
      <div class="noise"></div>
    </div>

    <div class="container hero-content">
      <div class="hero-text fade-in-up">
        <h1 class="hero-title" data-text="Transform Your Body">
          Transform <br/>Your Body
        </h1>
        <p class="hero-subtitle">
          Push your limits. Break your records. Become unstoppable.
        </p>
        <div class="hero-buttons">
          <a href="#pricing" class="btn btn-primary">Get Started</a>
          <a href="#classes" class="btn btn-outline">Explore Classes</a>
        </div>
      </div>
    </div>

    <div class="scroll-indicator">
      <div class="mouse">
        <div class="wheel"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  position: relative;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.hero-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.4);
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, 
    rgba(26, 15, 46, 0.9) 0%, 
    rgba(45, 27, 78, 0.7) 50%, 
    rgba(26, 15, 46, 0.9) 100%);
}

.noise {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 400 400' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.05'/%3E%3C/svg%3E");
  animation: grain 0.5s steps(10) infinite;
  opacity: 0.3;
}

@keyframes grain {
  0%, 100% { transform: translate(0, 0); }
  10% { transform: translate(-5%, -10%); }
  20% { transform: translate(-15%, 5%); }
  30% { transform: translate(7%, -25%); }
  40% { transform: translate(-5%, 25%); }
  50% { transform: translate(-15%, 10%); }
  60% { transform: translate(15%, 0%); }
  70% { transform: translate(0%, 15%); }
  80% { transform: translate(3%, 35%); }
  90% { transform: translate(-10%, 10%); }
}

.hero-content {
  position: relative;
  z-index: 1;
  text-align: center;
}

.hero-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(3rem, 10vw, 8rem);
  font-weight: 400;
  line-height: 0.9;
  color: var(--neon-green);
  margin-bottom: 1.5rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  text-shadow: 
    3px 3px 0px rgba(0, 0, 0, 0.8),
    6px 6px 0px rgba(0, 0, 0, 0.4),
    0 0 20px rgba(200, 255, 0, 0.3);
}

.hero-subtitle {
  font-size: clamp(1rem, 2.5vw, 1.5rem);
  color: var(--text-light);
  margin-bottom: 3rem;
  font-weight: 400;
  letter-spacing: 1px;
}

.hero-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
}

.scroll-indicator {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1;
}

.mouse {
  width: 26px;
  height: 40px;
  border: 2px solid var(--neon-green);
  border-radius: 13px;
  position: relative;
  animation: float 2s ease-in-out infinite;
}

.wheel {
  width: 4px;
  height: 8px;
  background: var(--neon-green);
  border-radius: 2px;
  position: absolute;
  top: 8px;
  left: 50%;
  transform: translateX(-50%);
  animation: scroll 1.5s ease-in-out infinite;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes scroll {
  0% {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }
  100% {
    opacity: 0;
    transform: translateX(-50%) translateY(15px);
  }
}

@media (max-width: 768px) {
  .hero-buttons {
    flex-direction: column;
    align-items: center;
  }

  .btn {
    width: 100%;
    max-width: 280px;
  }
}
</style>

