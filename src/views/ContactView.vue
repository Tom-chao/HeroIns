<template>
  <section id="contact" class="contact">
    <div class="contact-me p-3">
      <h3 class="specialtitle">get <span>in touch</span></h3>
      <div class="contact-container">
        <div class="map">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52992.27367296583!2d35.46917690127269!3d33.88921332207032!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x151f17215880a78f%3A0x729182bae99836b4!2sBeirut!5e0!3m2!1sen!2slb!4v1660499764902!5m2!1sen!2slb"
            width="100%"
            height="100%"
            style="border: 0"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
        <div class="info-list">
          <ul>
            <li><strong>address . . . . .</strong> California USA</li>
            <li><strong>email . . . . .</strong> adlard@example.com</li>
            <li><strong>phone . . . . .</strong> +123 654 78900</li>
            <li><strong>freelance . . . . .</strong> available</li>
          </ul>
        </div>
      </div>
      <div class="form-title">
        <h3 class="specialtitle">contact <span>form</span></h3>
      </div>
      <div class="contact-form">
        <form action="#">
          <div class="form-group">
            <input type="text" placeholder="Full Name" />
          </div>
          <div class="form-group">
            <input type="email" placeholder="Email Address" />
          </div>
          <div class="form-group message">
            <textarea placeholder="Your Message"></textarea>
          </div>
        </form>
        <button>send message<span></span></button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactView'
}
</script>

<style scoped>
.contact .contact-me .contact-container {
  margin-top: 2rem;
}

.contact-me .contact-container .map {
  height: 24rem;
  margin-bottom: 3rem;
}

.contact-me .contact-container .info-list li {
  position: relative;
  width: 100%;
  padding: 1.1rem 0;
  font-size: 1.6rem;
  text-transform: capitalize;
  text-align: right;
}

.contact-me .contact-container .info-list li::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 0.2rem;
  bottom: 0;
  left: 0;
  background: radial-gradient(
    ellipse at center,
    #ddd 0,
    rgba(255, 255, 255, 0) 70%
  );
}

.contact-me .contact-container .info-list li strong {
  padding: 0.1rem 0.8rem;
  float: left;
}

.contact-me .form-title {
  margin-top: 4rem;
}

.contact-me .contact-form {
  padding: 3rem 0;
}

.contact-me .contact-form form {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(20rem, 100%), 1fr));
  gap: 2rem;
}

.contact-me .contact-form form .message {
  grid-column: 1/-1;
}

.contact-me .contact-form form .form-group input,
.contact-me .contact-form form .form-group textarea {
  display: block;
  padding: 0 1.5rem;
  font-size: 1.6rem;
  height: 5rem;
  width: 100%;
  color: var(--greenColor);
  border: 0.2rem solid var(--veryLightGray);
  outline: none;
  transition: all 0.3s ease-in-out;
}

.contact-me .contact-form form .form-group textarea {
  resize: none;
  padding: 1.5rem;
  height: 9.4rem;
}

.contact-me .contact-form form .form-group input:focus,
.contact-me .contact-form form .form-group textarea:focus {
  border-color: var(--greenColor);
}

.contact-me .contact-form form .form-group input:focus::placeholder,
.contact-me .contact-form form .form-group textarea:focus::placeholder {
  color: var(--blackColor);
}

.contact-me .contact-form button {
  padding: 0 3rem;
  width: 25rem;
  height: 5rem;
  border-radius: 0.4rem;
  margin-top: 2rem;
  background-color: var(--veryLightGray);
  line-height: 5rem;
  color: var(--blackColor);
  text-transform: uppercase;
  font-size: 1.4rem;
  font-weight: 500;
  border: none;
  outline: none;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.contact-me .contact-form button span {
  position: relative;
  display: inline-block;
  font-size: 1.8rem;
  margin: 0 2rem;
}

.contact-me .contact-form button span::before,
.contact-me .contact-form button span::after {
  content: '';
  position: absolute;
  background-color: var(--blackColor);
  transition: all 0.3s ease-in-out;
}

.contact-me .contact-form button span::before {
  width: 1.5rem;
  height: 0.2rem;
  bottom: 0.3rem;
  right: 0;
  left: auto;
  top: auto;
}

.contact-me .contact-form button span::after {
  left: auto;
  top: -0.8rem;
  right: -0.2rem;
  bottom: 0.3rem;
  width: 1rem;
  height: 0.2rem;
  transform: rotate(45deg);
}

.contact-me .contact-form button:hover {
  color: var(--greenColor);
}

.contact-me .contact-form button:hover span::before,
.contact-me .contact-form button:hover span::after {
  background-color: var(--greenColor);
}
</style>
