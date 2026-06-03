<template>
  <section id="about" class="about sectionabout">
    <div
      class="container-fluid about-me"
      data-aos="fade-up"
      data-aos-delay="100"
    >
      <div class="row gy-4 justify-content-center">
        <div class="row gx-5">
          <div
            class="col-lg-5 left-content"
            data-aos="fade-up-left"
            data-aos-delay="100"
          >
            <div class="d-flex justify-content-center">
              <img
                src="/assets/img/brianz.png"
                class="profilecircle img-fluid"
                alt="Profile Image"
                id="profile"
              />
            </div>
            <br /><br />
          </div>

          <div
            class="col-lg-7 right-content content"
            data-aos="fade-up"
            data-aos-delay="100"
          >
            <!-- Personal Introduction Section -->
            <div
              class="info-container-wrapper"
              style="position: relative; overflow: visible"
            >
              <img
                src="/assets/img/glitter.svg"
                alt="Glitter Decoration"
                class="glitter-overlay"
                style="
                  position: absolute;
                  top: -60px;
                  left: 50%;
                  transform: translateX(-50%);
                  width: 750px;
                  height: auto;
                  opacity: 0.6;
                  z-index: 0;
                  pointer-events: none;
                "
              />
              <div
                class="info-container"
                style="position: relative; z-index: 1"
              >
                <div class="about-heading">
                  <h5 class="about-hero">Who is <span>Brian Inguito</span>?</h5>
                </div>
                <div>
                  Hi, I'm <strong>Brian Inguito</strong>, a graduate with a
                  Bachelor of Science in Information Technology from
                  <strong>Caraga State University</strong>. I'm super passionate
                  about creating art and creative projects, and I love to draw
                  and play different musical instruments. As a web developer and
                  web/graphic designer, I get to seamlessly blend my tech skills
                  with my creativity!
                </div>
                <br />
                <hr class="hr1" />
              </div>
            </div>

            <!-- Academic Highlights Section -->
            <div class="info-container">
              <h3 class="aboutpersonal">Academic Highlights</h3>
              <br />
              <div class="row">
                <div class="col-lg-12">
                  <ul>
                    <li>
                      <i class="bi bi-chevron-right"></i>
                      Bachelor of Science in Information Technology at Caraga
                      State University (CSU).
                    </li>
                    <li>
                      <i class="bi bi-chevron-right"></i>
                      Vice President's List honoree in BS Information Technology
                      at Caraga State University – Main Campus, in second-year
                      first semester.
                    </li>
                    <li>
                      <i class="bi bi-chevron-right"></i>
                      Dean's List honoree in BS Information Technology at Caraga
                      State University – Main Campus, from the first semester of
                      the first year to the second semester.
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Tech Stack Section -->
        <div class="container-fluid py-1">
          <div class="container" data-aos="fade-up-right" data-aos-delay="100">
            <div class="tools-header text-center">
              <div class="tools-title-top">Exploring the Tools</div>
              <div class="tools-title-bottom">Behind My Designs</div>
            </div>
            <br /><br />

            <div class="row g-5 justify-content-center">
              <!-- Design Tools — Left -->
              <div class="col-lg-3">
                <h4 class="tools-category-title text-center mb-4">
                  Design Tools
                </h4>
                <div class="row row-cols-3 g-4 justify-content-center">
                  <div
                    v-for="tool in designTools"
                    :key="tool.name"
                    class="col d-flex justify-content-center"
                  >
                    <div class="tool-circle text-center">
                      <img
                        class="svg-icon"
                        :src="`/assets/img/${tool.icon}`"
                        height="72px"
                        :alt="tool.name"
                      />
                      <div class="tool-name mt-2">{{ tool.name }}</div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Coding Tools — Right -->
              <div class="col-lg-3">
                <h4 class="tools-category-title text-center mb-4">
                  Coding Tools
                </h4>
                <div class="row row-cols-3 g-4 justify-content-center">
                  <div
                    v-for="tool in codingTools"
                    :key="tool.name"
                    class="col d-flex justify-content-center"
                  >
                    <div class="tool-circle text-center">
                      <img
                        class="svg-icon"
                        :src="`/assets/img/${tool.icon}`"
                        height="72px"
                        :alt="tool.name"
                      />
                      <div class="tool-name mt-2">{{ tool.name }}</div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- IDE — Third -->
              <div class="col-lg-3">
                <h4 class="tools-category-title text-center mb-4">IDE</h4>
                <div class="row row-cols-3 g-4 justify-content-center">
                  <div
                    v-for="tool in ideTools"
                    :key="tool.name"
                    class="col d-flex justify-content-center"
                  >
                    <div class="tool-circle text-center">
                      <img
                        class="svg-icon"
                        :src="`/assets/img/${tool.icon}`"
                        height="72px"
                        :alt="tool.name"
                      />
                      <div class="tool-name mt-2">{{ tool.name }}</div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- AI Agents — Fourth -->
              <div class="col-lg-3">
                <h4 class="tools-category-title text-center mb-4">AI Agents</h4>
                <div class="row row-cols-3 g-4 justify-content-center">
                  <div
                    v-for="tool in aiTools"
                    :key="tool.name"
                    class="col d-flex justify-content-center"
                  >
                    <div class="tool-circle text-center">
                      <img
                        class="svg-icon"
                        :src="`/assets/img/${tool.icon}`"
                        height="72px"
                        :alt="tool.name"
                      />
                      <div class="tool-name mt-2">{{ tool.name }}</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Interests Section -->
        <div class="myinterest">
          <div class="container" data-aos="fade-up-right" data-aos-delay="100">
            <h3 class="text-center mb-5">Interests</h3>
            <div
              class="row interests-row align-items-center justify-content-center"
            >
              <div
                class="col-lg-3 col-md-3 col-6 d-flex flex-column align-items-center gap-3"
              >
                <div
                  v-for="interest in interests.slice(0, 2)"
                  :key="interest.id"
                >
                  <img
                    class="interest-side-image"
                    :src="`/assets/img/${interest.image}`"
                    :alt="interest.title"
                  />
                </div>
              </div>
              <div class="col-lg-6 col-md-6 col-12">
                <div class="interest-photo-stage">
                  <img
                    class="interest-photo"
                    src="/assets/img/great%20photograp.png"
                    alt=""
                  />
                </div>
              </div>
              <div
                class="col-lg-3 col-md-3 col-6 d-flex flex-column align-items-center gap-3"
              >
                <div
                  v-for="interest in interests.slice(2, 4)"
                  :key="interest.id"
                >
                  <img
                    class="interest-side-image"
                    :src="`/assets/img/${interest.image}`"
                    :alt="interest.title"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutSection",
  data() {
    return {
      codingTools: [
        { name: "Vue.js", icon: "vue-svgrepo-com.svg" },
        { name: "React", icon: "react-svgrepo-com.svg" },
        { name: "JavaScript", icon: "javascript.svg" },
        { name: "Supabase", icon: "supabase-logo-icon.svg" },
        { name: "Php", icon: "Php.svg" },
        { name: "Bootstrap", icon: "Bootstrap.svg" },
      ],
      ideTools: [
        { name: "VS Code", icon: "vscode.svg" },
        { name: "Antigravity", icon: "antigravity-color.svg" },
      ],
      aiTools: [
        { name: "ChatGPT", icon: "openai.svg" },
        { name: "Gemini", icon: "gemini-color.svg" },
        { name: "Claude", icon: "claude-color.svg" },
      ],
      designTools: [
        { name: "Photoshop", icon: "Photoshop.svg" },
        { name: "Canva", icon: "canva-icon.svg" },
        { name: "Figma", icon: "figma.svg" },
        { name: "Krita", icon: "krita-logo-light.svg" },
      ],
      interests: [
        { id: 1, image: "drawfolder.png" },
        { id: 2, image: "codefolder.png" },
        { id: 3, image: "musicfolder.png" },
        { id: 4, image: "photofolder.png" },
      ],
    };
  },
};
</script>
