<template>
  <section id="pricing" class="pricing">
    <div class="container">
      <div class="section-header fade-in-up">
        <h2 class="section-title">Choose Your Plan</h2>
        <p class="section-subtitle">Select the perfect membership for your fitness journey</p>
      </div>

      <div class="pricing-cards">
        <div class="pricing-card fade-in-up" style="animation-delay: 0.1s">
          <h3 class="plan-name">Basic Plan</h3>
          <div class="price-tag">
            <span class="currency">$</span>
            <span class="amount">49</span>
            <span class="period">/month</span>
          </div>
          <ul class="features">
            <li>✓ Access to Gym Equipment</li>
            <li>✓ Personal Training Sessions</li>
            <li>✓ Personal Traidance</li>
            <li>✓ Nutrition Guidance</li>
            <li>✓ Paralleled Chitoring Sevling</li>
          </ul>
          <button class="btn btn-outline">Choose Plan</button>
        </div>

        <div class="pricing-card featured fade-in-up" style="animation-delay: 0.2s">
          <div class="featured-badge">Most Popular</div>
          <h3 class="plan-name">Premium Plan</h3>
          <div class="price-tag">
            <span class="currency">$</span>
            <span class="amount">99</span>
            <span class="period">/month</span>
          </div>
          <ul class="features">
            <li>✓ Access to Gym Equipment</li>
            <li>✓ Personal Training Sessions</li>
            <li>✓ Personal Traidance</li>
            <li>✓ Nutrition Guidance</li>
            <li>✓ Group Classes Access</li>
          </ul>
          <button class="btn btn-primary">Sign Up Now</button>
        </div>

        <div class="pricing-card fade-in-up" style="animation-delay: 0.3s">
          <h3 class="plan-name">Elite Plan</h3>
          <div class="price-tag">
            <span class="currency">$</span>
            <span class="amount">149</span>
            <span class="period">/month</span>
          </div>
          <ul class="features">
            <li>✓ Access to Gym Equipment</li>
            <li>✓ Personal Training Sessions</li>
            <li>✓ Nutrition Guidance</li>
            <li>✓ Nutrition Guidance</li>
            <li>✓ Paralleled Chitoring Sevling</li>
          </ul>
          <button class="btn btn-outline">Choose Plan</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.pricing {
  padding: 8rem 0;
  background: linear-gradient(180deg, var(--dark-purple) 0%, var(--mid-purple) 50%, var(--dark-purple) 100%);
  position: relative;
  overflow: hidden;
}

.pricing::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--neon-green), transparent);
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

.pricing-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.pricing-card {
  background: rgba(45, 27, 78, 0.5);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(200, 255, 0, 0.2);
  padding: 3rem 2rem;
  position: relative;
  transition: all 0.3s ease;
  clip-path: polygon(0 0, calc(100% - 30px) 0, 100% 30px, 100% 100%, 0 100%);
}

.pricing-card:hover {
  transform: translateY(-10px);
  border-color: var(--neon-green);
  box-shadow: 0 10px 40px rgba(200, 255, 0, 0.3);
}

.pricing-card.featured {
  background: rgba(45, 27, 78, 0.8);
  border-color: var(--neon-green);
  transform: scale(1.05);
}

.pricing-card.featured:hover {
  transform: scale(1.05) translateY(-10px);
}

.featured-badge {
  position: absolute;
  top: 20px;
  right: 20px;
  background: var(--neon-green);
  color: var(--text-dark);
  padding: 0.5rem 1rem;
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 0 100%);
}

.plan-name {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2rem;
  font-weight: 400;
  color: var(--text-light);
  margin-bottom: 1.5rem;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.price-tag {
  margin-bottom: 2rem;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  gap: 0.3rem;
}

.currency {
  font-size: 2rem;
  color: var(--neon-green);
  font-weight: 700;
  margin-top: 0.5rem;
}

.amount {
  font-size: 4rem;
  font-weight: 900;
  color: var(--neon-green);
  line-height: 1;
}

.period {
  font-size: 1.2rem;
  color: var(--text-light);
  opacity: 0.7;
  align-self: flex-end;
  margin-bottom: 0.8rem;
}

.features {
  list-style: none;
  margin-bottom: 2.5rem;
  text-align: left;
}

.features li {
  padding: 0.8rem 0;
  color: var(--text-light);
  font-size: 1rem;
  border-bottom: 1px solid rgba(200, 255, 0, 0.1);
}

.features li:last-child {
  border-bottom: none;
}

.pricing-card .btn {
  width: 100%;
}

@media (max-width: 968px) {
  .pricing-cards {
    grid-template-columns: 1fr;
    max-width: 400px;
  }

  .pricing-card.featured {
    transform: scale(1);
  }

  .pricing-card.featured:hover {
    transform: translateY(-10px);
  }
}
</style>

