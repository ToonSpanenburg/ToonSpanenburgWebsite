<script setup>

</script>

<template>
  <div class="mt-3">
    <h2 class="m-4">
      Contact en gegevens
    </h2>
    <div class="row mx-3">
      <div class="col-5">
        <div class="ContactBorder">
          <div class="card-header text-center ContactBoxHeader topBorder">
            <div class="pt-2 ">
              <img src="@/assets/TempProfilePic.jpg" alt="" style="height: 60px;">
            </div>
            <h5>
              Toon Spanenburg
            </h5>
          </div>
          <div class="py-2 pt-3 bg-white">
            <p class="ps-4">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam, asperiores assumenda consequatur doloribus inventore itaque quod vitae! Architecto cum cumque, doloremque esse illo itaque libero magnam, mollitia nostrum, tempora ut.
            </p>
            <ul>
              <li class="">
                <div class="">
                  <i class="bi bi-telephone-fill"></i>
                  <a class="px-2" href="tel:32471782397">+32 471 78 23 97</a>
                </div>
              </li>
              <li>
                <i class="bi bi-envelope-fill"></i>
                <a class="px-2" href="mailto: toonspanenburg@hotmail.com">toonspanenburg@hotmail.com</a>
              </li>
              <li>
                <i class="bi bi-github"></i>
                <a class="px-2" href="https://github.com/ToonSpanenburg">@ToonSpanenburg</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col-7 mt-0 CvElement">
        <a href="" class="CvFont">
          DOWNLOAD MIJN CV
        </a>
      </div>
    </div>
  </div>


</template>

<style scoped>
 ul
 {
   list-style: none;
 }
 a
 {
   font-size: 0.8em;
 }
 .ContactBorder
 {
   border-color: #d6c389;
   border-bottom-width: 3px;
   border-style: solid;
   background-color: #f5f5f5;
 }
 .ContactBoxHeader
 {
   border-bottom: #d6c389 solid 3px;
 }
 .CvFont
 {
   font-size: 8em;
   color: #d6c389;

 }
 .CvElement
 {
   transition: transform 0.3s ease;
 }
 .CvElement:hover
 {
   transform: scale(1.15);
 }

</style>