<script setup>

</script>

<template>
  <div class="mt-3">
    <h2 class="m-4 mb-3">
      Contact en gegevens
    </h2>

    <div class="row mx-3 mt-4 mb-4 pb-4">

      <div class="col-12 col-md-5">
        <img src="@/assets/TempProfilePic.jpg" alt="" class="text-center" style="height: 60px;">
        <h3 class="mb-0 mt-1">
          Toon Spanenburg
        </h3>

        <div class="text-muted mt-0 mb-3">
          {Programmeur}
        </div>
        <div class="mt-2">
          <ul class="ms-0 ps-0">

            <li class="mt-2 ">
              <a class="contactLink" href="tel:32471782397">
                <i class="bi bi-telephone-fill"></i>
                +32 471 78 23 97
              </a>
            </li>

            <li class="mt-2">

              <a class="contactLink" href="mailto: toonspanenburg@hotmail.com">
                <i class="bi bi-envelope-fill"></i>
                toonspanenburg@hotmail.com
              </a>

            </li>

            <li class="mt-2">
              <a class="contactLink" href="https://github.com/ToonSpanenburg">
                <i class="bi bi-github"></i>
                @ToonSpanenburg
              </a>
            </li>

            <li class="mt-2">
              <a class="contactLink" href="https://github.com/ToonSpanenburg/ToonSpanenburgWebsite">
                <i class="bi bi-github"></i>
                This website on Github
              </a>
            </li>

            <li class="mt-2">
              <a class="contactLink" href="Files/ToonSpanenburgCV.pdf" download="ToonSpanenburgCV.pdf">
                <i class="bi bi-download"></i>
                Download mijn Cv
              </a>
            </li>

          </ul>
        </div>
      </div>

      <div class=" d-none d-md-block col-md-7">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d39848.97531161168!2d4.829623072480251!3d51.37436747632918!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c6af01c4de5ebb%3A0x503aa8abb2714edf!2s2330%20Merksplas!5e0!3m2!1sen!2sbe!4v1707703810062!5m2!1sen!2sbe"
                style="border:0; width: 100%; height: 100%;"
                allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
        </iframe>

      </div>
    </div>
  </div>


</template>

<style scoped>
 ul
 {
   list-style: none;
 }
 li
 {
   padding-left: 0;
   margin-left: 0;
   font-size: 1.7em;
 }
 .contactLink
 {
   color: black;
 }
 .contactLink:hover
 {
   text-decoration: underline;
 }

 i
 {
   color: black;
   padding-right: 0.2em;
 }

 a
 {
   font-size: 0.8em;
 }


 @media only screen and (max-width: 950px)
 {
   li
   {
     font-size: 1.3em;
   }
 }

 @media only screen and (max-width: 767px)
 {
   li
   {
     font-size: 1.8em;
   }
   i
   {
     font-size: 1em;
   }
 }

 @media only screen and (max-width: 500px)
 {
   li
   {
     font-size: 1.2em;
   }
   i
   {
     font-size: 1.3em;
   }
 }

</style>