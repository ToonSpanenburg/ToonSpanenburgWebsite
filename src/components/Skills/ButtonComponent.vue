<script>
export default {
  props: ['buttonName']
};
</script>

<template>
  <div class="row mt-2">
    <button class="skillsButton">
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
    color: #123d67;
  }
  button:hover
  {
    color:#d6c389;
  }
</style>