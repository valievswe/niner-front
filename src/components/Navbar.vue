<template>
  <header class="navbar">
    <div class="nav-container">
      <router-link to="/" class="logo">niner</router-link>

      <!-- Hamburger Icon with accessibility improvements -->
      <button
        class="hamburger"
        @click="toggleMenu"
        aria-label="Toggle navigation menu"
        :aria-expanded="isOpen"
      >
        <span :class="{ open: isOpen }"></span>
        <span :class="{ open: isOpen }"></span>
        <span :class="{ open: isOpen }"></span>
      </button>

      <!-- Navigation Links -->
      <nav :class="['nav-links', { open: isOpen }]">
        <div class="nav-links-items">
          <router-link
            to="/"
            exact-active-class="active-link"
            @click="closeMenuIfMobile"
            >Home</router-link
          >
          <router-link
            to="/about"
            exact-active-class="active-link"
            @click="closeMenuIfMobile"
            >About</router-link
          >
          <router-link
            to="/contact"
            exact-active-class="active-link"
            @click="closeMenuIfMobile"
            >Contact</router-link
          >
        </div>

        <!-- Right side buttons -->
        <div class="action-buttons">
          <rpl_btn
            to="/login"
            class="rpl-btn-login"
            delay="100"
            @click="closeMenuIfMobile"
            >Login</rpl_btn
          >
          <rpl_btn
            to="/register"
            class="rpl-btn-register"
            delay="150"
            @click="closeMenuIfMobile"
            >Register
          </rpl_btn>
        </div>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import rpl_btn from "@/components/rpl_btn.vue";

const isOpen = ref(false);

// Toggle menu for mobile view
const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};

// Close menu when clicking links on mobile
const closeMenuIfMobile = () => {
  if (window.innerWidth <= 768) {
    isOpen.value = false;
  }
};

// Handle window resize
const handleResize = () => {
  if (window.innerWidth > 768 && isOpen.value) {
    isOpen.value = false;
  }
};

// Setup event listeners
onMounted(() => {
  window.addEventListener("resize", handleResize);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", handleResize);
});
</script>

<style scoped>
/* Reset and base styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  height: 100%;
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

/* Navbar styles */
.navbar {
  background-color: #ffffff;
  color: #000;
  padding: 1rem 2rem;
  position: sticky;
  top: 0;
  z-index: 10000000;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.05);
  font-family: "Raleway", sans-serif;
  width: 100%;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: auto;
}

.logo {
  font-weight: bold;
  font-size: 1.8rem;
  color: #000;
  text-decoration: none;
}

/* Navigation Links */
.nav-links {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.nav-links-items {
  width: 100%;
  display: flex;
  gap: 2.5rem;
  align-items: center;
  margin: 0 auto;
}

.nav-links a {
  font-size: 1rem;
  text-decoration: none;
  color: #000;
  font-weight: 500;
  padding: 5px 10px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.nav-links a:hover {
  background: #c5c5c544;
}

.active-link {
  text-decoration: underline;
  text-underline-offset: 4px;
}

/* Buttons container */
.action-buttons {
  display: flex;
  gap: 8px;
  margin-left: 2rem;
}

.rpl-btn-login {
  font-size: 16px;
  font-weight: 500;
  background-color: rgba(216, 216, 216, 0.7);
  border-radius: 5px;
  color: #000000;
}

.rpl-btn-login:hover {
  background-color: rgba(203, 203, 203, 0.9);
  transition: all ease 0.5s;
}

.rpl-btn-register {
  font-size: 16px;
  font-weight: 500;
  background-color: rgb(21, 21, 21);
  border-radius: 5px;
  color: #ffffff;
}

.rpl-btn-register:hover {
  background-color: rgb(37, 37, 37);
  transition: all ease 0.5s;
}

/* Hamburger for mobile */
.hamburger {
  display: none;
  flex-direction: column;
  gap: 4px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 8px;
}

.hamburger span {
  height: 3px;
  width: 24px;
  background: #000;
  border-radius: 2px;
  transition: 0.3s;
}

.hamburger span.open:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.hamburger span.open:nth-child(2) {
  opacity: 0;
}

.hamburger span.open:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
}

/* Responsive */
@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-links {
    position: absolute;
    top: 70px;
    left: 0;
    right: 0;
    background: white;
    flex-direction: column;
    align-items: flex-start;
    padding: 1rem 2rem;
    gap: 1rem;
    transform: scaleY(0);
    transform-origin: top;
    transition: transform 0.3s ease;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .nav-links.open {
    transform: scaleY(1);
  }

  .nav-links-items {
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
    gap: 1rem;
  }

  .action-buttons {
    flex-direction: column;
    width: 100%;
    margin-left: 0;
    gap: 0.5rem;
  }
}
</style>
