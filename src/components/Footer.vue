<template>
  <footer class="site-footer">
    <div class="footer-container">
      <div class="footer-grid">
        <div class="footer-column brand-column">
          <div class="footer-logo">
            <h2>niner</h2>
            <div class="accent-line"></div>
          </div>
          <p class="brand-description">
            Comprehensive IELTS preparation platform connecting test-takers and
            examiners with powerful tools designed for success.
          </p>
          <div class="social-links">
            <a href="#" class="social-icon" @click.prevent="createRipple">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="#" class="social-icon" @click.prevent="createRipple">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="#" class="social-icon" @click.prevent="createRipple">
              <i class="fab fa-instagram"></i>
            </a>
            <a href="#" class="social-icon" @click.prevent="createRipple">
              <i class="fab fa-linkedin-in"></i>
            </a>
          </div>
        </div>

        <div class="footer-column">
          <h3>Quick Links</h3>
          <ul class="footer-links">
            <li>
              <router-link to="/">Home</router-link>
            </li>
            <li>
              <router-link to="/about">About Us</router-link>
            </li>
            <li>
              <router-link to="/features">Features</router-link>
            </li>
            <li>
              <router-link to="/guide">Quick Guide</router-link>
            </li>
            <li>
              <router-link to="/faq">FAQ</router-link>
            </li>
          </ul>
        </div>

        <div class="footer-column">
          <h3>IELTS Resources</h3>
          <ul class="footer-links">
            <li>
              <router-link to="/resources/writing">Writing Tips</router-link>
            </li>
            <li>
              <router-link to="/resources/reading"
                >Reading Practice</router-link
              >
            </li>
            <li>
              <router-link to="/resources/listening"
                >Listening Strategies</router-link
              >
            </li>
            <li>
              <router-link to="/resources/speaking"
                >Speaking Preparation</router-link
              >
            </li>
            <li>
              <router-link to="/resources/vocabulary"
                >Vocabulary Builder</router-link
              >
            </li>
          </ul>
        </div>

        <div class="footer-column">
          <h3>Contact Us</h3>
          <ul class="contact-info">
            <li>
              <i class="fas fa-envelope"></i>
              <a href="mailto:info@ninertogether.com">info@ninertogether.com</a>
            </li>
            <li>
              <i class="fas fa-phone-alt"></i>
              <span>+1 234 567 8900</span>
            </li>
            <li>
              <i class="fas fa-map-marker-alt"></i>
              <span
                >123 Education Street, Suite 456<br />Learning City, LC
                12345</span
              >
            </li>
          </ul>
        </div>
      </div>

      <div class="newsletter">
        <h3>Subscribe to Our Newsletter</h3>
        <p>Get the latest news and updates about our platform launch.</p>
        <form @submit.prevent="subscribeNewsletter" class="newsletter-form">
          <input
            type="email"
            placeholder="Enter your email address"
            v-model="newsletterEmail"
            required
          />
          <button type="submit" class="btn">Subscribe</button>
        </form>
      </div>

      <div class="footer-bottom">
        <div class="copyright">
          <p>&copy; {{ currentYear }} niner. All rights reserved.</p>
        </div>
        <div class="legal-links">
          <router-link to="/terms">Terms of Service</router-link>
          <router-link to="/privacy">Privacy Policy</router-link>
          <router-link to="/cookies">Cookie Policy</router-link>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref, computed } from "vue";

const newsletterEmail = ref("");
const currentYear = computed(() => new Date().getFullYear());

function subscribeNewsletter() {
  // Here you would typically send the email to your backend
  console.log("Newsletter subscription:", newsletterEmail.value);
  alert("Thanks for subscribing to our newsletter!");
  newsletterEmail.value = "";
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
  --footer-bg: #000000;
  --footer-text: #333333;
  --footer-link: #555555;
  --footer-link-hover: #000000;
  --footer-border: #e0e0e0;
  --footer-bottom-bg: #eeeeee;
}

.site-footer {
  background-color: #181818;
  font-family: "Raleway", sans-serif;
  padding: 5rem 0 0;
  color: #ffffff;
}

.footer-container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
  margin-bottom: 4rem;
}

.footer-column h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  position: relative;
}

.brand-column {
  grid-column: span 1;
}

.footer-logo h2 {
  font-size: 1.8rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.footer-logo .accent-line {
  height: 3px;
  width: 50px;
  background-color: var(--accent-color);
  margin-bottom: 1.5rem;
}

.brand-description {
  line-height: 1.6;
  margin-bottom: 1.5rem;
  color: var(--footer-text);
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: var(--button-color);
  color: var(--button-text-color);
  border-radius: 50%;
  transition: transform 0.3s ease, background-color 0.3s ease;
  text-decoration: none;
  position: relative;
  overflow: hidden;
}

.social-icon:hover {
  transform: translateY(-3px);
}

.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 0.75rem;
}

.footer-links a {
  color: var(--footer-link);
  text-decoration: none;
  transition: color 0.2s ease, padding-left 0.2s ease;
  position: relative;
  display: inline-block;
}

.footer-links a:hover {
  color: #ffffff;
  padding-left: 5px;
}

.contact-info {
  list-style: none;
  padding: 0;
  margin: 0;
}

.contact-info li {
  display: flex;
  align-items: flex-start;
  margin-bottom: 1rem;
}

.contact-info i {
  margin-right: 10px;
  color: var(--accent-color);
  margin-top: 4px;
}

.contact-info a {
  color: var(--footer-link);
  text-decoration: none;
  transition: color 0.2s ease;
}

.contact-info a:hover {
  color: var(--footer-link-hover);
}

.newsletter {
  background-color: #eeeeee;
  padding: 2.5rem;
  border-radius: 10px;
  margin-bottom: 4rem;
  color: #000000;
}

.newsletter h3 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.newsletter p {
  margin-bottom: 1.5rem;
}

.newsletter-form {
  display: flex;
  gap: 1rem;
}

.newsletter-form input {
  flex: 1;
  padding: 0.75rem 1rem;
  border: 1px solid #000000;
  border-radius: 5px;
  font-family: "Raleway", sans-serif;
}

.newsletter-form input:focus {
  outline: none;
  border-color: var(--accent-color);
}

.btn {
  position: relative;
  background-color: #000000;
  border: none;
  outline: none;
  color: #ffffff;
  padding: 0.75rem 1.5rem;
  border-radius: 5px;
  font-family: "Raleway", sans-serif;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.btn:hover {
  transform: translateY(-3px);
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 0;
  border-top: 1px solid var(--footer-border);
  margin-top: 2rem;
  flex-wrap: wrap;
  gap: 1rem;
}

.copyright p {
  margin: 0;
  font-size: 0.9rem;
}

.legal-links {
  display: flex;
  gap: 1.5rem;
}

.legal-links a {
  color: var(--footer-link);
  text-decoration: none;
  font-size: 0.9rem;
  transition: color 0.2s ease;
}

.legal-links a:hover {
  color: var(--footer-link-hover);
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
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .newsletter-form {
    flex-direction: column;
  }

  .footer-bottom {
    flex-direction: column;
    text-align: center;
    gap: 1rem;
  }

  .legal-links {
    justify-content: center;
    flex-wrap: wrap;
  }
}
</style>
