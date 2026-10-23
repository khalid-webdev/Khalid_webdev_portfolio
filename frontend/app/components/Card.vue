<script setup>
const props = defineProps(["project"]);

</script>
<template>
  <div class="card">
    <div class="thumbnail">
      <img :src="project.cover" alt="cover image">
    </div>
    <div class="info">
      <h2 class="text-xl text-gray-200">{{ project.title }}</h2>
      <p>{{ project.description }}</p>

      <div class="stack">
        <h4 v-for="(skill, index) in project.skills" :key="index">{{ skill }}</h4>

      </div>
    </div>
  </div>
</template>
<style scoped>
.card {
  cursor: pointer;
  display: flex;
  align-items: start;
  gap: 1rem;
  transition: border .2s ease;
  padding: 1.3rem 1rem;
  border: 1px solid transparent;
  border-radius: 4px;
}
.card:hover{
  border: 1px solid rgb(0, 81, 82);
  background: rgba(0, 59, 59, 0.162);
}
.card:hover .info h2{
    color:rgb(0, 212, 212);
}
.thumbnail {
  flex-basis: 35%;
}
.info {
  flex-basis: 65%;
}
.thumbnail img {
width: 95%;
  border-radius: .21rem;
}
.info p {
  margin: 1rem 0;
}
.stack {
  display: flex;
  align-items: center;
  gap: 1rem;
}
.stack h4 {
  background: rgb(0, 59, 59);
  padding: .5rem 1rem;
  color:rgb(0, 212, 212);
  border-radius: 20px;
}
</style>
