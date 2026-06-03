<template>
  <section id="portfolio" class="portfolio section">
    <!-- Section Title -->
    <div class="container section-title" data-aos="fade-up">
      <span class="description-title">Portfolio</span>
      <h2>Portfolio</h2>
    </div>

    <div class="container">
      <div class="row gy-4" data-aos="fade-up" data-aos-delay="200">
        <div
          v-for="item in previewItems"
          :key="item.id"
          class="col-lg-4 col-md-6 portfolio-item"
        >
          <div class="portfolio-content">
            <a
              :href="`/assets/img/portfolio/${item.image}`"
              data-gallery="portfolio-gallery-app"
              class="glightbox"
            >
              <img
                :src="`/assets/img/portfolio/${item.image}`"
                class="img-fluid"
                :alt="item.title"
                loading="lazy"
                decoding="async"
              />
            </a>
            <div class="portfolio-info">
              <h4>{{ item.title }}</h4>
              <p>{{ item.shortDesc }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- See All Portfolio Button -->
      <div class="text-center mt-5" data-aos="fade-up" data-aos-delay="300">
        <router-link to="/portfolio" class="btn btn-dark btn-see-all">
          See All Portfolio <i class="bi bi-arrow-right ms-2"></i>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PortfolioSection",
  data() {
    return {
      previewItems: [
        {
          id: 1,
          title: "Website and Mobile Application",
          image: "merchandise.png",
          shortDesc: "Laravel, PHP, CSS, HTML, Vue.js, Dart, Flutter",
        },
        {
          id: 6,
          title: "Graphics Design",
          image: "summers.png",
          shortDesc: "Canva, Figma, Adobe Photoshop",
        },
        {
          id: 8,
          title: "Layout Design",
          image: "tshirt.png",
          shortDesc: "Print Layout",
        },
      ],
    };
  },
  mounted() {
    this.initializeGLightbox();
  },
  methods: {
    async initializeGLightbox() {
      let attempts = 0;
      const maxAttempts = 50;

      const checkGLightbox = () => {
        if (window.GLightbox) {
          window.GLightbox({
            selector: ".glightbox",
          });
          return true;
        }
        return false;
      };

      if (checkGLightbox()) return;

      const waitForGLightbox = () => {
        attempts++;
        if (checkGLightbox() || attempts >= maxAttempts) {
          return;
        }
        setTimeout(waitForGLightbox, 100);
      };

      setTimeout(waitForGLightbox, 100);
    },
  },
};
</script>

<style scoped>
.btn-see-all {
  padding: 14px 35px;
  border-radius: 30px;
  font-weight: 500;
  font-size: 1rem;
  transition: all 0.3s ease;
}

.btn-see-all:hover {
  background-color: white;
  color: black;
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.portfolio-content {
  overflow: hidden;
  border-radius: 8px;
  height: auto !important;
}

.portfolio-content img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  object-position: center;
  transition: transform 0.3s ease;
}

.portfolio-content:hover img {
  transform: scale(1.05);
}

.portfolio-info {
  padding: 15px;
}

.portfolio-info h4 {
  margin-bottom: 5px;
}

.portfolio-info p {
  margin-bottom: 0;
}
</style>
