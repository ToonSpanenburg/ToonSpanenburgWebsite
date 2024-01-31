<script setup>
import { ref, computed } from 'vue'
import vueSkillsComponent from './Skills/vueSkillComponent.vue';
import ButtonComponent from "@/components/Skills/ButtonComponent.vue";


const routes = {
  '/': vueSkillsComponent,
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/']
})
</script>

<template>
<div class="m-4">
  <div id="Skills" class="container mb-5">
    <div class="m-5">
      <h2 class="mb-3">
        Skills
      </h2>

      <div class="skillsBorder">
        <div class="row">
          <div class="col-3 skillsLine">

            <button-component/>
            <button-component/>
            <button-component/>
            <button-component/>
            <button-component/>
            <button-component/>


          </div>
          <div class="col-9">
            <component :is="currentView" />
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
  .skillsLine
  {
    border-right-style: solid;
    border-right-color: #d6c389;
    border-right-width: 3px;
  }


  .skillsBorder
  {
    display: inline-block;
    border-style: solid;
    border-color: #d6c389;
    border-width: 3px;
    margin-left: -9px;
  }
</style>