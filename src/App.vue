<script setup>

import MyHeader from "@/components/MyHeader.vue";
import TestComponent from "@/components/TestComponent.vue";
import WelcomeComponent from "@/components/WelcomeComponent.vue";
import SkillsComponent from "@/components/SkillsComponent.vue";
import ProjectsComponent from "@/components/ProjectsComponent.vue";
import ContactComponent from "@/components/ContactComponent.vue";
import FooterComponent from "@/components/FooterComponent.vue";
import VoorstellingComponent from "@/components/VoorstellingComponent.vue";
</script>

<template>
  <div style="width: 90%; margin: auto" class="fullSite">
    <MyHeader/>
    <welcome-component/>
    <VoorstellingComponent/>
    <SkillsComponent/>
    <ProjectsComponent/>
    <ContactComponent/>
    <FooterComponent/>
  </div>

</template>



<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Urbanist&display=swap');
@import url('https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css');
.fullSite {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
  font-family: 'Urbanist', sans-serif;
}
</style>
