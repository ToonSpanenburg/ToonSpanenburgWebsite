<script>
export default {
  props: ['buttonName']
};
</script>

<template>
  <div class="row">
    <button class="text-center  skillsButton bottomBorder">
      <h3>
        {{buttonName}}
      </h3>
    </button>
  </div>
</template>

<style scoped>
  button{
    border: none;
    background: none;
  }

</style>