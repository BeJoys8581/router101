<script setup>
import Detail from './Detail.vue';
</script>
<template>
   <!--Tea Prod Header--><br>
   <div class="position-relative overflow-hidden p-3 p-md-5 m-md-3 text-center bg-success">
  <div class="col-md-6 p-lg-5 mx-auto my-5">
    <h1 class="display-3 fw-bold text-light">Welcome to Joys Tea ☕</h1>
    <h3 class="fw-normal text-light mb-3">Discover Tranquility in Every Sip</h3>
    <div class="d-flex gap-3 justify-content-center lead fw-normal text-light">Crafting Moments of Calmness</div>
  </div>
  <div class="shadow-sm d-none "></div>
  <div class="product-device-2 shadow-sm d-none "></div>
</div>

<h2 class="page-section-heading text-center text-uppercase text-secondary mb-0 text-decoration-underline">Joys with Your Tea</h2>

 
 <br>
    <Detail/>
  </template>
  


<style>
.container {
  max-width: 960px;
}

.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(0, 0, 0, .85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #643400;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #643400;
  text-decoration: none;
}


.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #003c58;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #003c58;
}


.flex-equal > * {
  flex: 1;
}
@media (min-width: 768px) {
  .flex-md-equal > * {
    flex: 1;
  }
}

</style>