<template>
  <div class="container">
    <div class="hero offers-section">
      <div class="left">
        <h1 class="title">CD IELTS mock exam platform</h1>
        <p class="description">
          We Will make you <strong>niner</strong> together!
        </p>
        <rpl_btn to="/discovery" class="cta-button pulse-animation" delay="100"
          >Start Mock<i class="fa-solid fa-arrow-right"></i
        ></rpl_btn>
      </div>

      <div class="right">
        <img
          src="../assets/images/bwink_edu_02_single_02.jpg"
          alt="Hero Image"
          class="hero-image"
        />
      </div>
    </div>

    <AboutUs />
    <Weoffer />
  </div>
</template>

<script setup>
import rpl_btn from "@/components/rpl_btn.vue";
import AboutUs from "../components/AboutUs.vue";
import Weoffer from "../components/WeOffer.vue";
</script>

<style scoped>
@import "../assets/base.css";
@import "../assets/main.css";

.hero {
  background: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  gap: 2rem;
  z-index: 2;
  /* border: #000 1px solid; */
}
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
  background-image: radial-gradient(rgba(0, 0, 0, 0.096) 2px, transparent 2px);
  background-size: 50px 50px;
  z-index: 1;
}

.left {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  z-index: 2;
}

.right {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-image {
  width: 100%;
  max-width: 550px;
  height: auto;
  border-radius: 10px;
}

.title {
  font-size: 3.6rem;
  font-weight: 500;
  text-align: center;
  margin-top: 2rem;
  color: #000;
  font-family: "Raleway", sans-serif;
  text-align: left;
}

.description {
  font-size: 1.6rem;
  font-weight: 400;
  text-align: center;
  margin: 0.5rem 0 2rem 0;
  color: #000;
  font-family: "Raleway", sans-serif;
  text-transform: lowercase;
  text-align: left;
}

.description strong {
  color: #000;
  font-weight: 500;
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

/* Responsive styles */
@media screen and (max-width: 1024px) {
  .title {
    font-size: 3rem;
  }

  .description {
    font-size: 1.4rem;
  }
}

@media screen and (max-width: 768px) {
  .hero {
    flex-direction: column;
    text-align: center;
    padding: 1.5rem;
  }

  .left {
    align-items: center;
    order: 2;
    width: 100%;
  }

  .right {
    order: 1;
    width: 100%;
    margin-bottom: 1.5rem;
  }

  .title {
    font-size: 2.5rem;
    text-align: center;
    margin-top: 1rem;
  }

  .description {
    font-size: 1.2rem;
    text-align: center;
    margin: 0.5rem 0 1.5rem 0;
  }

  .cta-button {
    padding: 0.8rem 1.6rem;
    font-size: 1rem;
  }
}

@media screen and (max-width: 480px) {
  .hero {
    padding: 1rem;
  }

  .title {
    font-size: 2rem;
  }

  .description {
    font-size: 1rem;
    margin: 0.5rem 0 1rem 0;
  }

  .hero-image {
    max-width: 100%;
  }

  .cta-button {
    padding: 0.7rem 1.4rem;
    font-size: 0.9rem;
  }
}
</style>
