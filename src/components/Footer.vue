<template>
  <footer id="footer" class="footer position-relative">
    <div class="container footer-cta">
      <div class="footer-cta-text">
        <h3>Let's <span>Connect</span> there</h3>
      </div>
      <a class="footer-cta-btn" href="#">
        <span>View All Blogs</span>
        <span class="footer-cta-icon"><i class="bi bi-arrow-right"></i></span>
      </a>
    </div>

    <div class="container footer-main">
      <div class="footer-brand">
        <div class="brand-badge">B</div>
        <h4>Brian Inguito</h4>
        <p>
          Talent is a pursued interest. Anything that you're willing to
          practice, you can do.
        </p>
        <div class="social-links d-flex">
          <a href=""><i class="bi bi-facebook"></i></a>
          <a
            href="https://www.instagram.com/yangoghh?igsh=cTgxZDh0cnEyZGVm"
            target="_blank"
          >
            <i class="bi bi-instagram"></i>
          </a>
          <a href="https://github.com/inguitobrian" target="_blank">
            <i class="bi bi-github"></i>
          </a>
          <a
            href="https://www.linkedin.com/in/brian-inguito-449b3b282/"
            target="_blank"
          >
            <i class="bi bi-linkedin"></i>
          </a>
        </div>
      </div>

      <div class="footer-column">
        <h5>Navigation</h5>
        <ul class="footer-links">
          <li><a href="#hero">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#resume">Resume</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>

      <div class="footer-column">
        <h5>Contact</h5>
        <ul class="footer-links">
          <li><a href="tel:+9203919743">+9203919743</a></li>
          <li>
            <a href="mailto:inguitobrian6@gmail.com">inguitobrian6@gmail.com</a>
          </li>
          <li>
            <a href="https://github.com/inguitobrian" target="_blank"
              >github.com/inguitobrian</a
            >
          </li>
          <li>Philippines</li>
        </ul>
      </div>

      <div class="footer-column footer-subscribe">
        <h5>Get the latest information</h5>
        <form class="subscribe-form" action="#">
          <input
            type="email"
            name="email"
            placeholder="Email address"
            aria-label="Email address"
          />
          <button type="submit" aria-label="Subscribe">
            <i class="bi bi-send-fill"></i>
          </button>
        </form>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="container footer-bottom-inner">
        <span> Copyright © 2024 Brian Inguito. All Rights Reserved. </span>
        <div class="footer-bottom-links">
          <a href="#">User Terms & Conditions</a>
          <span>|</span>
          <a href="#">Privacy Policy</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>
