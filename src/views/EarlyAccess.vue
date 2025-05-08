<template>
  <section class="early-access">
    <div class="early-access-container">
      <div class="early-access-header">
        <h2>Early Access Registration</h2>
        <div class="accent-line"></div>
      </div>

      <div class="early-access-intro">
        <p>
          Join the <span class="highlight">niner</span> community and be among
          the first to access our comprehensive IELTS preparation platform.
          Register now to receive updates and secure your spot for our launch.
        </p>
      </div>

      <div class="registration-form">
        <form @submit.prevent="submitForm">
          <div class="form-grid">
            <div class="form-group">
              <label for="fullName">Full Name</label>
              <input
                type="text"
                id="fullName"
                v-model="formData.fullName"
                placeholder="Enter your full name"
                required
              />
            </div>

            <div class="form-group">
              <label for="email">Email Address</label>
              <input
                type="email"
                id="email"
                v-model="formData.email"
                placeholder="Enter your email"
                required
              />
            </div>

            <div class="form-group">
              <label for="purpose">Purpose</label>
              <select id="purpose" v-model="formData.purpose" required>
                <option value="" disabled selected>Select your purpose</option>
                <option value="student">Student preparing for IELTS</option>
                <option value="teacher">IELTS Teacher/Instructor</option>
                <option value="examiner">IELTS Examiner</option>
                <option value="institution">Educational Institution</option>
                <option value="other">Other</option>
              </select>
            </div>

            <div class="form-group">
              <label for="testDate">Expected Test Date (if applicable)</label>
              <input type="date" id="testDate" v-model="formData.testDate" />
            </div>

            <div class="form-group">
              <label for="currentLevel">Current English Level</label>
              <select id="currentLevel" v-model="formData.currentLevel">
                <option value="" disabled selected>
                  Select your current level
                </option>
                <option value="beginner">Beginner (IELTS 0-3.5)</option>
                <option value="intermediate">Intermediate (IELTS 4-5.5)</option>
                <option value="upperIntermediate">
                  Upper Intermediate (IELTS 6-7)
                </option>
                <option value="advanced">Advanced (IELTS 7.5+)</option>
                <option value="notSure">Not Sure</option>
                <option value="notApplicable">Not Applicable</option>
              </select>
            </div>

            <div class="form-group">
              <label for="targetScore">Target IELTS Score</label>
              <select id="targetScore" v-model="formData.targetScore">
                <option value="" disabled selected>
                  Select your target score
                </option>
                <option value="5">5.0</option>
                <option value="5.5">5.5</option>
                <option value="6">6.0</option>
                <option value="6.5">6.5</option>
                <option value="7">7.0</option>
                <option value="7.5">7.5</option>
                <option value="8">8.0+</option>
                <option value="notApplicable">Not Applicable</option>
              </select>
            </div>
          </div>

          <div class="form-group full-width">
            <label for="interests"
              >Areas of Interest (Select all that apply)</label
            >
            <div class="checkbox-group">
              <div class="checkbox-item">
                <input
                  type="checkbox"
                  id="writing"
                  v-model="formData.interests.writing"
                />
                <label for="writing">Writing</label>
              </div>
              <div class="checkbox-item">
                <input
                  type="checkbox"
                  id="reading"
                  v-model="formData.interests.reading"
                />
                <label for="reading">Reading</label>
              </div>
              <div class="checkbox-item">
                <input
                  type="checkbox"
                  id="listening"
                  v-model="formData.interests.listening"
                />
                <label for="listening">Listening</label>
              </div>
              <div class="checkbox-item">
                <input
                  type="checkbox"
                  id="speaking"
                  v-model="formData.interests.speaking"
                />
                <label for="speaking">Speaking</label>
              </div>
              <div class="checkbox-item">
                <input
                  type="checkbox"
                  id="examinerTools"
                  v-model="formData.interests.examinerTools"
                />
                <label for="examinerTools">Examiner Tools</label>
              </div>
            </div>
          </div>

          <div class="form-group full-width">
            <label for="message">Additional Comments (Optional)</label>
            <textarea
              id="message"
              v-model="formData.message"
              placeholder="Let us know what features you'd like to see or how we can help you prepare for IELTS"
              rows="4"
            ></textarea>
          </div>

          <div class="form-group full-width agreement">
            <div class="checkbox-item">
              <input
                class="checkbox-item-agreement"
                type="checkbox"
                id="agreement"
                v-model="formData.agreement"
                required
              />
              <label for="agreement"
                >I agree to receive updates about niner's launch
              </label>
            </div>
          </div>

          <div class="form-submit">
            <rpl_btn class="btn" type="submit">
              Register for Early Access
            </rpl_btn>
          </div>
        </form>
      </div>

      <div class="early-access-benefits">
        <h3>Benefits of Early Registration</h3>
        <ul>
          <li>
            <div class="benefit-icon"><i class="fas fa-ticket-alt"></i></div>
            <div class="benefit-text">Priority access when we launch</div>
          </li>
          <li>
            <div class="benefit-icon"><i class="fas fa-percentage"></i></div>
            <div class="benefit-text">
              Special discounts on premium features
            </div>
          </li>
          <li>
            <div class="benefit-icon"><i class="fas fa-star"></i></div>
            <div class="benefit-text">
              Exclusive content and practice materials
            </div>
          </li>
          <li>
            <div class="benefit-icon"><i class="fas fa-bullhorn"></i></div>
            <div class="benefit-text">
              Early announcements about new features
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
import rpl_btn from "@/components/rpl_btn.vue";
import { reactive } from "vue";

const formData = reactive({
  fullName: "",
  email: "",
  purpose: "",
  testDate: "",
  currentLevel: "",
  targetScore: "",
  interests: {
    writing: false,
    reading: false,
    listening: false,
    speaking: false,
    examinerTools: false,
  },
  message: "",
  agreement: false,
});

function submitForm() {
  // Here you would typically send the form data to your backend
  console.log("Form submitted:", formData);
  alert(
    "Thanks for registering! We will notify you when early access is available."
  );

  // Reset form after submission
  Object.keys(formData).forEach((key) => {
    if (key === "interests") {
      Object.keys(formData.interests).forEach((interest) => {
        formData.interests[interest] = false;
      });
    } else {
      formData[key] = "";
    }
  });
  formData.agreement = false;
}
</script>

<style scoped>
@import "../assets/base.css"; /* Import your CSS variables here */

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.early-access {
  background-color: #fff;
  padding: 5rem 0;
  font-family: "Raleway", sans-serif;
}

.early-access-container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 5rem 0;
}

.early-access-header {
  text-align: center;
  margin-bottom: 2rem;
}

.early-access-header h2 {
  font-size: 2.5rem;
  font-weight: 700;
  color: #000;
  margin-bottom: 1rem;
}

.accent-line {
  height: 4px;
  width: 80px;
  background-color: #bdbdbb;
  margin: 0 auto;
}

.early-access-intro {
  max-width: 800px;
  margin: 0 auto 3rem;
  text-align: center;
}

.early-access-intro p {
  font-size: 1.2rem;
  line-height: 1.7;
  color: #000;
}

.highlight {
  font-weight: 600;
  border-bottom: 2px solid var(--accent-color);
}

.registration-form {
  background-color: #dfdfdfb0;
  border-radius: 10px;
  padding: 2.5rem;
  margin-bottom: 3rem;
}

.form-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group.full-width {
  grid-column: span 2;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: var(--text-color);
}

input[type="text"],
input[type="email"],
input[type="date"],
select,
textarea {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid black;
  border-radius: 5px;
  background-color: var(--input-bg);
  font-family: var(--font-family-raleway);
  transition: border-color 0.3s ease;
}

input:focus,
select:focus,
textarea:focus {
  outline: none;
  border-color: var(--input-focus);
}

.checkbox-group {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 1rem;
}

.checkbox-item {
  display: flex;
  align-items: center;
  margin-bottom: 0.5rem;
}

/* Custom checkbox styling */
.checkbox-item input[type="checkbox"] {
  flex-shrink: 0;
  box-sizing: border-box;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 20px;
  height: 20px;
  border: 2px solid #000;
  border-radius: 4px;
  outline: none;
  margin-right: 10px;
  position: relative;
  cursor: pointer;
  background-color: #fff;
  vertical-align: middle;
}

.checkbox-item input[type="checkbox"]:checked {
  background-color: var(--button-color);
  border-color: var(--button-color);
}

.checkbox-item input[type="checkbox"]:checked::after {
  content: "";
  position: absolute;
  width: 5px;
  height: 10px;
  border: solid #000;
  border-width: 0 2px 2px 0;
  top: 2px;
  left: 6px;
  transform: rotate(45deg);
}

.agreement {
  gap: 1rem;

  margin-top: 1rem;
  margin-bottom: 2rem;
}
#agreement {
  width: 20px;
  height: 20px;
  margin-right: 10px;
}
.checkbox-item label {
  flex: 1; /* take remaining space */
  line-height: 1.4;
}
.form-submit {
  text-align: center;
}

.btn {
  position: relative;
  background-color: #000;
  border: none;
  outline: none;
  color: #fff;
  padding: 12px 36px;
  border-radius: 10px;
  text-decoration: none;
  font-family: "Raleway", sans-serif;
  font-size: 16px;
  font-weight: 500;
  cursor: pointer;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.btn:hover {
  transform: translateY(-3px);
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

/* Early access benefits section */
.early-access-benefits {
  margin-top: 4rem;
}

.early-access-benefits h3 {
  font-size: 1.5rem;
  font-weight: 600;
  text-align: center;
  margin-bottom: 2rem;
}

.early-access-benefits ul {
  list-style: none;
  padding: 0;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1.5rem;
}

.early-access-benefits li {
  display: flex;
  align-items: center;
  background-color: #dfdfdfb0;
  padding: 1.5rem;
  border-radius: 8px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.early-access-benefits li:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}

.benefit-icon {
  background-color: var(--button-color);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 1rem;
  color: var(--button-text-color);
}

.benefit-text {
  font-weight: 500;
}

/* Responsive styles */
@media (max-width: 768px) {
  .form-grid {
    grid-template-columns: 1fr;
  }

  .form-group.full-width {
    grid-column: span 1;
  }

  .checkbox-group {
    grid-template-columns: 1fr 1fr;
  }

  .early-access-benefits ul {
    grid-template-columns: 1fr;
  }

  .early-access-container {
    padding: 3rem 1rem;
  }

  .registration-form {
    padding: 1.5rem;
  }
}
</style>
