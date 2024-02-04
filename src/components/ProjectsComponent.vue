<script setup>
  import * as Projects from "@/components/Projects/Projects.js";
  import SingularProjectComponent from "@/components/Projects/SingularProjectComponent.vue";

  const allProjects = Projects.getAllProjects();

  function GoToUrl(link)
  {
    window.location.href = link;
  }
</script>

<template>
  <div class="m-4">
    <div id="Projects">
      <h2 class="mb-3">
        Projects
      </h2>
    </div>

    <div class="ProjectsBorder">
      <div class="row p-5 ">
        <div v-for="(project, index) in allProjects" :key="index" class="col SingularProjectBorder m-3 Project paddingRowFixer">
          <div @click="GoToUrl(project.gitLink)" style="cursor: pointer;" class="rowFix">
            <SingularProjectComponent :Project="project"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .ProjectsBorder
  {
    display: inline-block;
    border-style: solid;
    border-color: #d6c389;
    border-width: 3px;
  }
  .SingularProjectBorder
  {
    display: inline-block;
    border-style: solid;
    border-color: #d6c389;
    border-width: 3px;
  }
  .Project
  {
    transition: transform 0.3s ease;
    border-bottom-right-radius: 30%;
  }
  .Project:hover
  {
    transform: scale(1.15);
  }
  .paddingRowFixer
  {
    padding-left: 0px;
  }
</style>