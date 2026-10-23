<script setup>

</script>

<template>
  <div>
     <section id="about" class="page-section">
      <About/>
    </section>
     <section id="projects" class="page-section">
      <FeaturedProjects />
    </section>
     <section id="skills" class="page-section">
      <Expertise />
    </section>
  </div>
</template>
<style scoped>
.page-section {
  min-height: 50vh; /* Ensures sections take up screen height to allow scrolling */
  padding: 2rem;
}
</style>
