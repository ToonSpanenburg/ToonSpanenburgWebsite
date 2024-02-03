<script setup>
import ButtonComponent from "@/components/Skills/ButtonComponent.vue";
import {ref} from "vue";
import WebdesignSkillsComponent from "@/components/Skills/WebdesignSkillsComponent.vue";
import ProgrammerenSkillsComponent from "@/components/Skills/ProgrammerenSkillsComponent.vue";
import VariaSkillsComponent from "@/components/Skills/VariaSkillsComponent.vue";

const activeSkill = ref('webDesign');


const mySkills = [
    "webDesign",
    "programmeren",
    "varia"
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

      <div class="skillsBorder SkillsBox">
        <div class="row rowFix">
          <div class="col-3 skillsLine GreyBox buttonBox" >
            <div v-for="(item, index) in mySkills" :key="index" >
              <button-component @click="buttonClick(index)" :buttonName="item" />
            </div>
          </div>
          <div class="col-9 pb-4" id="SkillBox">

            <div v-if="activeSkill == 'webDesign'">
              <WebdesignSkillsComponent/>
            </div>

            <div v-if="activeSkill == 'programmeren'">
              <ProgrammerenSkillsComponent/>
            </div>

            <div v-if="activeSkill == 'varia'">
              <VariaSkillsComponent/>
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

  .rowFix{
    margin-left: 0;
  }

  .skillsBorder
  {
    display: inline-block;
    border-style: solid;
    border-color: #d6c389;
    border-width: 3px;
  }

  .SkillsBox
  {
    min-height: 400px;
  }

  .buttonBox
  {
    min-height: 400px;
  }

</style>