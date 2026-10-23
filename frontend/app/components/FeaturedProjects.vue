<script setup>

import authImg from "@/assets/images/authenticationSystem.jpg"
import ecommerceImg from '@/assets/images/ecommerce.jpg'
import foodImg from '@/assets/images/food.jpg'
import cmsImg from '@/assets/images/cms.jpg'
import notesImg from '@/assets/images/notes.jpg'
const projects = [
  {
    id: 1,
    title: "Secure Jwt Authentication system",
    description: "A premium login system that keeps apps secure using fast-expiring tokens and auto-refresh protection. It includes role permissions, active session tracking, and easy email or password recovery.",
    cover: authImg,
    skills: ["Nodejs","Express","Jwt","Mongodb","Sendgrid"],
  },
  {
    id: 2,
    title: "Ecommerce Backend Engineer",
    description: "Develop production-ready E-commerce REST API featuring secure authentication, advanced security hardening, and a race-condition safe checkout with a secure payment gateway integration. A robust, fully tested backend engineered for scale, handling products and order processing seamlessly.",
    cover: ecommerceImg,
       skills: ["Nodejs","Sendgrid","Bcrypt","Payment gateway"],
  },
  {
    id: 3,
    title: "Food Shoping Backend",
    description: "Build a high-performance food shopping REST API featuring secure authentication, product catalogs, and optimized cart and order management. Built with a secure payment gateway integration and advanced backend logic explicitly engineered to handle checkout race conditions under heavy traffic.",
    cover: foodImg,
       skills: ["Nodejs","Express","Sendgrid","Payment gateway"],
  },
  {
    id: 4,
    title: "Task (CMS) full stack",
    description: "CMS task management REST API featuring secure authentication, dynamic role-based access controls, and optimized project workflows. Engineered with advanced backend logic to handle concurrent task updates, custom pagination systems for high-volume data retrieval, and efficient order tracking.",
    cover: cmsImg,
    skills: ["Nodejs","Jwt","Mongodb","CRUD","RESTAPI"],
  },
  {
    id: 5,
    title: "Note Full stack",
    description: "Full-stack Note web application featuring secure authentication, dynamic category organization, and a highly responsive user interface. Built with smart logic to manage simultaneous note edits, easy page-by-page navigation for browsing large amounts of data, and a quick text search to find notes instantly.",
    cover: notesImg,
       skills: ["Nodejs","Express","CRUD","RESTAPI"],
  },
]

</script>
<template>
  <div class="text-gray-400 mb-[4rem]">
    <h1 class="text-2xl mb-12 font-medium text-gray-300">Featured Projects</h1>
    <div class="container flex-col flex gap-6">
      <Card v-for="project in projects" :key="project.id" :project="project"/>
    </div>
    <button class="font-medium text-gray-200 capitalize text-xl hover:text-teal-600 mt-6 cursor-pointer">View full projects archive --></button>
  </div>
</template>
