<script setup>

</script>

<template>
  <div v-if="windowWidth > 768">
    <div class="m-4 pt-4">
      <div class="container justify-content-center text-center">
        <div class="row">
          <div class="col navItem navLine">
            <a href="#voorstelling" class="navText">Voorstelling</a>
          </div>
          <div class="col navItem navLine">
            <a href="#Interesses" class="navText">interesses</a>
          </div>
          <div class="col navItem navLine">
            <a href="#Ervaring" class="navText">Ervaring</a>
          </div>
          <div class="col navItem navLine">
            <a href="#Skills" class="navText">Skills</a>
          </div>
          <div class="col navItem">
            <a href="#Contact" class="navText">Contact</a>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div v-else>
    <div class="navbar hamburger m-5 p-2">

      <button class="btn btn-lg btnHeader" type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse mt-2" id="collapseExample">
        <div class="row">
          <div class="col">
            <ul>
              <li>
                <a href="#voorstelling" class="navText">Voorstelling</a>
              </li>
              <li>
                <a href="#Interesses" class="navText">interesses</a>
              </li>
              <li>
                <a href="#Ervaring" class="navText">Ervaring</a>
              </li>
              <li>
                <a href="#Skills" class="navText">Skills</a>
              </li>
              <li>
                <a href="#Contact" class="navText">Contact</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>


<script>
export default {
  data() {
    return {
      windowWidth: window.innerWidth,
    };
  },
  mounted() {
    // Add an event listener to update windowWidth on resize
    window.addEventListener('resize', this.handleResize);
  },
  beforeDestroy() {
    // Remove the event listener when the component is destroyed
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    handleResize() {
      this.windowWidth = window.innerWidth;
    },
  },
};
</script>

<style scoped>
a:link {
  text-decoration: none;
}

a:visited {
  text-decoration: none;
}

a:hover {
  text-decoration: none;
}

a:active {
  text-decoration: none;
}

.navText
{
  color: #123d67;
}

.navItem
{
  text-decoration: none;
  padding: 5px;
  font-size: 35px;
  color: #123d67;
}
.navLine
{
  border-right: solid #d6c389;
}

.hamburger
{
  border: solid #d6c389;
  padding: 0px;
}

.btnHeader
{
  margin-right: 100%;
}
</style>