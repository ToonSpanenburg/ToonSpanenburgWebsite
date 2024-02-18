<script>
export default {
  props: ['Project']
};

</script>
<script setup>
function GetTypeColor(projectType)
{
  if (projectType == "vue.js")
  {
    return "#89D6C3";
  }
  if (projectType == ".net")
  {
    return "#C389D6";
  }
  if (projectType == "java")
  {
    return "#C3D689";
  }
  if (projectType == "php")
  {
    return "#D69C89";
  }
  if (projectType == "ervaring")
  {
    return "#d6c389";
  }
  else
  {
    return "#f5f5f5";
  }
}
</script>

<template>
<div class="ms-0">
  <h4 class="py-2 ps-2 projectType" :style="{ backgroundColor: GetTypeColor(Project.type) }">
    {{Project.type}}
  </h4>
  <div class="ms-3 mt-3 me-3">
    <h5>
      {{Project.name}}
    </h5>
    <p>
      {{Project.description}}
    </p>
    <a href="{{Project.link}}">
      <p class="text-muted py-2  ProjectTextLink">
        {{Project.link}}
      </p>
    </a>
  </div>

</div>
</template>

<style scoped>
.projectType
{
  margin: 0;
  border-bottom-right-radius: 50%;
}
.ProjectTextLink
{
  margin-bottom: 0;

}


</style>