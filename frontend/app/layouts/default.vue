<template>
  <div class="default">
    <div class="sidebar">
      <Sidebar/>
    </div>
    <div  class="min-h-screen content">
      <slot/>
    </div>
  </div>
</template>
<style scoped>

.default{
  margin-top: 3rem;
  padding: 1rem 7%;
  display: flex;
  gap:1rem;
}
.sidebar{
  flex-basis: 35%;
}
.content{

  flex-basis: 65%;
}


</style>
