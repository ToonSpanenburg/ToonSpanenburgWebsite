<script setup>

import MyHeader from "@/components/MyHeader.vue";
import TestComponent from "@/components/TestComponent.vue";
import WelcomeComponent from "@/components/WelcomeComponent.vue";
import SkillsComponent from "@/components/SkillsComponent.vue";
</script>

<template>
  <div style="width: 80%; margin: auto">
    <MyHeader/>
    <welcome-component/>
    <SkillsComponent/>
    <TestComponent/>
  </div>

</template>



<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Urbanist&display=swap');

body {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
  font-family: 'Urbanist', sans-serif;
}
</style>
