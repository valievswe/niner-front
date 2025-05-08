<!-- About Section -->
<template>
  <section class="about-section" id="about">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">
          About <span class="highlight">CD IELTS</span>
        </h2>
        <div class="title-underline"></div>
      </div>

      <div class="about-content">
        <div class="about-image-container">
          <div class="image-frame">
            <img
              src="../assets/images/bwink_edu_04_single_12.jpg"
              alt="Student practicing IELTS"
              class="about-image"
            />
          </div>
          <div class="experience-badge">
            <span class="years">3+</span>
            <span class="text">Years Experience</span>
          </div>
        </div>

        <div class="about-text">
          <p class="tagline">
            <i class="fa-solid fa-quote-left quote-icon"></i> Your path to IELTS
            success starts here
          </p>

          <p class="description">
            CD IELTS is a state-of-the-art computer-based IELTS preparation
            platform designed by certified examiners to mirror the exact testing
            conditions you'll face on exam day. Our mission is simple: to help
            you achieve the score you need with confidence.
          </p>

          <div class="features-grid">
            <div class="feature-item">
              <div class="feature-icon">
                <i class="fa-solid fa-computer"></i>
              </div>
              <div class="feature-text">
                <h4>Authentic Interface</h4>
                <p>Identical to the official IELTS computer-delivered test</p>
              </div>
            </div>

            <div class="feature-item">
              <div class="feature-icon">
                <i class="fa-solid fa-certificate"></i>
              </div>
              <div class="feature-text">
                <h4>Expert Created</h4>
                <p>Developed by certified IELTS examiners</p>
              </div>
            </div>

            <div class="feature-item">
              <div class="feature-icon">
                <i class="fa-solid fa-chart-line"></i>
              </div>
              <div class="feature-text">
                <h4>Proven Results</h4>
                <p>Thousands of students have improved their scores</p>
              </div>
            </div>

            <div class="feature-item">
              <div class="feature-icon">
                <i class="fa-solid fa-graduation-cap"></i>
              </div>
              <div class="feature-text">
                <h4>Targeted Practice</h4>
                <p>Focus on your weakest areas to maximize improvement</p>
              </div>
            </div>
          </div>

          <rpl_btn
            to="/discovery"
            class="cta-button pulse-animation"
            delay="100"
            >Discover More<i class="fa-solid fa-arrow-right"></i
          ></rpl_btn>
        </div>
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

.about-section {
  padding: 7rem 0;
  background-color: #f9f9f9;
  position: relative;
  overflow: hidden;
}

.about-section::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 300px;
  height: 300px;
  background-color: rgba(0, 0, 0, 0.03);
  border-radius: 50%;
  transform: translate(150px, -150px);
  z-index: 1;
}

.about-section::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 200px;
  height: 200px;
  background-color: rgba(0, 0, 0, 0.02);
  border-radius: 50%;
  transform: translate(-100px, 100px);
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
  margin-bottom: 4rem;
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

.about-content {
  display: flex;
  align-items: center;
  gap: 5rem;
}

.about-image-container {
  flex: 1;
  position: relative;
}

.image-frame {
  position: relative;
  border: 5px solid #fff;
  border-radius: 10px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transform: rotate(-2deg);
  transition: transform 0.5s ease;
}

.image-frame:hover {
  transform: rotate(0);
}

.about-image {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.5s ease;
}

.image-frame:hover .about-image {
  transform: scale(1.05);
}

.experience-badge {
  position: absolute;
  right: -20px;
  bottom: 40px;
  background-color: #000;
  color: #fff;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  z-index: 10;
}

.years {
  font-size: 2.5rem;
  font-weight: 700;
  line-height: 1;
  font-family: "Raleway", sans-serif;
}

.text {
  font-size: 0.9rem;
  text-align: center;
  max-width: 80px;
  font-family: "Raleway", sans-serif;
}

.about-text {
  flex: 1;
}

.tagline {
  font-size: 1.6rem;
  font-weight: 500;
  font-style: italic;
  color: #555;
  margin-bottom: 2rem;
  font-family: "Raleway", sans-serif;
  position: relative;
  padding-left: 1.5rem;
}

.quote-icon {
  position: absolute;
  left: 0;
  top: 2px;
  color: #000;
  opacity: 0.3;
  font-size: 1.2rem;
}

.description {
  font-size: 1.4rem;
  line-height: 1.7;
  color: #333;
  margin-bottom: 2.5rem;
  font-family: "Raleway", sans-serif;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.feature-icon {
  width: 50px;
  height: 50px;
  background-color: #000;
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
  flex-shrink: 0;
}

.feature-text h4 {
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #000;
  font-family: "Raleway", sans-serif;
}

.feature-text p {
  font-size: 1rem;
  color: #555;
  line-height: 1.4;
  font-family: "Raleway", sans-serif;
}

.cta-button {
  font-family: "Raleway", sans-serif;
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
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

/* Responsive Design */
@media (max-width: 992px) {
  .about-content {
    flex-direction: column;
    gap: 4rem;
  }

  .experience-badge {
    right: 0;
    bottom: -20px;
    width: 100px;
    height: 100px;
  }

  .years {
    font-size: 2rem;
  }

  .text {
    font-size: 0.8rem;
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2.8rem;
  }

  .tagline {
    font-size: 1.4rem;
  }

  .description {
    font-size: 1.2rem;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}

@media (max-width: 576px) {
  .section-title {
    font-size: 2.4rem;
  }

  .feature-item {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .feature-text h4 {
    font-size: 1.2rem;
  }
}
</style>
