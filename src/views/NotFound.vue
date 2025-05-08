<template>
  <section class="error-page">
    <div class="error-container">
      <div class="error-content">
        <div class="error-code">404</div>
        <div class="accent-line"></div>
        <h1>Page Not Found</h1>
        <p>The page you are looking for doesn't exist or has been moved.</p>

        <div class="error-suggestions">
          <h3>You might want to:</h3>
          <ul>
            <li>
              <i class="fas fa-home"></i>
              <span
                >Return to the
                <router-link to="/" @click="createRipple"
                  >homepage</router-link
                ></span
              >
            </li>
            <li>
              <i class="fas fa-search"></i>
              <span>Check the URL for typing errors</span>
            </li>
            <li>
              <i class="fas fa-book"></i>
              <span
                >Explore our
                <router-link to="/resources" @click="createRipple"
                  >IELTS resources</router-link
                ></span
              >
            </li>
            <li>
              <i class="fas fa-envelope"></i>
              <span
                ><router-link to="/contact" @click="createRipple"
                  >Contact us</router-link
                >
                for assistance</span
              >
            </li>
          </ul>
        </div>

        <div class="error-illustration">
          <div class="illustration-container">
            <div class="search-icon">
              <i class="fas fa-search"></i>
            </div>
            <div class="question-marks">
              <span>?</span>
              <span>?</span>
              <span>?</span>
            </div>
          </div>
        </div>

        <div class="error-cta">
          <router-link to="/" class="btn" @click="createRipple">
            Back to Home
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
function createRipple(event) {
  const button = event.currentTarget;

  // Remove any existing ripple elements (if necessary)
  const existingRipple = button.querySelector(".ripple");
  if (existingRipple) {
    existingRipple.remove();
  }

  // Create a new ripple element
  const ripple = document.createElement("span");
  ripple.classList.add("ripple");

  // Append the ripple to the button
  button.appendChild(ripple);

  // Set position of ripple
  const diameter = Math.max(button.clientWidth, button.clientHeight);
  const radius = diameter / 2;

  const rect = button.getBoundingClientRect();
  const x = event.clientX - rect.left - radius;
  const y = event.clientY - rect.top - radius;

  ripple.style.width = ripple.style.height = `${diameter}px`;
  ripple.style.left = `${x}px`;
  ripple.style.top = `${y}px`;

  // Add active class to trigger animation
  ripple.classList.add("active");

  // Remove the ripple element after animation completes
  setTimeout(() => {
    ripple.remove();
  }, 600);
}
</script>

<style scoped>
@import "../assets/base.css";
:root {
  --section-color: #dfdfdfb0;

  --button-color: #000000;
  --button-text-color: #ffffff;
  --text-color: #000000;
  --accent-color: #000000;
  --error-number-color: #f2f2f2;
}

.error-page {
  background-color: #fff;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: "Raleway", sans-serif;
  padding: 2rem 0;
}

.error-container {
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
  padding: 0 2rem;
}

.error-content {
  text-align: center;
  position: relative;
}

.error-code {
  font-size: 12rem;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 0.5rem;
  color: var(--error-number-color);
  text-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);
  letter-spacing: -0.05em;
}

.accent-line {
  height: 4px;
  width: 80px;
  background-color: var(--accent-color);
  margin: 1.5rem auto;
}

.error-content h1 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  color: var(--text-color);
}

.error-content p {
  font-size: 1.2rem;
  line-height: 1.7;
  color: var(--text-color);
  margin-bottom: 2.5rem;
}

.error-suggestions {
  background-color: var(--section-color);
  border-radius: 10px;
  padding: 2rem;
  margin-bottom: 3rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.error-suggestions h3 {
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  color: var(--text-color);
}

.error-suggestions ul {
  list-style: none;
  padding: 0;
  text-align: left;
}

.error-suggestions li {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
  line-height: 1.5;
}

.error-suggestions li:last-child {
  margin-bottom: 0;
}

.error-suggestions i {
  color: var(--accent-color);
  margin-right: 1rem;
  font-size: 1.2rem;
  width: 20px;
  text-align: center;
}

.error-suggestions a {
  color: var(--accent-color);
  font-weight: 600;
  text-decoration: none;
  position: relative;
  transition: color 0.2s ease;
}

.error-suggestions a:hover {
  text-decoration: underline;
}

.error-illustration {
  margin: 3rem 0;
}

.illustration-container {
  position: relative;
  height: 150px;
  width: 150px;
  margin: 0 auto;
}

.search-icon {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  font-size: 5rem;
  color: var(--section-color);
  opacity: 0.8;
}

.question-marks {
  position: absolute;
  width: 100%;
  height: 100%;
  animation: float 3s ease-in-out infinite;
}

.question-marks span {
  position: absolute;
  color: var(--accent-color);
  font-size: 2rem;
  font-weight: 700;
  opacity: 0.7;
}

.question-marks span:nth-child(1) {
  top: 20%;
  left: 0;
  animation: bounce 2s ease-in-out infinite;
}

.question-marks span:nth-child(2) {
  top: 10%;
  right: 20%;
  animation: bounce 2.3s ease-in-out infinite;
  animation-delay: 0.3s;
}

.question-marks span:nth-child(3) {
  bottom: 20%;
  right: 0;
  animation: bounce 1.7s ease-in-out infinite;
  animation-delay: 0.7s;
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes bounce {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-15px);
  }
}

.error-cta {
  margin-top: 2rem;
}

.btn {
  position: relative;
  background-color: var(--button-color);
  border: none;
  outline: none;
  color: var(--button-text-color);
  padding: 12px 36px;
  border-radius: 10px;
  text-decoration: none;
  font-family: "Raleway", sans-serif;
  font-size: 16px;
  font-weight: 500;
  cursor: pointer;
  overflow: hidden;
  transition: transform 0.3s ease;
  display: inline-block;
}

.btn:hover {
  transform: translateY(-3px);
}

/* Ripple effect */
.ripple {
  position: absolute;
  background-color: rgba(255, 255, 255, 0.7);
  border-radius: 50%;
  transform: scale(0);
  animation: ripple 0.6s linear;
  pointer-events: none;
}

@keyframes ripple {
  to {
    transform: scale(4);
    opacity: 0;
  }
}

.ripple.active {
  transform: scale(0);
  opacity: 1;
}

/* Responsive styles */
@media (max-width: 768px) {
  .error-code {
    font-size: 8rem;
  }

  .error-content h1 {
    font-size: 2rem;
  }

  .error-content p {
    font-size: 1.1rem;
  }

  .error-suggestions {
    padding: 1.5rem;
  }
}
</style>
