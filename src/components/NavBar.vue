<template>
  <nav class="navbar" :class="{ scrolled: isScrolled }">
    <div class="container nav-container">
      <div class="logo">
        <span class="logo-text" data-text="XEON">XEON</span>
      </div>
      
      <div class="nav-links" :class="{ active: menuOpen }">
        <a href="#home" @click="closeMenu">Home</a>
        <a href="#classes" @click="closeMenu">Classes</a>
        <a href="#trainers" @click="closeMenu">Trainers</a>
        <a href="#pricing" @click="closeMenu">Pricing</a>
        <a href="#contact" @click="closeMenu" class="btn btn-outline">Contact</a>
      </div>

      <div class="hamburger" @click="toggleMenu" :class="{ active: menuOpen }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const menuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 1.5rem 0;
  transition: all 0.3s ease;
  background: transparent;
}

.navbar.scrolled {
  background: rgba(26, 15, 46, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 4px 20px rgba(200, 255, 0, 0.1);
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
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
  text-shadow: 2px 2px 0px rgba(0, 0, 0, 0.5);
}

.nav-links {
  display: flex;
  gap: 3rem;
  align-items: center;
}

.nav-links a {
  color: var(--text-light);
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
  position: relative;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.nav-links a:not(.btn):hover {
  color: var(--neon-green);
}

.nav-links a:not(.btn)::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--neon-green);
  transition: width 0.3s ease;
}

.nav-links a:not(.btn):hover::after {
  width: 100%;
}

.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  cursor: pointer;
  z-index: 1001;
}

.hamburger span {
  width: 30px;
  height: 3px;
  background: var(--neon-green);
  transition: all 0.3s ease;
  border-radius: 2px;
}

.hamburger.active span:nth-child(1) {
  transform: rotate(45deg) translate(8px, 8px);
}

.hamburger.active span:nth-child(2) {
  opacity: 0;
}

.hamburger.active span:nth-child(3) {
  transform: rotate(-45deg) translate(8px, -8px);
}

@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-links {
    position: fixed;
    top: 0;
    right: -100%;
    height: 100vh;
    width: 70%;
    max-width: 300px;
    background: rgba(26, 15, 46, 0.98);
    backdrop-filter: blur(10px);
    flex-direction: column;
    justify-content: center;
    transition: right 0.3s ease;
    box-shadow: -5px 0 20px rgba(0, 0, 0, 0.5);
  }

  .nav-links.active {
    right: 0;
  }
}
</style>

