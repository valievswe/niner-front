<template>
  <!-- What We Offer Section -->
  <section class="offers-section" id="offers">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">
          What We <span class="highlight">Offer</span>
        </h2>
        <div class="title-underline"></div>
        <p class="section-subtitle">
          Comprehensive tools to prepare you for IELTS success
        </p>
      </div>

      <div class="services-wrapper">
        <div class="services-grid">
          <!-- Service 1 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-clipboard-check"></i>
            </div>
            <h3 class="service-title">Full-Length Mock Tests</h3>
            <div class="service-content">
              <p class="service-description">
                Experience authentic IELTS mock exams with precise timing and
                formatting that mirrors the official test. Available for both
                Academic and General Training modules.
              </p>
              <ul class="service-features">
                <li>
                  <i class="fa-solid fa-check"></i> Academic & General Training
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Identical timing conditions
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Up-to-date question formats
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>

          <!-- Service 2 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-robot"></i>
            </div>
            <h3 class="service-title">AI-Powered Scoring</h3>
            <div class="service-content">
              <p class="service-description">
                Receive instant scoring for Reading and Listening, plus detailed
                AI assessment for Writing and Speaking with personalized
                feedback to improve your performance.
              </p>
              <ul class="service-features">
                <li>
                  <i class="fa-solid fa-check"></i> Instant Reading & Listening
                  scores
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Advanced Writing evaluation
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Speaking assessment with
                  feedback
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>

          <!-- Service 3 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-laptop-code"></i>
            </div>
            <h3 class="service-title">Real-Time Practice</h3>
            <div class="service-content">
              <p class="service-description">
                Train with the exact same interface and time constraints as the
                official computer-delivered IELTS exam to eliminate test-day
                surprises.
              </p>
              <ul class="service-features">
                <li>
                  <i class="fa-solid fa-check"></i> Identical user interface
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Real exam time constraints
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Authentic question
                  navigation
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>

          <!-- Service 4 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-book-open"></i>
            </div>
            <h3 class="service-title">Study Materials</h3>
            <div class="service-content">
              <p class="service-description">
                Access our comprehensive library of practice resources,
                vocabulary builders, grammar exercises, and test-taking
                strategies.
              </p>
              <ul class="service-features">
                <li>
                  <i class="fa-solid fa-check"></i> Topic-focused exercises
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Vocabulary expansion tools
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Strategic test-taking guides
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>

          <!-- Service 5 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-comments"></i>
            </div>
            <h3 class="service-title">Expert Feedback</h3>
            <div class="service-content">
              <p class="service-description">
                Get personalized feedback from certified IELTS examiners who
                identify your strengths and weaknesses, providing targeted
                advice to boost your band score.
              </p>
              <ul class="service-features">
                <li><i class="fa-solid fa-check"></i> Examiner-led review</li>
                <li>
                  <i class="fa-solid fa-check"></i> Personalized improvement
                  plans
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Targeted error correction
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>

          <!-- Service 6 -->
          <div class="service-card">
            <div class="service-icon">
              <i class="fa-solid fa-chart-simple"></i>
            </div>
            <h3 class="service-title">Performance Analytics</h3>
            <div class="service-content">
              <p class="service-description">
                Track your progress with detailed analytics showing your
                improvement over time, highlighting strengths, weaknesses, and
                focus areas.
              </p>
              <ul class="service-features">
                <li><i class="fa-solid fa-check"></i> Progress tracking</li>
                <li>
                  <i class="fa-solid fa-check"></i> Detailed performance reports
                </li>
                <li>
                  <i class="fa-solid fa-check"></i> Improvement visualization
                </li>
              </ul>
            </div>
            <div class="service-overlay">
              <span class="learn-more">Learn More</span>
            </div>
          </div>
        </div>
      </div>

      <div class="cta-container">
        <p class="cta-text">
          Ready to experience the most authentic IELTS preparation?
        </p>
        <rpl_btn to="/register" class="cta-button pulse-animation" delay="100"
          >Start Your Journey<i class="fa-solid fa-arrow-right"></i
        ></rpl_btn>
      </div>
    </div>
  </section>
</template>

<script setup>
import rpl_btn from "./rpl_btn.vue";
</script>

<style scoped>
@import "../assets/base.css";
@import "../assets/main.css";
@import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css";

.offers-section {
  padding: 5rem 0;
  background-color: #fff;
  position: relative;
}

.offers-section::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-image: radial-gradient(rgba(0, 0, 0, 0.189) 2px, transparent 2px);
  background-size: 30px 30px;
  z-index: 1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  position: relative;
  z-index: 2;
}

.section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.section-title {
  font-size: 3.2rem;
  font-weight: 600;
  color: #000;
  font-family: "Raleway", sans-serif;
  margin-bottom: 1rem;
}

.highlight {
  position: relative;
  z-index: 1;
}

.highlight::after {
  content: "";
  position: absolute;
  bottom: 5px;
  left: 0;
  width: 100%;
  height: 8px;
  background-color: rgba(0, 0, 0, 0.1);
  z-index: -1;
}

.title-underline {
  width: 80px;
  height: 4px;
  background-color: #000;
  margin: 0 auto;
}

.section-subtitle {
  font-size: 1.4rem;
  color: #555;
  margin-top: 1.5rem;
  font-family: "Raleway", sans-serif;
}

.services-wrapper {
  position: relative;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

.service-card {
  position: relative;
  background-color: #d8d8d8;
  border-radius: 10px;
  padding: 2rem;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
  transition: all 0.4s ease;
  overflow: hidden;
  min-height: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
}

.service-icon {
  width: 70px;
  height: 70px;
  background-color: #000;
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  margin-bottom: 1.2rem;
  transition: all 0.4s ease;
}

.service-title {
  font-size: 1.5rem;
  font-weight: 600;
  text-align: center;
  color: #000;
  font-family: "Raleway", sans-serif;
  transition: all 0.4s ease;
  position: relative;
  z-index: 2;
}

.service-content {
  display: none;
  width: 100%;
  padding: 0 1rem;
}

.service-description {
  font-size: 1rem;
  line-height: 1.5;
  margin-bottom: 1.2rem;
  font-family: "Raleway", sans-serif;
  color: #333;
  text-align: left;
}

.service-features {
  list-style-type: none;
  padding: 0;
  margin: 0;
  text-align: left;
}

.service-features li {
  margin-bottom: 0.7rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-family: "Raleway", sans-serif;
  color: #333;
  font-size: 0.9rem;
}

.service-features li i {
  color: #000;
  font-size: 0.8rem;
}

.service-overlay {
  position: absolute;
  bottom: 1.5rem;
  width: 100%;
  text-align: center;
  transition: all 0.3s ease;
}

.learn-more {
  display: inline-block;
  color: #000;
  font-weight: 500;
  font-family: "Raleway", sans-serif;
  font-size: 1rem;
  position: relative;
}

.learn-more::after {
  content: "";
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: #000;
  transition: width 0.3s ease;
}

.cta-container {
  text-align: center;
  margin-top: 2rem;
  padding: 2.5rem 2rem;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
}

.cta-text {
  font-size: 1.8rem;
  font-weight: 500;
  color: #000;
  margin-bottom: 1.5rem;
  font-family: "Raleway", sans-serif;
}

.cta-button {
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  background-color: #000;
  color: #fff;
  padding: 1rem 2rem;
  border-radius: 5px;
  font-size: 1.2rem;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  font-family: "Raleway", sans-serif;
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

/* Hover effect for desktop */
@media (min-width: 993px) {
  .service-card {
    height: 340px;
  }

  .service-card:hover .service-icon {
    transform: translateY(-50px) scale(0.8);
    opacity: 0;
  }

  .service-card:hover .service-title {
    transform: translateY(-100px);
  }

  .service-card:hover .service-content {
    display: block;
    animation: fadeIn 0.4s forwards;
    position: absolute;
    top: 60%;
    left: 0;
  }

  .service-card:hover .service-overlay {
    opacity: 0;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(-80px);
    }
  }
}

/* Improved responsive styles */
@media (max-width: 1200px) {
  .section-title {
    font-size: 2.8rem;
  }

  .section-subtitle {
    font-size: 1.3rem;
  }

  .services-grid {
    gap: 1.5rem;
  }
}

@media (max-width: 992px) {
  .offers-section {
    padding: 4rem 0;
  }

  .services-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .service-card {
    padding: 1.8rem;
    min-height: auto;
  }

  /* Alternative card behavior for tablets */
  .service-content {
    display: block;
    opacity: 1;
    position: static;
    transform: none;
    margin-top: 1rem;
  }

  .service-icon {
    width: 60px;
    height: 60px;
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .service-title {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    transform: none;
  }

  .service-overlay {
    display: none;
  }
}

@media (max-width: 768px) {
  .offers-section {
    padding: 3rem 0;
  }

  .section-header {
    margin-bottom: 2rem;
  }

  .section-title {
    font-size: 2.4rem;
  }

  .section-subtitle {
    font-size: 1.2rem;
  }

  .service-description {
    font-size: 0.95rem;
  }

  .cta-text {
    font-size: 1.5rem;
  }

  .cta-button {
    padding: 0.9rem 1.8rem;
    font-size: 1.1rem;
  }

  .cta-container {
    padding: 2rem 1.5rem;
  }
}

@media (max-width: 576px) {
  .offers-section {
    padding: 2.5rem 0;
  }

  .services-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .section-title {
    font-size: 2.2rem;
  }

  .section-subtitle {
    font-size: 1.1rem;
    margin-top: 1rem;
  }

  .service-card {
    padding: 1.5rem;
  }

  .service-icon {
    width: 55px;
    height: 55px;
    font-size: 1.4rem;
  }

  .service-title {
    font-size: 1.2rem;
  }

  .service-description {
    font-size: 0.9rem;
    margin-bottom: 1rem;
  }

  .service-features li {
    font-size: 0.85rem;
    margin-bottom: 0.5rem;
  }

  .cta-container {
    padding: 1.5rem 1rem;
    margin-top: 1.5rem;
  }

  .cta-text {
    font-size: 1.3rem;
    margin-bottom: 1.2rem;
  }

  .cta-button {
    padding: 0.8rem 1.5rem;
    font-size: 1rem;
  }
}

@media (max-width: 400px) {
  .container {
    padding: 0 1rem;
  }

  .section-title {
    font-size: 2rem;
  }

  .section-subtitle {
    font-size: 1rem;
  }

  .service-card {
    padding: 1.2rem;
  }
}
</style>
