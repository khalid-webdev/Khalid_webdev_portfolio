<script setup>
import {Github,LinkedinSquare,Fiverr,TwitterX,Gmail} from '@boxicons/vue';
const navItems = [
  { id: 'about', label: 'About' },
  { id: 'projects', label: 'Featured Projects' },
  { id: 'skills', label: 'Technical Expertise' }
];
const activeNav = ref('about');
const setActive = (id) => {
  activeNav.value = id
}
</script>

<template>
  <div class="sidebar sticky top-[70px]">
    <div class="about mb-2">
      <div class="flex items-start justify-between">
        <h1 class="font-black italic text-5xl">Md Khalid</h1>
      </div>
      <h2 class="mt-5 mb-8 font-medium text-3xl">Backend Developer</h2>
      <p class="text-lg"> I develop high-performance, secure, and scalable backend solutions.</p>
    </div>

    <!-- Navigation -->
    <div class="navigator">
     <div class="nav" v-for="item in navItems"
      :key="item.id"
       :class="['nav-btn', { active: activeNav === item.id }]"
        @click="setActive(item.id)">
        <h4>_____</h4>
        <h3> <a :href="`#${item.id}`"> {{ item.label }} </a></h3>
      </div>
    </div>

    <!-- Github/linkdin/fiver/whatsapp -->
    <div class="social_icons flex items-center gap-5">
     <NuxtLink title="Github" to="https://github.com/khalid-webdev" target="_blank">
        <Github width="1.8rem" height="1.8rem"/>
      </NuxtLink>
      <NuxtLink title="Linkedin" to="https://www.linkedin.com/in/md-khaleduzzaman-0036111b5" target="_blank">
        <LinkedinSquare width="1.8rem" height="1.8rem"/>
      </NuxtLink>
      <NuxtLink title="Twitter X" to="https://github.com" target="_blank">
        <TwitterX width="1.8rem" height="1.8rem"/>
      </NuxtLink>
      <NuxtLink title="Fiverr" to="https://www.fiverr.com/khalid_webdev" target="_blank">
        <Fiverr width="1.8rem" height="1.8rem"/>
      </NuxtLink>
      <NuxtLink title="Gmail" to="https://www.fiverr.com/khalid_webdev" target="_blank">
        <Gmail width="1.8rem" height="1.8rem"/>
      </NuxtLink>



      </div>

  </div>
</template>
<style scoped>


.about{
  font-family: "Raleway", sans-serif;
}
.navigator{
  display: flex;
  flex-direction: column;
  margin: 3rem 0;
}
.nav{
  font-family: "Inter",sans-serif;
  display: flex;
  align-items: center;
  font-size: .8rem;
  color: #ababab;
  position: relative;
  transition: all .3s ease;
  text-transform: uppercase;
  font-weight: 600;
}
.nav h4{
  align-self: flex-start;
  margin-bottom: .75rem;
  margin-right: .75rem;
}
.nav:hover{
  transform: translateX(15px);
  cursor: pointer;
}
.about h2{
  color: #e2e2e2;
}
.about p{
  color: #ababab;

}

.nav-btn {
  align-self: flex-start;
  margin-bottom: .75rem;
  margin-right: .75rem;
  transition: all 0.2s ease;
}
.nav-btn.active {
  color: white;
    transform: translateX(20px);
}
a{
  transition: all .2s ease;
}
a:hover{
  color: #4c77d3;
}
</style>
