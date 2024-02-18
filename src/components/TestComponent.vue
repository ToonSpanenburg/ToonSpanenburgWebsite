<script setup>

import SingularProjectComponent from "@/components/Projects/SingularProjectComponent.vue";
import * as Projects from "@/components/Projects/Projects.js";
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
  <!--Colors -->
  <div class="m-4 pt-5">
    <h3 class="mt-5">
      Used Colors
    </h3>
    <ul>
      <li style="color: #d6c389">
        main: #d6c389
      </li>
      <li style="color: #f5f5f5;">
        background grey: #f5f5f5
      </li>
      <li style="color: #123d67;">
        main blue: #123d67
      </li>
      <li style="color: #89D6C3;">
        aqua type color:#89D6C3
      </li>
      <li style="color: #C389D6;">
        Pinkish color:#C389D6
      </li>
      <li style="color: #C3D689;">
        greenish color:#C3D689
      </li>
      <li style="color: #D69C89;">
        brownish color: #D69C89
      </li>
    </ul>
  </div>
  <!--Carousel test -->
  <div class="m-4 pt-5">
    <h3 class="pb-5">
      Carrousel test
    </h3>
    <div class="justify-content-center text-center">
      <div class="row">
        <div class="col-1">
          <button @click="leftArrowClick()">
            <
          </button>
        </div>
        <div class="col-10">
          <div class="row p-5">
            <div class="col-4 myElementBorder">
              <SingularProjectComponent :Project="allProjects[0]"/>
            </div>
            <div class="col-4">
              <SingularProjectComponent :Project="allProjects[1]"/>
            </div>
            <div class="col-4">
              <SingularProjectComponent :Project="allProjects[2]"/>
            </div>
          </div>
        </div>
        <div class="col-1">
          <button @click="rightArrowClick()">
            >
          </button>
        </div>
      </div>
    </div>
  </div>


</template>



<style scoped>
button
{
  align-items: center;
}
.myElementBorder
{
  border: #d6c389;
}
</style>