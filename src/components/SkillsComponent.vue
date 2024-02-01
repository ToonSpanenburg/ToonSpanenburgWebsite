<script setup>
import vueSkillsComponent from './Skills/vueSkillComponent.vue';
import ButtonComponent from "@/components/Skills/ButtonComponent.vue";
import TestSkillsComponent from "@/components/Skills/testSkillsComponent.vue";
import {ref} from "vue";

const activeSkill = ref('vue');


const mySkills = [
    "vue",
    "test",
    "Item 3"
];
function buttonClick(id)
{
  activeSkill.value = mySkills[id].toString();
}


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
          <div class="col-3 skillsLine" >
            <div v-for="(item, index) in mySkills" :key="index">
              <button-component @click="buttonClick(index)" :buttonName="item" />
            </div>
          </div>
          <div class="col-9 pb-4" id="SkillBox">
            <div v-if="activeSkill == 'vue'">
              <vueSkillsComponent/>
            </div>

            <div v-if="activeSkill == 'test'">
              <test-skills-component/>
            </div>
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