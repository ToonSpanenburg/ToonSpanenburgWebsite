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

<script>
export default {
  data() {
    return {
      windowWidth: window.innerWidth,
    };
  },
  mounted() {
    window.addEventListener('resize', this.handleResize);
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    handleResize() {
      this.windowWidth = window.innerWidth;
    },
  },
};
</script>

<template>
<div class="mx-4 mb-4">
  <div id="Skills" class="mb-1 mb-md-3">
    <div class="">
      <h2 class="mb-3">
        Skills
      </h2>

      <div class="skillsBorder SkillsBox">
        <div class="row rowFix">

          <div  class="col-12 col-md-3 skillsLine GreyBox buttonBox pt-lg-2" >
            <div class="row">
              <div v-for="(item, index) in mySkills" :key="index" class="col-4 col-sm-4 col-md-12 p-2" >
                <button-component @click="buttonClick(index)" :buttonName="item" />
              </div>
            </div>

          </div>


          <div class="col-sm-12 col-md-9 col-lg-9 pb-4" id="SkillBox">

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

  @media only screen and (max-width: 767px)
  {
    .buttonBox
    {
      min-height: 0px;
    }
    .skillsLine
    {
      border-right: none;
      border-bottom-style: solid;
      border-bottom-color: #d6c389;
      border-bottom-width: 3px;
    }
    .row
    {
      margin: 0;
    }
  }

  @media only screen and (max-width: 500px)
  {
    .skillsBorder
    {
      border: none;
    }
  }

</style>