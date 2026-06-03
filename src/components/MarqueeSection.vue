<template>
  <section class="skills-marquee" aria-label="Services marquee">
    <div class="marquee-track">
      <div
        v-for="(item, index) in items"
        :key="`first-${index}`"
        class="marquee-item"
      >
        <i class="bi bi-asterisk"></i>
        <span>{{ item }}</span>
      </div>
      <div
        v-for="(item, index) in items"
        :key="`second-${index}`"
        class="marquee-item"
      >
        <i class="bi bi-asterisk"></i>
        <span>{{ item }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MarqueeSection",
  data() {
    return {
      items: [
        "App Design",
        "Website Design",
        "Dashboard",
        "Wireframing",
        "Brand Identity",
      ],
    };
  },
};
</script>
