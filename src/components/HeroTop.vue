<template>
  <div id="hero" class="hero">
    <div class="hero-img">
      <img src="../assets/profile.jpg" alt="" />
    </div>
    <div class="hero-info">
      <h2 class="title">ryan adlard</h2>
      <div class="hero-details">
        <!-- <h3 class="subtitle" ref="subtitle"></h3> -->
        <vue-typed-js
          class="subtitle"
          :strings="words"
          :loop="true"
          :typeSpeed="200"
          :startDelay="300"
          :backSpeed="50"
        >
          <h3 class="typing"></h3>
        </vue-typed-js>
        <!-- <p class="blink">|</p> -->
      </div>
    </div>
    <div class="social">
      <a href="#"><i class="fab fa-dribbble"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
      <a href="#"><i class="fab fa-github"></i></a>
      <a href="#"><i class="fab fa-spotify"></i></a>
      <a href="#"><i class="fab fa-stack-overflow"></i></a>
    </div>
    <div class="links">
      <a href="#">download cv</a>
      <!-- <a href="#contact" data-menu="contact" id="contact-me">contact me</a> -->
      <router-link to="/contact" data-menu="contact" id="contact-me"
        >contact me</router-link
      >
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  data() {
    return {
      words: ['web designer', 'developer', 'freelancer']
    }
  }
}
</script>

<style scoped>
.hero {
  margin-top: 6.9rem;
  background-color: var(--whiteColor);
}

.hero .hero-img {
  width: 100%;
}

.hero .hero-img img {
  max-width: 100%;
  clip-path: polygon(0 0, 100% 0%, 100% 84%, 48% 100%, 0 84%);
}

.hero .hero-info {
  text-align: center;
}

.hero .hero-info .title {
  text-transform: capitalize;
  font-size: 3.4rem;
  font-weight: 400;
  line-height: 2.8rem;
  margin: 2rem 0 1rem 0;
  color: var(--blackColor);
}

.hero .hero-info .hero-details {
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero .hero-info .subtitle {
  text-transform: capitalize;
  color: var(--greenColor);
  font-size: 1.6rem;
  line-height: 2rem;
  font-weight: 400;
}

.hero .social {
  margin-top: 1.6rem;
  text-align: center;
}

.hero .social a {
  display: inline-block;
  margin: 0 0.6rem;
}

.hero .social a i {
  color: var(--blackColor);
  font-size: 1.6rem;
  transition: all 0.3s;
}

.hero .social a:hover i {
  color: var(--greenColor);
}

.hero .links {
  position: relative;
  margin-top: 6rem;
  text-align: center;
  display: flex;
}

.hero .links::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 0.2rem;
  background: radial-gradient(
    ellipse at center,
    #ddd 0,
    rgba(255, 255, 255, 0) 70%
  );
}

.hero .links a {
  text-transform: uppercase;
  font-size: 1.4rem;
  font-weight: 500;
  height: 7rem;
  line-height: 7rem;
  color: var(--blackColor);
  position: relative;
  flex-basis: 50%;
  cursor: pointer;
  transition: all 0.3s;
}

.hero .links a:hover {
  color: var(--greenColor);
}

.hero .links a:last-of-type::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 0.3rem;
  background: radial-gradient(
    ellipse at center,
    #ddd 0,
    rgba(255, 255, 255, 0) 70%
  );
}

.blink {
  color: var(--greenColor);
  animation: blink 0.5s infinite;
}

@keyframes blink {
  to {
    opacity: 0;
  }
}

@media (min-width: 1200px) {
  .hero {
    max-width: 48rem;
    transform: scale(1, 1.1);
  }
}
</style>
