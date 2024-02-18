<script>
export default {
  props: ['buttonName']
};
</script>

<template>
  <div class="row mt-2">
    <button class="skillsButton">
      <h3 class="buttonText">
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
  @media only screen and (max-width: 1240px) {
    h3
    {
      font-size: large;
    }
  }
  @media only screen and (max-width: 500px) {
    h3
    {
      font-size: 0.8em;
      font-weight: bold;
    }
  }
</style>