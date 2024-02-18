<script setup>
  import * as Projects from "@/components/Projects/Projects.js";
  import SingularProjectComponent from "@/components/Projects/SingularProjectComponent.vue";
  import {ref} from "vue";

  const allProjects = ref(Projects.getAllProjects());

  function leftArrowClick()
  {
    let lastElement = allProjects.value.pop();
    allProjects.value.unshift(lastElement);
  }

  function rightArrowClick()
  {
    let firstElement = allProjects.value.shift();
    allProjects.value.push(firstElement);
  }


</script>

<template>
  <div class="m-4">
    <div id="Projects">
      <h2 class="mb-3">
        Projects
      </h2>
    </div>

    <!-- might add border back later -->
    <div class="">
      <div class="pb-4">
        <div class="row">

          <div class="col-1 d-flex align-items-center justify-content-center">
            <a @click="leftArrowClick()" class="btn p-0 p-sm-2">
              <i class="bi bi-arrow-left-short"></i>
            </a>
          </div>

          <div class="col-10">
            <div class="row">

              <div class="col-12 col-md-6 col-lg-4">
                <div class="ProjectsBorder Project paddingRowFixer mt-3 mb-3">
                  <div style="cursor: pointer;" class="rowFix">
                    <SingularProjectComponent :Project="allProjects[0]"/>
                  </div>
                </div>
              </div>

              <div class="d-none d-md-block col-md-6 col-lg-4">
                <div class="ProjectsBorder Project paddingRowFixer mt-3 mb-3 ms-2">
                  <div style="cursor: pointer;" class="rowFix">
                    <SingularProjectComponent :Project="allProjects[1]"/>
                  </div>
                </div>
              </div>

              <div class="d-none d-lg-block col-lg-4">
                <div class="ProjectsBorder Project paddingRowFixer mt-3 mb-3 ms-2">
                  <div style="cursor: pointer;" class="rowFix">
                    <SingularProjectComponent :Project="allProjects[2]"/>
                  </div>
                </div>
              </div>

            </div>


          </div>


          <div class="col-1 d-flex align-items-center justify-content-center">
            <a @click="rightArrowClick()" class="btn p-0 p-sm-2">
              <i class="bi bi-arrow-right-short"></i>
            </a>
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

<style scoped>
  .ProjectsBorder
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
  .btn
  {
    background-color: #d6c389;
    border-color: #d6c389;
  }
  .btn:hover
  {
    background-color: whitesmoke;
  }

</style>